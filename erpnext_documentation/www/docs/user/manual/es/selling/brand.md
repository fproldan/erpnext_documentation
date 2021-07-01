<!-- add-breadcrumbs -->
# Marca

**Una Marca identifica productos, relacionándolos con un nombre específico.**

Normalmente una Marca es el fabricante o empaquetador de un producto específico. Por ejemplo, Apple es una marca que fabrica laptops. Una Marca no es necesariamente el [Fabricante](/docs/user/manual/en/stock/manufacturer) de un producto, es simplemente el nombre bajo el cual se vende dicho producto. Por ejemplo, si una empresa fabrica vasos de plástico, le puede ceder la licencia a una gran marca para que los venda bajo su nombre.

En ERPNext, se pueden asignar Marcas a los Productos para identificar y asignar ciertas configuraciones predeterminadas.

Para acceder al listado de Marcas ir a: 

> Inicio > Almacén > Configuración > Marca

## 1. Creación de una Marca
1. Ir al listado de Marcas y hacer click en Nueva.
1. Ingresar el nombre de la Marca y su descripción si fuese necesario.
1. Guardar.

    ![Marca](/docs/assets/img/selling/brand.png)

Ahora esa Marca puede ser asociada a diferentes Productos. 

![Marca en Producto](/docs/assets/img/selling/brand-in-item.png)

## 2. Características
### 2.1 Establecer configuraciones predeterminadas para productos de una Marca

![Configuraciones predeterminadas de Marca](/docs/assets/img/selling/brand-defaults.png)

Para una Marca pueden establecerse las siguientes configuraciones predeterminadas. Al asignar esa Marca a un Producto, la configuración establecida se utilizará al realizar trasacciones de Compra/Venta con Productos pertenecientes a esa Marca. 

* **Almacén predeterminado**: El almacén desde el cual el Producto será obtenido o donde será almacenado, dependiendo de la transacción. 
* **Lista de precios predeterminada**: La Lista de Precios configurada será utilizada al realizar transacciones de Compra/Venta. 

#### Configuraciones de Compra
Al realizar transacciones de Compra como una Orden de Compra, Recibo de Compra, o Factura de Compra, se utilizarán las configuraciones establecidas en esta sección al seleccionar un Producto de esta Marca. 

* Centro de Costo de Compra Preestablecido
* Proveedor Preestablecido
* Cuenta de Gastos Preestablecida 

#### Configuraciones de Venta
Al realizar operaciones de Venta, como Orden de Venta, Nota de Entrega, o Factura de Venta, se utilizarán las configuraciones establecidas en esta sección al seleccionar un Producto de esta Marca.

* Centro de Costo de Venta Preestablecido
* Cuenta de Ingresos Preestablecida

## 3. Temas Relacionados
1. [Orden de Compra](/docs/user/manual/es/buying/purchase-order)
1. [Orden de Venta](/docs/user/manual/es/selling/sales-order)
1. [Recibo de Compra](/docs/user/manual/es/stock/purchase-receipt)
1. [Nota de Entrega](/docs/user/manual/es/stock/delivery-note)
1. [Factura de Venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice)
