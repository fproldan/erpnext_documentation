<!-- add-breadcrumbs -->
# Revalorización del tipo de cambio

En ERPNext se pueden realizar entradas contables en múltiples divisas. Por ejemplo, si se tiene una cuenta bancaria en una moneda extranjera, es posible hacer transacciones en dicha divisa y el sistema mostrará el balance en la moneda seleccionada.

El propósito de la Revalorización del tipo de cambio es ajustar las cuentas del Balance General de acuerdo a las modificaciones en el Cambio de divisas. Esto es útil cuando se quiere cerrar los libros contables y actualizar las cuentas del Balance general trayendo el dinero de cuentas con otras divisas.

Para acceder a la lista de Revalorización del tipo de cambio, ir a:
> Inicio > Contabilidad > Multi moneda > Revalorización del tipo de cambio

## 1. Configuración de la moneda en una cuenta

1. Primero se debe asignar la divisa en un registro de cuenta.
1. Se puede definir la Divisa desde el Plan de cuentas al crear una.

 <img class="screenshot" alt="Set Currency from Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/multi-currency/chart-of-accounts.png">
 
3. También es posible asignar o modificar la divisa de cuentas existentes abriendo el registro de la cuenta que se desea editar.
4. Hacer click en la Cuenta y luego en Editar.

 <img class="screenshot" alt="Modify Account Currency"  src="{{docs_base_url}}/assets/img/accounts/multi-currency/account-set-currency.png">

## 2. Habilitar la Revalorización del tipo de cambio

La funcionalidad de Revalorización del tipo de cambio está diseñada para poder lidiar con situaciones en las que se tienen diferentes divisas en el Plan de cuentas de una Compañía.

1. Ir a: **Configuración > Compañía > *seleccionar la compañía***.
1. Establecer la cuenta correspondiente en el campo "Cuenta de Ganancia / Pérdida de Canje no realizado" en la Compañía. Esta cuenta ayudará a balancear la diferencia entre el total de crédito y el total de débito.
 <img class="screenshot" alt="Field Set for Company"   src="{{docs_base_url}}/assets/img/accounts/field_set_company.png">
 
3. Ir a **Contabilidad > Configuración > Revalorización del tipo de cambio > Nuevo**.
4. Seleccionar la Compañía.
5. Hacer click en el botón "Obtener entradas". Esto traerá las cuentas que tienen divisa diferente de la predeterminada definida en la Compañía.
6. Esto traerá el nuevo Valor de cambio automáticamente si no fue definido en el [Tipo de cambio](/docs/user/manual/es/accounts/currency-exchange). Si fue definido, traerá ese Valor de cambio.
 <img class="screenshot" alt="Exchange Rate Revaluation"   src="{{docs_base_url}}/assets/img/accounts/exchange-rate-revaluation.png">

7. Al validar aparecerá el botón **Crear Asiento contable**.
<img class="screenshot" alt="Exchange Rate Revaluation Submitting"    src="{{docs_base_url}}/assets/img/accounts/exchange-rate-revaluation-submit.png">

8. Al hacer click en este botón se creará el asiento contable para la Revalorización del tipo de cambio.
<img class="screenshot" alt="Journal Entry"   src="{{docs_base_url}}/assets/img/accounts/journal-entry-exchange.png">

9. Al validar el asiento contable, el Balance general se verá afectado de la siguiente manera:
<img class="screenshot" alt="Journal Entry"   src="{{docs_base_url}}/assets/img/accounts/journal-entry-exchange-submit.png">

### 3. Temas relacionados
1. [Asiento contable entre compañías](/docs/user/manual/es/accounts/inter-company-journal-entry)
1. [Facturas entre compañías](/docs/user/manual/es/accounts/inter-company-invoices)
