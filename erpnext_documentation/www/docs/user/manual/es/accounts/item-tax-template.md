<!-- add-breadcrumbs -->
# Plantilla de impuestos de productos

**La Plantilla de impuestos de productos es útil para calcular los impuestos de cada producto de forma individual.**

Si alguno de los productos tiene impuestos diferentes a los estándares asignados en la tabla Impuestos y cargos, se puede crear una plantilla de impuestos y asignársela a los [Productos](/docs/user/manual/en/stock/item) o [Grupo de Productos](/docs/user/manual/en/stock/item-group) correspondientes. El Porcentaje asignado en la Plantilla tendrá prioridad sobre el estándar definido en la tabla de Impuestos y cargos.

Por ejemplo, si el IVA en Impuestos y cargos es de 21%, entonces será aplicado a todos los productos de la Orden de venta. Sin embargo, si se necesita un valor diferente para algunos de los productos se deberá seguir los siguientes pasos:

Para acceder a la lista de Plantillas de impuestos de productos ir a:
> Inicio > Contabilidad > Impuestos > Plantilla de impuesto de producto

Puede darse un caso en el que se esté creando una Orden de venta y se tenga una [Plantilla de impuestos (ventas)](/docs/user/manual/es/selling/sales-taxes-and-charges-template) con IVA 21%; pero a uno de los productos de la Orden se le deba aplicar IVA 10,5% y otro sea exento de impuestos. Para esto se deberá seleccionar la cuenta del impuesto y su porcentaje.

## 1. Prerrequisitos
Antes de crear y usar una Plantilla de impuesto de producto, se aconseja crear lo siguiente:

1. [Producto](/docs/user/manual/es/stock/item)
1. Habilitar la opción "Añadir automáticamente Impuestos y cargos desde la Plantilla de impuestos" en [Configuración de cuentas](/docs/user/manual/es/accounts/accounts-settings)

## 2. Creación de una Plantilla de impuestos de producto
1. Ir al listado de Plantillas de impuestos de productos y hacer click en Nuevo.
1. Ingresar un título para la plantilla.
1. Seleccionar la cuenta en el campo de la columna Impuesto, y el Tipo de impuesto. Al hacer esto se autocompletará el campo Porcentaje del impuesto con el definido en el Tipo de impuesto. Se puede añadir más filas si es necesario.
1. Guardar.

A continuación se podrá asignar la plantilla al producto correspondiente. Para hacer esto, ir al producto y seleccionar la plantilla en la sección IMPUESTOS DEL PRODUCTO:

![Item Tax In Item](/docs/assets/img/accounts/item-tax-in-item.png)

> Nota: se recomienda no utilizar la misma plantilla de impuesto de compra/venta seleccionada en la [Regla fiscal](/docs/user/manual/es/accounts/tax-rule) ya que puede causar interferencias. Si se desea usar el mismo porcentaje para la regla fiscal y la plantilla de impuesto de producto, usar un nombre diferente para la plantilla de impuesto de compra/venta.

### 2.1 Definición de los impuestos a aplicar en el Producto

Las plantillas de impuestos tienen valores predefinidos. Para productos con impuestos diferentes al resto, se deben especificar en el producto mismo. Para esto se debe ir al producto, añadir una fila en la tabla de impuestos, seleccionar el tipo de impuesto y la tasa correspondiente. Así, al crear una nueva orden/factura, se tomará este valor y no el de la plantilla.

<img class="screenshot" alt="Opening Account" src="{{docs_base_url}}/assets/img/accounts/item-wise-tax.png">

Para un producto exento de impuestos, se asigna un procentaje del 0% para el impuesto en cuestión.

<img class="screenshot" alt="Opening Account" src="{{docs_base_url}}/assets/img/accounts/exempted-item.png">

> Nota: para que la plantilla de impuesto del producto funcione correctamente, los tipos de impuestos (cuentas) definidos en la misma deben coincidir con los de la Plantilla de impuestos (ventas).

> Si se desea incluir múltiples productos con diferentes impuestos, se los debe registrar con diferentes nombres (ej: IVA 21%, IVA 10,5%).

### 2.2 Cálculo del impuesto en la transacción

Teniendo un caso en el que el producto tiene asignada una plantilla con dos impuestos del 5%.

<img class="screenshot" alt="Opening Account" src="{{docs_base_url}}/assets/img/accounts/tax-calculation.png">

El impuesto será obtenido de la plantilla y calculado:
<img class="screenshot" alt="Opening Account" src="{{docs_base_url}}/assets/img/accounts/tax-calculation1.png">

### 2.3 Plantilla de impuesto por cada producto

También se puede seleccionar manualmente una Plantilla diferente para cada producto en la transacción:

![Item Tax individual](/docs/assets/img/accounts/item-tax-each.png)


### 2.4 Impuesto de producto en un Grupo de productos

Se puede asignar una plantilla de impuestos de productos a un Grupo de productos modificando la tabla de impuestos ubicada en la sección correspondiente.

<img class="screenshot" alt="Item Tax in Item Group" src="{{docs_base_url}}/assets/img/accounts/item-group-tax.png">

Esta plantilla será aplicada a todos los Productos del grupo, excepto aquellos que tengan una plantilla asignada de forma individual.


### 2.5 Validez de los impuestos de productos

<img class="screenshot" alt="Item Tax in Item Group" src="{{docs_base_url}}/assets/img/accounts/item-tax-in-item.png">

También se puede determinar una fecha de validez para las plantillas.

* Dependiendo de la fecha de creación de la transacción, una plantilla de impuesto vigente será traída automáticamente.
* Si existe más de una Plantilla de impuestos válida entonces será obtenida la primera de la tabla del producto.
* En el caso de que no haya plantillas válidas entonces será obtenida la primera de la tabla del producto que no tenga fecha en "Válida desde".

> Nota: al agregar productos en una Factura de Compra se considerará primero la "Fecha de factura de proveedor" en lugar de la "Fecha de creación" para obtener la Plantilla.

### 2.6 Puntos a tener en cuenta

- Si se deja la Categoría de impuesto vacía, la plantilla aplicada a los productos de las transacciones será la predeterminada.

- Se puede aplicar diferentes plantillas para distintas categorías.

- Para una plantilla que sobrescribe impuestos debe haber una fila en la tabla Impuestos y cargos con la misma cuenta y una tasa estándar.

- Si se desea aplicar impuestos solo en los productos con una plantilla vinculada se debe establecer la tasa estándar en 0.

### 3. Temas relacionados
1. [Regla fiscal](/docs/user/manual/es/accounts/tax-rule)
1. [Facturas de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Facturas de compra](/docs/user/manual/es/accounts/purchase-invoice)
