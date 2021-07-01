<!-- add-breadcrumbs -->
# Perfil de POS

**En ERPNext, un perfil de POS permite usar la funcionalidad de Punto de venta (POS).**

POS incluye opciones avanzadas para cubrir diferentes funcionalidades, tales como manejo de inventarios, CRM, finanzas, almacenamiento, etc. Antes de la aparición del POS, todas estas operaciones eran realizadas independientemente y requerían el ingreso manual de la información, lo cual podía generar errores.

Si se trabaja en el ámbito de retail (ventas minoristas), se necesita un Punto de venta lo más rápido y eficiente posible. Para esto se puede crear un perfil de POS para un usuario.

Para acceder a la lista de Perfiles de POS, ir a:
> Inicio > Retail > Configuraciones > Perfiles de punto de venta (POS)

## 1. Creación de un Perfil de POS
1. Ir a la lista de Perfiles de punto de venta (POS) y hacer click en Nuevo.
1. Ingresar un nombre para el perfil.
1. Seleccionar una [Secuencia](/docs/user/manual/es/setting-up/settings/naming-series).
1. Elegir una Cuenta de desajuste y Centro de costos de desajuste en los cuales se registrarán las transacciones.
1. Agregar los Métodos de pago deseados en la tabla, el predeterminado si no se selecciona ninguno es Caja/Efectivo. Al utilizar el POS solo estarán disponibles los definidos en esta tabla. Se deberá elegir uno de ellos como Método predeterminado tildando dicha opción en la tabla.

 <img class="screenshot" alt="POS Setting" src="{{docs_base_url}}/assets/img/pos-setting/default_mop.png">
 
6. Definir los montos predefinidos para cada método de pago (recomendado: 0).
7. Guardar.

 <img class="screenshot" alt="POS Setting" src="{{docs_base_url}}/assets/img/pos-setting/pos_profile.png">

### 1.1 Opciones adicionales

* **Clientes**: se puede vender ciertos productos a Clientes en particular especificando Grupos de productos y Categorías de clientes.
* **Almacén**: el inventario del almacén seleccionado se verá afectado por transacciones de POS que utilicen este perfil.
* **Campaña**: una [Campaña](/docs/user/manual/es/CRM/campaign) de ventas puede vincularse al perfil para realizar el seguimiento de las ventas generadas dentro de la misma.
* **Dirección de la Compañía**: si el dispositivo POS está instalado en una sucursal, la dirección puede especificarse en este campo.

* **Actualizar el Inventario**: si se tilda esta opción, el inventario del almacén seleccionado se verá afectado por transacciones de POS que utilicen este perfil. Esto es porque al validar la factura se generarán automáticamente entradas de inventario, eliminando la necesidad de crear una Nota de entrega aparte.
* **Ignorar la Regla de precios**: toda [Regla de precios](/docs/user/manual/es/accounts/pricing-rule) será ignorada al usar este perfil.
* **Permitir al usuario editar Tasa**: con esta opción, el usuario del POS podrá editar el "Precio" de los productos añadidos en las transacciones.
* **Permitir que el usuario edite el Descuento**: con esta opción, el usuario del POS podrá editar el "Descuento" de los productos añadidos en las transacciones.
* **Permitir imprimir antes de pagar**: esto permite que el usuario imprima la factura antes de que se efectúe el pago.
* **Mostrar artículos en stock**: se indicará la cantidad restante de los Productos del almacén seleccionado.

## 2. Características

### 2.1 Aplicable para Usuarios
Por defecto, todos los usuarios de ventas pueden acceder a los Perfiles de POS creados. Sin embargo, si se desea que solo algunos puedan acceder a ciertos Perfiles, se los deberá agregar en esta tabla. Al haber agregado al menos un usuario, los demás ya no podrán usar el perfil.

**Perfil de POS predeterminado**: al tildar esta opción en la tabla, el perfil de POS se convierte en el predeterminado para ese usuario. Así, la próxima vez que el usuario ingrese al sistema, aparecerá este perfil por defecto.

