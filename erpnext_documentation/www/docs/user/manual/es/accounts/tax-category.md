<!-- add-breadcrumbs -->
# Categoría de impuestos

**Una Categoría permite aplicar una o más Reglas fiscales a transacciones en función de varios criterios.**

Si se desea aplicar diferentes tipos de impuestos basados en Categorías, se deben crear las mismas desde:

> Inicio > Contabilidad > Impuestos > Categoría de impuestos

## 1. Prerrequisitos 
Antes de crear y usar Categorías de impuestos se recomienda crear lo siguiente:

1. [Regla fiscal](/docs/user/manual/es/accounts/tax-rule)

## 2. Funcionamiento de las Categorías de impuestos
Para crear una Categoría ir a la lista de Categorías de impuestos, hacer click en Nuevo e ingresar un nombre.

- Una Categoría de impuestos puede estar vinculada a una o varias [Reglas fiscales](/docs/user/manual/es/accounts/tax-rule).
- Esta Categoría de impuestos puede ser asignada a un Cliente, así al seleccionarlo se traerá la categoría automáticamente. Esto aplica también para Proveedores.
- Mediante la Categoría se obtendrá la Plantilla de impuesto de venta vinculada a la Regla fiscal, lo que hará que se completen automáticamente las filas de la tabla de Impuestos.
- La Categoría de impuestos puede ser utilizada para agrupar Clientes a los cuales se les aplicarán los mismos impuestos. Por ejemplo, gobierno, comercial, etc.

  <img class="screenshot" alt="Tax Category" src="{{docs_base_url}}/assets/img/accounts/tax-category.gif">

> Tip: una Categoría puede asignarse a varias Reglas fiscales, por lo que se pueden crear diferentes combinaciones para aplicar los impuestos necesarios en cada transacción.

## 3. Asignación de Categorías de impuestos
La Categoría se determina automáticamente en la transacción ya sea por la Dirección de la entidad o por el Cliente/Proveedor en sí. Se puede asignar la Categoría de impuesto en base a: 

1. [Cliente](/docs/user/manual/es/CRM/customer)
1. [Proveedor](/docs/user/manual/es/buying/supplier)
1. [Dirección](/docs/user/manual/es/CRM/address) de facturación o envío.
Se puede definir si utilizar la dirección de facturación o la de envío en la opción "Determinar la categoría de impuestos de la dirección de" de la Configuración de cuentas. La Categoría de impuesto se determina primero por la Dirección. Si en la dirección no está asignada a ninguna Categoría, se toma la de la entidad.
      ![Tax Cat Address](/docs/assets/img/accounts/tax-cat-address.png)
1. [Producto](/docs/user/manual/es/stock/item#316-item-tax)
1. También se puede seleccionar manualmente en la transacción.
  
## 4. Impacto de la Categoría de impuestos en la transacción

* Plantillas de impuesto de producto específicas para esa Categoría son traídas automáticamente.
* Se pueden crear [Reglas fiscales]({{docs_base_url}}/user/manual/es/accounts/tax-rule) para tomar automáticamente Plantillas de impuestos de venta/compra en base a la diferentes Categorías de la transacción.

## 5. Temas relacionados
1. [Reglas fiscales](/docs/user/manual/es/accounts/tax-rule)
1. [Cliente](/docs/user/manual/es/CRM/customer)
1. [Proveedor](/docs/user/manual/es/buying/supplier)
1. [Dirección](/docs/user/manual/es/CRM/address)
