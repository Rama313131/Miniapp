# Calendario anual · tareas, eventos y gastos

Aplicación de un solo archivo HTML. **No necesita instalación ni servidor**: basta
con abrir `index.html` con doble clic en cualquier navegador (Chrome, Edge, Firefox,
Safari). Funciona sin conexión y no envía datos a ningún sitio.

## Qué hace

- **Panel anual completo**: los 12 meses a la vista en **3 filas de 4 meses**,
  centrado en la pantalla (pasa a 3, 2 y 1 columna al estrechar la ventana). Las
  semanas empiezan en lunes y el día de hoy va resaltado.
- **Aspecto de juego, en modo oscuro**: fondo oscuro con marcadores de colores
  vivos, nivel y barra de XP (10 XP por cada anotación que marcas como hecha),
  racha de días seguidos, barra de progreso y trofeo en cada mes, logros
  desbloqueables y confeti al completar algo. El botón 🌙/☀️ cambia a modo claro
  si algún día lo prefieres.
- **Colores a tu gusto**: el botón 🎨 Colores permite dar a cada categoría el
  color que quieras (16 colores rápidos o el selector del sistema). El número del
  día se pone claro u oscuro solo para que siempre se lea. «Restaurar los de
  fábrica» vuelve a los colores originales.
- **Anotaciones por día**: pincha en cualquier día para añadir tareas, eventos,
  citas, cumpleaños o pagos. Cada anotación admite hora, notas y categoría; el día
  se pinta con el color vivo de su categoría (a dos o tres bandas si hay varias),
  así que se ve de un vistazo qué hay anotado.
- **Anexo de importe**: cualquier anotación puede llevar un importe (por ejemplo
  *Seguro del coche · 412,50 €*). Los días con gasto llevan una moneda dorada en
  la esquina, y los días con todo hecho una marca verde.
- **Total gastado bajo cada mes** y **total del año** en la barra superior, con
  desglose por categoría al pie de la página.
- **Repeticiones**: «cada mes» o «cada año», con fecha de fin opcional. Al borrar
  una anotación repetida puedes quitar solo ese día o toda la serie.
- **Filtros**: búsqueda por texto, por categoría, «solo con importe» y «solo
  pendientes». Los totales se recalculan según el filtro activo.
- **Moneda configurable** (EUR, USD, GBP, MXN, ARS, COP, CLP, BRL).
- **Marcar como hecho** cada anotación (día a día en las repetidas).
- **Imprimir** el año en 3 columnas y **copia de seguridad** en JSON (botón
  «Datos»: copiar para guardar, pegar para restaurar).
- Animaciones desactivadas si el sistema pide reducir el movimiento, e impresión
  siempre sobre fondo blanco aunque estés en modo oscuro.

## Dónde se guardan los datos

En el almacenamiento local del navegador (`localStorage`) del equipo donde abras
el archivo. No hay cuenta ni servidor. Consecuencias prácticas:

- Si cambias de navegador o de dispositivo, no verás las anotaciones: usa el
  botón **Datos → Copiar** para llevártelas y **Datos → Importar** para
  restaurarlas. La copia incluye también la moneda, los colores elegidos y el
  tema. Ojo: importar **sustituye** lo que hubiera, no lo fusiona.
- Borrar los datos de navegación del sitio borra también las anotaciones.
- En modo incógnito se pierden al cerrar la ventana.

## Atajos

- `Esc` cierra la ventana abierta.
- Botón **Hoy**: vuelve al año actual y abre el día de hoy.