![POS User](/docs/assets/img/pos-setting/pos-profile-default.png)

> Nota: si se especifica un usuario en particular, la configuración de POS será aplicada solo para ese usuario. Si no se elige ningún usuario, la configuración aplicará para cualquier usuario. Para comprender cómo funciona el POS, visitar la página [Punto de venta POS](/docs/user/manual/es/accounts/point-of-sales).


### 2.2 Filtros
Al especificar un Grupo de productos/Categoría de Clientes en un Perfil de POS, dichas agrupaciones serán seleccionadas automáticamente al realizar transacciones.

<img class="screenshot" alt="POS Setting" src="{{docs_base_url}}/assets/img/pos-setting/item_customer_group.png">

### 2.3 Ajustes de Impresión

![POS Print](/docs/assets/img/pos-setting/pos-profile-print.png)

#### Formato de Impresión

Se puede especificar un Formato de impresión en el cual se determinará el diseño que tendrá el documento. Para saber más, visitar la página [Formato de impresión](/docs/user/manual/es/setting-up/print/print-format).

#### Membrete

Se puede imprimir la Factura de POS con el membrete de la Compañía. Más información [aquí](/docs/user/manual/es/setting-up/print/letter-head).

#### Imprimir Encabezado

El encabezado también puede ser modificado al imprimir el documento. Por ejemplo, puede decir "Factura" o "Comprobante". Se puede hacer esto seleccionando un **Encabezado de impresión**. Para crear un nuevo Encabezado de impresión ir a: Inicio > Configuración > Impresión > Ajustes de Impresión. Más información [aquí](/docs/user/manual/es/setting-up/print/print-headings).

#### Términos y Condiciones

Puede haber ciertos términos y condiciones sobre el producto que se está vendiendo, los cuales pueden ser mencionados aquí. Para saber más sobre agregar Términos y condiciones hacer click [aquí](/docs/user/manual/es/setting-up/print/terms-and-conditions).

### 2.4 Contabilidad

* **Lista de precios**: una [Lista de precios](/docs/user/manual/es/stock/price-lists) almacena los [Precios de productos](/docs/user/manual/es/stock/item-price). Elegir una Lista de precios hará que se traigan solo los precios de esa lista al usar determinado perfil.
* **Divisa / Moneda**: por defecto se tomará la moneda de la Compañía; pero se puede elegir una diferente en cada perfil. Si se cambia la moneda, se deben seleccionar las cuentas correspondientes a la misma.
* **Impuestos y cargos**: seleccionar una [Plantilla de impuestos de ventas](/docs/user/manual/es/selling/sales-taxes-and-charges-template) o [Plantilla de impuestos de compras](/docs/user/manual/es/buying/purchase-taxes-and-charges-template) hará que se apliquen automáticamente dichos impuestos y cargos en la transacción.
* **Aplicar descuento en**: aquí se puede definir si el descuento se aplicará sobre el Total (antes de aplicar los impuestos) o sobre el Total Neto (después de aplicar los impuestos).
* **Categoría de impuestos**: al seleccionar una [Categoría de impuestos](/docs/user/manual/es/accounts/tax-category), las Reglas de precios asociadas a la misma serán aplicadas a cada transacción hecha desde el POS.

Las siguientes cuentas pueden configurarse en el perfil para que el Balance general sea actualizado respectivamente:

* Cuenta para monto de cambio
* Cuenta de desajuste
* Centro de costos de desajuste
* Cuenta de ingresos
* Cuenta de gastos

### 2.5 Dimensiones contables
Las Dimensiones contables te permiten clasificar transacciones dependiendo del Territorio, Sucursal, Cliente, etc. Esto ayuda a visualizar los estados contables por separado según el criterio elegido. Para saber más, visitar la página [Dimensiones contables](/docs/user/manual/es/accounts/accounting-dimensions).

> Nota: el Centro de costos es tratado como una dimensión por defecto.

## 3. Temas relacionados
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Factura de compra](/docs/user/manual/es/accounts/purchase-invoice)
1. [Punto de venta](/docs/user/manual/es/accounts/point-of-sales)
