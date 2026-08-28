# Portafolio (estado actual)

> La rutina actualiza este archivo en cada ejecución con datos reales de Alpaca (`GET /v2/account` y `/v2/positions`).

## Estado inicial
- Capital (paper): ~$100,000
- Efectivo: 100%
- Posiciones abiertas: ninguna
- vs SPY (desde inicio): 0.00%

## Última actualización
- Fecha/hora: 2026-08-28 12:44 UTC (pre-mercado)
- Valor de la cuenta (equity): $100,047.48
- Efectivo: $8,895.90 (~8.9%)
- Posiciones (market value): $91,151.58 (~91.1% invertido)
- Notas: datos en vivo desde `/v2/account` y `/v2/positions` (Alpaca es la fuente de verdad; esto es solo una foto de referencia).

## Posiciones abiertas (en vivo, pre-mercado 2026-08-28)
| Símbolo | Rol | Qty | Precio entrada | Precio actual | Valor mercado | P&L no realizado |
|---|---|---|---|---|---|---|
| SPY | Core (ver nota) | 85.851065749 | 775.98 | 771.84 | $66,263.29 | -$355.72 (-0.53%) |
| ABBV | Satélite | 20 | 248.99 | 258.80 | $5,176.00 | +$196.20 (+3.94%) |
| MSFT | Satélite | 10 | 487.89 | 506.03 | $5,060.30 | +$181.40 (+3.72%) |
| JPM | Satélite | 14 | 357.13 | 355.48 | $4,976.75 | -$23.09 (-0.46%) |
| CAT | Satélite | 6 | 816.00 | 815.31 | $4,891.86 | -$4.14 (-0.09%) |
| GOOGL | Satélite | 14 | 342.51 | 341.67 | $4,783.38 | -$11.76 (-0.25%) |

**Nota — desviación del core:** el core está en **SPY** (66.3% del equity), no en **SPLG** como indica `estrategia.md` (núcleo-satélite, decisión 2026-07-29). El libro activo (satélite) sí está completo y correcto: 5 posiciones, cada una ~5% del equity. Esta posición de SPY parece anterior a la decisión de usar SPLG como instrumento del core (cuenta creada 2026-07-24, decisión SPLG del 2026-07-29) y no se ha migrado. No se tocó hoy (rutina de pre-mercado = solo investigar, no operar); queda para que Apertura/Gestión lo evalúe.

## Régimen de mercado (pre-mercado 2026-08-28)
- **SPY**: $771.18 (cierre 2026-08-27) vs SMA200 ≈ $709.38 → **+8.7% por encima → régimen ALCISTA**.
- **QQQ**: $721.20 vs SMA200 ≈ $654.67 → **+10.2% por encima → alcista**, tech acompaña.
- Régimen alcista confirmado en ambos índices: sigue permitido abrir nuevas posiciones en el libro activo (satélite) si aparecen setups sanos.
