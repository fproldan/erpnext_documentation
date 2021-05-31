<!-- add-breadcrumbs -->
# Factura de venta

**Una Factura de venta es un documento que se envía a los Clientes contra el cual se realizará el pago.**

Las Facturas de venta son transacciones contables. Al validarlas, el sistema actualiza las cuentas a cobrar y registra el ingreso contra la cuenta del cliente.

Para ingresar al listado de Facturas de venta, ir a:
> Inicio > Contabilidad > Factura de venta

![SO Flow](/docs/assets/img/accounts/so-flow.png)

## 1. Prerrequisitos
Antes de crear y usar facturas de venta, se recomienda crear lo siguiente:

* [Producto](/docs/user/manual/es/stock/item)
* [Cliente](/docs/user/manual/es/CRM/customer)
* [Punto de venta](/docs/user/manual/es/accounts/punto-de-venta)

Opcional:
 * [Orden de venta](/docs/user/manual/es/selling/sales-order)
 * [Nota de entrega](/docs/user/manual/es/stock/delivery-note)

También se debe ingresar el CBU y Alias CBU de la empresa en la Compañía si se encuadra dentro del régimen MiPyME. Para ciertas transacciones, AFIP solicita esta información, y si la misma no se encuentra el sistema arrojará un mensaje advirtiéndolo.

## 2. Creación de facturas de venta
Una Factura de venta es generalmente creada desde Ordenes de venta o Notas de entrega. Los detalles del producto serán traídos de forma automática a la factura. Sin embargo, también se puede crear facturas de venta directamente.

Para traer los detalles de otros documentos a la factura, hacer click en **Obtener artículos de**. Los detalles pueden ser traídos de Ordenes de venta, Notas de entrega o Cotizaciones.

Para la creación manual, se debe seguir los siguientes pasos:

1. Ir al listado de Facturas de venta y hacer click en Nuevo.
1. Seleccionar Punto de venta, Cliente, Secuencia y Concepto incluído.
1. Definir la Fecha de pago.
2. Seleccionar la Opción de transmisión (especialmente importante bajo el régimen MiPyME).
3. En la tabla de Producto, añadir los que correspondan y especificar las cantidades.
4. Los precios serán traídos automáticamente si exite el correspondiente [Precio de Producto](/docs/user/manual/es/stock/item-price), sino se debe agregar en la tabla.
5. La fecha y hora de contabilización serán completadas por defecto con los datos actuales, aunque se pueden editar luego de tildar la opción "Editar fecha y hora de envío".
6. Guardar y validar.
 ![SI](/docs/assets/img/accounts/sales-invoice-1.png)

### 2.1 Opciones adicionales

* **Es una Nota de Crédito**: tildar esta opción si el cliente devolvió los productos. Para más detalles, visitar la página de [Nota de crédito](/docs/user/manual/es/accounts/credit-note).

<img class="screenshot" alt="Sales Invoice" src="{{docs_base_url}}/assets/img/accounts/sales-invoice.png">

### 2.2 Estados

Estos son los estados que se asignan automáticamente a las facturas de venta:

* **Borrador**: la factura fue guardada pero no validada.
* **Validado**: la factura está validada en el sistema y el Balance general fue actualizado.
* **Pagado**: el Cliente realizó el pago y la [Entrada de pago](/docs/user/manual/es/accounts/payment-entry) fue validada.
* **Impagado**: la factura fue generada pero el pago está pendiente.
* **Atrasado**: el pago está pendiente pasada la fecha de vencimiento.
* **Cancelado**: la factura fue cancelada. Al cancelarla, se deshace el impacto que haya tenido en las cuentas y el inventario.
* **Nota de Crédito emitida**: el producto fue devuelto por el Cliente y se crea una [Nota de crédito](/docs/user/manual/es/accounts/credit-note) contra esta factura.
* **Retornar**: es asignado a una Nota de crédito creada contra la factura original. Aunque también se pueden crear Notas de crédito independientes.
* **Impaga y descontada**: el pago está pendiente y cualquier suscripción en curso fue descontada usando un [Descuento de facturas](/docs/user/manual/es/accounts/invoice_discounting).
* **Atrasada y descontada**: el pago está pendiente pasada la fecha de vencimiento y cualquier suscripción en curso fue descontada usando un [Descuento de facturas](/docs/user/manual/es/accounts/invoice_discounting).

## 3. Características

### 3.1 Aspectos Fiscales

* **Punto de Venta**: debe crearse previamente, cargando los datos de AFIP, según corresponda. Para más información, hacer click [aquí](/docs/user/manual/es/accounts/punto-de-venta).

