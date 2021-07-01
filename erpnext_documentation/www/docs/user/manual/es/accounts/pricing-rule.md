<!-- add-breadcrumbs -->
# Regla de precios

**Una Regla de precios define el descuento/precio que se aplicará en base a una serie de condiciones.**

Una Regla de precios tiene múltiples aplicaciones siendo el objetivo principal controlar el precio de un Producto. Pueden establecerse filtros como cantidad, fecha, grupos y otras condiciones.

Una Regla de precios es en cierta forma similar a una [Regla fiscal](/docs/user/manual/en/accounts/tax-rule).

A continuación se listan algunos casos en los que puede ser de ayuda la Regla de precios:

- Como una política promocional de ventas, en la que si el Cliente compra más de 10 unidades de un Producto obtiene un descuento del 20%.
- Para un determinado Cliente, el precio de venta de un Producto específico debe actualizarse según el precio establecido en la regla.
- Los Productos de un determinado Grupo tienen el mismo precio de venta/compra.
- Clientes de determinado Grupo deberían obtener un precio especial o bien un descuento en todos los productos.
- Proveedores dentro de cierto Grupo deberían tener un precio de compra específico.

Para aplicar automáticamente un Descuento o Tarifa a la Lista de precios de un Producto, se debe crear la Regla de precios.

Para acceder a la lista de Reglas de precios, ir a:
> Inicio > Contabilidad > Regla de precios

## 1. Prerrequisitos

Antes de crear y usar una Regla de precios se recomienda crear lo siguiente:

1. [Producto](/docs/user/manual/es/stock/item)
1. [Grupo de Productos](/docs/user/manual/es/stock/item-group)
1. [Cliente](/docs/user/manual/es/CRM/customer)
1. [Proveedor](/docs/user/manual/es/buying/supplier)

## 2. Creación de Regla de precios

1. Ir a la lista de Reglas de precios y hacer click en Nuevo.
1. Ingresar un título para la regla.
1. Seleccionar la opción deseada en "Aplicar en", ya sea Código del Producto, Grupo de Productos, Marca o Transacción.
1. Seleccionar si se desea aplicar un Descuento de precio o de producto. Si se pretende dar productos gratis se debe seleccionar el descuento de producto.
 <img alt="Applicable On" class="screenshot" src="{{docs_base_url}}/assets/img/articles/pricing-rule-on.png">
 
