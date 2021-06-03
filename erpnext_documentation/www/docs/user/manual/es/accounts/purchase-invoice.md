<!-- add-breadcrumbs -->
# Factura de compra

**Una Factura de compra es un recibo que envía el Proveedor contra el cual se debe hacer el pago.**

La factura de compra es exactamente lo opuesto a la factura de venta. Aquí se contabilizan los gastos de proveedores. Hacer una factura de venta es muy similar a hacer una Orden de compra.

Para acceder a la lista de Facturas de compra, ir a:
> Inicio > Contabilidad > Facturación > Factura de Compra

![PI Flow](/docs/assets/img/accounts/pi-flow.png)

## 1. Prerrequisitos
Antes de crear y usar una Factura de compra, se debe crear lo siguiente:

* [Producto](/docs/user/manual/es/stock/item)
* [Proveedor](/docs/user/manual/es/buying/supplier)
* [Orden de compra](/docs/user/manual/es/buying/purchase-order)
* [Recibo de compra](/docs/user/manual/es/stock/purchase-receipt) (opcional)


## 2. Creación de una factura de compra
La Factura de compra se crea por lo general desde una Orden de compra o de un Recibo de compra. Los detalles del producto del proveedor serán traídos automáticamente. Sin embargo, también se pueden crear directamente desde cero.

Para traer detalles en la factura, se debe hacer click en el botón **Obtener artículos de**. Esta información puede ser obtenida de una Orden o de un Recibo de compra.

Para la creación manual, se deben seguir los siguientes pasos:

1. Ir al listado de Facturas de compra, hacer click en Nuevo.
1. Seleccionar el proveedor.
1. La fecha de contabilización por defecto será la del momento de creación, pero esto se puede modificar luego tildando la opción "Editar fecha y hora de envío".
1. Definir la fecha de vencimiento para el pago.
1. Agregar productos y cantidades en la tabla de productos.
1. El Precio y el Importe serán traídos automáticamente.
1. Guardar y validar.

 <img class="screenshot" alt="Purchase Invoice" src="{{docs_base_url}}/assets/img/accounts/purchase-invoice.png">

### 2.1 Opciones adicionales en la creación de Facturas de compra

* **Está pagado**: se puede tildar "Está pagado" si ya se realizó el pago mediante un [Pago adelantado](/docs/user/manual/es/accounts/advance-payment-entry). Esto debería hacerse ya sea un pago adelantado completo o parcial.
* **Es Retorno (Nota de Débito)**: tildar esta opción si el Cliente devolvió los productos. Para saber más detalles, visitar la página [Nota de débito](/docs/user/manual/es/accounts/debit-note).
* **Aplicar Monto de retención de impuestos**: si el Proveedor seleccionado tiene definida una categoría de retención de impuestos, esta opción aparecerá habilitada. Para más información, visitar la página [Categoría de retención de impuestos](/docs/user/manual/es/accounts/tax-withholding-category).

### 2.2 Estados

* **Borrador**: un borrador está guardado pero no validado en el sistema.
* **Retornar**: los productos fueron devueltos al Proveedor.
* **Nota de Débito Emitida**: los productos fueron devueltos y se creó una [Nota de Débito](/docs/user/manual/es/accounts/debit-note) contra la factura.
* **Validado**: la factura de compra fue validada en el sistema y el Balance general fue actualizado.
* **Pagado**: el importe de la factura fue pagado al Proveedor y se validó la [Entrada de pago](/docs/user/manual/es/accounts/payment-entry) correspondiente.
* **Imagado**: todavía no se realizó el pago de la factura.
* **Atrasado**: se superó la fecha de vencimiento del pago.
* **Cancelado**: la factura fue cancelada.


## 3. Características

### 3.1 Dimensiones contables
Las dimensiones contables permiten clasificar transacciones basándose en un determinado territorio, sucursal, cliente, etc. Esto ayuda a visualizar los estados contables por separado dependiendo de los criterios seleccionados. Para saber más, visitar la página [Dimensiones contables](/docs/user/manual/es/accounts/accounting-dimensions).

> Nota: Proyecto y Centro de costos son tratados como dimensiones por defecto.

### 3.2 Retener la Factura

A veces se necesita retener la factura para que no sea validada hasta determinada fecha.

**Retener la Factura**: tildar esta opción para poner la factura en espera. Esto solo puede realizarse antes de validar la factura. Una vez que "Retener la Factura" es seleccionado y la factura validada, el estado cambiará a "Temporalmente en Espera".

![PI Hold](/docs/assets/img/accounts/pi-hold.png)

Si la factura está validad y se quiere cambiar la "Fecha de Lanzamiento" se puede utilizar el botón "Cambiar Fecha de Lanzamiento" ubicado en el desplegable "Retener la factura".

