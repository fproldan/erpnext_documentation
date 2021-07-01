<!-- add-breadcrumbs -->
# Herramienta de Creación de Facturas de apertura

La Herramienta de Creación de Facturas de apertura permite importar en ERPNext los datos de Facturas de venta o compra pendientes. Esta herramienta es utilizada en reemplazo de la Importación de Datos para casos en los que la información del producto es irrelevante y se necesita importar en ERPNext los saldos pendientes con clientes/proveedores.

Para acceder a la Herramienta de Creación de Facturas de apertura, ir a:
> Inicio > Contabilidad > Apertura y cierre > Herramienta de Creación de Facturas de apertura

## Importación de facturas de apertura
1. Seleccionar la Compañía para la cual se desea importar los datos de apertura.
1. Seleccionar el Tipo de factura a generar.
1. Tildar la opción "Crear entidad faltante" hará que se creen automáticamente los clientes o proveedores que no existan en ERPNext pero sí en los registros que se están importando, basándose en el nombre provisto en la columna "Tercero".

![Opening Invoice Creation Tool](/docs/assets/img/setup/opening-invoice-creation-tool.png)

4. Completar la tabla "Facturas", compuesta por los siguientes campos:

    * **Tercero**: se puede seleccionar un cliente/proveedor existente o ingresar el nombre de uno nuevo, el cual será creado automáticamente.
    * **Fecha de Contabilización**: la fecha en la cual fue creada la factura.
    * **Fecha de vencimiento**: fecha de vencimiento de la factura.
    * **Nombre del producto**: (opcional) el nombre del producto aquí ingresado aparecerá en la tabla de productos de la factura.
    * **Monto pendiente**: monto pendiente de la factura.

> Tip: se puede hacer click en el botón "Descargar" para obtener un excel, el cual será más fácil de completar con los datos correspondientes. Una vez hecho esto se debe subir haciendo click en el botón "Subir". Así la tabla será completada automáticamente con todos los datos ingresados en el excel.
