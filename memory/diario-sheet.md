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

## Cuándo registrar
- **Apertura**: una fila por cada operación colocada (Tipo=operacion).
- **Mediodía**: una fila si vendes o ajustas un stop (Tipo=gestion).
- **Cierre**: una fila con el resumen del día (Tipo=cierre) — valor de cuenta, P&L del día, vs SPY.
- **Revisión semanal**: una fila con el resumen de la semana (Tipo=review) — rendimiento, vs SPY, mejor/peor trade, calificación.
- **Pre-mercado**: opcional, una fila con el resumen de investigación (Tipo=investigacion).

Escribe filas concisas pero completas; este diario es la base de la revisión semanal.
