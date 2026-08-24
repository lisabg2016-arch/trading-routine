# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-08-24 (pre-mercado)
- Valor de la cuenta (equity): $99,480.67 (last_equity $99,645.38 → día previo ~-0.17%)
- Efectivo: $9,167.46 (~9.2%) | Valor posiciones: $90,313.21 (~90.8% invertido)
- Posiciones (libro activo, 5/5 — al máximo):
  - ABBV: 20 acc @ $248.99 → $266.62 (+7.08%, +$352.60)
  - CAT: 6 acc @ $816.00 → $819.00 (+0.37%, +$18.00) — intradía -1.07% hoy
  - GOOGL: 14 acc @ $342.51 → $343.81 (+0.38%, +$18.20)
  - JPM: 14 acc @ $357.13 → $351.85 (-1.48%, -$73.94)
  - NVDA: 22 acc @ $199.16 → $214.71 (+7.81%, +$342.10)
- Core (núcleo-satélite): posición SPY 85.851065749 acc @ $775.98 → $764.16 (-1.52%, -$1,015.06).
  Nota: `estrategia.md`/`watchlist.md` dicen que el instrumento del core debe ser **SPLG**, no SPY —
  esta posición existente es SPY. Discrepancia detectada 2026-08-24; NO se toca en pre-mercado
  (rutina informativa, no opera), queda para revisión/decisión en Apertura o Revisión Semanal.
- Régimen: SPY (764.16) > SMA200 (~707.52) → **alcista** (+8.0% sobre SMA200). Núcleo-satélite: mantener core.
- Notas: libro activo al máximo (5/5) — no se pueden abrir nuevas posiciones hasta liberar un cupo
  (guardarraíl 3). **NVDA reporta earnings el miércoles 2026-08-26 tras cierre** — posición en verde,
  dentro de la ventana de 1-2 sesiones → aplica guardarraíl 16 (cerrar antes del reporte). Ver diario
  de investigación de hoy para detalle y catalizadores.
