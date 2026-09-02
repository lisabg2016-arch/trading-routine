# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-09-02, pre-mercado
- Valor de la cuenta (equity): $98,938.28 | Cash: $8,895.90 | Invertido: ~91%
- P&L del día (vs. last_equity $98,840.06): +$98.22 (+0.10%)
- P&L desde inicio (~$100k, cuenta creada 2026-07-24): ≈ −1.06%
- Posiciones (libro activo satélite, 5/5 — al máximo):
  - ABBV: 20 acc. @ 248.99, actual 261.90 (+5.19%), stop GTC 249.00
  - CAT: 6 acc. @ 816.00, actual 781.36 (−4.25%), stop GTC 767.69
  - GOOGL: 14 acc. @ 342.51, actual 334.60 (−2.31%), stop GTC 322.95
  - JPM: 14 acc. @ 357.13, actual 356.12 (−0.28%), stop GTC 336.58
  - MSFT: 10 acc. @ 487.89, actual 499.50 (+2.38%), stop GTC 475.52
  - Core: SPY 85.851065 acc. @ 775.98, actual 762.38 (−1.75%) — nota: la estrategia documenta el core como SPLG, en la práctica el core existente es SPY (ver diario de investigación 2026-09-02).
- Régimen: SPY $761.63 > SMA200 $710.63 (alcista); QQQ $707.65 > SMA200 $656.05.
- Notas: todas las posiciones activas tienen stop GTC vigente (verificado vía /v2/orders). Sin earnings inminentes en próximos 5 días hábiles para ninguna posición. Nota: este archivo estaba desactualizado desde la creación de la cuenta — Alpaca sigue siendo la fuente de verdad; este snapshot es solo referencia.
