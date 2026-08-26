# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-08-26 (pre-mercado)
- Valor de la cuenta (equity): $99,471.55 (equity previo: $99,601.83)
- P&L del día (hasta el momento de la consulta): -$130.28 (-0.13%)
- Efectivo: $8,895.90 (~8.9% de la cuenta)
- Régimen: **ALCISTA** — SPY $765.79 vs SMA200 $708.40 (+8.1%); QQQ $710.66 vs SMA200 $653.62 (+8.7%)
- Posiciones (vía `/v2/positions`, fuente de verdad = Alpaca):
  | Símbolo | Cant. | Precio entrada | Precio actual | Valor mercado | P&L no realizado |
  |---|---|---|---|---|---|
  | SPY | 85.851066 | 775.98 | 764.75 | $65,654.60 | -$964.41 (-1.45%) |
  | ABBV | 20 | 248.99 | 266.41 | $5,328.20 | +$348.40 (+7.00%) |
  | CAT | 6 | 816.00 | 809.36 | $4,856.14 | -$39.86 (-0.81%) |
  | GOOGL | 14 | 342.51 | 346.00 | $4,844.00 | +$48.86 (+1.02%) |
  | JPM | 14 | 357.13 | 358.00 | $5,012.00 | +$12.16 (+0.24%) |
  | MSFT | 10 | 487.89 | 488.07 | $4,880.70 | +$1.80 (+0.04%) |
- Libro activo (satélite): 5/5 posiciones abiertas (ABBV, CAT, GOOGL, JPM, MSFT) — **lleno, sin espacio para nuevas** hasta liberar un slot.
- Nota — **discrepancia core**: la posición grande (~66% de la cuenta) es **SPY**, no **SPLG** como define la estrategia núcleo-satélite vigente (commit "Nucleo-satelite: core SPLG..."). El watchlist indica que SPY es solo señal/benchmark y NO debería comprarse como posición activa. Puede ser una posición legacy previa al cambio a SPLG que aún no se ha migrado — pendiente de revisión (no se tocó hoy; pre-mercado no opera).
- Notas: sin operaciones hoy (rutina pre-mercado = solo investigación, no opera).
