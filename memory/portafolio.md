# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-09-14 (pre-mercado)
- Valor de la cuenta (equity): $98,383.11 | Efectivo: $5,117.74 (5.2%)
- P&L del día (vs último cierre): -$513.25 (-0.52%)
- P&L desde inicio (~$100k): -1.62%
- Régimen: SPY $764.29 (cierre 9/11) > SMA200 $714.23 → **alcista** (QQQ también > SMA200)
- Posiciones activas (libro satélite, 5/5 — LLENO):
  - CAT: 6 acc @ $816.00, actual $786.66, P&L -3.60% (~$4,720, ~4.8% equity)
  - GOOGL: 14 acc @ $342.51, actual $344.06, P&L +0.45% (~$4,817, ~4.9% equity)
  - MA: 8 acc @ $567.87, actual $572.86, P&L +0.88% (~$4,583, ~4.7% equity)
  - UNH: 12 acc @ $392.81, actual $378.98, P&L -3.52% (~$4,548, ~4.6% equity)
  - V: 13 acc @ $366.86, actual $372.25, P&L +1.47% (~$4,839, ~4.9% equity)
- Core núcleo-satélite: SPY (no SPLG) — 91.86 acc @ $775.18, actual $759.38, P&L -2.04% (~$69,759, ~70.9% equity).
  **Nota/discrepancia**: `estrategia.md` especifica SPLG como instrumento del core; la posición real en Alpaca está en SPY. No se tocó hoy (pre-mercado no opera); señalar para revisión en Apertura/Cierre.
- Invertido total (core + activo): ~94.8% del equity (objetivo ~90%, dentro del margen de no-rebalanceo <10% de desviación).
- Ninguna posición cerca de su stop -8%. Sin alertas de tope de pérdida diaria (-3%) ni circuit breaker (-15%).
- Notas: libro activo a máximo de posiciones (5/5); cualquier candidata nueva requiere liberar un slot primero.
