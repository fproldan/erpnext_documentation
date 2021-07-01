<!-- add-breadcrumbs -->
# Informe de Nivel de Stock

El Informe de Nivel de Stock muestra las cantidades de productos disponibles en un almacén en particular. 

Hay muchos informes disponibles para observar el nivel de stock de los productos. 

#### Informe de Cantidad de inventario proyectada

Se puede acceder a este informe desde
> Inventario > Reportes de Stock > Cantidad de inventario proyectada

Este informe muestra los niveles de existencias en base a productos y depósitos teniendo en cuenta todas las transacciones de existencias. Muestra la Cantidad Real de un producto pero también da otros detalles como: 

1. Cantidad Real: Cantidad disponible en el almacén.
2. Cantidad Planeada: Cantidad para la cual se ha creado una Orden de Trabajo pero que está pendiente de fabricación. 
3. Cantidad Requerida: Cantidad requerida para compra pero todavía no pedida.
4. Cantidad Pedida: Cantidad pedida para compra, pero no recibida.
5. Cantidad Reservada: Cantidad pedida para venta pero no enviada.
6. Cantidad Proyectada: se calcula de la siguiente manera:

<div class="well">Cantidad Proyectada = Cantidad Real + Cantidad Planeada + Cantidad Requerida + Cantidad Pedida - Cantidad Reservada</div>

El inventario proyectado es utilizado por el sistema de planeación para determinar el punto de pedido y la cantidad de pedido. La Cantidad proyectada es utilizada por el motor de planificación para monitorear los niveles de existencias mínimos. Estos niveles son mantenidos para satisfacer demandas inesperadas. 

Tener un control preciso del inventario proyectado es crucial para determinar faltantes y calcular la cantidad de pedido adecuada. 
