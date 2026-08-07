# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-08-07 ~12:16 (rutina mediodía)
- Valor de la cuenta (equity): $101,019.09 (last_equity $100,885.94, día ~+0.13%)
- Efectivo: $76,720.36 | Posiciones: $24,298.73
- Posiciones abiertas (5):
  - AVGO: 12 acc @ entry 379.69, precio 424.79 (+11.88%). Stop GTC subido 387.89 → 390.81.
  - NVDA: 22 acc @ entry 199.16, precio 223.50 (+12.22%). Stop GTC subido 201.84 → 205.62.
  - GE: 13 acc @ entry 363.97, precio 370.75 (+1.86%). Stop GTC sin cambio: 350.75 (bajó hoy intradía, un trail al 8% habría quedado por debajo del stop actual, no se baja).
  - JPM: 14 acc @ entry 357.13, precio 356.685 (-0.13%). Stop GTC sin cambio: 331.60 (posición ~plana, sin trail que subir).
  - UNH: 11 acc @ entry 419.12, precio 406.575 (-2.99%). Stop GTC sin cambio: 392.00 (perdedora, no aplica trailing; no rompió tesis ni cayó -7% intradía, no se corta).
- Notas: ninguna posición cortada. Nota operativa: el registro en Google Sheets (Zapier) falló con "insufficient tasks on account" — cuenta de Zapier sin tareas disponibles. Este archivo local queda como respaldo del snapshot; falta registrar la fila de gestión en el diario cuando se restablezca la cuota de Zapier.
