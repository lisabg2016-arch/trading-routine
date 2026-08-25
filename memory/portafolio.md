# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-08-25 (pre-mercado)
- Valor de la cuenta (equity): $99,737.28
- Cash: $13,774.81
- Valor posiciones: $85,962.47
- P&L del día (vs last_equity $99,338.34): +$398.94 (+0.40%)
- Posiciones abiertas (libro activo + core):
  - ABBV: 20 acc @ 248.99, valor $5,283.10, P&L no realizado +$303.30 (+6.09%)
  - CAT: 6 acc @ 816.00, valor $4,974.36, P&L no realizado +$78.36 (+1.60%)
  - GOOGL: 14 acc @ 342.51, valor $4,897.48, P&L no realizado +$102.34 (+2.13%)
  - JPM: 14 acc @ 357.13, valor $5,019.00, P&L no realizado +$19.16 (+0.38%)
  - SPY: 85.85 acc @ 775.98, valor $65,788.53, P&L no realizado -$830.48 (-1.25%) — **nota: el core está en SPY, no en SPLG** como indica `estrategia.md`/`watchlist.md`. Discrepancia a revisar (no corregida hoy, la rutina de pre-mercado no opera).
- Régimen (SPY vs SMA200): SPY cierre $763.46 (2026-08-24) vs SMA200 ≈ $705.41 → **+8.2%, régimen ALCISTA**. SPY retrocedió desde ~$778 (13-ago) — pullback sano, sigue muy por encima de su SMA200.
- Notas: 4 posiciones activas del libro satélite (ABBV, CAT, GOOGL, JPM) + core en SPY. Ninguna alcanza el máx 5%/posición individualmente a este valor de cuenta salvo evaluarlo con precisión; libro activo dentro de los límites (4/5 posiciones).
