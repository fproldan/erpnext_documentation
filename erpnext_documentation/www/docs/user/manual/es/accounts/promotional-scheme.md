# Esquema promocional

**Un esquema promocional es un descuento temporal aplicado sobre uno o más productos.**

Los esquemas promocionales ayudan a los negocios a atraer clientes con sus precios bajos por tiempo limitado. En ERPNext pueden ser facilmente configurados y vinculados a una regla de precios.

Al crear un esquema promocional, el sistema genera una [Regla de precios](/docs/user/manual/es/accounts/pricing-rule). Un esquema promocional puede tener múltiples Reglas asociadas. En ERPNext, un esquema promocional es una manera más sencilla de gestionar precios en múltiples productos/grupos dependiendo de las distintas entidades y condiciones.

Para acceder a la lista de Esquemas promocionales, ir a:
> Inicio > Ventas > Productos y Precios > Esquema promicional

## 1. Prerrequisitos
Antes de crear y usar un Esquema promocional se recomienda crear lo siguiente:

1. [Producto](/docs/user/manual/es/stock/item)
1. [Grupo de productos](/docs/user/manual/es/stock/item-group)
1. [Cliente](/docs/user/manual/es/CRM/customer)
1. [Proveedor](/docs/user/manual/es/buying/supplier)

## 2. Creación de un esquema promocional

1. Ir a la lista de esquemas promocionales y hacer click en Nuevo.
1. Ingresar un título para el esquema.
1. Seleccionar la opción deseada en el campo "Aplicar en", la cual puede ser Código de producto, Grupo de productos, Marca o Transacción. Seleccionar "Transacción" aplicará el esquema sobre el monto total de la transacción.
1. Dependiendo de lo elegido en el paso anterior, el sistema permitirá seleccionar el Producto, Grupo de productos o Marca en la tabla.
1. Seleccionar si el esquema es para venta, compra o ambas y completar la información correspondiente.
1. En la tabla de Bloque de descuento de precio definir el descuento de precio o de producto.
1. También se puede aplicar el descuento en otros Productos/Grupos de productos/Marcas seleccionando la opción correspondiente en el campo "Aplicar regla en otro".

 <img alt="Promotional Scheme" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/promotional-schemes.png">
 
8. Guardar.

> Nota: al guardar un esquema promocional se creará ua nueva Regla de precios.

### 2.1 Campos adicionales

#### Condiciones mixtas
Si se seleccionan dos o más Productos y se definieron valores para los campos "Cantidad mínima" y "Cantidad máxima", el esquema será aplicado solo si la suma total de Productos es igual a las cantidades especificadas. Por ejemplo, si se crea una Regla de precios para Producto 1 y Producto 2 y se decidió que Cantidad mínima y Cantidad máxima sean 30, entonces el esquema se aplicará solo si la suma de productos es 30.

#### Es acumulativo
Habilitar esta opción permite que el esquema se aplique de forma acumulativa. Para esto se debe especificar el "Monto mínimo" y "Monto máximo".

Se puede considerar el caso en que el Monto mínimo sea de $1500 y el máximo de $2000. Así, si una transacción es creada por $1400, el esquema no será aplicado. Sin embargo, al crear una segunda transacción por $600 sí se aplicará, ya que el total acumulado entre ambas transacciones está dentro del rango definido ($2000). Nótese que el descuento será aplicado solo en la última transacción.

Esto puede ser útil para dar descuentos a Clientes que compraron un determinado producto múltiples veces y se desea recompensarlos con descuentos/precios especiales.

## 3. Características

### 3.1 Aplicar esquema en otro producto
Esta opción hace que se verifiquen las condiciones en un Producto pero se aplique el descuento en otro Producto.


Por ejemplo, si se seleccionan Producto 1 y Producto 2 en la tabla de la condición "Aplicar en" y Producto 3 en "Aplicar regla en otro", al hacer una transacción con estos tres productos, el esquema se aplicará solo a Producto 3 ya que los otros dos productos están presentes en la transacción.

### 3.2 Información de la entidad

Especificar si el Esquema promocional es para la venta o la compra del producto.

Dependiendo de la selección realizada, se puede elegir para cuál de los siguientes aplicar el esquema:

* [Cliente](/docs/user/manual/es/CRM/customer)
* [Grupo de clientes](/docs/user/manual/es/CRM/customer-group)
* [Territorio](/docs/user/manual/es/selling/territory)
* [Socio de ventas](/docs/user/manual/es/selling/sales-partner)
* [Campaña](/docs/user/manual/es/CRM/campaign)
* [Proveedor](/docs/user/manual/es/buying/supplier)
* Grupo de proveedores

### 3.3 Validez
También se puede definir un intervalo de tiempo dentro del cual el esquema estará vigente. Esto es útil para promociones de venta. Dejando los campos de fecha vacíos el Esquema promocional no tendrá límite de tiempo. 

**Divisa**: establecer la divisa hará que el descuento solo se aplique si la transacción usa la misma que se definió en el esquema.

### 3.4 Descuento de precio

**Descripción de la regla**: ingresar una descripción para definir el objetivo de cada esquema.

#### Cantidad y monto

Es posible especificar Cantidad mínima, Cantidad máxima, Monto mínimo o Monto máximo de un Producto según los cuales el esquema debería ser aplicado.

