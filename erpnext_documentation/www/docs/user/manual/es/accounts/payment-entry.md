<!-- add-breadcrumbs -->
# Entrada de pago

**Una Entrada de pago es el registro del pago de una factura.**

Las Entradas de pago pueden realizarse contra las siguientes transacciones:

* Facturas de venta
* Facturas de compra
* Ordenes de venta (Pago adelantado)
* Orden de compra (Pago adelantado)
* Reembolso de gastos
* Transferencia interna

En ERPNext, hay dos formas de las cuales se puede registrar un pago:

* Entrada de pago (predeterminada)
* Asiento contable

Los siguientes diagramas muestran el ciclo dentro del cual se genera el pago:

En ventas:
![Payment Sales]({{docs_base_url}}/assets/img/accounts/pe-sales.png)

En compras:
![Payment Purchase]({{docs_base_url}}/assets/img/accounts/pe-purchase.png)


Para ingresar a la lista de Entradas de pago, ir a:
> Inicio > Contabilidad > Cuentas por cobrar/pagar > Entrada de pago

## 1. Prerrequisitos
Se pueden crear Entradas de pago directamente desde la lista para luego vincularlas a una orden o factura. Antes de crear y usar una Entrada de pago, se recomienda crear lo siguiente:

1. [Cliente](/docs/user/manual/en/CRM/customer)
1. [Proveedor](/docs/user/manual/en/buying/supplier)
1. [Cuenta bancaria](/docs/user/manual/en/accounts/bank-account)

Si se está siguiendo el ciclo de ventas/compras se necesita lo siguiente:

1. [Orden de venta](/docs/user/manual/en/selling/sales-order) (Pago adelantado)
1. [Orden de compra](/docs/user/manual/en/buying/purchase-order) (Pago adelantado)
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Factura de compra](/docs/user/manual/es/accounts/purchase-invoice)

Configuración:

1. [Plan de cuentas](/docs/user/manual/es/accounts/chart-of-accounts)
1. [Compañía](/docs/user/manual/es/setting-up/company-setup) (cuentas predeterminadas)

## 2. Creación de una Entrada de pago
Al validar un documento contra el cual se puede generar Entradas de pago, se encontrará la opción "Pago" debajo del botón **Crear**.

![Payment Entry from SO]({{docs_base_url}}/assets/img/accounts/payment-entry-so.png)

1. Cambiar la fecha de creación.
2. El Tipo de pago se asignará automáticamente dependiendo de la transacción desde la cual se lo haya generado. Puede ser Tipo de pago "Recibir/Recibido", "Pagar", "Transferencia interna".
3. El Tipo de entidad, Tercero y Nombre de Parte serán traídos automáticamente.
4. Las cuentas "Cuenta pagado hasta" y "De cuenta de pago" se obtendrán de la [Compañía](/docs/user/manual/es/setting-up/company-setup).
5. El importe Cantidad Pagada se tomará de la factura.
6. Guardar y validar.
 ![Payment Entry from SO]({{docs_base_url}}/assets/img/accounts/payment-entry-so.gif)

### 2.1 Creación manual de una Entrada de pago
Una Entrada de pago creada manualmente no estará vinculada con ninguna orden o factura. Estos pagos se registrarán en la cuenta del Cliente/Proveedor y pueden ser conciliados luego usando la herramienta de [Conciliación de pagos](/docs/user/manual/es/accounts/payment-reconciliation).

1. Ir a la lista de Entradas de pago.
1. Seleccionar el Tipo de entidad y el respectivo Cliente/Proveedor.
1. Seleccionar la cuenta bancaria/de caja en "Cuenta pagado hasta" y "De cuenta de pago". Ingresar el número de cheque y fecha si es una transferencia bancaria.
1. Ingresar el importe Cantidad Pagada.
1. Guardar y validar.

## 3. Características

### 3.1 Método de pago

Este atributo ayuda a clasificar las Entradas de pago basándose en el método de pago usado. Este puede ser Banco, Caja, Transferencia directa, etc.

> **Tip**: En el [Método de pago](/docs/user/manual/es/accounts/mode-of-payment) se puede definir una cuenta predeterminada, la cual será usada en las Entradas de pago.

En el caso de seleccionar un Método de pago de tipo **Cheque**, aparecerá una tabla para cargar los mismos debajo de la sección Cuentas. Para más información sobre el uso de Entradas de pago con Cheques visitar los artículos [Cheque de tercero](/docs/user/manual/es/accounts/cheque-de-tercero) y [Cheque propio](/docs/user/manual/es/accounts/cheque-propio).

