# Configuración — Bull (rutinas de trading)

## Estructura
```
trading-routine/
├── CLAUDE.md              # el "cerebro": cómo se comporta el agente
├── SETUP.md              # este archivo
├── .gitignore
├── memory/               # la memoria persistente (se lee y se actualiza cada rutina)
│   ├── estrategia.md
│   ├── guardarrailes.md
│   ├── watchlist.md
│   ├── portafolio.md
│   ├── diario_operaciones.md
│   ├── diario_investigacion.md
│   └── revision_semanal.md
└── rutinas/              # los prompts exactos de cada rutina
    ├── 1-premercado.md
    ├── 2-apertura.md
    ├── 3-mediodia.md
    ├── 4-cierre.md
    └── 5-revision-semanal.md
```

## Variables de entorno (van en el ENTORNO de la nube, NO en el repo)
Nombres EXACTOS (deben coincidir letra por letra con lo que dicen los prompts):
- `ALPACA_API_KEY_ID`     = tu API Key ID (PK...)
- `ALPACA_API_SECRET_KEY` = tu Secret Key
- `ALPACA_BASE_URL`       = https://paper-api.alpaca.markets
- (opcional) canal de aviso, p. ej. `NOTIFY_EMAIL` = tu correo

## Horarios sugeridos (cron) — zona horaria del mercado: America/New_York (ET)
| Rutina | Hora ET | Hora MT (tú) | Cron | Días |
|--------|---------|--------------|------|------|
| Pre-mercado | 8:00 | 6:00 | `0 8 * * 1-5` | L–V |
| Apertura | 9:30 | 7:30 | `30 9 * * 1-5` | L–V |
| Mediodía | 12:00 | 10:00 | `0 12 * * 1-5` | L–V |
| Cierre | 15:45 | 13:45 | `45 15 * * 1-5` | L–V |
| Revisión semanal | 16:00 (vie) | 14:00 | `0 16 * * 5` | Viernes |

Configura la zona horaria de la rutina en **America/New_York** para que los cron coincidan con el mercado.

## Pasos que faltan
1. [ ] Subir este proyecto a un repo de GitHub (privado).
2. [ ] En Claude Desktop: crear un **Entorno en la nube** con las variables de entorno de arriba.
3. [ ] Crear las **5 rutinas remotas**, cada una con su cron, su prompt (de `rutinas/`), el repo de GitHub y el entorno.
4. [ ] En cada rutina: Permisos → permitir **push sin restricción de rama** (para que pueda commitear a `main`).
5. [ ] Probar cada una con **"Run Now"** y leer la conversación para ajustar.
```
