# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-09-23 ~12:21 UTC (pre-mercado)
- Valor de la cuenta (equity): $99,438.38 | Efectivo: $5,117.74
- P&L del día (vs. last_equity): -$117.49 (-0.12%)
- Régimen (SPY vs SMA200): SPY $773.44 vs SMA200 $717.16 → **+7.85%, alcista**
- Core (núcleo): posición en **SPY** (no SPLG) — 91.86 acc, valor ~$70,964 (~71% del portafolio). Nota: `estrategia.md` especifica SPLG como instrumento de core; el core actual quedó en SPY (probable legado). No se toca hoy (rutina de pre-mercado no opera); dejar anotado para revisión.
- Libro activo (satélite) — **5/5 posiciones abiertas (máximo, guardarraíl 3): sin espacio para nuevas entradas hoy.**
  | Símbolo | Cant. | Precio entrada | Precio actual | P&L no realizado | Stop GTC |
  |---|---|---|---|---|---|
  | CAT | 6 | 816.00 | 802.00 | -84.00 (-1.72%) | 767.69 |
  | GOOGL | 14 | 342.51 | 350.45 | +111.16 (+2.32%) | 330.62 |
  | MA | 8 | 567.87 | 556.79 | -88.64 (-1.95%) | 530.27 |
  | UNH | 12 | 392.81 | 372.64 | -242.04 (-5.14%) | 361.39 |
  | V | 13 | 366.86 | 362.40 | -57.94 (-1.22%) | 346.28 |
- Todas las posiciones satélite tienen stop GTC vigente (verificado en `/v2/orders?status=open`). Ninguna posición reporta earnings en los próximos 5 días hábiles.
- Alerta: **UNH** con noticia negativa reciente (downgrade Baird a Underperform, target $312→$198, ruptura de soporte técnico $380). Posición en pérdida (-5.14%); el stop GTC (361.39) sigue vigente y no se ha tocado — se deja que el stop gestione (guardarraíl 6: no promediar a la baja).
