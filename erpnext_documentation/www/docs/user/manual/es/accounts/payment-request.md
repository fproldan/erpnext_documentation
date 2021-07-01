<!-- add-breadcrumbs -->
# Solicitud de pago

**Este documento es utilizado para solicitar a los Clientes el pago de Ordenes o Facturas de venta.**

La solicitud de pago es enviada por medio de correo electrónico y puede contener un enlace a una Pasarela de pago. Se puede crear solicitudes de pago desde Ordenes o Facturas de venta. Una solicitud de pago también puede ser creada contra una Orden o Factura de compra para registro interno. Luego, los pagos pueden ser procesados de forma masiva usando una [Orden de pago](/docs/user/manual/es/accounts/payment-order).

Para acceder al listado de solicitudes de pago ir a:
> Inicio > Contabilidad > Facturación > Solicitud de pago

## 1. Prerequisitos
Antes de crear y usar una solicitud de pago, se aconseja crear lo siguiente:

1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Factura de compra](/docs/user/manual/es/accounts/purchase-invoice)
1. [Orden de venta](/docs/user/manual/es/selling/sales-order)
1. [Orden de compra](/docs/user/manual/es/buying/purchase-order)

## 2. Creación de una solicitud de pago
Una soliticud de pago no puede ser creada de forma manual, sino que se genera desde una Orden o Factura de venta/compra.

### 2.1 Creación desde Orden de venta
En una Orden de venta hacer click en Crear -> Solicitud de Pago.

<img class="screenshot" alt="Payment Request" src="{{docs_base_url}}/assets/img/accounts/pr-from-so.png">

### 2.2 Creación desde Factura de venta
En una Factura de venta hacer click en Crear -> Solicitud de Pago.

<img class="screenshot" alt="Payment Request" src="{{docs_base_url}}/assets/img/accounts/pr-from-si.png">

A continuación seleccionar la Cuenta de Pasarela de Pago correspondiente, la cual será utilizada en el Asiento contable.

> Nota: la divisa de la Orden/Factura debe ser la misma que la de la cuenta de la pasarela de pago.

<img class="screenshot" alt="Payment Request" src="{{docs_base_url}}/assets/img/accounts/pr-details-1.png">

### 2.3 Notificación al Cliente
Se puede notificar al cliente desde la Solicitud de pago usando el [Formato de impresión](/docs/user/manual/es/setting-up/print/print-format). Si la dirección de correo del cliente está especificada, esta será traída automáticamente. Si no se deberá ingresar en la solicitud misma. 

<img class="screenshot" alt="Payment Request" src="{{docs_base_url}}/assets/img/accounts/pr-details-2.png">

### 2.4 Correo de la solicitud
El siguiente es un ejemplo de una solicitud enviada por correo. La URL es generada automáticamente si se posee instalada la integración correspondiente para la generación de links de pago. Más información al respecto en la siguiente [página](/docs/user/manual/en/erpnext_integration).

<img class="screenshot" alt="Payment Request" src="{{docs_base_url}}/assets/img/accounts/pr-email.png">

### 2.5 Solicitud de pago sin Pasarela de pago

En el caso de que no se desee usar ninguna integración o pasarela de pago y solo se quiera notificar al cliente, se debe seleccionar una cuenta bancaria en el campo Cuenta de pagos. Se deberá redactar un mensaje con los datos bancarios correspondientes. El cliente puede luego tranferir el monto a dicha cuenta bancaria.

## 3. Temas relacionados
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Término de pago](/docs/user/manual/es/accounts/payment-terms)
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Factura de compra](/docs/user/manual/es/accounts/purchase-invoice)
