# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-09-17 (pre-mercado)
- Valor de la cuenta (equity): $98,765.58 | Cash: $5,117.74
- P&L del día anterior (16/09 vs equity previo $97,750.53): +$1,015.05 (+1.04%)
- Régimen: SPY $754.05 vs SMA200 $715.45 → **alcista** (+5.4%). QQQ $704.70 vs SMA200 $661.56 → alcista (+6.5%).
  Pullback leve últimos ~6 sesiones: SPY -1.3%, QQQ -1.6% desde el máximo reciente.
- Core (núcleo): posición en **SPY** (no SPLG) de 91.86 acc. @ $775.18 avg, valor $69,996.64 (-1.7% no realizado). Es el core núcleo-satélite (nota: la estrategia prefería SPLG por fee/precio, pero el core actual está en SPY; no se toca hoy, es sólo información — el rebalanceo de core no es tarea de esta rutina).
- Libro activo (satélite) — **FULL 5/5**, sin espacio para nuevas posiciones esta semana salvo que se cierre una:
  | Símbolo | Qty | Entrada | Precio actual | P&L no realizado | Stop GTC |
  |---|---|---|---|---|---|
  | CAT | 6 | $816.00 | $806.22 | -$58.68 (-1.2%) | $767.69 (GTC) |
  | GOOGL | 14 | $342.51 | $347.19 | +$65.52 (+1.4%) | $322.95 (GTC) |
  | MA | 8 | $567.87 | $573.81 | +$47.52 (+1.0%) | $530.27 (GTC) |
  | UNH | 12 | $392.81 | $377.40 | -$184.92 (-3.9%) | $361.39 (GTC) |
  | V | 13 | $366.86 | $372.00 | +$66.86 (+1.4%) | $346.28 (GTC) |
  Todas las 5 posiciones tienen stop GTC activo confirmado en `/v2/orders?status=open` — sin bug de protección nocturna.
- Earnings: ninguna de las 5 posiciones reporta en las próximas ~2 sesiones (CAT ~29-oct, GOOGL ~27-oct, MA ~22-29 oct, UNH ~13-oct, V ~3-nov). Sin necesidad de cierre forzado por guardarraíl 16 hoy.
- Noticias relevantes de hoy:
  - **CAT**: catalizador negativo fresco — downgrade de Baird a Neutral (14-sep), PT recortado a $900, por riesgo regulatorio (Texas/NY) al segmento de generación eléctrica para data centers desde 2027. Stock cayó ~-4.2% el 14-sep. Precio actual $806 sigue ~4.8% por encima del stop ($767.69); el stop GTC sigue siendo la protección, ninguna acción adicional hoy (esta rutina no opera).
  - **UNH**: sin noticia nueva puntual, pero overhang estructural conocido (investigación DOJ por facturación de Medicare Advantage, demanda de accionistas) sigue vigente; ya es la posición más negativa (-3.9%), protegida por su stop.
  - **GOOGL**: 16-sep, el DOJ ganó medidas en el caso de ad-tech (interoperabilidad forzada); reacción de mercado mixta/tenue, no claramente negativo para el precio.
  - **MA, V**: sin noticia negativa fresca relevante.
- Vigilar para cuando se libere un cupo (no accionable hoy, book lleno): sector semis (NVDA/AMD/AVGO, en watchlist) tuvo venta masiva el 14-sep por ensayo de seguridad de IA de Dario Amodei — NVDA -3.4%, AMD -4.4/-4.8%, AVGO -4.8%. Es retroceso por sentimiento de sector, no noticia específica de la empresa — a confirmar estabilización (no perseguir un cuchillo cayendo) y re-chequear RECOM/target/earnings en vivo antes de cualquier entrada futura.
- Notas: primera actualización real de este archivo con datos en vivo de Alpaca. Sin operaciones hoy (rutina pre-mercado: solo investigación, no opera).
