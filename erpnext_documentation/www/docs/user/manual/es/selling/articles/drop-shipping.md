<!-- add-breadcrumbs -->
# Envío Triangulado

El **Envío Triangulado** es una técnica de administración de la cadena de suministro en la cual el vendedor no mantiene existencias de los productos. En cambio, transfiere los pedidos de los clientes y los detalles de envío al fabricante, a otro vendedor o a un mayorista, quien se encarga de enviar directamente los bienes al cliente. 

En ERPNext, se puede administrar el Envío Triangulado creando una Orden de Compra desde la Orden de Venta. 

> Ventas > Documentos > Orden de Venta > Orden de Compra

#### Configuración en el Producto

Configurar **_Entregado por el Proveedor (Envío Triangulado)_** y el **_Proveedor_** predeterminado.

<img class="screenshot" alt="Setup Item Master" src="{{docs_base_url}}/assets/img/selling/setup-drop-ship-on-item-master.png">

#### Configuración en la Orden de Venta
Si el Envío Triangulado fue configurado en el Producto, entonces en la Orden de Venta de ese producto, se establecerá automáticamente la configuración **Entregado por el Proveedor** y el **Proveedor** encargado de tal envío. 

Se puede configurar el Envío Triangulado para el Producto desde la Orden de Venta. Ir a la sección **Envío Triangulado**, configurar **Entregado por el Proveedor** y seleccionar el **Proveedor** al cual se le enviará la Orden de Compra. 

<img class="screenshot" alt="Setup Drop Shipping on Sales Order Item" src="{{docs_base_url}}/assets/img/selling/setup-drop-ship-on-sales-order-item.png">

#### Creación de la Orden de Compra
Luego de validar la Orden de Venta, crear la Orden de Compra. 

<img class="screenshot" alt="Setup Drop Shipping on Sales Order Item" src="{{docs_base_url}}/assets/img/selling/drop-ship-sales-order.png">

Desde Orden de Venta, todos los Productos que tengan tildada la opción **Entregado por el Proveedor**  o **Proveedor** (coincidente con el proveedor seleccionado en la ventana emergente Para Proveedor) mencionado, serán llevados a la Orden de Compra.

Automáticamente se configurará el Cliente, su Dirección y la persona de Contacto. 

Luego de validar la Orden de Venta, para actualizar el estado de envío, utiizar el botón **Marcar como Entregado** en la Orden de Compra. De esa forma se actualizará el porcentaje de envío y la cantidad enviada en la Orden de Venta. 

<img class="screenshot" alt="Purchase Order for Drop Shipping" src="{{docs_base_url}}/assets/img/selling/drop-ship-purchase-order.png">

<span style="color:#18B52D">**_Cerrar_**</span>, es una función de **Orden de Compra** y **Orden de Venta**, a fin de cerrar o marcar el cumplimiento.

<img class="screenshot" alt="Close Sales Order" src="{{docs_base_url}}/assets/img/selling/close-sales-order.png">

### Envío Triangulado en Formato de Impresión
Se puede notificar a los Proveedores enviándoles un email luego de validar la Orden de Compra adjuntando el Envío Triangulado en formato de impresión. 

<img class="screenshot" alt="Drop Dhip Print Format" src="{{docs_base_url}}/assets/img/selling/drop-ship-print-format.png">