### 3.2 Pago de/a

![Payment Party]({{docs_base_url}}/assets/img/accounts/payment-party.png)

* **Tipo de entidad**: Cliente, Proveedor, Empleado, Accionista, Estudiante o Miembro.
* **Tercero**: para quien se realiza la entrada de pago.
* **Nombre de Parte**: nombre del tercero (es traído automáticamente).
* **Cuenta bancaria de la compañía**: [cuenta bancaria](/docs/user/manual/es/accounts/bank-account) de la compañía.
* **Cuenta bancaria del tercero**: [cuenta bancaria](/docs/user/manual/es/accounts/bank-account) de la entidad.
* **Contacto**: si el tercero es una organización se puede especificar el contacto de una persona que la represente.

### 3.3 Cuentas

![Payment Accounts]({{docs_base_url}}/assets/img/accounts/payment-accounts.png)

* **Saldo de tercero/s**: monto general recibido/pagado de/a un Cliente/Proveedor por las facturas vinculadas con la actual Entrada de pago. Los importes pagados serán positivos y los pagos adelantados se mostrarán como negativos.
* **De cuenta de pago**: la [cuenta](/docs/user/manual/es/accounts/chart-of-accounts) de la cual se debitará el importe cuando el pago sea validado.
* **Cuenta pagado hasta**: [cuenta](/docs/user/manual/es/accounts/chart-of-accounts) a la cual se sumará el monto de la Entrada de pago al validarla.
* **Divisa de cuenta**: las divisas de estas [cuentas](/docs/user/manual/en/accounts/chart-of-accounts) serán traídas como se lo haya definido en cada una de ellas y no podrán ser editadas aquí. Para saber más sobre transacciones con múltiples divisas visitar la siguiente [página](/docs/user/manual/en/accounts/articles/managing-transactions-in-multiple-currency).
* **Balance de la cuenta**: monto total del balance de todas las facturas de las cuentas seleccionadas.
* **Cantidad Pagada**: es el **monto total** pagado en la Entrada de pago.

> **Nota**: al realizar Entradas de pago, la cuenta bancaria será traída en el siguiente orden dependiendo de dónde esté definido algún valor predeterminado:
> * Compañía
> * Cuenta predeterminada del método de pago
> * Cuenta bancaria predeterminada del Cliente/Proveedor
> * Cuenta seleccionada manualmente en la Entrada de pago

### 3.4 Referencia

#### Obtención de facturas pendientes

Esto puede ser usado para realizar pagos sobre múltiples Facturas de venta usando una sola Entrada de pago. Al crear una nueva Entrada de pago, clickeando el botón **Obtener facturas pendientes** todas las facturas y ordenes pendientes de la organización serán añadidas a la tabla. Es necesario ingresar un valor en el campo "Cantidad pagada" para ver este botón. También se puede seleccionar un rango de fechas y facturas específicas para agregar.

![Outstanding Invoice]({{docs_base_url}}/assets/img/accounts/outstanding-pe.png)

Si la entidad no ha realizado un pago completo, se debe ingresar el monto pagado en el campo "Numerado".

Si se está creando una Entrada de pago para un Cliente, el monto pagado será asignado contra las Facturas de Venta. De igual forma, al crear una Entrada de pago para un Proveedor, el monto pagado se asignará contra Facturas de Compra.

#### Tabla de referencias del pago

* **Tipo**: el pago puede realizarse contra Ordenes de venta, Facturas de venta o Asientos contables.
* **Nombre**: el identificador de la transacción en particular aparece en este campo.
* **Importe Total**: el importe total de la transacción de la fila en cuestión.
* **Excepcional**: el monto a recibir/pagar por la factura.
* **Numerado**: si la Cantidad pagada es menor que el monto de la factura, solo el monto pagado será asignado contra la/s factura/s de la Entrada de pago. El pago puede realizarse en partes, por ejemplo, si hubiera tres facturas con importes de 20, 20 y 20, entonces la cantidad pagada es 60 por lo que este valor será repartido en partes iguales. Los [Términos de pago](/docs/user/manual/es/accounts/payment-terms) también pueden estar involucrados en la obtención del importe asignado.

 ![Outstanding Invoice]({{docs_base_url}}/assets/img/accounts/outstanding-pe.png)

