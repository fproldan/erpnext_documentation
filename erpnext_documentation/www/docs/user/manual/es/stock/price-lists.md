<!-- add-breadcrumbs -->
# Lista de Precios

**Una Lista de Precios es una colección de Precios de Productos, sean estos de Venta, Compra, o ambos.**

ERPNext, a través de la Lista de Precios, permite mantener múltiples [Precios de Productos](/docs/user/manual/es/stock/item-price), tanto para Compras como para Ventas. 

Las Listas de Precios pueden utilizarse en situaciones donde es necesario tener distintos precios para distintas zonas (de acuerdo a los gastos de envío), o diferentes precios para diferentes monedas, etc. Un Producto puede tener precios múltiples de acuerdo con el cliente, la moneda, la región, los gastos de envío, etc, los cuales pueden ser almacenados como planes de precios diferentes. 

En ERPNext, todos los Precios de Productos son almacenados de forma separada. El Precio de Compra para un producto es diferente del Precio de Venta, y por ende, son almacenados por separado. 

Para acceder al listado de Listas de Precio ir a: 

> Inicio > Ventas/Compras/Almacén > Productos y Precios > Lista de Precios

<img class="screenshot" alt="Price List" src="{{docs_base_url}}/assets/img/stock/price-list.png">

## 1. Utilización de una Lista de Precios

* Las Listas de Precios serán utilizadas al crear el [Precio de Producto](/docs/user/manual/es/stock/item-price) a fin de registrar el precio de compra o venta de un producto determinado. 

* La Lista de Precios puede asignarse a países específicos. 

* Para desactivar una Lista de Precios determinada, destildar la opción "Habilitado". Las Listas de Precios desactivadas no podrán ser seleccionadas en las transacciones de Compra y Venta.

* **Precio no dependiente de UdM**: considérese un producto como tomates que se compra en Cajas y se vende en Kilos. 1 Caja = 10 kilos y el precio de compra de 1 Kilo es $10. Si esta opción está destilda y se selecciona una Caja en la transacción, el precio se mostrará para un Kilo, debido a que ese es el único precio guardado para el Producto. 

    Ahora, si esta opción está tilda y se realiza una transacción por una Caja de tomates, entonces el precio será configurado automáticamente como $100 debido a que el precio de una Caja (10 Kilos) es 100. 

* De forma predeterminada se crearán Listas de Precio Estándar tanto para Compra como para Venta. 

**Observación**: Si se cuenta con múltiples Listas de Precios, se puede seleccionar una Lista de Precios o asignárselo a un Cliente (de forma que sea seleccionado automáticamente). Los Precios de Productos serán actualizados automáticamente desde la Lista de Precios.

* **Duplicar lista completa**: es posible crear una nueva Lista de precios usando de base otra existente. Para esto ingresar a la Lista que se desea duplicar, hacer click en el botón "Duplicar lista completa", ingresar el nombre y modificar si se desea algun aspecto de la nueva Lista y guardar. Hacer esto no solo ayuda a crear de forma sencilla una nueva lista sino que generará todos los Precios de Productos que existían para la Lista original, con la lista nueva en su lugar.

### Temas Relacionados
1. [Precio de Producto](/docs/user/manual/es/stock/item-price)
