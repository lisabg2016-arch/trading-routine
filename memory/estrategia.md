# Estrategia — Swing discrecional disciplinado

## Decisión sobre el estilo de entrada (2026-07-29)
Las entradas se mantienen **DISCRECIONALES** a propósito. Se evaluó pasar a una regla
mecánica RSI-2, pero se descartó por una razón concreta y comprobada: **el RSI-2 mecánico
compra el "dip" sin distinguir un retroceso sano de un cuchillo cayendo** — en backtest perdió
~76% en NVDA justamente por comprar caídas del 50-85% una y otra vez. **El juicio del bot SÍ
evita esos cuchillos** (declinó AMD/NVDA/CRWD/PANW en una semana risk-off = buena decisión).
Ese filtro humano es el edge que la regla mecánica no tiene. Se conserva.

## Objetivo
Correr un libro pequeño y disciplinado en cuenta **paper**, comparándose honestamente contra
**SPY** (comprar y mantener). No se busca ganarle al mercado a toda costa; se busca **proceso
y disciplina**. El edge está en la **gestión de riesgo y la asimetría**, no en adivinar dirección.

## Estilo
- **Swing / posición** (días a semanas), datos diarios. NO day trading, NO 0DTE, NO scalping, NO opciones.
- Solo símbolos de la watchlist (`watchlist.md`).
- Preferir entradas con la tendencia mayor a favor y con catalizador cuando lo haya.

## Señal de entrada (discrecional, pero apuntada a la ZONA MEDIA)
El bot decide con criterio, buscando el punto entre las dos puntas malas:
- ✅ **Tendencia alcista**: por encima de su media de ~200 días.
- ✅ **Retroceso o base sana**: un pullback ordenado hacia soporte / media, que se estabiliza.
- ✅ **SPY/QQQ acompañando** (mercado no en clara caída; SPY sobre su SMA200 para nuevas).
- ❌ **NO cuchillos cayendo**: nada que esté desplomándose o rompiendo estructura (aunque el RSI esté bajo).
- ❌ **NO extensión vertical / sobrecompra extrema**: nada disparado muy por encima de sus medias
  (lección: comprar GE con RSI 96.9 fue un error del mismo tipo, en la otra punta). Comprar fuerza ≠ perseguir.

Ante la duda entre estas puntas, **NO operar es una decisión válida y preferida.**

## Salidas (la parte que importa — el edge asimétrico)
- **Cortar pérdidas rápido**: stop inicial **−8%** desde la entrada. Si hay un soporte lógico más
  cercano puede ir ahí, pero **el stop NUNCA arriesga más de −8%** (si el soporte está más abajo, manda el −8%).
- **IMPORTANTE — stops como orden GTC** (persistente), NUNCA "day": una orden "day" expira al
  cierre y deja la posición sin protección de noche (bug detectado 2026-07-28). Verificar que todo
  stop quede GTC.
- **Dejar correr ganadores**: trailing que solo sube (nunca lo bajes); sin objetivo fijo que corte
  a los grandes ganadores.
- **Excepción — earnings manda:** ante un earning inminente (próxima sesión / ~1-2 sesiones), cerrar
  la posición GANADORA antes del reporte **tiene precedencia** sobre dejar-correr (guardarraíl 16),
  para evitar el gap binario.
- Tomar parcial es opcional; por defecto, dejar correr con trailing.

## Filtro de régimen
- Si SPY < su media de 200 días (mercado bajista), NO abrir posiciones nuevas; solo gestionar
  las abiertas. Reduce drawdown; es seguro anti-catástrofe, no generador de retorno.

## Núcleo-satélite (core SPY — para no quedar atrás de SPY)
Problema del lastre de caja: con máx 5%/pos × 5 = 25% invertido, el ~75% en efectivo hace que el
libro pierda contra SPY en mercados alcistas. Solución: **parkear el efectivo ocioso en un core de S&P 500**.
- **Instrumento del core = SPLG** (SPDR Portfolio S&P 500 ETF): mismo índice que SPY pero ~1/10 del
  precio por acción y fee más bajo (0.02%). **SPY se usa SOLO como señal de régimen (200D) y benchmark.**
  (Alpaca permite fraccionarias, así que SPY también serviría; se elige SPLG por precio/fee.)
- **Core (SPLG):** cuando **SPY > SMA200** (régimen alcista), mantén una posición de **SPLG** con el
  efectivo que no usa el libro activo, apuntando a que el portafolio total (core + activo) quede
  **~90% invertido** (deja ~10% de colchón para nuevas entradas activas y fills). Cuando **SPY < SMA200**
  (bajista), **vende el core a efectivo** — es tu sistema 200D probado (protege del bear).
- El **core NO cuenta** para los límites del libro activo (máx 5% / máx 5 / máx 3 nuevas) y **NO lleva
  stop −8%**: lo gobierna el régimen 200D (dentro sobre 200d, fuera debajo).
- **Satélite:** el libro activo de siempre (máx 5 posiciones × 5%, entradas discrecionales con filtros
  13-17, stops −8%). Solo abre nuevas en régimen alcista.
- **Rebalanceo sin churn:** ajusta el core solo si se desvía **>~10% del equity** respecto al objetivo
  (no lo toques a diario por variaciones pequeñas).
- **NOTA (2026-08-13): SPLG no está disponible en Alpaca.** `GET /v2/assets/SPLG` devuelve
  `asset not found` (no es un problema de datos ni de mercado cerrado — el ticker simplemente no
  existe en el universo de Alpaca ahora mismo). Mientras esto siga así, el core se implementa con
  **SPY fraccionario** (ya contemplado como alternativa válida arriba: "SPY también serviría").
  Comprado el core inicial 2026-08-13: 85.851065749 SPY @ 775.983495 (~$66,619.02). Si en una
  rutina futura `GET /v2/assets/SPLG` vuelve a existir y es `tradable:true`, se puede evaluar
  migrar el core de SPY a SPLG (o simplemente mantener SPY, ya que es funcionalmente equivalente
  salvo fee).
- Resultado: portafolio ≈ **SPY ± el alfa del libro activo**. Ya no pierde contra SPY por estructura,
  y en bear el core en efectivo lo protege.

## Cadencia
- Revisar en pre-mercado, apertura, mediodía, cierre. Revisión semanal los viernes.
- Pocas operaciones buenas > muchas operaciones. Está bien no operar.
