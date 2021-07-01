<!-- add-breadcrumbs -->
# Inventario recibido pero no facturado

Al recibir productos comprados, se realizan registros de acuerdo con el valor de los mismos en las cuentas Existencias Disponibles/Activos Fijos. Cuando se venden y entregan esos productos, se registra un gasto (costo de bienes vendidos), equivalente al valor de compra de los productos. 

A medida que aumenta el balance de existencias a través de Recibos de compra, la cuenta Almacén es debitada y se acredita una cuenta de ajuste llamada **Inventario recibido pero no facturado**. Al mismo tiempo, el gasto negativo es registrado en la cuenta principal con categoría "Valoración" o "Valoración y Total" en la tabla de impuestos y cargos, por el monto añadido con fines de valoración, para evitar el doble registro de gastos.

Al recibir la Factura del proveedor, se realizará una Factura de Compra desde el Recibo de Compra. Aquí la cuenta **Inventario recibido pero no facturado** es debitada, y por ende se anula el saldo en la cuenta.

El saldo en la cuenta Inventario recibido pero no facturado indica el valor de los productos para los cuales se ha creado el Recibo de Compra, pero tienen pendiente la facturación.
