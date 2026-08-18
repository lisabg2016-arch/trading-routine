# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-08-18 (pre-mercado)
- Valor de la cuenta (equity): $100,003.01 | Efectivo: $14,209.81 (14.2%)
- P&L del día (vs. last_equity $100,357.20): ≈ −$354 (−0.35%)
- Posiciones (libro activo, 4/5): ABBV 20@248.99 (+1.21%), GE 13@363.97 (+0.84%),
  JPM 14@357.13 (+1.39%), NVDA 22@199.16 (+10.90%)
- Core: posición en **SPY** (no SPLG) por $66,053.81 (~66% del equity), −0.85% no realizado.
  ⚠️ Desviación de estrategia: `estrategia.md` especifica SPLG como instrumento del core;
  la posición real es SPY. No se actuó (rutina de pre-mercado no coloca órdenes) — revisar
  en Gestión/Cierre si conviene migrar a SPLG o si se mantiene así a propósito.
- Régimen: SPY cierre 772.62 (17-ago), SMA200 ≈705.86 (+9.46%), SMA50 ≈749.20 → **alcista**,
  nuevas posiciones permitidas por el filtro de régimen.
- Operaciones de la semana (desde el lunes): 0 aperturas nuevas registradas en Alpaca
  (solo una venta total de UNH el 17-ago) → quedan las 3 aperturas/semana disponibles.
- Vigilar: NVDA reporta earnings el 26-ago (después del cierre) y está en verde (+10.9%);
  aún no cae dentro de la ventana de 1-2 sesiones del guardarraíl 16, pero Gestión/Cierre debe
  vigilarlo esta semana para cerrarlo antes del reporte si sigue en verde.
- Notas: contexto de mercado hoy es risk-off (tensión Irán, petróleo y yields en máximos
  plurianuales, futuros de SPY/QQQ en rojo). No se colocaron órdenes (rutina de pre-mercado
  es solo investigación). Candidatas del día en el diario de investigación / notificación.
