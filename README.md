# 🗺️ Mapa Tele Salud — Municipalidad de Córdoba

Aplicación web interactiva de mapeo epidemiológico para la Secretaría de Salud de la Municipalidad de Córdoba, Argentina.

## 🔗 Ver mapa en línea

> **[👉 Abrir Mapa Tele Salud](https://TU_USUARIO.github.io/TU_REPOSITORIO/)**
> *(Reemplazá `TU_USUARIO` y `TU_REPOSITORIO` con tus datos de GitHub)*

---

## ✨ Funcionalidades

- 📍 **Búsqueda de dirección** — Geolocaliza una dirección dentro de Córdoba Capital y muestra los efectores más cercanos con distancia calculada
- 🏥 **Filtro por zona** — Filtra efectores por zona programática (Norte, Sur, Este, Oeste, Centro)
- 🏘️ **Búsqueda por barrio** — Busca un barrio y muestra su polígono en el mapa con los efectores dentro, CPC, Zona y Área Programática
- 📊 **Panel de centros** — Información detallada de cada efector: horarios, servicios, atenciones
- 🗺️ **Capas GeoJSON** — Visualización de zonas, áreas programáticas, seccionales y departamentos

---

## 📁 Estructura del proyecto

```
├── index.html              ← Aplicación principal (todo en un archivo)
├── assets/                 ← Imágenes e íconos
│   ├── CS.png
│   ├── EFECTORES.png
│   ├── HOSP-HPA-PLM.png
│   └── ...
├── data/                   ← Datos de efectores y centros
│   ├── efectores.geojson       ← Puntos de todos los efectores
│   ├── centros_horarios.json   ← Horarios y CPC
│   ├── atenciones_centros.json ← Estadísticas de atenciones
│   ├── servicios_centros.json  ← Servicios por centro
│   ├── HorariosEfectores.json  ← Horarios detallados
│   └── zonas_valores.json      ← Valores por zona
└── layers/                 ← Capas geográficas GeoJSON
    ├── barrios_cordoba.json    ← Polígonos de barrios (485 barrios)
    ├── ZONA.json               ← Zonas programáticas
    ├── AP.json                 ← Áreas programáticas
    ├── CIRCUITO_SECCIONALES.json
    ├── DEPARTAMENTOS.json
    └── zonas_completas.json
```

---

## 🚀 Cómo publicar en GitHub Pages

1. **Crear repositorio en GitHub** (público)
2. **Subir todos los archivos** (excepto la carpeta `backup/` y `.claude/`)
3. Ir a **Settings → Pages**
4. En *Source* seleccionar: `Deploy from a branch` → `main` → `/ (root)`
5. Guardar — en unos minutos el mapa estará disponible en `https://TU_USUARIO.github.io/TU_REPOSITORIO/`

---

## 🛠️ Tecnologías utilizadas

| Tecnología | Uso |
|---|---|
| [Leaflet.js](https://leafletjs.com/) | Motor de mapas interactivo |
| [CartoDB Voyager](https://carto.com/basemaps/) | Tiles del mapa base |
| [Nominatim (OpenStreetMap)](https://nominatim.org/) | Geocodificación de direcciones y polígonos de barrios |
| HTML / CSS / JavaScript | Interfaz completa en un solo archivo |

---

## 📌 Notas

- El mapa funciona completamente en el navegador, sin servidor backend
- Los datos de efectores corresponden a la red de salud municipal de Córdoba Capital
- La búsqueda de barrios usa primero OpenStreetMap (Nominatim) y, si no encuentra resultado, usa el JSON local como fallback

---

*Municipalidad de Córdoba — Secretaría de Salud*
