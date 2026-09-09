# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-09-09 (pre-mercado), datos en vivo de Alpaca (`GET /v2/account`, `/v2/positions`)
- Cuenta: PAPER confirmada (account_number PA3BMDAXVD5J, status ACTIVE)
- Valor de la cuenta (equity): $98,748.00 | Efectivo: $18,824.64
- P&L del día (vs last_equity): -$456.18 (-0.46%)
- Rendimiento desde inicio (~$100,000 el 2026-07-24): -1.25%
- **vs SPY desde inicio**: SPY +3.68% (2026-07-24→2026-09-08) → el portafolio va **-4.93pp por debajo de SPY**
- Régimen (SPY vs SMA200): SPY $766.06 > SMA200 $712.65 (+7.5%) → **alcista**, nuevas entradas permitidas (guardarraíl 11 OK)
- Posiciones (libro activo, 3/5 usadas):
  - CAT: 6 acc @ $816.00, valor $4,878, P&L no realizado -$18.00 (-0.37%)
  - GOOGL: 14 acc @ $342.51, valor $4,632.32, P&L no realizado -$162.82 (-3.40%)
  - JPM: 14 acc @ $357.13, valor $4,915.54, P&L no realizado -$84.30 (-1.69%)
- Core núcleo-satélite: SPY 85.851065749 acc @ $775.98, valor $65,495.78, P&L no realizado -$1,123.23 (-1.69%)
  - ⚠️ Nota: la estrategia (`estrategia.md`) define el instrumento del core como **SPLG**, no SPY. La posición real de core está en SPY. Queda anotado para que la rutina de Apertura/Gestión lo evalúe (no se opera en esta rutina, que es solo informativa).
- Notas: sin operaciones nuevas hoy (rutina de pre-mercado, no opera). Ver `diario_investigacion.md` para candidatas del día (LRCX, AMD en observación — ver detalle).
