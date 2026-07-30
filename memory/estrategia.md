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
- **Cortar pérdidas rápido**: stop inicial ~−8% desde la entrada (o bajo el soporte lógico).
- **IMPORTANTE — stops como orden GTC** (persistente), NUNCA "day": una orden "day" expira al
  cierre y deja la posición sin protección de noche (bug detectado 2026-07-28). Verificar que todo
  stop quede GTC.
- **Dejar correr ganadores**: trailing que solo sube (nunca lo bajes); sin objetivo fijo que corte
  a los grandes ganadores.
- Tomar parcial es opcional; por defecto, dejar correr con trailing.

## Filtro de régimen
- Si SPY < su media de 200 días (mercado bajista), NO abrir posiciones nuevas; solo gestionar
  las abiertas. Reduce drawdown; es seguro anti-catástrofe, no generador de retorno.

## Cadencia
- Revisar en pre-mercado, apertura, mediodía, cierre. Revisión semanal los viernes.
- Pocas operaciones buenas > muchas operaciones. Está bien no operar.
