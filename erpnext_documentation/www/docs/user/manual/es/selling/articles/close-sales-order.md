<!-- add-breadcrumbs -->
# Cerrar Orden de Venta

En la Orden de Venta validada se encuentra la opción **Cerrar**. Cerrar la Orden de Venta impide a los usuarios crear una Nota de Entrega y Factura de Venta desde la misma. 

<img alt="Close SO" class="screenshot"  src="{{docs_base_url}}/assets/img/articles/close-1.png">

#### Ejemplo

Se recibe una orden por diez Turbinas de Viento. La Orden de Venta también se crea por diez unidades. Debido a una falta de existencias, solo se envían siete unidades al cliente. Las tres unidades restantes serán entregadas prontamente. Sin embargo, el cliente informa que no quiere las unidades faltantes porque las compró a otro proveedor. 

En esta caso, se creará la Nota de Entrega y la Factura de Venta por siete unidades. Y la Orden de Venta debería ser cerrada. 

<img alt="Closed SO" class="screenshot"  src="{{docs_base_url}}/assets/img/articles/close-2.png">

Una vez que la Orden de Venta se cierra, no habrá cantidades pendientes (que en el ejemplo eran tres) lo cual se reflejará en los informes de Pendientes por Entregar y Pendientes por Facturar. Para realizar más transacciones desde una Orden de Venta Cerrada, en necesario abrirla nuevamente. 

La misma funcionalidad será encontrada en las Órdenes de Compra

<!-- markdown -->
