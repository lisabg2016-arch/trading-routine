# Diario de Operaciones

Registro de cada operación. La rutina agrega una fila cuando compra o vende.

| Fecha | Símbolo | Lado | Cantidad | Precio | Motivo / tesis | Stop | Resultado |
|-------|---------|------|----------|--------|----------------|------|-----------|
| 2026-07-28 | GE | buy | 13 | 363.97 (avg) | (no registrado en diario — reconstruido desde Alpaca activities) | GTC 350.75 | abierta, +1.49% |
| 2026-07-28 | JPM | buy | 14 | 357.13 (avg) | (no registrado en diario — reconstruido desde Alpaca activities) | GTC 331.60 | abierta, +0.11% |
| 2026-07-28 | UNH | buy | 11 | 419.12 (avg) | (no registrado en diario — reconstruido desde Alpaca activities) | GTC 392.00 | abierta, -2.87% |
| 2026-08-03 | NVDA | buy | 22 | 199.16 (avg) | (no registrado en diario — reconstruido desde Alpaca activities) | GTC 205.62 (trailed) | abierta, +12.20% |
| 2026-08-03 | AVGO | buy | 12 | 379.69 (avg) | (no registrado en diario — reconstruido desde Alpaca activities) | GTC 390.81 (trailed) | abierta, +12.41% |

**Nota de auditoría (2026-08-07):** este archivo estaba vacío pese a haber 5 operaciones reales en Alpaca. Las rutinas anteriores no escribieron aquí (probablemente porque su persistencia era solo el Google Sheet). Las filas de arriba se reconstruyeron desde `/v2/account/activities/FILL`; falta la tesis/motivo original de cada trade porque no quedó registrada en ningún lado accesible.
