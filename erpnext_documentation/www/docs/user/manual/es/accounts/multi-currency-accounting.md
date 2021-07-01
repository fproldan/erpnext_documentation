<!-- add-breadcrumbs -->
# Contabilidad con múltiples divisas

**Realizar transacciones en dos monedas diferentes se conoce como Contabilidad con múltiples divisas.**

En ERPNext se pueden hacer entradas contables con diferentes monedas. Por ejemplo, si se tiene una cuenta bancaria en una moneda extranjera, se pueden hacer transacciones en esa divisa y el sistema mostrará el balance bancario solo en esa moneda.

Se puede tener cuentas en monedas extranjeras por las diferentes sucursales de la Compañía o cuentas de deudores/acreedores para Clientes/Proveedores extranjeros.

## 1. Configuración
### 1.1 Establecer la divisa en el Plan de cuentas
Para comenzar a utilizar contabilidad con múltiples divisas, se necesita asignar la moneda en la Cuenta. Se puede definir desde el [Plan de cuentas](/docs/user/manual/es/accounts/chart-of-accounts) al crear la cuenta.

<img class="screenshot" alt="Modify Account Currency" src="{{docs_base_url}}/assets/img/accounts/multi-currency/account-set-currency.png">


### 1.2 Nueva cuenta con diferente divisa
También se puede asignar/modificar la moneda de una cuenta existente.

<img class="screenshot" alt="Set Currency from Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/multi-currency/account-set-currency-1.png">

### 1.3 Divisa por Cliente/Proveedor
Es posible elegir una moneda de facturación para cada Cliente/Proveedor (entidad), si esta es diferente a la de la Compañía. También se deberá mencionar la Cuenta por cobrar/pagar en esa moneda.

<img class="screenshot" alt="Customer Accounting Currency"    src="{{docs_base_url}}/assets/img/accounts/multi-currency/customer-currency.png">

### 1.4 Después de la configuración
Una vez que se define la divisa en las cuentas requeridas y se seleccionan las cuentas relevantes en la entidad, es posible realizar transacciones contra ellos.

Si la moneda de la cuenta de la entidad es diferente a la de la Compañía, el sistema no permitirá realizar la transacción. Se deberá cambiar la moneda en la transacción (Orden o Factura de Compra/Venta).

Si la moneda de la cuenta de la entidad es la misma que la de la Compañía, se puede realizar transacciones para esa entidad en cualquier moneda.

Las entradas contables (Balance general) se harán siempre en la moneda de la entidad.

> **Nota**: al realizar facturas/pagos asegurarse de que está seleccionada la cuenta con la moneda correcta en el campo "Debitar a".

Se puede cambiar la moneda en la entidad/cuenta antes de hacer cualquier transacción. Luego de generar las entradas contables, el sistema no permitirá cambiar la divisa de ambos.

En el caso de que se tengan múltiples compañías, la moneda de la entidad debe ser la misma para todas las compañías. 

## 2. Tipos de cambio
ERPNext cuenta con el Cambio de divisas para manejar los tipos de cambio al trabajar con múltiples divisas. Esto permite guardar las cotizaciones de cambio que se requieran. Para saber más, visitar la página [Cambio de divisa](/docs/user/manual/es/accounts/currency-exchange).

Para transacciones con moneda extranjera, ERPNext chequea tipos de cambio desde:

1. El Cambio de divisas.
1. Si no se encuentra ninguno, ERPNext intentará obtener el tipo de cambio actual del mercado.
1. Si esto también falla, el tipo de cambio deberá ser ingresado manualmente.

Las tasas de cambio del Cambio de divisas son obtenidas si está habilitada la opción "Permitir Tipos de Cambio Obsoletos" en la configuración de cuentas. Para saber más, visitar la página [Configuración de cuentas](/docs/user/manual/es/accounts/accounts-settings).

## 3. Transacciones

### 3.1 Facturas de venta

En una Factura de venta, la moneda de la transacción debe ser la misma que la del Cliente, si es que es diferente a la de la Compañía. Sino, se puede seleccionar cualquier divisa en la factura. Al seleccionar un Cliente, el sistema traerá una cuenta por cobrar del mismo o de la Compañía. La divisa de la cuenta debe ser la misma que la del Cliente.

En las facturas, el Monto pagado será ingresado en la moneda de la transacción y no en la de la Compañía. El Importe de cancelación también estará en la misma moneda que la transacción.

El Monto pendiente y el Importe anticipado siempre serán calculados y mostrados en la moneda del Cliente. Los montos pagados se verán reflejados en la [Entrada de pago](/docs/user/manual/es/accounts/payment-entry):

<img class="screenshot" alt="Sales Invoice Outstanding"   src="{{docs_base_url}}/assets/img/accounts/multi-currency/paid-amount.png">

### 3.2 Facturas de compra

De la misma forma, las entradas contables serán hechas en base a la moneda del Proveedor, al igual que el Monto pendiente y el Importe anticipado. El Importe de cancelación estará en la moneda de la transacción.

### 3.3 Asiento contable

En un Asiento contable se pueden hacer transacciones en diferentes divisas. Existe una opción "Multi moneda", la cual habilita la selección de cuentas con distintas monedas.

<img class="screenshot" alt="Journal Entry Exchange Rate" src="{{docs_base_url}}/assets/img/accounts/multi-currency/journal-entry-multi-currency.png">
 
En la tabla de cuentas, al seleccionar una con moneda extranjera, el sistema mostrará la sección Divisa / Moneda y traerá la moneda de la cuenta y el Tipo de cambio de forma automática. Se puede modificar la tasa de cambio manualmente. Los montos de debe/haber deberán ser ingresados en la moneda de la cuenta, el sistema se encargará de calcular y mostrar estos valores en la divisa de la Compañía.

<img class="screenshot" alt="Journal Entry in multi currency" src="{{docs_base_url}}/assets/img/accounts/multi-currency/journal-entry-row.png">

## 4. Reportes

### 4.1 Balance general

En el Balance general, el sistema muestra los montos de debe/haber en la moneda de la entidad **si se está filtrando** por una cuenta y la moneda de la misma es diferente a la de la Compañía.

<img class="screenshot" alt="General Ledger Report"   src="{{docs_base_url}}/assets/img/accounts/multi-currency/general-ledger.png">

### 4.2 Cuentas por cobrar/pagar

En el reporte de Cuentas por cobrar/pagar, el sistema muestra todos los importes en la moneda de la entidad/cuenta.

<img class="screenshot" alt="Accounts Receivable Report"  src="{{docs_base_url}}/assets/img/accounts/multi-currency/accounts-receivable.png">

### 5. Temas relacionados
1. [Revalorización del tipo de cambio](/docs/user/manual/es/accounts/exchange-rate-revaluation)
1. [Cambio de Divisas](/docs/user/manual/es/accounts/currency-exchange)
1. [Divisa/moneda](/docs/user/manual/es/accounts/currency)
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Factura de compra](/docs/user/manual/es/accounts/purchase-invoice)