Nótese que si la cantidad o el monto no alcanza o excede estos límites, el Esquema promocional no será aplicado. Sin embargo, será aplicado si se encuentran habilitadas las opciones "Condiciones mixtas" o "Es acumulativo".

### Configuración del descuento/precio

* **Precio**: de esta forma se actualizará el precio del producto. Por ejemplo, si se vende el producto por $100 y se desea verderlo por $112 solo a un cliente particular, aquí se seleccionará "Precio" y $112 en el campo correspondiente.
* **Porcentaje de descuento**: se puede especificar un procentaje de descuento. Por ejemplo, un descuento del 10% en un Producto que vale $500 lo dejará con un precio de $450.
* **Descuento**: se aplica un monto de descuento fijo. Por ejemplo, si se vende un Producto a $100 con un descuento de $7, entonces ese valor deberá ser definido en el campo "Descuento".

#### Filtros para la aplicación de descuentos

* **Almacén**: elegir un almacén hará que el esquema promocional sea aplicado solo si el Producto seleccionado pertenece a dicho almacén

* **Prioridad**: considérese que se tiene un Grupo de productos y se desea definir reglas específicas para uno de los productos que lo componen. Para esto se puede crear un nuevo Esquema promocional y asignarle mayor prioridad.

* **Umbral de sugerencia**: este es el umbral en base al cual el sistema notificará para ajustar la cantidad de producto a la cual aplicar el descuento. Por ejemplo, si la Cantidad mínima es 10 y el umbral se definió en 9, el sistema sugerirá agregar un producto más para obtener el descuento. Esto también aplica para el Monto mínimo.

* **Validar regla aplicada**: si el precio ingresado manualmente en la transacción no es válido para el Producto, el sistema no permitirá aplicar un descuento/precio distinto.

### 3.5 Descuento de producto

El descuento de producto se aplica cuando al comprar cierto Porducto uno o más Productos son gratis. La mayoría de los campos de esta sección son los mismos que los de la anterior.

Las opciones adicionales son:
* **Mismo artículo**: si se desea dar de forma gratis un producto con la compra de otro igual, se debe tildar esta opción. Si se desea dar otro producto, destildar esta opción y seleccionar el producto correspondiente.

* **Aplicar múltiples reglas de precios**: considérese un producto que vale $500 y posee dos reglas de precios P1 y P2. P1 aplica un descuento del 10% y P2 del 5%. Habilitar esta opción hará que se aplique un descuento del 15%, quedando un precio de $425.

* **UoM**: el Esquema promocional será aplicado solo si la unidad de medida (UoM) especificada aquí es la misma que la de la transacción.

* **Tasa**: un producto puede ser ofrecido gratis por el proveedor pero aún así tener impuestos. Ingresar una tasa hará que el Cliente deba pagar dichos impuestos.


## 4. Tipos de esquema promocional
### 4.1 Descuento de precio

En este tipo de esquema se puede definir un precio fijo o bien un descuento en un porcentaje o monto determinado en base a las cantidades y los montos de los productos.

<img alt="Promotional Scheme" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/promotional-schemes-price-discount.png">

### 4.2 Descuento de producto

En este tipo de esquema se elige dar uno o más productos gratis con la compra de otro producto, respetando condiciones de cantidad y monto.

<img alt="Promotional Scheme" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/promotional-schemes-product-discount.png">

## 5. Ejemplos de configuración de Esquemas promocionales


### 5.1 Esquemas con Condiciones mixtas

El Cliente A compró 10 unidades de Porducto 1 y 5 de Producto 2 y el Proveedor desea darle un 10% de descuento. El Proveedor también desea otorgar el mismo descuento al Cliente B quien compró 15 unidades de Producto 1.

En resumen se desea aplicar el descuento solo si se adquirieron 15 unidades de alguno de los dos productos o en total.

Para configurar esto en ERPNext se debe seguir los siguientes pasos:

1. Seleccionar "Código de producto" en el campo "Aplicar en".
1. Seleccionar ambos productos en la tabla correspondiente.
1. Tildar la opción "Condiciones mixtas".
1. Ingresar 15 en los campos cantidad mínima y máxima.
1. Ingresar 10 en porcentaje de descuento.

<img alt="Promotional Scheme" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/promotional-schemes-mixed-conditions.png">

### 5.2 Aplicar descuento en otro producto

El Cliente A compró 30 unidades de Producto 1 y 2 unidades de Producto 2. El Proveedor desea vender el Producto 2 a $120, siendo su precio original de $150.

El proveedor desea aplicar la regla solo si el cliente compró como mínimo 30 unidades de Producto 1.

Para configurar esto en ERPNext se debe seguir los siguientes pasos

1. Seleccionar "Código de producto" en el campo "Aplicar en".
1. Seleccionar Producto 1 en la tabla correspondiente.
1. Seleccionar Producto 2 en la sección de "Aplicar regla en otro".
1. Ingresar 30 en el campo cantidad mínima.
1. Ingresar 120 en precio de descuento.

<img alt="Promotional Scheme" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/promotional-schemes-discount-on-other.png">

## 6. Temas relacionados
1. [Regla de precios](/docs/user/manual/es/accounts/pricing-rule)
1. [Cliente](/docs/user/manual/es/CRM/customer)
1. [Proveedor](/docs/user/manual/es/buying/supplier)
1. [Producto](/docs/user/manual/es/stock/item)