5. Para un solo producto, seleccionar Código de producto y el Producto.
6. Si se desea aplicar la Regla de precios a todos los Productos, seleccionar "Grupo de Productos" y "Todos los grupos de productos".
7. Definir el descuento/precio a aplicar. Para saber más, ir a la siguiente [sección](/docs/user/manual/es/accounts/pricing-rule#35-price-discount-scheme).
8. Guardar. 

### 2.1 Opciones adicionales al crear una Regla de precios

#### Almacén

Configurar un almacén aquí hará que la Regla de precios se aplique solo si el Producto seleccionado pertenece a dicho almacén.

#### Aplicar Regla en

Dependiendo del atributo seleccionado en el campo "Aplicar en", se puede definir la regla para un determinado:

* [Producto](/docs/user/manual/es/stock/item)
* [Grupo de productos](/docs/user/manual/es/stock/item-group)
* Marca
* Transacción (sobre el importe total de la transacción)

En esta tabla, se puede seleccionar el Producto/Grupo/Marca específico. Por ejemplo, si se selecciona "Aplicar en: Grupo de productos" y "Materia prima" en la tabla, esta Regla de precios será aplicada solo para los Productos que pertenecen a dicho grupo.

**UoM**: la Regla de precios será aplicada solo si la unidad de medida (UoM) especificada aquí es la misma que la de la transacción.

#### Condiciones mixtas

Si se seleccionan dos o más Productos y se definieron valores para los campos "Cantidad mínima" y "Cantidad máxima", la regla será aplicada solo si la suma total de Productos es igual a las cantidades especificadas. Por ejemplo, si se crea una Regla de precios para Producto 1 y Producto 2 y se decidió que Cantidad mínima y Cantidad máxima sean 30, entonces la regla se aplicará solo si la suma de productos es 30.

#### Es acumulativo

Habilitar esta opción permite que la Regla se aplique de forma acumulativa. Para esto se debe especificar el "Monto mínimo" y "Monto máximo".

Se puede considerar el caso en que el Monto mínimo sea de $1500 y el máximo de $2000. Así, si una transacción es creada por $1400, la Regla de precios no será aplicada. Sin embargo, al crear una segunda transacción por $600, la regla será aplicada, ya que el total **acumulado** entre ambas transacciones está dentro del rango definido ($2000). Nótese que el descuento será aplicado solo en la última transacción.

Esto puede ser útil para dar descuentos a Clientes que compraron un determinado producto múltiples veces y se desea recompensarlos con descuentos/precios especiales.

## 3. Características

### 3.1 Aplicar regla en otro

Esta opción hace que se verifiquen las condiciones en un Producto pero se aplique el descuento en otro Producto.

![Apply rule on other](/docs/assets/img/articles/pricing-rule-other.png)

Por ejemplo, si se seleccionan Producto 1 y Producto 2 en la tabla de la condición "Aplicar en" y Producto 3 en "Aplicar regla en otro", al hacer una transacción con estos tres productos, la Regla se aplicará solo a Producto 3 ya que los otros dos productos están presentes en la transacción.

### 3.2 Información de la entidad

Especificar si la Regla de precios es para la venta o la compra del producto.

Dependiendo de la selección realizada, se puede elegir para cuál de los siguientes aplicar la regla:

* [Cliente](/docs/user/manual/es/CRM/customer)
* [Grupo de clientes](/docs/user/manual/es/CRM/customer-group)
* [Territorio](/docs/user/manual/es/selling/territory)
* [Socio de ventas](/docs/user/manual/es/selling/sales-partner)
* [Campaña](/docs/user/manual/es/CRM/campaign)
* [Proveedor](/docs/user/manual/es/buying/supplier)
* Grupo de proveedores

### 3.3 Cantidad y monto

Es posible especificar Cantidad mínima, Cantidad máxima, Monto mínimo o Monto máximo de un Producto según los cuales la regla debería ser aplicada.

Nótese que si la cantidad o el monto no alcanza o excede estos límites, la Regla de precios no será aplicada. Sin embargo, será aplicada si se encuentran habilitadas las opciones "Condiciones mixtas" o "Es acumulativo".

<img alt="Applicable Qty" class="screenshot" src="{{docs_base_url}}/assets/img/articles/pricing-rule-qty-amt.png">

### 3.4 Validez

También se puede definir un intervalo de tiempo dentro del cual la regla estará vigente. Esto es útil para promociones de venta. Dejando los campos de fecha vacíos la Regla no tendrá límite de tiempo. 

<img alt="Period" class="screenshot" src="{{docs_base_url}}/assets/img/articles/pricing-rule-period.png">

### 3.5 Margen

![Pricing Rule Margin](/docs/assets/img/articles/pricing-rule-margin1.png)

* **Tipo de Margen**: puede que se quiera vender un producto por un cierto margen. Para evitar tener que agregar precios de venta, aquí se puede configurar para que el margen se aplique de forma automática. 

* **Tasa de margen o Monto**: puede ser basado en un porcentaje o monto (ej: 5% o $50).

Para más detalles sobre agregar márgenes hacer click [aquí](/docs/user/manual/es/selling/articles/adding-margin).

### 3.6 Esquema de descuento de precio

Los parámetros a aplicar con la regla de precios se definen en esta sección.

![Pricing Rule](/docs/assets/img/articles/pricing-rule-rule.png)

* **Precio**: de esta forma se actualizará el precio del producto. Por ejemplo, si se vende el producto por $100 y se desea verderlo por $112 solo a un cliente particular, aquí se seleccionará "Precio" y $112 en el campo Precio.
* **Porcentaje de descuento**: se puede especificar un procentaje de descuento, el cual puede aplicarse a una determinada [Lista de precios](/docs/user/manual/es/stock/price-lists). Dejar el campo "Por lista de precios" en blanco hará que la regla se aplique a todas las Listas de precios.
* **Descuento**: se aplica un monto de descuento fijo. Por ejemplo, si se vende un Producto a $100 con un descuento de $7, entonces ese valor deberá ser definido en el campo "Descuento".

### 3.7 Ajustes avanzados

![Pricing Rule Advance](/docs/assets/img/articles/pricing-rule-adv.png)

* **Umbral de sugerencia**: este es el umbral en base al cual el sistema notificará para ajustar la cantidad de producto a la cual aplicar el descuento. Por ejemplo, si la Cantidad mínima es 10 y el umbral se definió en 9, el sistema sugerirá agregar un producto más para obtener el descuento. Esto también aplica para el Monto mínimo.

* **Prioridad**: considérese que se tiene un Grupo de productos y se desea definir reglas específicas para uno de los productos que lo componen. Para esto se puede crear una nueva Regla de precios y asignarle mayor prioridad. Esto aplica también para Grupos de clientes o de proveedores.

* **Aplicar múltiples reglas de precios**: considérese un producto que vale $500 y posee dos reglas de precios P1 y P2. P1 aplica un descuento del 10% y P2 del 5%. Habilitar esta opción hará que se aplique un descuento del 15%, quedando un precio de $425.

* **Aplicar descuento en tarifa**: el descuento será compuesto. Considérese el escenario anterior. Al habilitar esta opción, 10% será aplicado sobre $500 lo que dejará un precio de $450. Luego se aplicará el descuento de 5% sobre $450 quedando un precio final de $427,5. 

* **Validar regla aplicada**: muestra el mensaje de validación definido en "Descripción de la regla" en el caso de que el descuento/precio ingresado manualmente en la transacción no coincida con la Regla de precios.
Esto es útil cuando el distribuidor ubicado en la cima de la jerarquía decide que el descuento se aplique y el sistema solo está validando si la Regla de precios se aplica correctamente.

## 4. Tipos de descuentos de las Reglas de precios
### 4.1 Descuento de precio

1. En Tipo de margen se puede elegir si el margen se calcula como porcentaje o importe. Ej: un margen de 10% en la lista de precios de proveedor al momento de la venta.

1. La tarifa definida en la Regla de precios tendrá prioridad sobre la de la lista de precios (precio del producto).

 <img alt="Applicable Rate" class="screenshot" src="/docs/assets/img/articles/pricing-rule-price.png">

3. Se puede aplicar porcentajes de descuento para Listas de precios (para venta o compra) específicas. Para aplicarlos para ambos se debe dejar el campo "Por lista de precios" vacío.

 <img alt="Discount" class="screenshot" src="{{docs_base_url}}/assets/img/articles/pricing-rule-discount.png">

4. El descuento también se puede definir como un importe fijo.

 <img alt="Discount" class="screenshot" src="{{docs_base_url}}/assets/img/articles/pricing-rule-discount-amt.png">

### 4.2 Descuento de Producto

1. "Comprando 2 se obtiene 1 gratis". Para configurar este tipo de reglas se debe elegir "Producto" en "Precio o descuento del producto", tildar la opción "Mismo articulo" e ingresar la "Cantidad".

 <img alt="Discount" class="screenshot" src="{{docs_base_url}}/assets/img/articles/pricing-rule-same-product-free.png">

2. "Comprando 2 productos A se obtiene 1 producto B gratis". Para configurar este tipo de reglas se debe elegir "Producto" en "Precio o descuento del producto", elegir el producto en cuestión en el campo "Articulo libre" y la Cantidad.

 <img alt="Discount" class="screenshot" src="{{docs_base_url}}/assets/img/articles/pricing-rule-other-product-free.png">

### 5. Temas relacionados
1. [Esquema Promocional](/docs/user/manual/es/accounts/promotional-scheme)
1. [Regla fiscal](/docs/user/manual/es/accounts/tax-rule)
1. [Proveedor](/docs/user/manual/es/buying/supplier)
1. [Producto](/docs/user/manual/es/stock/item)