#### Monto sin asignar
Cuando se crea una Entrada de pago en ERPNext y la Cantidad pagada es mayor al monto total de las facturas, el excedente se almacena en la cuenta del Cliente/Proveedor. Por lo tanto este importe está actualmente "sin asignar" y puede ser usado luego contra facturas futuras.

Por ejemplo, si se crea una Factura de venta por $1.000 y el Cliente paga $1.500. Al hacer otra factura para este cliente se podrán usar los $500 sobrantes del pago anterior.

### 3.5 Deducciones o pérdidas

Cuando se crea una Entrada de pago contra una factura, puede llegar a haber alguna diferencia entre la Cantidad pagada y el monto pendiente de la factura. Esto puede deberse a errores en el redondeo o variaciones en el Cambio de Divisas. Se puede definir aquí una cuenta donde se almacenará esta diferencia.

![Outstanding Invoice]({{docs_base_url}}/assets/img/accounts/pe-get-outstanding.gif)

La pérdida/deducción puede ser cancelada:

![Payment Deductions]({{docs_base_url}}/assets/img/accounts/payment-deductions.png)

En el siguiente ejemplo la cantidad pagada es $25 pero el monto asignado es $30 ya que $30 es el importe de la factura. La "Diferencia de Monto" será de $5 en este caso. Esta diferencia puede darse debido a descuentos o Cambio de Divisas. La Diferencia de Monto debe ser 0 para poder validar la Entrada de pago. Esto puede ajustarse usando el botón **Crear una entrada con una diferencia**. El monto será asignado a la cuenta de cancelación.

<img class="screenshot" alt="Making Payment" src="{{docs_base_url}}/assets/img/accounts/payment-entry-5.gif">

### 3.6 Cancelación

La cancelación ocurre cuando el monto pagado es menor al importe asignado. Por ejemplo, el excedente es considerado una pérdida en diversos cargos o cuando ese monto no va a ser pagado.

![Payment Write Off]({{docs_base_url}}/assets/img/accounts/payment-write-off-1.png)

En esta tabla, las deducciones o pérdidas de los pagos pueden ser ajustadas como se explica en el ejemplo anterior.

![Payment Write Off]({{docs_base_url}}/assets/img/accounts/payment-write-off.png)

### 3.7 Luego de validar
Al validar la Entrada de pago, el monto pendiente será actualizado en las facturas.

<img class="screenshot" alt="Making Payment" src="{{docs_base_url}}/assets/img/accounts/payment-entry-8.png">

Si la Entrada de pago fue creada contra una Orden de venta o de compra, el campo "Pago adelantado" será actualizado. Al crear una factura contra esas transacciones, la Entrada de pago será actualizada automáticamente en esa factura por lo que se puede asignar el monto de la misma contra la Entrada de pago.

Para pagos recibidos, la contabilización se realizará de la siguiente forma:

 * Debe: cuenta bancaria o de efectivo
 * Haber: Cliente (deudor)

Para pagos efectuados:

 * Debe: proveedor (acreedor)
 * Haber: cuenta bancaria o de efectivo

## 4. Otros casos

### 4.1 Entrada de pago con múltiples divisas

Si se desea tener una cuenta de cobro/pago en una moneda extranjera, es necesario crear una cuenta por cada divisa (distinta de la de la compañía) y seleccionarla en la cuenta de la entidad. Por ejemplo:

![Foreign Account in Customer]({{docs_base_url}}/assets/img/accounts/cust-foreign-acc.png)

ERPNext permite facturar y llevar la contabilidad de la empresa en [múltiples divisas](/docs/user/manual/en/accounts/multi-currency-accounting). Si se realiza una factura en la moneda de la entidad, se debe definir un Cambio de Divisas entre esta moneda y la de la compañía.

> Nota: se debe crear y seleccionar en la Factura/Orden de venta una cuenta de deudor/acreedor distinta para que el cambio de divisas funcione correctamente. Por ejemplo, si el Cliente es de Estados Unidos, se creará una cuenta A cobrar llamada "Deudores EU".

Al crear la Entrada de pago contra esa factura, el cambio de divisas correspondiente será traído, pero es posible seleccionar un cambio de divisas al momento de realizar el pago.

Haciendo click en el botón **Ajustar ganancia/pérdida de cambio** se agregará automáticamente una fila para cancelar el monto de la diferencia.

