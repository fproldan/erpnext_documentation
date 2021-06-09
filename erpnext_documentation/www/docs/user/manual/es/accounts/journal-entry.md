<!-- add-breadcrumbs -->
# Asiento contable

Todas las entradas contables que no son transacciones de venta o compra se realizan usando el **Asiento contable**. Un **Asiento contable** es una transacción estándar que afecta múltiples Cuentas, en la cual la suma de los débitos es igual a la suma de los créditos. Estas transacciones impactan en el Balance general.

Los Asientos contables pueden ser usados para registrar gastos, entradas de apertura, contra-entradas, pagos bancarios, entradas de impuestos especiales, etc. Por ejemplo, el registro de gastos corrientes, gastos directos como combustible/transporte, gastos varios, entradas de ajuste y ajuste del importe de facturas.

Para acceder a la lista de Asientos contables, ir a:
> Inicio > Contabilidad > Balance general > Asiento contable

## 1. Creación de un asiento contable
1. Ir a la lista de asientos contables y hacer click en Nuevo.
1. El Tipo de entrada por defecto es "Asiento contable". Este es un tipo de entrada de propósito general. Visitar la [sección 3](/docs/user/manual/es/accounts/journal-entry#3-journal-entry-types) para saber más sobre tipos de entrada.
1. Se puede cambiar la Fecha de Contabilización.
1. En la tabla seleccionar la cuenta desde la cual se debitará el monto.
1. Ciertos datos pueden ser agregados seleccionando una [Plantilla de asiento contable](/docs/user/manual/es/accounts/journal-entry-template) en el campo "Desde plantilla".
1. Seleccionar el "Tipo de entidad" y el "Tercero" si es una entrada de deuda.
1. Agregar una fila donde el monto será acreditado.
1. Nótese que, al final, el total del debe y el total del haber deben ser iguales.
1. Guardar y validar.

  <img class="screenshot" alt="Journal Entry" src="{{docs_base_url}}/assets/img/accounts/journal-entry.png">

**Libro de finanzas**: se puede asignar la entrada a un [Libro de finanzas](/docs/user/manual/es/accounts/finance-book) específico. Al dejar este campo vacío, el Asiento contable se mostrará en todos los Libros de finanzas.

### 1.1 Entrada rápida
Al crear un asiento contable, se puede ver el botón **Entrada rápida** arriba a la derecha. Esto simplifica el proceso de creación de entradas. Solo es necesario ingresar el monto, seleccionar las cuentas y agregar una observación. Así se crearán las "Entradas contables" en la tabla con los datos especificados.

![Quick Entry](/docs/assets/img/accounts/quick-entry.png)

## 2. Características
### 2.1 Entradas contables

* **Dimensiones contables**: un Proyecto o Centro de costos puede ser vinculado aquí para tener un seguimiento separado de los costos. Para saber más, visitar esta [página](/docs/user/manual/es/accounts/accounting-dimensions).

  ![Acc Dim](/docs/assets/img/accounts/je-acc-dim.png)

* **Cuenta bancaria Nro**: si se agregó una [Cuenta bancaria](/docs/user/manual/es/accounts/bank-account), se traerá el número asociado con dicha cuenta.
* **Tipo de referencia**: si esta entrada contable está asocida con otra transacción, puede ser referenciada aquí. Se debe seleccionar el tipo de referencia y el documento específico. Por ejemplo, si se está creando un asiento contable contra una factura de venta en específico se vinculará ambos documentos. El monto "pendiente" de esa factura se verá afectado.

  ![Reference](/docs/assets/img/accounts/je_table_reference.png)

  A continuación se listan los documentos que pueden ser seleccionados en el Asiento contable en el campo Tipo de referencia:

    * [Facturas de venta](/docs/user/manual/es/accounts/sales-invoice)
    * [Facturas de compra](/docs/user/manual/es/accounts/purchase-invoice)
    * Asiento contable
    * [Orden de venta](/docs/user/manual/en/selling/sales-order)
    * [Orden de compra](/docs/user/manual/en/buying/purchase-order)
    * [Reembolso de gastos](/docs/user/manual/en/human-resources/expense-claim)
    * [Activo](/docs/user/manual/en/asset/asset)
    * [Préstamo](/docs/user/manual/en/loan-management/loan)
    * [Entrada de Nómina](/docs/user/manual/en/human-resources/payroll-entry)
    * [Anticipo a empleado](/docs/user/manual/en/human-resources/employee-advance)
    * [Revalorización del tipo de cambio](/docs/user/manual/es/accounts/exchange-rate-revaluation)
    * [Descuento de facturas](/docs/user/manual/es/accounts/invoice_discounting)


* **Es un anticipo**: si es un pago adelantado de un Cliente, seleccionar "Sí". Esto es útil cuando se vinculó un documento al asiento contable. Seleccionar "Sí" hará que se lo vincule con el documento elegido en "Nombre de referencia". Para saber más, visitar la página [Pagos adelantados](/docs/user/manual/es/accounts/advance-payment-entry).

* **Observaciones**: cualquier comentario adicional sobre la entrada puede ser agregado en este campo.

### 2.2 Invertir Asiento Contable
En cualquier Asiento contable validado hay un botón para invertirlo. Al hacer click en el botón "Invertir Asiento Contable", el sistema crea un nuevo Asiento contable invirtiendo los montos del debe y el haber contra las cuentas correspondientes.

<img alt="Reverse Journal Entry" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reverse-journal-entry.png">

### 2.3 Crear una entrada con una diferencia
La "diferencia" es el monto restante luego de que se sumen todos los importes del debe y el haber.

Como se trata de un sistema contable de doble entrada, el total del debe debería ser igual al total del haber.

La diferencia debe ser cero para poder validar el Asiento. Si este número es distinto de cero, se puede "Crear una entrada con una diferencia" y el sistema agregará automáticamente una nueva fila con el monto requrido para igualar los totales. Sólo resta seleccionar la cuenta de crédito/débito.

  ![Make Difference](/docs/assets/img/accounts/make-difference.png)

### 2.4 Referencia

El Número de referencia puede ser ingresado de forma manual, junto con una Fecha de referencia. Al especificar un Número de referencia aparecerá una Observación, por ejemplo:

> Nota: proveedor

> Referencia #00036 de fecha 18-04-2019 $1.000,00 contra Factura de venta ACC-SINV-2019-00064

En la sección Referencia, los siguientes campos pueden ser ingresados de forma manual si el comprobante fue generado offline y no en ERPNext. Esto es sólo a modo informativo.

* Factura No.
* Fecha de factura
* Fecha de vencimiento

### 2.5  Multi Moneda

Si las cuentas seleccionadas tienen distintas monedas, tildar la opción "Multi Moneda". Si este campo no está seleccionado, no será posible seleccionar divisas extranjeras en el asiento contable. Esta funcionalidad mostrará las distintas monedas y traerá el "Tipo de cambio". Para saber más, visitar la página [Contabilidad con múltiples divisas](/docs/user/manual/es/accounts/multi-currency-accounting).

![Multi Currency](/docs/assets/img/accounts/je-multi-currency.png)

### 2.6 Plantilla de asientos contables

Campo **Desde plantilla**: seleccionar una opción en este campo cargará los siguientes datos de la plantilla:

- Tipo de entrada
- Compañía
- Secuencia
- Cuenta de cada entrada contable
- De apertura

Para aprender más ir a la página de [Plantilla de asientos contables](/docs/user/manual/es/accounts/journal-entry-template).

### 2.7 Ajustes de impresión

![Journal Print Settings](/docs/assets/img/accounts/je_print_settings.png)

**Pagar a / Recibido de**: el nombre ingresado aquí se verá en las Facturas de venta. Esto es útil para la impresión de cheques. Ir a la vista de impresión en el Asiento contable y seleccionar la opción "Formato de impresión de cheque".

**Membrete**: se puede imprimir el membrete de la compañía en el asiento contable. Más información [aquí](/docs/user/manual/en/setting-up/print/letter-head).

**Imprimir Encabezado**: también es posible elegir un título personalizado para la impresión de asientos contables.
Esto se hace seleccionando una de las opciones en **Imprimir Encabezado**. Para crear una nuevo ir a:

Inicio > Configuración > Impresión > Imprimir Encabezado

Más información [aquí](/docs/user/manual/en/setting-up/print/print-headings).

### 2.7 Más información

* **Método de pago**: ya que se el pago se realice por transferencia directa, transferencia bancaria,tarjeta de crédito, cheque o efectivo. Se pueden crear nuevos Métodos de pago. Si se seleccionó una cuenta bancaria en el método d epago, esta será traída a asiento contable al elegir dicho método.
* **De apertura**: si el asiento es de tipo "Asiento de apertura" este campo pasará a ser "Sí". Para más información visitar la página [Apertura de cuentas](/docs/user/manual/es/accounts/opening-balance).
* **Desde plantilla**: cuando se selecciona una plantilla, la tabla de entradas contables será vaciada y completada con las cuentas definidas en la plantilla. Luego es posible agregar más cuentas de forma manual.

## 3. Tipos de asiento contable
Estas son algunas de las entradas contables que se pueden realizar mediante asiento contable en ERPNext.

### 3.1 Asiento contable

Este es el tipo de entrada de propósito general, la cual puede ser usada con distintos fines, por ejemplo:

#### Gastos (no acumulable)

Mucas veces no será necesario acumular los gastos, por lo que puede ser registrado contra una cuenta de gastos en el pago. Por ejemplo, el costo de transporte o la factura de teléfono. Esto se puede debitar directamente de Gastos de teléfono (en lugar de la compañía de teléfono) y acreditar el pago al Banco.

  * Debe: cuenta de gasto (como gasto de teléfono).
  * Haber: cuenta de banco o efectivo.

#### Acreditar salarios

Para acreditar los salarios de los empleados se utiliza el asiento contable. En este caso,

  * Debe: los componentes del salario.
  * Haber: la cuenta de banco.

### 3.2 Asiento contable entre compañías

Se puede usar este tipo de asiento si una transacción se realiza entre compañía padre y compañía hija, o compañías hermanas, o dos compañías que pertenecen al mismo grupo.

Para saber más visitar la página [Asiento contable entre compañías](/docs/user/manual/es/accounts/inter-company-journal-entry).

### 3.3 Registro de banco

Este tipo de asiento se usa al realizar o recibir pagos usando una [Cuenta bancaria](/docs/user/manual/es/accounts/bank-account). Por ejemplo, pagar gastos de entretenimiento etc. usando la cuenta bancaria de la compañía.

### 3.4 Entrada de caja

Similar al "Registro de banco" pero cuando el pago se realiza mediante cuentas de efectivo.

### 3.5 Ingreso de tarjeta de crédito

Con este tipo de entrada se puede identificar facilmente las entradas de trarjeta de crédito.

### 3.6 Nota de débito

Este documento es enviado por un cliente (la compañía propia) a un proveedor (de la compañía) al realizar una devolución.

También pueden crearse Notas de débito diretamente desde Facturas de compra.

Una "Nota de débito" es realizada para un proveedor contra una factura de compra o aceptada como nota de crédito de un proveedor cuando la compañía devuelve productos. Al hacer esto, la compañía puede recibir un pago del proveedor o ajustar el monto en otra factura.

  * Debe: cuenta del proveedor.
  * Haber: cuenta de devolución de la compra.

Para saber más visitar esta [página](/docs/user/manual/es/accounts/debit-note).

### 3.7 Nota de crédito

Este documento es enviado por un proveedor a un cliente al devolver productos.

Una "Nota de crédito" es realizada para un cliente contra una factura de venta cuando la compañía necesita ajustar un pago por devoluición de bienes. Al hacer esto, el vendedor puede hacer un pago al cliente o ajustar el monto en otra factura.

  * Debe: cuenta de devolución de venta.
  * Haber: cuenta del cliente.

Para saber más visitar la [página](/docs/user/manual/es/accounts/credit-note).

> Generalmente la nota de débito/crédito se genera por el monto de los bienes devueltos o menos.

### 3.8 Contra entrada

Una contra entrada se realiza cuando la transacción registra dentro de la misma compañía entradas del tipo:

* Efectivo a efectivo
* Banco a banco
* Efectivo a banco
* Banco a efectivo

Esto se usa para registrar retiros o depósitos en una cuenta bancaria. Al usar esta entrada, el dinero no sale de la compañía a menos que sea usado nuevamente para pagar algo.

### 3.9 Registro de impuestos especiales

Cuando una compañía compra bienes a un proveedor, paga impuestos especiales sobre los mismos. Cuando la compañía vende estos productos a los clientes, recibe el importe de esos impuestos. La compañía descontará el pago de los impuestos y depositará el saldo en las cuentas gubernamentales.

  * Cuando una compañía compra productos con impuestos especiales:
    * Debe: cuenta de compra, cuenta de impuesto especial.
  	* Haber: cuenta de proveedor.

  * Cuando una compañía vende productos con impuestos especiales:
    * Debe: cuenta de cliente.
  	* Haber: cuenta de venta, cuenta de impuesto especial.

### 3.10 Diferencia de desajuste

Si se está cancelando una deuda por incobrable, se puede crear un asiento contable similar a un pago, salvo que en lugar de debitar de la cuenta de banco se selecciona una cuenta de gasto llamada deudas incobrables.

  * Debe: cuenta de deudas incobrables.
  * Haber: cliente.

> Nota: en ciertos países se deben cumplir ciertas regulaciones antes de cancelar una deuda incobrable.

### 3.11 Asiento de apertura

Esta entrada es utilizada al trasladarse desde otro sistema a ERPNext en cualquier momento del año. Las facturas pendientes y demás pueden ser registradas usando este tipo de asiento. Seleccionar esta opción traerá las cuentas del Balance general.

### 3.12 Entrada de Depreciación

Se produce una depreciación cuando se cancela un valor de entre los activos y pasa a ser un gasto. Por ejemplo, si se tiene una computadora que se usará por 5 años, se puede distribuír el gasto a lo largo de este período y generar un asiento al fin de cada año reduciendo este valor por un determinado porcentaje.

  * Debe: depreciación (gasto).
  * Haber: activo (cuenta en la cual se registró el activo que se depreciará).

Para saber más, visitar la página [Depreciacion de activos](/docs/user/manual/en/asset/asset-depreciation).

> Nota: en ciertos países hay regulaciones que definen un monto máximo por el cual se puede depreciar cierta clase de activos.

### 3.13 Revalorización del tipo de cambio

Si el Plan de cuentas posee múltiple divisas, un asiento contable del tipo "Revalorización del tipo de cambio" ayuda a lidiar con esta situación. Este asiento debe crearse desde el documento de Revalorización del tipo de cambio. Para saber más visitar la página [Revalorización del tipo de cambio](/docs/user/manual/es/accounts/exchange-rate-revaluation).

### 3.14 Ajuste por inflación

Este tipo de asiento se genera al utilizar la herramienta [Ajuste por inflación](/docs/user/manual/es/accounts/ajuste-por-inflacion).

### 3.15 Cheque Rechazado / Depositado / Cobrado

Cada uno de estos asientos se utiliza para registrar la operación respectiva realizada sobre cheques. Al seleccionar una de estas opciones aparecerá el campo Cheque en el cual se eligirá el cheque sobre el cual se está realizando la operación. Más información al respecto en los artículos [Cheque de tercero](/docs/user/manual/es/accounts/cheque-de-tercero) y [Cheque propio](/docs/user/manual/es/accounts/cheque-propio).

### 4. Temas relacionados
1. [Asiento contable entre compañías](/docs/user/manual/es/accounts/inter-company-journal-entry)
1. [Nota de crédito](/docs/user/manual/es/accounts/credit-note)
1. [Nota de débito](/docs/user/manual/es/accounts/debit-note)
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Botón de entrada con una diferencia](/docs/user/manual/es/accounts/articles/difference-entry-button)
1. [Libro de finanzas](/docs/user/manual/es/accounts/finance-book)
