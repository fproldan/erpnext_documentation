<!-- add-breadcrumbs -->
# Listado de Precios

**Un Listado de Precios es una coleccion de Precios de Productos, sean estos de Venta, Compra, o ambos.**

ERPNext, a través de su función de Listado de Precios, permite mantener múltiples [Precios de Productos](/docs/user/manual/en/stock/item-price), tanto para Compras como para Ventas. 

Los Listados de Precios pueden utilizarse en situaciones donde es necesario tener distintos precios para distintas zonas (de acuerdo a los gastos de envío), o diferentes precios para diferentes monedas, etc. Un Producto puede tener precios múltiples de acuerdo con el cliente, la moneda, la región, los gastos de envío, etc, los cuales pueden ser almacenados como planes de precios diferentes. 

En ERPNext, todos los Precios de Productos son almacenados de forma separada. El Precio de Compra para un producto es diferente del Precio de Venta, y por ende, son almacenados por separado. 

Para acceder al Listado de Precio ir a: 

> Inicio > Comercialización/Compra/Existencias > Precios y Productos> Listado de Precios

<img class="screenshot" alt="Price List" src="{{docs_base_url}}/assets/img/stock/price-list.png">

## 1. Cómo utilizar un Listado de Precios

* Los Listados de Precios serán utilizados al crear el [Precio de Producto](/docs/user/manual/en/stock/item-price) a fin de registrar el precio de compra o venta de un producto determinado. 

* El Listado de Precios puede asignarse a países específicos. 

* Para desactivar un Listado de Precios determinado, desmarcar la casilla de verificación "Habilitado". Los Listados de Precios desactivados no podrán ser seleccionados en las transacciones de Compra y Venta.

* **Precio no dependiente de la UdM**: Pensemos en un producto como tomates que se compra en Cajas y se vende en Kilos. 1 Caja = 10 kilos y el precio de compra de 1 Kilo es 10 dólares. Si esta casilla está desactivada y se selecciona una Caja en la transacción, el precio se mostrará para un Kilo, debido a que ese es el único precio guardado para el Producto. 

    Ahora, si esta casilla esta seleccionada y se realiza una transacción por una Caja de tomates, entonces el precio será configurado automáticamente como 100 dólares debido a que el precio de una Caja (10 Kilos) es 100. 

* De forma predeterminada se crearán Listados de Precio Estándar tanto para Compra como para Venta. 

**Observación**: Si se cuenta con Listados de Precios múltiples, se puede seleccionar un Listado de Precios o asignárselo a un Cliente (de forma que sea seleccionado automáticamente). Los Precios de Productos serán actualizados automáticamente desde el Listado de Precios. 

### Temas Relacionados
1. [Precio de Producto](/docs/user/manual/en/stock/item-price)
