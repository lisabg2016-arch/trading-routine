# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-09-08 (pre-mercado)
- Valor de la cuenta (equity): $99,487.72 | Cash: $8,895.90 | Buying power: $289,240.69
- P&L desde inicio (~$100,000): -0.51% aprox. (comparación detallada vs SPY en la Revisión Semanal)
- Posiciones abiertas (6, vía Alpaca `/v2/positions`):
  | Símbolo | Cant. | Precio entrada | Precio actual | P&L no realizado |
  |---|---|---|---|---|
  | ABBV | 20 | 248.99 | 254.24 | +$105.00 (+2.11%) |
  | CAT | 6 | 816.00 | 818.00 | +$12.00 (+0.25%) |
  | GOOGL | 14 | 342.51 | 336.10 | -$89.74 (-1.87%) |
  | JPM | 14 | 357.13 | 355.72 | -$19.76 (-0.40%) |
  | MSFT | 10 | 487.89 | 496.70 | +$88.14 (+1.81%) |
  | SPY | 85.851065749 | 775.98 | 768.18 | -$669.94 (-1.01%) |
- Nota sobre el "core": la posición grande es **SPY** (65,949 = ~66% del equity), no SPLG como indica `estrategia.md` (que recomienda SPLG por precio/fee, aunque señala que SPY fraccionario también serviría). No es una violación de guardarraíles — SPY es igual de válido como core — pero es una inconsistencia con la nota de diseño; no se toca hoy (día de pre-mercado, no se opera), se deja registrada para la Revisión Semanal.
- Régimen (SMA200, calculado con ~289 barras diarias vía Alpaca data API):
  - SPY: 770.18 vs SMA200 712.12 → **+8.15%, régimen ALCISTA** (nuevas entradas permitidas).
  - QQQ: 719.10 vs SMA200 657.67 → +9.34%.
- Notas: sin operaciones hoy (rutina de pre-mercado, solo investigación). Contexto de mercado: futuros mixtos/algo negativos por tensión geopolítica en Medio Oriente + subida del petróleo (Brent >$98) y nuevos aranceles Canadá-EEUU; UST10y ~4.80%; mercado pricing ~60% prob. de subida de tasas de la Fed la próxima semana (CPI 11-sep, FOMC 15-16 sep). Régimen mecánico (200D) sigue alcista pese al ruido macro de corto plazo.
