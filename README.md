# ⚾ MLB Weekly Parlay Tracker - Frontend

Dashboard en tiempo real para visualizar apuestas de MLB.

## 🚀 Configuración

### 1. Obtener API URL del Backend

Después de deployar el backend:

```bash
cd ../mlb-weekly-parlay-backend/terraform
terraform output api_url
```

### 2. Actualizar index.html

Edita `index.html` y reemplaza `YOUR_API_GATEWAY_URL_HERE` con tu API URL:

```javascript
const API_URL = 'https://YOUR-API-ID.execute-api.us-east-1.amazonaws.com/prod';
```

### 3. Deploy a GitHub Pages.

#### Opción A: Desde GitHub UI

1. Push este repo a GitHub
2. Ve a Settings → Pages
3. Source: Deploy from a branch
4. Branch: `main` / `root`
5. Save

#### Opción B: Desde CLI

```bash
git add .
git commit -m "Initial commit"
git push origin main

# Habilitar GitHub Pages
gh repo edit --enable-pages --pages-branch main
```

### 4. Acceder al Dashboard

Tu dashboard estará disponible en:
```
https://YOUR-USERNAME.github.io/mlb-weekly-parlay-frontend/
```

## 🎨 Características

- ✅ Auto-refresh cada 30 segundos
- ✅ Indicadores visuales de ganador/perdedor
- ✅ Información de equipos (récord, pitcher, odds)
- ✅ Hora de inicio de juegos
- ✅ Responsive design

## 🔧 Desarrollo Local

```bash
# Servidor simple con Python
python3 -m http.server 8000

# O con Node.js
npx http-server
```

Luego abre: http://localhost:8000

## 📱 Mobile Friendly

El dashboard es completamente responsive y funciona en móviles.

## 🐛 Troubleshooting

### Error: CORS

Asegúrate de que el API Gateway tenga CORS habilitado (ya está configurado en el backend).

### No se cargan datos

1. Verifica que el API_URL esté correcto
2. Abre la consola del navegador (F12) para ver errores
3. Verifica que el backend esté deployado y funcionando

### GitHub Pages no actualiza

1. Espera 1-2 minutos después del push
2. Limpia el cache del navegador (Ctrl+Shift+R)
3. Verifica que GitHub Pages esté habilitado en Settings

## 📝 Licencia

MIT License
