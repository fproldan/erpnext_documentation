<!-- add-breadcrumbs -->
# Regla fiscal

**Una regla fiscal aplica automáticamente impuestos a transacciones basadas en reglas preestablecidas.**

Se puede definir qué [Plantilla de impuesto](/docs/user/manual/es/setting-up/setting-up-taxes.html) debe aplicarse en transacciones de ventas/compras usando reglas fiscales. Esto se decide considerando diversos factores como Cliente, Categoría de cliente, Proveedor, Grupo de proveedores, Producto, Grupo de productos o una combinación de los mismos.

Para acceder a la lista de Reglas fiscales, ir a:
> Inicio > Contabilidad > Taxes > Regla fiscal

## 1. Prerrequisitos
Antes de crear y usar una Regla fiscal, se recomienda crear lo siguiente primero:

1. [Plantilla de impuestos (ventas)](/docs/user/manual/es/selling/sales-taxes-and-charges-template)
    
    o

1. [Plantilla de impuestos (compras)](/docs/user/manual/es/buying/purchase-taxes-and-charges-template)

## 2. Creación de una Regla fiscal
1. Ir a la lista de Reglas fiscales y hacer click en Nuevo.
1. En "Tipo de impuesto" seleccionar si el impuesto será aplicado a ventas o compras. 
1. Seleccionar la Plantilla de impuesto a utilizar.
1. Guardar.
 <img class="screenshot" alt="Tax Rule" src="{{docs_base_url}}/assets/img/accounts/tax-rule.png">

Se pueden publicar productos online mediante el módulo de Website. Seleccionando "Utilizar para Carrito de compras" se usará esta Regla fiscal para transacciones generadas mediante esta modalidad. Para saber más, visitar la página [Carrito de compras](/docs/user/manual/es/website/shopping-cart).

> Nota: se recomienda no usar la misma Plantilla de Ventas/Compras seleccionada en [Plantilla de impuestos de productos](/docs/user/manual/es/accounts/item-tax-template), ya que puede generar interferencias. Si se desea usar la misma tasa para la Regla fiscal y la Plantilla de impuestos de productos, se deberá asignar un nombre diferente para la Plantilla de impuestos de Ventas/Compras.

## 3. Características
### 3.1 Aplicar automáticamente Regla fiscal en base al Cliente/Proveedor
Seleccionar un Cliente/Proveedor si la regla debe aplicarse a una entidad específica. Si se desea aplicar para todos los Clientes/Proveedores dejar la opción por defecto Todos los grupos de clientes/Todos los grupos de proveedores.

Al seleccionar un Cliente/Proveedor, su dirección de facturación y de envío serán traídas desde el mismo si fueron especificadas.

### 3.2 Aplicar automáticamente Regla fiscal en base al Producto/Grupo de producto

Al configurar un Producto o Grupo de productos específico en la Regla fiscal, la misma será aplicada automáticamente en las transacciones de los mismos.

### 3.3 Configuración de Categoría de impuestos
Configurar una Categoría de impuestos permite aplicar múltiples Reglas fiscales a transacciones en base a diferentes factores. Para saber más, visitar la página [Categoría de impuestos](/docs/user/manual/es/accounts/tax-category).

### 3.4 Validez
Se pueden definir fechas de inicio y fin si el impuesto solo debe aplicarse por un período específico. Dejar ambos campos vacíos hará que la Regla fiscal no tenga límite de tiempo.

### 3.5 Prioridad
Establecer un número de prioridad ayudará a decidir el orden en el cual las Reglas fiscales serán aplicadas en el caso de que varias de ellas tengan criterios similares. La mayor prioridad la tendría la regla con el número '1', seguida por la del número '2' y así sucesivamente.

## 4. Funcionamiento de las Reglas fiscales
Funcionan como un filtro para aplicar impuestos de forma automática:

1. Seleccionar un Cliente o una región específica
1. La plantilla de impuesto seleccionada será aplicada según las condiciones definidas en la Regla fiscal
1. Esto será aplicado a nuevas transacciones de venta/compra dependiendo del tipo seleccionado en la Regla

Por ejemplo, seleccionar "Cliente A" en el campo Cliente y "Todos los grupos de productos" hará que la Regla fiscal se aplique en todas las ventas en las que el Cliente sea "Cliente A". De la misma forma, seleccionar "Producto A" y "Todos los grupos de clientes" hará que se aplique a todos los Clientes pero solo cuando el producto es "Producto A". 

Al crear una nueva transacción el sistema seleccionará y aplicará la plantilla de impuesto en base a la regla fiscal definida.

### 5. Temas relacionados
1. [Regla de precios](/docs/user/manual/es/accounts/pricing-rule)
1. [Plantilla de impuestos de producto](/docs/user/manual/es/accounts/item-tax-template)
1. [Categoría de impuesto](/docs/user/manual/es/accounts/tax-category)
1. [Cliente](/docs/user/manual/es/CRM/customer)
1. [Proveedor](/docs/user/manual/es/buying/supplier)
