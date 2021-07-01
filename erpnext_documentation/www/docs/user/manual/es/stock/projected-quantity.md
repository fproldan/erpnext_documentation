<!-- add-breadcrumbs -->
# Cantidad Proyectada

**La Cantidad Proyectada es el nivel de existencias que se predice para un Producto en particular de acuerdo con los niveles actuales y otros requerimientos.**

Es la cantidad de inventario bruto que incluye oferta y demanda en el pasado, que es realizado como parte del proceso de planificación.

El inventario proyectado es utilizado por el sistema de planificacion para monitorear el punto de pedido y la cantidad. La Cantidad proyectada es utilizada por el motor de planificación para monitorear los niveles de existencias mínimas. Estos niveles son mantenidos para satisfacer demandas inesperadas. 

Tener un control preciso del inventario proyectado es crucial para determinar faltantes y calcular la cantidad de pedido adecuada. 

<img class="screenshot" alt="Projected Quantity" src="{{docs_base_url}}/assets/img/stock/projected_quantity.png">

La fórmula para calcular la cantidad proyectada es como se muestra a continuación:

*Cantidad Proyectada = Cantidad Real + Cantidad Planeada + Cantidad Requerida + Cantidad Pedida - Cantidad Reservada - Cantidad Reservada para Producción - Cantidad Reservada para Subcontratación*

* **Cantidad Real**: Cantidad disponible en el Almacén. Estas son las existencias físicas reales que se tienen. 
* **Cantidad Planeada**: Cantidad para la cual se armó una Orden de Trabajo pero está pendiente de Fabricación. 
* **Cantidad Requerida**: Cantidad Requerida a través de una [Solicitud de Material](/docs/user/manual/es/stock/material-request). Se añade al validar la Solicitud y se quita cuando se crea una Orden de Compra/Orden de Trabajo/Entrada de inventario desde la misma de acuerdo con el tipo de Solicitud. 
* **Cantidad Pedida**: Cantidad pedida para Compra ([Orden de Compra](/docs/user/manual/es/buying/purchase-order)), pero no recibida a través de un [Recibo de Compra](/docs/user/manual/es/stock/purchase-receipt) o una [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice). 
* **Cantidad Reservada**: Cantidad pedida para venta por el Cliente ([Orden de Venta](/docs/user/manual/es/selling/sales-order)), pero no enviada (a través de una [Nota de Entrega](/docs/user/manual/es/stock/delivery-note)). Esta cantidad aumenta cuando se valida una Orden de Venta y disminuye cuando se crea y valida una Nota de Entrega o Factura de Compra desde esa Orden de Venta.
* **Cantidad Reservada para Producción**: Las materias primas son reservadas cuando se valida una [Orden de Trabajo](/docs/user/manual/en/manufacturing/work-order) y se reducen cuando las materias primas son transferidas al almacén de Trabajo en Curso a través de una Entrada de Inventario.
* **Cantidad Reservada para Subcontratación**: Materias primas reservadas cuando se valida una Orden de Compra de subcontratación. Cuando las materias primas son transferidas al Almacén del Proveedor a través de una Entrada de Inventario, esta cantidad se reduce. Para saber más respecto a subcontratación [click aquí](/docs/user/manual/en/manufacturing/subcontracting).

#### Temas Relacionados
1. [Almacén](/docs/user/manual/es/stock/warehouse)
1. [Solicitud de Material](/docs/user/manual/es/stock/material-request)
