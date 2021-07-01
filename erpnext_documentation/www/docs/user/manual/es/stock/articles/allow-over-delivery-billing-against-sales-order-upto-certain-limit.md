<!-- add-breadcrumbs -->
# Límite de sobre facturación/entrega contra Orden de Venta

Al crear una Nota de Entrega, el sistema valida si la cantidad de producto es la misma que en la Orden de Venta. Si la cantidad de producto es mayor, se recibirá un mensaje de validación de sobre-entrega o recepción. 

En el caso de ventas, si se quiere enviar más productos que los mencionados en la Orden de Venta, se debe actualizar el campo "Porcentaje permitido de sobreentrega/recibo" en el Producto.

<img alt="Itemised Limit Percentage" class="screenshot" src="{{docs_base_url}}/assets/img/articles/limit-1.png">

Al crear una factura, también se valida el precio del producto de acuerdo con la transacción anterior, como Orden de Venta. Esto también aplica al crear Recibo de Compra o Factura de Compra desde Orden de Compra. Al actualizar el campo "Porcentaje permitido de sobreentrega/recibo" éste se aplicará a todas las transacciones de compra y venta. 

Por ejemplo, si se pidieron 100 unidades de un producto, y si el porcentaje de sobre recepción es 50, entonces se podrá hacer un Recibo de Compra de hasta 150 unidades. 

El valor global para "Porcentaje permitido de sobreentrega/recibo" se actualiza desde las Configuración de Inventarios. El valor actualizado aquí será aplicable para todos los productos. 

1. Ir a `Almacén > Configuración > Configuración de Inventarios`

2. Configurar `Porcentaje permitido de sobreentrega/recibo`.

3. Guardar Configuración de Inventarios.

<img alt="Item wise Allowance percentage" class="screenshot" src="{{docs_base_url}}/assets/img/articles/limit-2.png">


<!-- markdown -->
