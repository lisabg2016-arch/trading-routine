# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-09-18 (pre-mercado)
- Valor de la cuenta (equity): $98,550.50 (last_equity $98,663.74 → ~-0.11% vs cierre anterior)
- Efectivo: $5,117.74 · Buying power: $282,082.68
- Régimen: **ALCISTA** — SPY $762.60 > SMA200 $715.87; QQQ $716.92 > SMA200 $662.08.
- Posiciones (libro activo/satélite, 5/5 — al máximo, todas con stop GTC confirmado):
  - CAT: 6 acc @ $816 → $799.00, P&L −$102 (−2.08%), stop GTC $767.69
  - GOOGL: 14 acc @ $342.51 → $354.40, P&L +$166.46 (+3.47%), stop GTC $322.95
  - MA: 8 acc @ $567.87 → $564.73, P&L −$25.12 (−0.55%), stop GTC $530.27
  - UNH: 12 acc @ $392.81 → $375.95, P&L −$202.33 (−4.29%), stop GTC $361.39
  - V: 13 acc @ $366.86 → $368.25, P&L +$18.11 (+0.38%), stop GTC $346.28
- Core: SPY 91.86 acc (fraccionaria) @ $775.18 → $760.54, valor ~$69,865 (~70% del equity), sin stop (gobernado por régimen 200D).
  **Nota de diseño:** `estrategia.md` especifica **SPLG** como instrumento de core (mismo índice, menor precio/fee); el core actual está en **SPY**, no SPLG. No se toca hoy (pre-mercado no opera); dejar para revisión en apertura/semanal si vale la pena migrar (costo: evento fiscal/spread al vender SPY y comprar SPLG en cuenta paper es irrelevante, pero requiere decisión explícita, no es urgente).
- Notas: ningún guardarraíl violado. Ninguna posición tiene earnings dentro de 5 días hábiles (ver diario de investigación). Ninguna noticia negativa aguda en las 5 posiciones del libro activo hoy.
