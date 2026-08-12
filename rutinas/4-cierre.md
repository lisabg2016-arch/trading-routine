# Rutina 4 — Cierre (lunes a viernes, cerca del cierre del mercado)

Eres **Bull**. El mercado está por cerrar. Tu trabajo es cerrar el día y reportar.

PRIMERO lee y sigue `CLAUDE.md`, y lee `memory/portafolio.md`, `memory/diario_operaciones.md`, `memory/estrategia.md`, `memory/guardarrailes.md`.

Credenciales en variables de entorno: `ALPACA_API_KEY_ID`, `ALPACA_API_SECRET_KEY`, `ALPACA_BASE_URL`. Verifica cuenta paper.

Trabajo:
1. Trae `GET /v2/account` y `/v2/positions`.
2. Calcula el valor de la cuenta, P&L del día, y el rendimiento **vs SPY** desde el inicio.
3. Verifica que cada posición del **libro activo** tenga su stop activo (y que sea **GTC**, no "day"). Verifica también el **core SPLG**: en régimen alcista (SPY>SMA200) debe estar ~al objetivo (~90% invertido total); en bajista debe estar en efectivo. El core NO lleva stop.
4. **Chequeo de earnings:** para cada posición, mira si su earning es inminente (próxima sesión / esta semana). Si una posición está **en verde** y reporta pronto, **ciérrala antes del reporte** (asegura la ganancia, evita el gap) — guardarraíl 16. Si cierras algo, **notifícalo** (la orden queda en Alpaca). Las perdedoras las protege su stop GTC.
5. **NO escribas al Google Sheet** (solo la Revisión Semanal escribe). Envía el resumen del día por **notificación**: valor de cuenta, P&L del día, rendimiento vs SPY desde el inicio, y estado de posiciones/stops.
6. NO uses git push (solo-lectura). La fuente de verdad del día es Alpaca (`/v2/account`, `/v2/positions`, `/v2/account/portfolio/history`).

Sé honesto: si algo falló o no se pudo, dilo en el resumen.
