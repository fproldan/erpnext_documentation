<!-- add-breadcrumbs -->
# Cuenta bancaria

En ERPNext, las cuentas bancarias pueden crearse para una Compañía o para Clientes, Proveedores, etc. Hacer esto permite registrar correctamente todas las transacciones bancarias para un mayor control. Luego estas cuentas pueden elegirse en [Entradas de pago](/docs/user/manual/es/accounts/payment-entry) como [Método de pago](/docs/user/manual/es/accounts/mode-of-payment).

Para acceder a Cuentas bancarias, ir a:
> Inicio > Contabilidad > Extracto Bancario > Banco

![Bank Account](/docs/assets/img/accounts/bank-account.png)

## 1. Prerequisitos
Antes de crear y usar una cuenta bancaria, se recomienda haber creado previamente el [Banco](/docs/user/manual/es/accounts/bank) correspondiente.

## 2. Creación de Cuentas bancarias
1. Ingresar el nombre de la cuenta.
1. Vincular la cuenta del Balance general definida en "Cuentas bancarias" en el [Plan de cuentas](/docs/user/manual/es/accounts/chart-of-accounts).
1. Seleccionar un banco.
1. Guardar.

### 2.1 Opciones adicionales en la creación de cuentas bancarias

* **Es la cuenta predeterminada**: tildar esta opción hará que se tome esta cuenta como predeterminada para todas las transacciones contables.
* **Es la cuenta de la empresa**: tildar esta opción si esta es la cuenta bancaria de la compañía.
* Se puede especificar el tipo y subtipo de cuenta, para una clasificación más detallada en reportes, etc.

## 3. Características
### 3.1 Detalles de la entidad

* **Tipo de entidad**: si no es una cuenta de la compañía se debe especificar a quién pertenece. Las opciones posibles son: Cliente, Empleado, Miembro, Accionista, Estudiante y Proveedor. 
* **Tercero**: seleccionar el Cliente/Proveedor, etc en particular.

### 3.2 Detalles de la cuenta

A modo informativo, ERPNext permite definir los siguientes datos sobre la cuenta bancaria:

* IBAN
* Número de Cuenta Bancaria
* Código de la sucursal
* Número SWIFT 

### 3.3 Dirección y contacto

* **Dirección**: un banco puede tener múltiples en la misma localidad. La dirección de la sucursal puede especificarse aquí.
* **Contacto**: los bancos por lo general proporcionan un contacto para cuentas corporativas. Dicho dato puede agregarse aquí.
* **Sitio Web**: aquí se puede guardar la URL del sitio web del banco.