* **Secuencia**: dependiendo del Punto de venta y del Cliente seleccionados se desplegarán posibles opciones de secuencia conforme los diferentes documentos que se puedan emitir. Las opciones dependerán de aspectos impositivos (particularmente, la Condicion de IVA) de la Compañía y del Cliente.

* **Concepto incluído**: debe seleccionarse alguno de los conceptos incluídos en el desplegable. En el caso de que se trate de "Servicios", deberá colocarse la fecha de prestación de los mismos. Es solicitado por AFIP para la validación de la factura.

* **Opción de transmisión**: debe seleccionarse alguna de las opciones de transmisión que aparecen en el desplegable, de acuerdo a la información que el contador le brinde. La opción de transmisión es obligatoria para clientes MiPyME, según normativa de AFIP.

* **Posición fiscal**: Debe completarse sólo cuando se trate de alguna de las operaciones comprendidas en el desplegable (No alcanzado, Operaciones de canje, No gravado, Operaciones exentas, Operaciones al exterior, Operaciones a zona franca).

* **Comprobante asociado**: Si se trata de una Nota de Crédito/Débito debe completar el comprobante asociado con la factura sobre la cual impacta la transacción. Además, en caso de una Nota de crédito, debe tildar el checkbox Es una Nota de Crédito.

### 3.2 Fechas

* **Fecha de contabilización**: fecha en la cual la factura de venta afectará la contabilidad de la organización, por ejemplo, en el Balance general. Esto afectará todos los balances en ese período contable.

