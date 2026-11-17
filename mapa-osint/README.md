# OSINTMap · mapa de fuentes abiertas

Aplicación web de un solo archivo (`index.html`, sin compilación) para explorar el mundo, seleccionar
regiones, cargar los elementos de fuentes abiertas que hay en ellas, marcarlos y exportarlos a ATAK y
otras herramientas SIG.

Ábrela con doble clic o sírvela con cualquier servidor estático (`npx serve mapa-osint`).

## Funciones
- **Mapas base**: Esri (calles, satélite, topográfico, grises), **ortofoto PNOA y mapa del IGN** (España), OpenTopoMap y,
  servidos desde web, OSM/CARTO/HOT. Capas superpuestas: **Catastro** (clic en una parcela → referencia catastral, dirección,
  uso, superficie y año de construcción), etiquetas IGN, carreteras, ferrocarril y relieve.
- **Búsqueda** de lugares (Nominatim) o coordenadas en DD, DMS, DDM, UTM y MGRS.
- **Regiones** rectangulares, poligonales, circulares, con la vista actual o a partir de un resultado de búsqueda.
- **Fuentes**: OpenStreetMap vía Overpass API (restaurantes, comercios, cámaras de vigilancia/tráfico/webcams,
  semáforos, salud, emergencias, hidrantes, administración, transporte, antenas, energía, calles, puentes,
  vías férreas, líneas eléctricas…) y artículos de Wikipedia geolocalizados.
- **Precisión**: cada categoría permite elegir tipos concretos (p. ej. solo «Restaurante», sin bares ni cafeterías).
  Además puedes crear **categorías personalizadas** con cualquier etiqueta OSM (`amenity=atm & operator~santander`).
- **Fiabilidad**: cada elemento de OSM recibe una puntuación 0–100 (nombre coherente con el tipo, horario, teléfono,
  web, fecha de revisión, etiquetado mixto, FIXME…). Se pueden ocultar los posibles cerrados, filtrar por confianza
  y **confirmar manualmente** cada elemento tras revisarlo en Street View / Mapillary.
- **Descartar** elementos, **deshacer / rehacer** (Ctrl+Z / Ctrl+Y) e **iconos** por tipo editables.
- **Marcar / desmarcar** elementos uno a uno, por filtro o dibujando un área; marcadores propios.
- **Exportar**: ATAK Data Package (.zip con CoT), KML, KMZ, GeoJSON, GPX y CSV.
- **Importar**: GeoJSON, KML/KMZ, GPX, CSV, CoT y Data Packages de ATAK (también arrastrando archivos al mapa).
- **Configuración** al estilo Google Earth: formato de coordenadas, unidades, retícula lat/lon o UTM/MGRS,
  escala, navegación, posición inicial, tema, servidor Overpass y parámetros de CoT.
- Medición de distancias, áreas y rumbos.

El estado (regiones, marcados, ajustes) se guarda en el `localStorage` del navegador.
Respeta las políticas de uso de Overpass, Nominatim y los proveedores de teselas.
