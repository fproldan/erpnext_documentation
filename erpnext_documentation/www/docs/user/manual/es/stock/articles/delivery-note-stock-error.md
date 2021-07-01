<!-- add-breadcrumbs -->
# Error de Inventario en Nota de Entrega 

Puede darse el caso de que al validar una Nota de Entrega se reciba un mensaje advirtiendo que las existencias del producto son insuficientes, pero las mismas están disponibles en el Almacén. 

Esto se da porque al validar una Nota de Entrega, el nivel de existencias se revisa de acuerdo con la Fecha y Hora de contabilización de la misma. Es posible que haya existencias disponibles del Producto en el Almacén. Pero, si se está creando una Nota de Entrega con fecha anterior, y si los productos no estaban disponbiles en el almacén en esa Fecha y Hora de la Nota de Entrega, es muy probable que se reciba un mensaje de error respecto a las existencias negativas. Para confirmar esto, referirse al Mayor de Inventario. 

Si este es el caso, se deberá editar la Fecha y Hora de contabilización de la Nota de Entrega y asegurarse que es posterior a la Fecha y Hora de contabilización de la Entrada de inventario de recepción del producto. 
