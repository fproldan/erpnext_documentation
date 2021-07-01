<!-- add-breadcrumbs -->
# Asiento contable entre compañías	

**Un Asiento contable entre compañías se realiza entre organizaciones que pertenecen al mismo grupo.**

Se puede crear un Asiento contable entre compañías si se realizan transacciones con múltiples compañías.
Se pueden seleccionar las cuentas que se desea usar en la transacción. Un posible caso de uso sería el de una compañía que compra bienes de otra compañía.

Antes de crear un Asiento contable entre compañías se necesita tener definido el Plan de cuentas.

1. Ir a: **Contabilidad > Empresa y Contabilidad > Plan de cuentas**.
1. Seleccionar la cuenta que se desea usar como cuenta interna en la transacción tildando el campo "Cuenta entre empresas". Se recomienda crear nuevas cuentas para este tipo de transacciones.

    <img class="screenshot" alt="Internal Account" src="{{docs_base_url}}/assets/img/accounts/internal-account.png">

Se debe hacer lo mismo para todas las compañías que van a formar parte de estas transacciones.

En el caso de compañías padre-hijo, al crear una cuenta en la compañía padre, esta se agrega en la compañía hija. Esto funciona solo si se seleccionó la opción de crear Plan de cuentas de la compañía hija basándose en el de la compañía padre.

Los Asientos contables entre compañías se crean por medio de un Asiento contable. Para acceder a la lista de Asientos contables, ir a:

> Inicio > Contabilidad > Empresa y Contabilidad > Asiento contable

## 1. Prerrequisitos
Antes de crear un Asientos contables entre compañías, se necesita lo siguiente:

* Tener al menos dos [Compañías](/docs/user/manual/es/setting-up/company-setup)
* Definir en el [Plan de cuentas](/docs/user/manual/es/accounts/chart-of-accounts) las cuentas a utilizar

## 2. Creación de Asientos contables entre compañías
1. Ir al listado de Asientos contables y hacer click en Nuevo.
1. Seleccionar "Asiento contable entre compañías" en "Tipo de entrada".
1. Seleccionar la compañía que está comprando los productos.
1. Añadir las filas para cada entrada contable. Solo se podrá seleccionar cuentas entre compañías.
1. En cada fila se debe especificar:
  * la cuenta interna. 
  * el monto a debitar o acreditar.
  * el centro de costo (si es un ingreso o un gasto).
6. Al validar el asiento, se encontrará un botón en la esquina superior derecha con el texto **Hacer el asiento contable entre compañías**.

   <img class="screenshot" alt="Submitted Inter Company Journal Entry" src="{{docs_base_url}}/assets/img/accounts/inter-company-jv-submit.png">

1. Hacer click en el botón. Se deberá seleccionar la compañía contra la cual se desea crear el asiento asociado.

    <img class="screenshot" alt="Select Company" src="{{docs_base_url}}/assets/img/accounts/select-company-jv.png">

1. Al seleccionar la compañía se redirigirá a otro asiento donde los campos relevantes serán completados automáticamente (Compañía, Tipo de entrada, referencia al Asiento contable entre compañías, etc.) 

    <img class="screenshot" alt="Linked Journal Entry" src="{{docs_base_url}}/assets/img/accounts/linked-jv.png">

1. Seleccionar las cuentas internas para la segunda compañía.
1. Validar el asiento contable.
1. Revisar que el total del debe y del haber sean iguales pero opuestos a los del asiento previamente creado.

**Nota:** las cuentas del segundo asiento deben seleccionarse de forma opuesta a como se lo hizo en el primer asiento.
Por ejemplo, si la compañía A compra algo a la compañía B, así es como deberían verse los asientos creados:

1. Se debitan 500 de la cuenta bancaria y se acredita 500 a la cuenta de deudores de la compañía B.
1. En el Asiento contable entre compañías, se debitan 500 de la cuenta de acreedores de la compañía A y se acreditan 500 a la cuenta bancaria. 
1. También se deben seleccionar las entidades para los acreedores y deudores.

Se encontrará el link de referencia en dicha sección, el cual será añadido en ambos asientos y será eliminado si alguno de los asientos fuera cancelado.

### 3. Temas relacionados
1. [Asiento contable](/docs/user/manual/es/accounts/journal-entry)
1. [Facturas entre compañías](/docs/user/manual/es/accounts/inter-company-invoices)
