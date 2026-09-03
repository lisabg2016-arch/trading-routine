# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-09-03 pre-mercado (datos Alpaca a cierre de 2026-09-02)
- Valor de la cuenta (equity): $99,318.03 | cash: $8,895.90 | en posiciones: $90,422.13
- P&L del día (vs last_equity): +$69.29 (+0.07%, aún sin abrir el mercado)
- Posiciones satélite (5/5, TOPE — guardarraíl 3, no se pueden abrir nuevas hoy):
  - ABBV 20 @ 248.99, actual 261.72, +$254.60 (+5.11%)
  - CAT 6 @ 816.00, actual 794.86, -$126.84 (-2.59%)
  - GOOGL 14 @ 342.51, actual 338.07, -$62.16 (-1.30%)
  - JPM 14 @ 357.13, actual 357.07, -$0.79 (-0.02%)
  - MSFT 10 @ 487.89, actual 499.76, +$118.70 (+2.43%)
- Core: SPY 85.85 @ 775.98, actual 765.15, -$930.07 (-1.40%) — **nota:** debería ser SPLG según `estrategia.md`/`watchlist.md` (SPY es solo señal de régimen/benchmark, no se compra como trade); queda anotado en `diario_investigacion.md` 2026-09-03 para revisión, no se tocó (rutina de pre-mercado no opera).
- Régimen (SPY vs SMA200): ALCISTA — SPY 765.13 > SMA200 ≈ 711.09.
- Notas: pre-mercado 2026-09-03 — sin operaciones (rutina informativa). Ninguna posición con earnings en los próximos 5 días hábiles.
