# Revisión Semanal (viernes)

Resumen honesto de la semana. La rutina del viernes lo llena.

## Semana del 2026-08-03 al 2026-08-07
- Valor de cuenta (inicio → fin): $99,822.54 (cierre viernes 07-31) → $101,043.08 (cierre viernes 08-07)
- Rendimiento de la semana: **+1.22%** ($+1,220.54)
- Acumulado desde inicio (2026-07-24, $100,000): **+1.04%**
- **vs SPY esta semana: -2.31pp** (SPY 746.79→773.16, +3.53%) — la vara honesta
- **vs SPY acumulado: -3.59pp** (SPY 738.90→773.16 desde inicio, +4.64%)
- Operaciones nuevas esta semana: 2 (NVDA, AVGO, ambas 2026-08-03) | 0 cierres/ventas | dentro del límite de 3 nuevas/semana
- Posiciones totales: 5/5 (máximo alcanzado) — AVGO, GE, JPM, NVDA, UNH
- Mejor performer (no realizado): AVGO +12.41% (+$565.44) y NVDA +12.20% (+$534.38)
- Peor performer (no realizado): UNH -2.87% (-$132.49), lejos aún de su stop (-8% máx.)
- No hubo trades cerrados esta semana → no hay P&L realizado que reportar como mejor/peor "trade" en sentido estricto.
- ¿Se respetaron los guardarraíles? **Sí, en todo lo verificable con datos de Alpaca**: solo paper, tamaños de entrada ≤5%, máximo 5 posiciones respetado, ritmo de nuevas posiciones (≤3/semana) respetado, todas las posiciones con stop **GTC** dentro de -8% de riesgo, ninguna promediada a la baja, sin apalancamiento/opciones, solo símbolos de watchlist, sin breach de -3% diario ni de -15% circuit breaker, régimen SPY>SMA200 intacto (SPY 773.16 vs SMA200 702.94).
  - **No verificable retroactivamente** (guardarraíles 13-17: RECOM, target price, cercanía de earnings, noticias negativas) — no hay registro de esos checks al momento de comprar NVDA/AVGO ni de las operaciones previas. Se asume que se hicieron (están descritos como obligatorios en la rutina de apertura) pero no hay evidencia archivada.
- Qué funcionó: la disciplina de stops (todos GTC, todos dentro del límite de riesgo, varios ya trailed hacia arriba en AVGO/NVDA). Ritmo de apertura respetado.
- Qué no funcionó: **75.9% del portafolio en efectivo** durante una semana de rally fuerte de SPY (+3.53%) — la baja exposición es la causa principal del rezago vs SPY, no una mala selección (AVGO/NVDA rindieron +12% cada uno). Además, **hueco de auditoría**: `diario_operaciones.md` y `diario_investigacion.md` locales estaban vacíos pese a 5 operaciones reales — reconstruidos hoy desde Alpaca, pero sin la tesis original de cada trade.
- Ajustes propuestos: (1) no forzar más exposición — la selección discrecional es el edge, no hay que romperla por FOMO de una semana; (2) corregir el hueco de registro para que las rutinas diarias dejen tesis/motivo en el diario (Sheet o archivo local) en el momento de la compra, no reconstruido después; (3) **incidente de infraestructura**: el conector de Zapier a Google Sheets devolvió "insufficient tasks on account" tanto en lectura como en escritura durante esta revisión — el diario en Sheets probablemente no se ha estado actualizando. Revisar/renovar la cuota de Zapier cuanto antes.
- **Nota de autocrítica (calificación de la semana): B-.** Proceso y guardarraíles respetados sin excepción verificable; el resultado quedó por debajo de SPY por baja exposición (no por mala selección) en una semana alcista fuerte. Se resta un poco por el hueco de auditoría en el diario local.
