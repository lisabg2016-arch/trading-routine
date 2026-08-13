# Watchlist (universo permitido)

Solo se puede operar lo que está en esta lista. Es el universo de MONITOREO; cada rutina revisa a diario si un nombre está en un setup sano (tendencia alcista + retroceso ordenado, evitando cuchillos cayendo y extensión vertical) antes de decidir. **Estar en la lista NO es una orden de compra.**

## Referencia de mercado y CORE (no son trades activos)
- **SPY**: señal de **régimen** (200D) y **benchmark**. NO se compra como trade activo.
- **SPLG**: instrumento del **core** núcleo-satélite (se mantiene con el efectivo ocioso en régimen alcista; ver `estrategia.md`). NO cuenta como posición del libro activo. **No disponible en Alpaca desde al menos 2026-08-13** (`/v2/assets/SPLG` → asset not found) — mientras dure, el core usa **SPY fraccionario** en su lugar (ver nota en `estrategia.md`).
- **QQQ**: solo referencia (tech). NO se compra.

## Semiconductores / IA (sleeve medido — sector en auge)
- NVDA, AVGO, LRCX, AMD
- (Se opera CON el filtro de régimen: SPY<200d = no abrir semis. Eso es lo que los hace
  manejables — te saca en los crashes. Sleeve acotado a propósito: en un pinchazo del ciclo
  semi devuelven mucho. Alternativas: KLAC/AMAT/MU/TSM.)

## Financieras
- JPM, V, MA, BAC, AXP

## Salud
- UNH, ABBV, JNJ, MRK, LLY

## Consumo básico / defensivo
- KO, PG, COST, WMT

## Industriales
- CAT, GE, RTX, HON

## Energía
- XOM, CVX, COP

## Tecnología (mega-cap estable)
- AAPL, MSFT, GOOGL

## Servicios públicos (baja volatilidad)
- NEE

---
## Filtros de analistas (aplicados 2026-07-29, RE-VERIFICAR en vivo antes de comprar)
- **RECOM (recomendación media de analistas, 1=Strong Buy .. 5=Sell): comprar solo si ≤ 2.5.**
  Quitados por RECOM>2.5: GS (2.60), PEP (2.67), SO (2.67). Si el RECOM de un nombre sube sobre 2.5,
  el bot deja de comprarlo (aunque ya lo tenga, no promedia/añade).
- **Target price: NUNCA comprar por encima del target price medio de analistas**, salvo que haya
  upgrades o subidas de target RECIENTES. Al 2026-07-29 estaban ARRIBA de su target: **KO (−0%), AAPL (−4%)**
  → siguen en la lista pero NO comprables hasta que retrocedan bajo el target o les suban el target.
  Poco margen (<5%, comprar con cuidado): MRK, ABBV.
- Estos valores cambian; **el bot debe re-checarlos en vivo** (Finviz Elite / datos de analistas) antes de cada compra.

---
## Nota de diseño (2026-07-29): diversificación CON sleeve de semis
Rebalanceada tras un backtest por-símbolo (2016-2026, filtro SPY>200d, stop −8%+trail, 20%/trade,
fills en apertura, costes). Hallazgo clave: **con el filtro de régimen, los semis NO son mal terreno
en esta era** — son de los mejores (NVDA/AMD/LRCX/KLAC/AMAT: +100/+218%, maxDD solo −10/−14%,
Profit Factor alto). El filtro de régimen te SACA de los semis en los crashes (2018/2022), que es
lo que los vuelve manejables. (El −76/−100% de NVDA que vimos antes era un artefacto de empezar en
1999 con puntocom+2008 y 100% equity.) Por eso:
- **Sleeve de semis medido** (NVDA, AVGO, LRCX, AMD) — acotado porque es era-IA + supervivencia;
  en un pinchazo del ciclo semi devuelven mucho. Se descartaron los semis flojos: QCOM, NXPI, ADI, MRVL, TXN.
- **Quita** proxies/growth de peor perfil: CRWD, PANW (ciber), COIN, MSTR (cripto), MU/TSM (semis
  de segundo nivel, opcionales), META/AMZN (opcionales, buen PF pero mayor beta).
- **Mantiene** un núcleo diversificado de large-caps de calidad en 7 sectores (financieras, salud,
  consumo básico, industriales, energía, tech estable, utilities).
Evitar penny stocks (<$10) e ilíquidos. Revisar/actualizar periódicamente; las tendencias cambian.
Script del ranking: `C:\Users\lisab\Desktop\YOUTUBE\bull_backtest\per_symbol_rank.py`.
