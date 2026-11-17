# Cafetería — control de consumos y gastos

Aplicación de un solo archivo (`index.html`) para llevar la cuenta de lo que consume
cada cliente en una cafetería pequeña y pasarle el listado a fin de mes.

## Cómo se usa

Abre `index.html` con doble clic en cualquier navegador. No necesita instalación,
ni internet, ni servidor: **los datos se guardan en el propio navegador**
(`localStorage`), así que conviene descargar una copia de seguridad de vez en
cuando desde *Ajustes*.

### Aviso importante para Android

Abrir el archivo directamente desde el gestor de archivos del móvil es la peor
forma de usarla: Android suele dejar la página en un origen sin permiso de
almacenamiento, así que **no guarda nada** y las descargas se bloquean. La
aplicación lo detecta y avisa en pantalla, y si no puede descargar la copia de
seguridad te enseña el texto para que puedas guardarlo a mano.

Lo correcto es **abrirla desde una dirección web** (vale cualquier hosting
estático gratuito) y añadirla a la pantalla de inicio. Así guarda los datos, las
descargas funcionan y se abre como una app más.

**En el móvil** está pensada para usarla con una mano en la barra: la cabecera es
compacta, los listados se ven como fichas (sin scroll lateral), las ventanas suben
desde abajo y el ticket es un panel deslizante — mientras tocas productos ves el
total en la barra inferior, y pulsándola se abre el ticket para ajustar cantidades.
Cópiala al teléfono o publícala en cualquier hosting estático y añádela a la
pantalla de inicio para que se abra como una app más.

## Qué hace

| Pestaña | Para qué sirve |
| --- | --- |
| **Apuntar consumo** | Se elige el cliente, se tocan los productos que se lleva y se apunta en su cuenta. Debajo de cada nombre se ve lo que debe. |
| **Deudas** | Lo que debe cada cliente (consumido − pagado), con el detalle de movimientos y el botón de cobrar. |
| **Clientes** | Alta, edición y baja de clientes, con nota o teléfono, y el listado de deudas en PDF. |
| **Productos** | Catálogo con precios y categorías. Los productos se pueden ocultar sin borrarlos. |
| **Caja** | El balance acumulado, los ingresos directos (ventas cobradas en el momento) y los gastos del negocio. |
| **Informe mensual** | El listado de fin de mes por cliente: imprimir o guardar en PDF, exportar a CSV, copiar como texto (para WhatsApp) y marcar el mes como cobrado. |
| **Ajustes** | Nombre del negocio, moneda, copia de seguridad y borrado de datos. |

## El balance de arriba

En la cabecera van siempre cuatro cifras:

- **Ingresos** (verde): lo cobrado de verdad, sea al cobrar a un cliente o una venta
  de barra apuntada con el botón verde **+** que hay a su izquierda.
- **Gastos** (rojo): todo lo registrado en la pestaña Gastos.
- **Balance** (gris): ingresos − gastos. En positivo, las ventas ya han amortizado lo comprado.
- **Previsión por cobrar** (cian): lo que los clientes ya han consumido y aún no han
  pagado, y entre paréntesis cómo quedaría el balance si se cobrara todo.

Son cifras acumuladas desde el principio, no del mes. La pestaña *Gastos* las
desglosa con una frase que dice si ya se ha amortizado o cuánto falta.

## Detalles que conviene saber

- **Los precios quedan congelados en el apunte**: si mañana subes el café, lo ya
  apuntado conserva el precio del día en que se consumió.
- **La deuda es acumulada**, no mensual: es todo lo consumido menos todos los pagos
  registrados. El informe muestra a la vez el total del mes y el pendiente real.
- **«Marcar mes como cobrado»** registra un pago por el consumo del mes a cada
  cliente; úsalo cuando ya hayas cobrado de verdad.
- **Borrar un cliente borra también sus apuntes y sus pagos** (se pide confirmación).
- Los importes admiten coma o punto decimal y el CSV sale con `;` y coma decimal,
  listo para abrirlo en Excel en español.
