<!-- add-breadcrumbs -->
# Conciliación bancaria

**La Conciliación bancaria es utilizada en ERPNExt para vincular los estados contables con los estados bancarios.**

Pueden existir diferencias entre los movimientos bancarios registrados en sistema y los que se visualizan en el extracto bancario por distintos motivos. 

El Banco puede, y de hecho es habitual, que debite gastos de la cuenta bancaria que no se conocen a priori con importe y fecha cierta (y por ende no se podrán tener registrados de antemano en el sistema).

A su vez, si se recibe o realiza un pago mediante cheque, el estado bancario no coincidirá exactamente con las fechas de la entrada de pago. Desde la fecha de pago del cheque, el tenedor del mismo dispone de un plazo cierto para enviarlo al cobro (actualmente en Argentina es de 30 días). A su vez, también hay una demora entre el depósito y el cobro del cheque (debido al clearing bancario), que oscila alrededor de las 48 horas hábiles.

Todo esto hace que las fechas de las entradas de pagos, las fechas de depósito de los cheques, y las fechas de débito/crédito en las cuentas bancarias sean diferentes.

En ERPNext se pueden sincronizar los estados contables y los Asientos contables mediante las fechas de transacciones.

## 1. Estado de conciliación bancaria
El reporte de Conciliación bancaria muestra la diferencia entre el balance informado en el estado bancario de la organización provisto por el banco contra el importe registrado en el Plan de cuentas de la compañía.

Así se ve un estado de Conciliación bancaria:

<img class="screenshot" alt="Bank Reconciliation statement" src="{{docs_base_url}}/assets/img/accounts/bank-reconciliation-2.png"> 

En el reporte, verificar que el campo 'Balance as per bank' coincida con el Bank Account Statement. Si coincide, significa que la fecha de liquidación está actualizada para todas las entradas bancarias. Si hay alguna discordancia significa que la fecha de liquidación todavía no está actualizada en las entradas bancarias.

Para acceder a la Conciliación bancaria, ir a:
> Inicio > Contabilidad > Banco y Pagos > Actualizar Fechas de Transacciones Bancarias

## 2. Actualización de Fechas de Transacciones Bancarias

1. Ir a Actualizar Fechas de Transacciones Bancarias.
1. Seleccionar la cuenta bancaria.
1. Seleccionar fecha desde y hasta.
1. Se puede optar por incluír entradas reconciliadas y transacciones POS.
1. Hacer click en el botón **Obtener entradas de pago**.
1. Aparecerán en la tabla las entradas de pago de Banco.
1. En cada entrada se deberá actualizar la "Fecha de liquidación" y luego hacer click en el botón **Actualizar fecha de liquidación**.

Luego de hacer esto se podrá sincronizar las entradas y los estados bancarios en el sistema.

<img class="screenshot" alt="Bank Reconciliation" src="{{docs_base_url}}/assets/img/accounts/bank-reconciliation.png">
 
## 3. Herramienta de conciliación bancaria

ERPNext ofrece una herramienta de conciliación semi-automática, que permite liquidar transacciones bancarias contra pagos a facturas de venta o compra, entradas de pago o reembolsos de gastos.

### Actualización del estado bancario

Se puede importar en el sistema el estado bancario en formato CSV o XLS mediante la herramienta de conciliación bancaria.

1. Descargar el reporte desde el sistema del banco

 <img class="screenshot" alt="Reconcile bank transactions" src="{{docs_base_url}}/assets/img/accounts/sample_bank_statement.png">
 
Es importante asegurarse de que este reporte contenga al menos la fecha, el débito/crédito y la moneda en cada fila.

2. Configurar el formato de importación en el Banco correspondiente

 <img class="screenshot" alt="Reconcile bank transactions" src="{{docs_base_url}}/assets/img/accounts/bank_configuration.png">

El archivo será procesado por ERPNext y se usará la información obtenida para completar los campos correspondientes en la transacción bancaria.

3. Actualizar el archivo en el sistema

 <img class="screenshot" alt="Reconcile bank transactions" src="{{docs_base_url}}/assets/img/accounts/bank_transaction_upload.gif">
 
### Conciliación de cuentas bancarias

Luego de haber cargado en el sistema todas las transacciones bancarias, se las puede conciliar con los pagos existentes. Si se encuentra un pago que parece coincidir con la transacción bancaria seleccionada, ERPNext propondrá dicho pago para conciliar con la transacción.

Si el pago cioncide, solo se deberá hacer click en Conciliar para confirmar la operación.

<img class="screenshot" alt="Reconcile bank transactions" src="{{docs_base_url}}/assets/img/accounts/auto_reconciliation.gif">

Si ERPNext no propone ningún pago, es posible seleccionarlo de forma manual:

<img class="screenshot" alt="Reconcile bank transactions manually" src="{{docs_base_url}}/assets/img/accounts/manual_reconciliation.gif">

También se puede crear un nuevo pago o factura directamente desde el tablero de Conciliación bancaria.

<img class="screenshot" alt="New payment entry" src="{{docs_base_url}}/assets/img/accounts/new_payment.gif">

### Conciliación de cheques de terceros desde la herramienta de conciliación bancaria

Si se verifica en el extracto un movimiento correspondiente a un pago, cobro o depósito de un cheque de terceros; el mismo puede matchearse de acuerdo a la opción *Match against Voucher* con el movimiento que corresponda.

Se deberán completar los campos restantes y validar la operación.

### Conciliación de cheques propios desde la herramienta de conciliación bancaria

Si se verifica en el extracto un movimiento correspondiente a un pago, cobro o depósito de un cheque propio; la conciliación adquiere ciertas particularidades.

En primer lugar, deberá seleccionarse en el selector de *Acción* la opción *Create Voucher*, y en *Tipo de Documento* deberá seleccionarse *Asiento Contable*. Luego, en *Journal Entry Type* deberá elegirse entre *Cheque Rechazado, Cheque Depositado y Cheque Cobrado*, y eso permitirá que se desplieguen los valores posibles a elegir en el selector de *Cheque*. 

Se deberán completar los restantes campos y validar la operación.

## 4. Temas relacionados
1. [Conciliación de pagos](/docs/user/manual/es/accounts/payment-reconciliation)
1. [Garantía Bancaria](/docs/user/manual/es/accounts/bank-guarantee)
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
