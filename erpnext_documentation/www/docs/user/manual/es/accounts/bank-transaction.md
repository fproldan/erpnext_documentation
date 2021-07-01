<!-- add-breadcrumbs -->
# Transacción bancaria

Este formulario muestra las transacciones bancarias en ERPNext. 

## 1. Prerequisitos
Antes de usar una Entrada de Transacción Bancaria se recomienda crear lo siguiente:

1. [Banco](/docs/user/manual/es/accounts/bank)
1. [Cuenta bancaria](/docs/user/manual/es/accounts/bank-account)

## 2. Uso de transacciones bancarias
Una entrada de transacción bancaria no debería crearse de forma manual, sino que es creada automáticamente usando [Conciliación bancaria](/docs/user/manual/es/accounts/bank-reconciliation)

### 2.1 Campos adicionales en transacciones bancarias

* Fecha
* Estado:
    * Pendiente
    * Saldado
    * No conciliado
    * Conciliado
* **Cuenta bancaria**: cuenta bancaria desde la cual fueron hechas las transacciones.

## 3. Características/campos 

> Estos campos son actualizados mediante conciliación bancaria y no deberían ser modificados desde el documento mismo.

### 3.1 Divisa/Moneda y Debe - Haber

* **Debe**: monto debitado.
* **Haber**: monto acreditado.
* **Divisa/Moneda**: moneda en la cual se hizo la transacción.
* **Descripción:** una descripción para el extracto bancario.

### 3.2 Referencia

**Número de referencia**: número del cheque u otro documento.

### 3.3 Entradas de pago

* **Documento de pago**: documento contra el cual fue realizada la transacción, ya sea Factura de venta, Reclamación de gastos, Factura de compra, Entrada de pago o Asiento contable.
* **Entrada de pago**: la transacción específica. 
* **Monto asignado**: el monto asignado por la transacción en particular.


- **Monto asignado**: el monto asignado total.
- **Monto sin asignar**: el monto total sin asignar.
