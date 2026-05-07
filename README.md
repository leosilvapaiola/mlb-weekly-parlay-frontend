# MLB Parlay Tracker - Frontend

Dashboard de seguimiento de apuestas MLB desplegado en GitHub Pages.

## � Páginas

| Página | URL | Propósito |
|--------|-----|-----------|
| `index.html` | [Tracker](https://leosilvapaiola.github.io/mlb-weekly-parlay-frontend/) | Seguimiento en vivo de la jornada |
| `stats.html` | [Tabla General](https://leosilvapaiola.github.io/mlb-weekly-parlay-frontend/stats.html) | Ranking general de jugadores |
| `dashboards.html` | [Estadísticas](https://leosilvapaiola.github.io/mlb-weekly-parlay-frontend/dashboards.html) | Dashboards avanzados |

## 🔌 Fuentes de Datos

- **Tracker en vivo** (`index.html`): lee de `GET /data` cada 30 segundos
- **Estadísticas** (`stats.html`, `dashboards.html`): leen de `GET /history` on-demand

Ambos endpoints están en API Gateway del backend AWS. No se requiere exportar ni pushear datos manualmente.

## 📊 Dashboards Disponibles

1. **Tabla General por Grupo** — Ranking separado por Grupo A y B
2. **Métricas Fav/NoFav** — Distribución de selección favorito/no favorito, aciertos, y recomendación semanal
3. **Rachas por jugador y grupos** — Aciertos por semana por grupo + grilla de rachas individuales

## ⚾ Features del Tracker

- Scores en tiempo real (auto-refresh 30s)
- Indicador de ganador anticipado (regla 5+ carreras)
- Sección "Resultados Hoy" con botón copiar para WhatsApp
- Botones de acceso rápido a Tabla General y Estadísticas

## 🛠️ Desarrollo

Para hacer cambios al frontend:
```bash
# Editar archivos HTML
# Push a GitHub Pages
git add .
git commit -m "descripción del cambio"
git push
```

GitHub Pages se actualiza automáticamente en ~1 minuto después del push.

## 📈 Analytics

Google Analytics (GA4) configurado con ID `G-1C21KF9QS6` en las 3 páginas.
Dashboard en [analytics.google.com](https://analytics.google.com).