<img class="screenshot" alt="Making Payment" src="{{docs_base_url}}/assets/img/accounts/payment-entry-6.png">

Dado que el cambio de divisas fluctúa a lo largo del tiempo, puede que se produzca una diferencia en el monto del pago respecto al importe de la factura. Esta diferencia puede ser registrada como importe de Ganancia/pérdida de cambio de divisas.

<img class="screenshot" alt="Making Payment" src="{{docs_base_url}}/assets/img/accounts/payment-entry-7.png">

Los pagos también pueden generarse independientemente de las facturas creando una nueva Entrada de pago.

Para saber más sobre la gestión de transacciones en distintas divisas visitar esta [página](/docs/user/manual/en/accounts/articles/managing-transactions-in-multiple-currency).

### 4.2 Transferencia interna

Las transferencias internas se utilizan en casos en los que el dinero es tranferido entre cuentas de la misma compañía. Por ejemplo, si un cliente de Estados Unidos usa PayPal, transferir dinero desde PayPal a una cuenta bancaria puede ser considerada una transferencia interna.

Se puede realizar mediante Entrada de pago las siguientes transferencias internas:

1. Banco - Efectivo
4. Banco - Banco
3. Efectivo - Efectivo
2. Efectivo - Banco

<img class="screenshot" alt="Making Payment" src="{{docs_base_url}}/assets/img/accounts/payment-entry-9.png">

### 4.3 Gestión de diferentes escenarios de pago

Teniendo una factura impaga cuyo monto pendiente es igual al total neto, al crear la Entradas de pago, el valor pendiente reducirá.

En la mayoría de los casos, excepto para ventas minoristas, la facturación y la generación de pagos son actividades separadas. Existen muchas combinaciones en las cuales se realizan estos pagos. Estos casos aplican tanto para ventas como para compras.

 * Pueden hacerse 100% por adelantado.
 * En el momento de la entrega o a los pocos días de la misma.
 * Una parte por adelantado y otra parte en o después de la entrega.
 * Se puede hacer un solo pago que incluye varias facturas.
 * Los anticipos se pueden realizar para varias de facturas (y se pueden dividir luego entre las facturas).

ERPNext permite manejar todos estos escenarios. Todas las entradas contables (entrada de Balance general) pueden realizarse contra Facturas de venta, Facturas de compra o Entradas de pago como pago adelantado.

El monto total pendiente contra una factura es la suma de todas las entradas contables hechas contra (o vinculadas a) esa factura. De esta forma se puede combinar o dividir los pagos para manejar los diferentes escenarios.

### 4.4 Diferencia entre Entrada de pago y Asiento contable

1. Usar un Asiento contable requiere conocer las cuentas específicas sobre las cuales se debitará o acreditará el monto correspondiente. En una Entrada de pago, esto lo realiza el sistema, resultando más simple para el usuario.
1. La Entrada de pago es más eficiente en la gestión de pagos en monedas extranjeras.
1. Es posible imprimir Cheques desde Entradas de pago usando dicho formato de impresión.
1. Por su parte, los Asientos contables son usados para:
 - Realizar la apertura de cuentas.
 - Hacer entradas de depreciación de activos fijos.
 - Para ajustar Notas de crédito contra Facturas de ventas y Notas de débito contra Facturas de compras, en el caso de que no se haya realizado el pago.

### 4.5 Pagos por medio de Asientos contables

Para hacer un pago utilizando un Asiento contable se debe seguir los siguientes pasos:

1. Activar la funcionalidad en **Contabilidad > Configuración > Configuración de cuentas** tildando la opción "Realizar pago mediante asiento contable".

2. Realizar el pago. Al validar un documento contra los cuales se puede generar Asientos contables, aparecerá la opción Pago debajo del botón **Crear**.

 <img class="screenshot" alt="Making Payment" src="{{docs_base_url}}/assets/img/accounts/payment-entry-1.png">

3. Esto llevará al Asiento contable. Guardar y validarlo hará que se registre el pago contra la factura correspondiente.
 <img class="screenshot" alt="Making Payment" src="{{docs_base_url}}/assets/img/accounts/journal-entry.png">


## 5. Temas relacionados
1. [Solicitud de pago](/docs/user/manual/es/accounts/payment-request)
1. [Términos de pago](/docs/user/manual/es/accounts/payment-terms)
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Factura de compra](/docs/user/manual/es/accounts/purchase-invoice)
