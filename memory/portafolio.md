# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Última actualización
- Fecha/hora: 2026-11-20 pre-mercado. Equity $93,776 (-0.01% vs cierre previo $93,787; -6.2% desde ~$100k inicial), efectivo $75,740 (~81%).
- Cuenta: PAPER, ACTIVE. Posiciones (libro activo, sin core): ABBV 16 @282.42 (+1.3%), CVX 22 @214.79 (-4.0%), JPM 14 @342.97 (-6.1%), MSFT 9 @525.62 (-6.6%).
- Órdenes abiertas: stop ABBV 259.83 GTC, stop CVX 205.00 GTC (a ~0.5% del precio), stop JPM 315.60 GTC (~2%), stop MSFT 483.60 GTC (~1.5%).
- Fills desde 11/18: 11/18 venta core SPY 104.51 @~729.8 (régimen). 11/19: compra ABBV 16 @282.42 + compra core SPYM 728 @~86.79 a la apertura; MRK salió por stop 34 @~134.45 (-8.0%); core SPYM vendido 728 @~84.82 al cierre (-2.3%, churn por régimen).
- Nuevas semana del 11/16: 2 de 3 (MSFT, ABBV).
- Régimen: BAJISTA. SPY 715.84 cierre IEX 11/19 (-2.0%) < SMA200 730.2 (-2.0%); QQQ 645.1 < SMA200 682.0 (-5.4%). Core en efectivo; NO abrir nuevas.
- Nota: instrumento core aparece como SPYM en Alpaca (SPLG renombrado).

## 2026-10-29 (pre-mercado)
- Contexto: SPY 772.28 vs SMA200 728 (ALCISTA), SMA50 768; QQQ 725.6 vs SMA200 679. Equity $100,443 (-0.13% vs cierre previo), efectivo $19,952.
- Posiciones: SPY core 91.86 (-0.8%), UNH 12 @392.81 (+5.1%), MRK 34 @146.13 (-1.2%). Stops GTC vigentes: MRK 134.50, UNH 405 (precio ~413).
- Earnings: MRK reporta hoy 10/29 9:00 ET (perdedora, protegida por stop; riesgo de gap). Ideas: ninguna (RECOM/target/earnings no confirmables -> fallo-cerrado). Sin órdenes.


## 2026-10-30 (pre-mercado)
- Contexto: SPY ~761 (pre) vs SMA200 ~723 (ALCISTA); QQQ ~698-715 vs SMA200 ~672 (caída fuerte el 10/29). Equity $99,844 (-0.61% vs cierre previo), efectivo $24,810.
- UNH cerrada 10/29 por stop GTC (12 @404.80, ~+3% vs entrada 392.81). Posiciones: SPY core 91.86 (-1.8%), MRK 34 @146.13 (+2.3%, post-earnings 10/29; stop GTC 134.50 vigente).
- Ideas: ninguna (RECOM/target/earnings no confirmables -> fallo-cerrado). Sin órdenes.

## 2026-11-02 (pre-mercado)
- Contexto: SPY 769.28 vs SMA200 ~710 (ALCISTA), SMA50 ~754; QQQ 716.4 vs SMA200 ~655. Equity $99,646 (+0.43% vs cierre previo $99,222), efectivo $10,310.
- Posiciones: SPY core 110.92 @772.69 (-1.7%), MRK 34 @146.13 (+2.8%; stop GTC 134.50 vigente). Única orden abierta: stop MRK GTC.
- Ideas: ninguna (RECOM/target/earnings no confirmables -> fallo-cerrado). Sin órdenes.

## 2026-11-03 (pre-mercado)
- Equity $98,591, efectivo $10,310. SPY core 110.92 (-2.8%), MRK 34 (+0.6%, stop 134.50 GTC). SPY 752 vs SMA200 ~729 (alcista, margen estrecho); QQQ ~en SMA200. Sin órdenes.

## 2026-11-04 (pre-mercado)
- Contexto: SPY ~761 vs SMA200 ~715 (ALCISTA), SMA50 ~759; QQQ ~709 vs SMA200 ~661. Equity $99,847, efectivo $10,310.
- Posiciones: SPY core 110.92 (-1.3%), MRK 34 @146.13 (+0.2%; stop GTC 134.50 vigente, única orden abierta). Ideas: ninguna (RECOM/target/earnings no confirmables -> fallo-cerrado). Sin órdenes.

## 2026-11-05 (pre-mercado)
- Contexto: SPY ~761 (último cierre IEX) vs SMA200 ~715 (ALCISTA), SMA50 ~759; QQQ ~709 vs SMA200 ~661. Equity $100,683 (+0.2% vs cierre previo $100,480), efectivo $10,310.
- Posiciones: SPY core 110.92 (-0.6%), MRK 34 @146.13 (+3.7%; stop GTC 134.50 vigente, única orden abierta). Ideas: ninguna (RECOM/target/earnings no confirmables -> fallo-cerrado). Sin órdenes.

## 2026-11-06 (pre-mercado)
- ALERTA: caída fuerte el 11/05: SPY 733.43 (-4.3%), QQQ 648.05 (-6.3%). SPY a ~0.4% de su SMA200 (~730, IEX) -> régimen al borde de cambiar a BAJISTA. QQQ ya bajo SMA200 (~681).
- Equity $96,797 (-3.7% desde $100,480 de 11/04; G9 aplica: no abrir nuevas), efectivo $10,310. SPY core 110.92 (-4.8%), MRK 34 @146.13 (-1.4%; stop GTC 134.50 única orden abierta).
- Ideas: ninguna (régimen frágil + fallo-cerrado). Sin órdenes. Si SPY cierra < SMA200, el core se vende a efectivo (estrategia.md) en rutina de operación.
