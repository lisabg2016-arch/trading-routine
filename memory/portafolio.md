# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-08-31 (pre-mercado)
- Valor de la cuenta (equity): $99,584.36 (cash $8,895.90)
- P&L del día (vs last_equity $99,850.76): −$266.40 (−0.27%)
- Invertido: $90,688.46 (~91% del equity) + ~9% efectivo
- Posiciones (satélite + core, vía `/v2/positions`):
  | Símbolo | Qty | Precio | Valor mercado | P&L no realizado |
  |---|---|---|---|---|
  | SPY | 85.851 | 767.61 | $65,900.14 | −$718.87 (−1.08%) |
  | MSFT | 10 | 508.40 | $5,084.00 | +$205.10 (+4.20%) |
  | ABBV | 20 | 255.08 | $5,101.60 | +$121.80 (+2.45%) |
  | JPM | 14 | 356.69 | $4,993.66 | −$6.18 (−0.12%) |
  | GOOGL | 14 | 344.10 | $4,817.40 | +$22.26 (+0.46%) |
  | CAT | 6 | 798.61 | $4,791.66 | −$104.34 (−2.13%) |
- Notas:
  - **Discrepancia detectada:** el core núcleo-satélite está en **SPY** (65.9k, ~66% del equity), no en **SPLG** como manda `estrategia.md` desde el 2026-07-29. SPY se supone que es solo señal de régimen/benchmark, no un holding. Probablemente quedó de antes de esa decisión y nunca se migró. No se opera hoy (rutina de pre-mercado no coloca órdenes) — queda para que Apertura/Mediodía lo evalúen o para decisión humana.
  - Las posiciones satélite (MSFT, ABBV, JPM, GOOGL, CAT) suman 5 de 5 máx — el libro activo está lleno; no hay espacio para candidatas nuevas hoy aunque las hubiera.
  - Los archivos de memoria (portafolio, diario) estaban vacíos/plantilla pese a que ya existen posiciones reales — parece la primera vez que una rutina los actualiza con datos reales.
