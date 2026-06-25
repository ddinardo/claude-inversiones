# Inversiones — Centro de Comando

Gestión y análisis de portafolio multiactivo con seguimiento diario de mercados.

## Estructura

```
inversiones/
├── acciones/              — Análisis de acciones individuales
├── bonos/                 — Seguimiento de bonos y renta fija
├── monedas/               — Forex y divisas
├── criptomonedas/         — Crypto (Binance, 3Commas)
├── plataformas/           — Scripts, bots y configuraciones por plataforma
│   ├── tradingview-pine/  — Indicadores y estrategias en Pine Script
│   ├── 3commas/           — Bots DCA y configuraciones
│   ├── binance/           — API keys y estrategias spot/futures
│   ├── mt5/               — Expert Advisors y backtests
│   ├── interactive-brokers/ — TWS scripts y reportes
│   └── exness/            — Configuraciones y resultados
└── analisis-diario/       — Rutina diaria de evaluación de mercados
    ├── reportes-lovable/  — Informes de https://valordeacciones.lovable.app
    ├── coherencia-predicciones/ — Tracking de aciertos vs predicciones
    ├── apertura-japon/    — Sesión asiática (23:00–08:00 UTC)
    ├── apertura-europa/   — Sesión europea (07:00–16:00 UTC)
    └── apertura-america/  — Sesión americana (13:00–22:00 UTC)
```

## Flujo de trabajo diario

1. **Pre-apertura Japón** (~22:30 UTC) — revisar macro Asia
2. **Apertura Europa** (~07:00 UTC) — leer reporte Lovable del día
3. **Apertura América** (~13:00 UTC) — evaluar coherencia de predicciones
4. **Cierre** — registrar aciertos/errores en `coherencia-predicciones/`
