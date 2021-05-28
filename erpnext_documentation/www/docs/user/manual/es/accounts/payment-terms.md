<!-- add-breadcrumbs -->
# Términos de pago

**Un Término de pago ayuda a crear un cronograma acorde al cual se deberán registrar los pagos.**

Un Término de pago define una tabla de pagos específica. Por ejemplo, 50% del pago en el envío y 50% en la entrega del producto. Se puede guardar estos términos de pago del negocio en ERPNext e incluírlos en todos los documentos del ciclo de compra/venta. ERPNext generará las entradas del Balance general correspondientes.

En ERPNext, el Término de pago define únicamente porcentajes. El cronograma de pagos real puede generarse fácilmente usando una [Plantilla de términos de pago](/docs/user/manual/es/accounts/payment-terms-template).

Se puede aplicar Términos de pago en los siguientes documentos:

- Facturas de venta
- Facturas de compra
- Orden de venta
- Orden de compra
- Cotización

Para acceder a los Términos de pago ir a:
> Inicio > Contabilidad > Facturación > Término de pago

Nótese que la introducción de Términos de pago hace innecesarios los campos "Días de crédito" y "Días de crédito basado en" del Cliente/Proveedor. El Término de pago contiene esta misma información y es más sencillo de usar.

![Payment Terms]({{docs_base_url}}/assets/img/accounts/payment-terms.png)

## 1. Creación de un Término de pago

1. Ir al listado de Término de pago y hacer click en Nuevo.
1. Ingresar un nombre para el Término de pago (ej: 50% en el envío).
1. Ingresar la "Porción de Factura". Si se ingresa 50%, se considerará el 50% del monto de la factura.
1. Seleccionar una opción para "Fecha de Vencimiento basada en".
1. En el campo "Días de Crédito" ingresar el número de días luego de los cuales el importe pendiente debe ser pagado.
1. Guardar.

A continuación se explica cada uno de los campos antes mencionados:

* **Nombre del Término de Pago:** el nombre del término de pago.
* **Fecha de Vencimiento basada en:** criterio según el cual se calculará la fecha de vencimiento para el pago. Esto se calcula X días desde la **fecha de contabilización** de la factura/orden. Existen tres opciones:
    - **Día(s) después de la fecha de la factura**: la fecha de vencimiento se calculará en días tomando como referencia la fecha de contabilización de la factura. Por ejemplo, si se ingresa 7 en el campo Días de crédito y la fecha de la factura era del día 20, la fecha de vencimiento será el 27 del mes.
    - **Día(s) después del final del mes de la factura**: la fecha de vencimiento se calculará en días tomando como referencia el último día del mes en que se realizó la factura. Por ejemplo, si se ingresa 7 en el campo Días de Crédito, la fecha de vencimiento será el día 7 del mes próximo.
    - **Mes(es) después del final del mes de la factura**: la fecha de vencimiento será calculada en meses tomando como referencia el final del mes en el que se creó la factura. Por ejemplo, si se define 3 y la fecha de contabilización de la factura es el 20 de enero, la fecha de vencimiento será el 20 de marzo.
* **Porción de Factura:** la parte del total de la factura a la cual se aplicará el pago. El valor ingresado será tomado como porcentaje (ej: 50 = 50%) del total de la factura/orden.
* **Días de Crédito (opcional):** número de días o meses hasta la fecha de vencimiento dependiendo de la opción elegida en "Fecha de Vencimiento basada en". 0 significa que no se permite ningún crédito.
* **Descripción (opcional):** breve descripción del Término de pago.

### 1.1 Descuento en pagos adelantados

Se puede definir un término de pago de forma que si este es efectuado en el período correspondiente, se aplica un determinado descuento al valor de la factura. Para esto se debe completar los siguientes campos:

* **Tipo de descuento:** por defecto es Porcentaje, pero se puede cambiar por Importe.
* **Descuento:** en porcentaje o importe (10% o $100).
* **Vigencia del descuento en base a:** este campo funciona de la misma forma que "Fecha de Vencimiento basada en".
* **Vigencia del descuento:** número de días o meses en los que el descuento será válido respecto a la fecha de la factura (por ejemplo, 10 días después de la fecha de la factura).

<img class="screenshot" alt="Payment Terms with Discount" src="{{docs_base_url}}/assets/img/accounts/payment-terms-with-discount.png">

Habiendo vinculado el Término de pago con una factura, al registrar el pago se aplicará el descuento correspondiente.

### 1.2 Término de pago en documentos convertidos
Al convertir o copiar documentos en el ciclo de compra/venta, las Términos de pago asociados serán copiados también. Al crear una Orden de venta desde una Cotización, la fecha de vencimiento del Término de pago se calculará acorde a la Cotización, por lo que es necesario actualizarla.

Para simplificar su uso, también se puede especificar una Plantilla de términos de pago.

### 1.3 Agregar de Términos de pago a documentos

Una vez se haya armado la Plantilla de términos de pago, se la puede utilizar en transacciones de compra y venta. Basado en el valor definido para el Término de pago y el valor de la transacción, el cronograma de pagos será definido, con la fecha de vencimiento correspondiente para cada pago.

![Payment Schedule]({{docs_base_url}}/assets/img/accounts/payment-term-table.png)

Nota: el cronograma de pagos puede verse en la vista de impresión usando el [Constructor de formatos de impresión](/docs/user/manual/es/setting-up/print/print-format-builder).

### 2. Temas relacionados
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Factura de compra](/docs/user/manual/es/accounts/purchase-invoice)