* **Fecha de pago**: fecha de vencimiento del pago (si se vendió con un método de pago que admite crédito).
El límite de crédito puede establecerse desde el [Cliente](/docs/user/manual/en/CRM/customer#24-credit-limit-and-payment-terms) mismo.

### 3.3 Exportación
* **Inconterms**: Deberá completarse sólo en el caso de que se trate de una factura de exportación de bienes.

### 3.4 Dimensiones contables
Las dimensiones contables permiten diferenciar las transacciones basándose en un aspecto específico, como territorio, sucursal, cliente, etc. Esto ayuda a visualizar estados financieros por separado en base a la dimensión seleccionada. Para saber más, visitar la sección [Dimensiones contables](/docs/user/manual/es/accounts/accounting-dimensions).

> Nota: Proyecto y Centro de costos son tratados como dimensiones por defecto.

### 3.5 Detalles de la Orden de compra del cliente

* **Ordenes de compra de clientes**: rastrear el número de la orden de compra del cliente, principalmente para prevenir la creación de ordenes o facturas de venta duplicadas para la misma orden. Se pueden configurar más aspectos relacionados con la validación de las ordenes de compra del cliente en [Configuración de Ventas](/docs/user/manual/es/selling/selling-settings#44-allow-multiple-sales-orders-against-a-customers-purchase-order)
* **Fecha de pedido de compra del cliente**: la fecha en la que el cliente generó la orden de compra.

 ![Customer Address](/docs/assets/img/accounts/si-customer.png)

### 3.6 Dirección y contacto

* **Dirección del cliente:** dirección de facturación del cliente.
* **Persona de contacto**: si el cliente es una compañía, la persona que se contactará es traída a este campo si está definida en el [Cliente](/docs/user/manual/es/CRM/customer).
* **Territorio:** el [Territorio](/docs/user/manual/es/selling/territory) es la región a la cual pertenece el Cliente. El valor por defecto es "Todos los territorios".
* **Dirección:** dirección a la cual se enviarán los productos.


### 3.7 Divisa
Se puede elegir la divisa en la cual se debe enviar la factura. Este dato puede ser tomado del Cliente o de transacciones anteriores como Ordenes de venta.

* Si bien se puede usar la divisa especificada en el Cliente para la factura, el registro contable se hará solo en la moneda de la compañía. Para saber más visitar el siguiente [artículo](/docs/user/manual/en/accounts/articles/managing-transactions-in-multiple-currency).
* Mantener cuentas a cobrar separadas en la divisa del cliente. El cobro de la factura deberá ser registrado en esa misma moneda. Hacer click [aquí](/docs/user/manual/es/accounts/multi-currency-accounting) para aprender más sobre Contabilidad con múltiples divisas.

### 3.8 Lista de precios

Si se seleccionó una lista de precios, entonces el precio del producto será obtenido de dicha lista. Al tildar la opción "Ignorar la Regla Precios" ya no se tendrán en cuenta las [Reglas de precios](/docs/user/manual/es/accounts/pricing-rule) establecidas en Contabilidad > Reglas de precios.

Para saber más sobre listas de precios, hacer click [aquí](/docs/user/manual/es/stock/price-lists).


### 3.9 Tabla de productos

#### Actualización de inventario
Tildando esta opción se actualizará el Mayor de Inventarios al validar la Factura de venta. Si se creó una Nota de entrega, el Mayor de Inventarios cambiará de igual forma. Este tilde en la factura permite saltearse la creación de la Nota de entrega en el caso de no ser necesaria.

* **Escanear código de barras**: se pueden agregar productos a la tabla escaneando su código si se tiene el escáner. Para más información el respecto visitar el siguiente [artículo](/docs/user/manual/en/stock/articles/track-items-using-barcode)

* El código del producto, nombre, descripción, imagen y fabricante serán traídos del [Producto](/docs/user/manual/en/stock/item) mismo.

* **Descuento y margen**: se puede aplicar un descuento por producto en forma de porcentaje o de monto fijo. Leer [Aplicación de descuentos](/docs/user/manual/en/selling/articles/applying-discount) para más detalles.

* **Precio**: el precio es traído automáticamente si se lo definió para la [Lista de precio](/docs/user/manual/en/stock/price-lists) y se calcula el Importe total.

* **Envío triangulado**: el envío triangulado se realiza cuando se creó la transacción de venta, pero el producto es entregado por el proveedor. Para saber más, visitar la página [Envío triangulado](/docs/user/manual/es/selling/articles/drop-shipping).

* **Detalles de contabilidad**: las cuentas de ingreso y de costo en esta sección pueden ser cambiadas si se desea. Si el producto es un [Activo](/docs/user/manual/es/asset/asset), también puede ser seleccionado aquí. Esto es útil cuando se está realizando la [venta de activos](/docs/user/manual/es/asset/selling-an-asset).

* **Ingresos diferidos**: si el ingreso para el producto será facturado en los meses próximos de forma parcial, se debe tildar la opción "Habilitar ingresos diferidos". Para saber más, visitar la página [Ingresos diferidos](/docs/user/manual/es/accounts/deferred-revenue).

* **Detalles del peso del producto**: el peso del producto por unidad y la unidad de medida son traídos a la factura si se lo definió en el producto.

* **Detalles de almacén**: los siguientes detalles serán traídos del producto:
    * **Almacén**: almacén del cual se obtendrán los productos.
    * **Cantidad disponible en almacén**: cantidad disponible en el almacén seleccionado.

* **Lote Nro. y Número de serie**: si el producto forma parte de un lote o serie, se deberá ingresar el [Número de serie](/docs/user/manual/es/stock/serial-no) y [Lote](/docs/user/manual/es/stock/batch) en la tabla de productos. Se pueden ingresar distintos números de serie en una fila (uno por línea) y la cantidad de números debe ser igual a la cantidad.

* **Plantilla de impuestos**: se puede definir una plantilla de impuestos para aplicar un determinado impuesto al producto. Para saber más visitar esta [página](/docs/user/manual/es/accounts/item-tax-template).

* Referencias: si la factura de venta fue creada desde una Orden de venta/Nota de entrega, dicho documento será referenciado aquí. Además, se mostrará la Cantidad entregada.

* **Salto de página** creará un salto de página justo antes de este producto en la impresión.

### 3.10 Hoja de tiempo

Si se desea facturar las horas trabajadas por los empleados (según contrato), se pueden completar Registros de hora. Al hacer una nueva Factura de venta, se debe seleccionar el proyecto para el cual se realizará la facturación, y el Registro de hora correspondientes al proyecto serán traídas automáticamente.

Si los empleados de la compañía están trabajando en una determinada ubicación y se necesita hacer la facturación correspondiente, se puede crear una factura basada en el registro de horas.

![SI Timesheet](/docs/assets/img/accounts/si-timesheet.png)

Para saber más, visitar la [página](/docs/user/manual/es/projects/sales-invoice-from-timesheet).

### 3.11 Impuestos y cargos
Los Impuestos y cargos son traídos desde la [Orden de venta](/docs/user/manual/es/selling/sales-order) o de la [Nota de entrega](/docs/user/manual/es/stock/delivery-note).

Visitar la página [Plantilla de Impuestos y Gastos](/docs/user/manual/es/selling/sales-taxes-and-charges-template) para saber más sobre impuestos.

El Total Impuestos y Cargos se muestra en la sección debajo de la tabla.

Para agregar impuestos de forma automática mediante Categoría de impuesto visitar esta [página](/docs/user/manual/es/accounts/tax-category).

Es importante seleccionar todos los impuestos de forma correcta para una facturación precisa.

![SI Tax](/docs/assets/img/accounts/si-tax.png)

#### Regla de envío
Una Regla de envío ayuda a calcular el costo del envío de un producto. Este incrementará con la distancia del envío. Para saber más, visitar la página [Regla de envío](/docs/user/manual/en/selling/shipping-rule).

### 3.12 Redención de puntos de lealtad

Si el cliente forma parte de algún programa de lealtad, se puede elegir canjear los puntos obtenidos. Para saber más, visitar la página [Programa de lealtad](/docs/user/manual/es/accounts/loyalty-program).

### 3.13 Descuento adicional
Cualquier descuento adicional aplicado al total de la factura puede ser especificado en esta sección. El descuento puede calcularse en base al Total (después de sumarle los impuestos y cargos) o sobre el Total Neto. El descuento adicional puede definirse en porcentaje o ser un monto fijo.
Visitar la página [Aplicar un descuento](/docs/user/manual/es/selling/articles/applying-discount) para más detalles.

![SI Add Discount](/docs/assets/img/accounts/si-add-discount.png)

### 3.14 Pago adelantado
Para productos de costo elevado, el vendedor puede solicitar un pago adelantado antes de procesar la orden. El botón **Obtener anticipos recibidos** permite traer a la factura los pagos adelantados. Para saber más, visitar la página [Pagos adelantados](/docs/user/manual/es/accounts/advance-payment-entry).

### 3.15 Términos de pago
El pago de una factura puede realizarse en partes dependiendo de lo acordado con el proveedor. Esto es traído desde la Orden de venta si se lo definió ahí. Para saber más, visitar la página [Términos de pago](/docs/user/manual/es/accounts/payment-terms).

### 3.16 Desajuste
El desajuste ocurre cuando el Cliente paga un importe menor al total de la factura. Puede ser una diferencia mínima de $0,50. Si ocurre en muchas ordenes, puede sumar una cifra mucho mayor. Para precisión contable esta diferencia es "anulada". Para saber más, visitar la página [Entrada de pago](/docs/user/manual/es/accounts/payment-entry#25-deductions-or-loss).

### 3.17 Términos y condiciones
Puede haber ciertos términos y condiciones respecto al producto que se está vendiendo, los cuales pueden ser definidos en esta sección. Para saber más sobre agregar Términos y condiciones hacer click [aquí](/docs/user/manual/es/setting-up/print/terms-and-conditions).

### 3.18 Información del transporte

Si se subcontrata el transporte de los productos, los detalles de la entidad encargada de esto pueden agregarse en esta sección. Esto no es lo mismo que [envío triangulado](/docs/user/manual/es/selling/articles/drop-shipping).

* **Transporte**: el proveedor que llevará el producto al cliente. Debería estar tildada la opción "Es transportista" en el [Proveedor](/docs/user/manual/en/buying/supplier) para poder seleccionarlo aquí.
* **Conductor**: se puede especificar quién conducirá el medio de tranporte.

Los detalles son generalmente traídos desde la Nota de entrega.

 ![Delivery Note Transport](/docs/assets/img/accounts/si-transporter.png)

Se pueden registrar los siguientes detalles:

* Distancia en km
* Medio de transporte ya sea ruta, aire, ferrocarril o barco.

### 3.19 Ajustes de impresión

#### Membrete
Se puede imprimir la factura utilizando el membrete de la compañía. Más información [aquí](/docs/user/manual/es/setting-up/print/letter-head).

'Agrupar mismos artículos' agrupará los productos que aparecen en más de una fila de la tabla. Esto se verá solo en la impresión.

#### Imprimir Encabezado
El encabezado de las facturas también puede ser seleccionado al imprimir el documento. Para esto se debe seleccionar el **Encabezado** deseado. Para crear un nuevo Encabezado ir a: Inicio > Configuración > Impresión > Encabezado. Más información [aquí](/docs/user/manual/es/setting-up/print/print-headings).

Existen ajustes adicionales para la impresión de Facturas de venta sin el importe, esto puede ser útil para productos con precio elevado.

### 3.20 Más información
Se pueden registrar los siguientes detalles de ventas:

* **Campaña**: si esta factura es parte de una campaña de venta en curso, la misma puede ser vinculda aquí. Para saber más, visitar la página [Campaña](/docs/user/manual/es/CRM/campaign).
* **Referencia**: un tipo de referencia puede ser seleccionado en este campo para conocer el origen de la venta. Para saber más, visitar la página [Referencia](/docs/user/manual/es/CRM/lead_source).

 ![SI More info](/docs/assets/img/accounts/si-more-info.png)

### 3.21 Detalles de contabilidad

* **Debitar a**: cuenta contra la cual se registrará lo cobrado al Cliente.
* **Es una entrada de apertura**: si esta es una entrada de apertura seleccionar "Sí". Ej: si se está migrando desde otro sistema a ERPNext, se necesitará usar un Asiento de apertura para actualizar los balances en ERPNext.
* **Observaciones**: cualquier observación adicional sobre Facturas de ventas pueden agregarse acá.

 ![SI Accounting Details](/docs/assets/img/accounts/si-acc-details.png)

### 3.22 Comisión

Si la venta fue realizada por uno de los Socios de ventas de la empresa, se puede agregar un detalle sobre su comisión. Generalmente esto se trae desde la Orden de venta o la Nota de entrega.

### 3.23 Equipo de ventas

**Vendedor:** ERPNext permite asignar los distintos vendedores que hayan estado involucrados en la venta. Esto también es traído desde la Orden de venta o la Nota de entrega.

### 3.24 Obtención automática de números de lote de artículos

Si se está vendiendo un producto desde un [Lote](/docs/user/manual/es/stock/batch),
ERPNext traerá automáticamente el número de lote si está tildada la opción "Actualizar el Inventario". El número de lote será traído usando la regla Primero en expirar primero en salir (FEFO). Esta es una variante de FIFO (primero en entrar primero en salir) que da la mayor prioridad al que está más cerca de expirar.

Se debe tener en cuenta que si el primer lote en la fila no es suficiente para hacer el pedido, se seleccionará el siguiente lote con los productos necesarios. Si ningún lote posee la cantidad necesaria, ERPNext no seleccionará ningún lote de forma automática.

### 3.25 Luego de validar

Al validar la factura, se pueden crear los siguentes documentos contra la misma:

1. [Asiento contable](/docs/user/manual/es/accounts/journal-entry)
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Solicitud de pago](/docs/user/manual/es/accounts/payment-request)
1. [Descuento de facturas](/docs/user/manual/es/accounts/invoice_discounting)
1. [Nota de entrega](/docs/user/manual/es/stock/delivery-note)

![SI Submit](/docs/assets/img/accounts/si-submit.png)

### 3.26 Datos AFIP
De acuerdo a la normativa vigente en Argentina, al emitir la factura, se generará un código QR que se encontrará en esta sección. Para mayor información hacer click aquí.

## 4. Más
### Impacto contable

Todas las ventas se registran contra una "Cuenta de ingreso", es decir, una cuenta de la sección INGRESOS del Plan de cuentas. Es una buena práctica clasificar los ingresos por tipo (producto, servicio, etc). Esta cuenta debe definirse para cada fila de la tabla de productos.

> Tip: para definir una cuenta de ingreso por defecto para productos, se puede definir en el producto o en el Grupo de Productos.

La otra cuenta que se ve afectada es la del Cliente, la cual es automáticamente asignada como "Debitar a".

También se puede mencionar el Centro de costos en el cual el ingreso debe ser registrado.
Se debe recordar que los Centros de costo indican la rentabilidad de las diferentes líneas de negocio o producto. También se puede definir un Centro de costos predeterminado en el producto. Ver también: [Dimensiones contables](/docs/user/manual/es/accounts/accounting-dimensions).

### Entradas contables (Balance general) de una venta:
Al registrar una venta (aumento):

* **Debe:**
  * Cliente (total general)
* **Haber:**
  * Ingreso (total neto menos los impuestos de cada producto)
  * Impuestos (pasivos a pagar al gobierno)

 ![SI Ledger](/docs/assets/img/accounts/si-ledger.png)

> Para ver las entradas de la factura luego de validar, hacer click en "Ver - Libro de contabilidad".

## 5. Temas relacionados
1. [Centro de costos](/docs/user/manual/es/accounts/cost-center)
1. [Asiento contable](/docs/user/manual/es/accounts/journal-entry)
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Factura de compra](/docs/user/manual/es/accounts/purchase-invoice)
1. [Recibo de compra](/docs/user/manual/es/stock/purchase-receipt)
1. [Impuestos del producto](/docs/user/manual/es/accounts/item-tax-template)
1. [Orden de venta](/docs/user/manual/es/selling/sales-order)
1. [Cotización](/docs/user/manual/es/selling/quotation)
1. [Nota de entrega](/docs/user/manual/es/stock/delivery-note)
