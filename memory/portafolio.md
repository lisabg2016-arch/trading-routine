# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-09-15 (pre-mercado)
- Valor de la cuenta (equity): $98,499.51
- Efectivo: $5,117.74 (5.2%)
- P&L del día anterior: −$186.79 (−0.19%)
- Posiciones (libro activo, 5/5 — al máximo):
  - CAT: 6 acc @ 816.00, valor $4,736.16 (4.81%), P&L no realizado −$159.84 (−3.27%)
  - GOOGL: 14 acc @ 342.51, valor $4,846.94 (4.92%), P&L no realizado +$51.80 (+1.08%)
  - MA: 8 acc @ 567.87, valor $4,548.08 (4.62%), P&L no realizado +$5.12 (+0.11%)
  - UNH: 12 acc @ 392.81, valor $4,601.52 (4.67%), P&L no realizado −$112.20 (−2.38%)
  - V: 13 acc @ 366.86, valor $4,846.27 (4.92%), P&L no realizado +$77.13 (+1.62%)
- Core núcleo-satélite: **SPY** 91.86 acc @ 775.18, valor $69,802.81 (70.87% del equity), P&L no realizado −$1,407.78 (−1.98%).
  - Nota: el core está en **SPY**, no en SPLG como indica `estrategia.md`/`watchlist.md`. No es una violación de guardarraíles (SPY es válido como proxy S&P 500, fraccionario), pero es una desviación del diseño documentado — señalarlo, no es urgente corregir hoy.
- Notas: libro activo satélite al **máximo de posiciones (5/5)** — no hay espacio para candidatas nuevas hoy aunque el régimen es alcista. `memory/diario_operaciones.md` está sin filas pese a haber operaciones reales (confirmadas en `/v2/account/activities`, ej. compras de V/MA/SPY el 9-10 sep) — el diario local de operaciones no se está manteniendo; Alpaca sigue siendo la fuente de verdad.