Si se quiere retener facturas ya validadas, se debe usar el botón "Bloquear factura" y si se desea desbloquear hacer click en "Desbloquear factura".

![Block PI](/docs/assets/img/accounts/pi_block.png)

Esta tipo de bloqueo es a nivel de factura; se puede también aplicar una retención al Proveedor. Para aprender más hacer click [aquí](/docs/user/manual/es/buying/supplier#23-credit-limit).

### 3.3 Detalles de la factura del proveedor

* **Factura de proveedor No.**: el Proveedor puede tener un código propio para identificar cada factura, esto solo sirve como referencia.
* **Fecha de factura de proveedor**: fecha en la cual el Proveedor generó o confirmó la orden.

### 3.4 Dirección y contacto

* **Dirección del proveedor:** esta es la dirección de facturación del Proveedor.
* **Persona de contacto**: si el Proveedor es una Compañía, la persona con la cual se realizará la comunicación es definida en este campo si se la seleccionó también en el [Proveedor](/docs/user/manual/es/buying/supplier).
* **Dirección de envío:** dirección a la cual se enviarán los productos.

### 3.5 Divisa y listas de precios
Se puede definir la divisa en la cual se debe enviar la Factura de compra. Esto es traído de la Orden de compra. Si se elige una Lista de precio, entonces el precio del producto será traído de esa lista. Tildando "Ignorar la Regla Precios" se ignorará la [Regla de precios](/docs/user/manual/es/accounts/pricing-rule) existente en Cuentas > Regla de precios.

![PI Price List](/docs/assets/img/accounts/pi-price-list.png)

Para saber sobre Listas de precios, hacer click [aquí](/docs/user/manual/es/stock/price-lists).

Para saber sobre gestión de transacciones en distintas divisas, hacer click [aquí](/docs/user/manual/es/accounts/articles/managing-transactions-in-multiple-currency).

### 3.6 Materias primas suministradas

Esta opción es útil para subcontrataciones en las que se provee la materia prima para la fabricación del producto. Para saber más, visitar la página [Subcontratación](/docs/user/manual/en/manufacturing/subcontracting).

### 3.7 Productos

* **Escanear código de barras**: se puede agregar productos a la tabla escaneando sus códigos de barra. Para saber cómo hacer esto visitar la siguiente [página](/docs/user/manual/es/stock/articles/track-items-using-barcode)

* El código del producto, nombre, descripción, imagen y fabricante serán traídos desde el [Producto](/docs/user/manual/es/stock/item) mismo.

* **Fabricante**: si el producto posee un fabricante específico, esto puede ser definido aquí. Este dato será traído si se especificó en el Producto.

* **Cantidad y precio**: al seleccionar el código del producto, su nombre, descripción y UoM serán traídas automáticamente. El "Factor de Conversión de Unidad de Medida" es 1 por defecto; pero se puede cambiar dependiendo de la UoM recibida del vendedor.

La "Tarifa de la lista de precios" será traída si se especificó un precio para la compra. El "Precio de la última compra" muestra el precio del producto de la última Orden de compra. Se puede adjuntar una Plantilla de impuestos para aplicar un impuesto específico al producto.

* **Peso del producto** será traído si se definió en el Producto, sino se puede ingresar manualmente.

* **Descuento sobre la tarifa de la lista de precios**: se puede aplicar un porcentaje de descuento para cada producto o en el importe total del producto. Leer [Aplicar un Descuento](/docs/user/manual/es/selling/articles/applying-discount) para más detalles al respecto.

* **Detalles del peso del artículo**: los detalles del peso por unidad y por UoM son traídos si se los definió en el producto, sino se puede ingresar manualmente.

* **Contabilidad**: la Cuenta de gastos puede ser cambiada aquí.

* **Gastos diferidos**: si el gasto por el producto será facturado de forma parcial en los meses próximos, entonces tildar la opción "Habilitar gastos diferidos". Para saber más, visitar la página [Gastos diferidos](/docs/user/manual/es/accounts/deferred-expense).

* **Permitir tasa de valoración cero**: tildar la opción "Permitir tasa de valoración cero" permitirá validar el Recibo de compra incluso si la tasa de valoración del producto es 0. Puede ser el caso de un producto de muestra o de un mutuo acuerdo con el Proveedor.

* **BOM**: si hay una [Lista de materiales](/docs/user/manual/en/manufacturing/bill-of-materials) creada para el producto, la misma será traída a este campo. Esto es útil como referencia al [subcontratar](/docs/user/manual/en/manufacturing/subcontracting).

* **Plantilla de impuesto**: se puede especificar una Plantilla de impuesto para aplicar un impuesto a cada producto en particular. Para saber más, visitar la siguiente [página](/docs/user/manual/es/accounts/item-tax-template).

* **Salto de página** insertará un espacio después de cada producto en la impresión.

#### Actualizar el Inventario

> Nota: a partir de la versión 13 se implementó el balance inmutable, el cual cambia las reglas de cancelación de entradas de inventario y registro de transacciones de stock con fecha anterior. Más información [aquí](/docs/user/manual/en/accounts/articles/immutable-ledger-in-erpnext).

La opción **Actualizar el Inventario** debería estar tildada si se desea que el sistema actualice automáticamente el inventario. Al hacer esto no es necesario crear una Nota de entrega.

### 3.8 Impuestos y cargos

Los impuestos y cargos serán traídos desde la [Orden de compra](/docs/user/manual/es/buying/purchase-order) o el [Recibo de compra](/docs/user/manual/es/stock/purchase-receipt).

![PI Tax](/docs/assets/img/accounts/pi-tax.png)

Visitar la página [Plantilla de Impuestos y Gastos de Compra](/docs/user/manual/es/buying/purchase-taxes-and-charges-template) para saber más sobre impuestos.

En caso de que existan percepciones sufridas, las mismas deberán ingresarse de manera manual, asignando la cuenta contable sobre la cual se desea que impacten. Más información acerca de Percepciones [aquí](/docs/user/manual/es/accounts/percepciones). 

Los impuestos y cargos totales aparecerán debajo de la tabla.

Para agregar impuestos automáticamente mediante Categoría de impuesto, visitar la siguiente [página](/docs/user/manual/es/accounts/tax-category).

Es importante asegurarse de marcar todos los Impuestos y cargos correctamente para una facturación precisa.

#### Regla de envío

Una Regla de envío ayuda a calcular el costo del envío de un producto. Este incrementará con la distancia del envío. Para saber más, visitar la página [Regla de envío](/docs/user/manual/es/selling/shipping-rule).

### 3.9 Descuento adicional

Cualquier descuento adicional hecho sobre el total de la factura puede ser asignado en esta sección. El descuento puede calcularse en base al Total (después de sumarle los impuestos y cargos) o sobre el Total Neto. El descuento adicional puede definirse en porcentaje o ser un monto fijo.

![PI Discount](/docs/assets/img/accounts/pi-discount.png)

Visitar la página [Aplicar un descuento](/docs/user/manual/es/selling/articles/applying-discount) para más detalles.

### 3.10 Pagos adelantados

Para productos de costo elevado, el vendedor puede solicitar un pago adelantado antes de procesar la orden. El botón **Obtener anticipos recibidos** permite traer a la factura los pagos adelantados. Para saber más, visitar la página [Pagos adelantados](/docs/user/manual/es/accounts/advance-payment-entry).

### 3.11 Términos de pago

El pago de una factura puede realizarse en partes dependiendo de lo acordado con el Proveedor. Esto es traído si se lo especificó en la Orden de compra.

![PI Payment Terms](/docs/assets/img/accounts/pi-pay-terms.png)

Para saber más, visitar la página [Términos de pago](/docs/user/manual/es/accounts/payment-terms).

### 3.12 Desajuste

El desajuste ocurre cuando el Cliente paga un importe menor al total de la factura. Puede ser una diferencia mínima de $0,50. Si ocurre en muchas ordenes, puede sumar una cifra mucho mayor. Para precisión contable esta diferencia es "anulada". Para saber más, visitar la página [Entrada de pago](/docs/user/manual/es/accounts/payment-entry#25-deductions-or-loss).

### 3.13 Términos y condiciones

En transacciones de compra/venta puede haber ciertos términos y condiciones dependiendo de si el Proveedor suministra bienes o servicios al Cliente. Se pueden aplicar estos términos a las transacciones y los mismos aparecerán en la impresión del documento. Para saber sobre Términos y condiciones hacer click [aquí](/docs/user/manual/es/setting-up/print/terms-and-conditions).

### 3.14 Ajustes de impresión

#### Membrete

Se puede imprimir la factura utilizando el membrete de la compañía. Más información [aquí](/docs/user/manual/es/setting-up/print/letter-head).

'Agrupar mismos artículos' agrupará los productos que aparecen en más de una fila de la tabla. Esto se verá solo en la impresión.

#### Imprimir Encabezado

El encabezado de las facturas también puede ser seleccionado al imprimir el documento. Para esto se debe seleccionar el Encabezado deseado. Para crear un nuevo Encabezado ir a: Inicio > Configuración > Impresión > Encabezado. Más información [aquí](/docs/user/manual/es/setting-up/print/print-headings).

Existen ajustes adicionales para la impresión de Facturas de compra sin el importe, esto puede ser útil para productos con precio elevado.

### 3.15 Más información

* **De apertura**: si esta es una entrada de apertura seleccionar "Sí". Ej: si se está migrando desde otro sistema a ERPNext, se necesitará usar un Asiento de apertura para actualizar los balances en ERPNext.
* **Observaciones**: cualquier observación adicional sobre la factura puede agregarse en este campo.

### 3.16 Luego de validar

Al validar la factura, se pueden crear los siguentes documentos contra la misma:

1. [Asiento contable](/docs/user/manual/es/accounts/journal-entry)
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Solicitud de pago](/docs/user/manual/es/accounts/payment-request)
1. [Comprobante de Costo de Destino](/docs/user/manual/es/stock/landed-cost-voucher)
1. [Activo](/docs/user/manual/es/asset/asset)

![PI Submit](/docs/assets/img/accounts/pi-submit.png)

## 4. Más

### 4.1 Impacto contable

Similar a las Facturas de venta, en una Factura de compra se debe ingresar una cuenta de gastos o de activos para cada fila de la tabla de productos, dependiendo de si el producto es precisamente un gasto o un activo. También se puede cambiar el Centro de costos, el cual puede ser definido de antemano en el producto mismo o en la Compañía.

La Factura de compra afectará la contabilidad de la siguiente forma:

#### Entradas contables (Balance general) de una compra:
* **Debe**:
    * Gasto o Activo (total neto, excluyendo impuestos)
    * Impuestos (puede ser activo o gasto)
* **Haber**:
    * Proveedor

![PI Ledger](/docs/assets/img/accounts/pi-ledger.png)

### 4.2 Contabilidad cuando la opción "Está pagado" fue tildada

Si **Está pagado** fue tildada, ERPNext generará también la siguiente entrada contable:

Debe:
 * Proveedor
Haber:
 * Cuenta bancaria/de efectivo

Para ver las entradas generadas para la factura luego de validar, hacer click en "Ver > Libro de contabilidad".

### 4.3 ¿La compra es "Gasto" o "Activo"?

Si el producto es consumido inmediatamente o si es un servicio, entonces la compra se convierte en un gasto. Por ejemplo, un recibo telefónico o de viaje.

La compra de productos de inventario no representa todavía un gasto, ya que estos poseen un valor mientras permanecen en el almacén. Por esto se los considera un activo. Si son materias primas (utilizadas en un proceso), son convertirán en gasto en el momento en que sean consumidas. Si son para la venta, se convierten en gasto cuando son enviados al Cliente.

### 4.4 Deducción de impuestos

En mucho países, la ley exige que se deduzcan los impuestos al realizar el pago a los proveedores. Estos impuestos pueden estar basados en un precio estándar. Por lo general, bajo este tipo de esquemas, si un proveedor supera un determinado límite de pago, y el tipo de producto está sujeto a impuestos, se deberá deducir dicho impuesto (el cual se paga al gobierno en beneficio del proveedor).

Para hacer esto se deberá crear una nueva cuenta de impuesto dentro de "Pasivos impositivos" o similar y acreditar a esta cuenta el procentaje correspondiente por cada transacción.

### 4.5 Retención de pagos en una Factura de Compra

Existen dos formas de retener una factura de compra:
- Retención explícita
- Retención por fecha

#### Retención explícita
De esta forma se retiene la factura de forma indefinida. Para hacer esto simplemente se debe tildar la opción "Retener la Factura". En el campo "Motivo de Poner en Espera" se puede especificar el motivo de dicha retención.

Si se necesita retener una factura ya validada hacer click en el botón "Crear > Bloquear factura". Además se puede agregar un comentario explicando por qué la factura se puso en espera.

#### Retención por fecha
De esta forma se retiene la factura hasta la fecha especificada. Para esto, luego de tildar la opción "Retener la Factura", completar el campo "Fecha de Lanzamiento".

Luego de validar la factura, se puede cambiar esta fecha haciendo click en "Retener la Factura > Cambiar Fecha de Lanzamiento".

<img class="screenshot" alt="Purchase Invoice on hold" src="{{docs_base_url}}/assets/img/accounts/purchase-invoice-hold.png">

Tener en cuenta lo siguiente:
- Todas las compras puestas en espera serán excluídas de la tabla de referencias de las Entradas de pago.
- La Fecha de Lanzamiento no puede ser anterior al día actual.
- Solo se puede bloquear o desbloquear una factura de compra si está Impaga.
- Solo se puede cambiar la Fecha de Lanzamiento si la factura está Impaga.

### 5. Temas relacionados
1. [Facturas de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Impuestos del producto](/docs/user/manual/es/accounts/item-tax-template)
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Solicitud de pago](/docs/user/manual/es/accounts/payment-request)
1. [Pedido de Cotización](/docs/user/manual/es/buying/request-for-quotation)
1. [Orden de compra](/docs/user/manual/es/buying/purchase-order)
1. [Recibo de compra](/docs/user/manual/es/stock/purchase-receipt)
