# Diario en Google Sheets (persistencia real)

El diario persistente de Bull vive en una hoja de Google Sheets, escrita vía el **conector de Zapier** (la app "Google Sheets" ya está habilitada en la cuenta). Esto reemplaza el commit/push a GitHub (que en este entorno está en solo-lectura).

## Cómo escribir una fila
Usa la acción de Zapier **"Google Sheets: Create Spreadsheet Row"** (`add_row`) con:
- **spreadsheet** (ID): `1FewQ6IGe2qnL50E_hsgDqFyTabHJ-QJpKKUrw5mQTd0`  (hoja "Bull-Diario")
- **worksheet**: `Sheet1` (valor `0`)

## Mapa de columnas
| Columna | Campo | Qué poner |
|---------|-------|-----------|
| COL$A | Fecha | fecha (YYYY-MM-DD) |
| COL$B | Tipo | investigacion / operacion / gestion / cierre / review |
| COL$C | Simbolo | ticker (o "-") |
| COL$D | Accion | compra / venta / ajuste-stop / resumen / etc. |
| COL$E | Cantidad | nº de acciones (o "-") |
| COL$F | Precio | precio (o "-") |
| COL$G | P&L | P&L del día o del trade (o "-") |
| COL$H | vs.SPY | rendimiento vs SPY (o "-") |
| COL$I | Notas | tesis, contexto, lecciones, resumen |

## IMPORTANTE — evitar errores de fórmula (#ERROR! / #NAME?)
Google Sheets interpreta como **fórmula** cualquier celda que empiece con `=`, `+` o `-`. Los valores de
P&L y vs.SPY suelen empezar con `-` o `+` → salen como `#ERROR!`/`#NAME?` (pasó filas 19 y 25).
**Regla:** en P&L (COL$G), vs.SPY (COL$H) y cualquier celda que pudiera empezar con `-`/`+`/`=`,
**antepón un apóstrofo `'`** (fuerza texto) o empieza con una letra. Ejemplos:
- P&L: escribe `'-428.80 (-0.43%)` (con apóstrofo) en vez de `-428.80 (-0.43%)`.
- vs.SPY: escribe `'-1.36pp` en vez de `-1.36pp`.
- Alternativa: `PnL -428.80 (-0.43%)` (empieza con letra, también seguro).

## Cuándo registrar — SOLO SEMANAL (ahorro de cuota Zapier)
El Sheet se escribe **UNA sola vez por semana**: la **Revisión Semanal** del viernes (Tipo=review). Son ~4 filas/mes, dentro del plan gratis de Zapier.
- **Pre-mercado / Apertura / Mediodía / Cierre: NO escriben al Sheet.** Reportan por **notificación**; el registro real de trades/posiciones/P&L queda en **Alpaca** (fuente de verdad, `/v2/account/activities` y `/v2/account/portfolio/history`).
- La review **reconstruye la semana desde Alpaca**, no desde filas diarias del Sheet.
- Escribe la fila del review concisa pero completa (recuerda el apóstrofo en P&L/vs.SPY para evitar errores de fórmula).
