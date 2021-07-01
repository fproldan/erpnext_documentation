<!-- add-breadcrumbs -->
# Punto de venta

**Un Punto de venta hace referencia al momento y lugar en el que se realiza una transacción de venta minorista.**

En operaciones de retail, la entrega de productos, devengo de la venta y el pago sucede en un mismo evento, que se suele denominar "Punto de venta" (POS).

En ERPNext las Facturas de venta pueden ser generadas desde el POS.

Para acceder al POS, ir a:
> Inicio > Retail > Punto de venta

## 1. Prerrequisitos
Antes de crear y usar un Punto de venta, se recomienda crear lo siguiente:

1. [Perfil de POS](/docs/user/manual/es/accounts/pos-profile)

## 2. Creación de una Factura de POS
Una vez que se creó un Perfil de POS, se puede comenzar a facturar.

1. Ir al POS y seleccionar un Cliente.
1. Agregar Productos desde la lista visible a la derecha haciendo click en cada uno.
1. El Producto deberá tener un precio de venta en el Precio de producto.
1. Editar las cantidades si es necesario.
1. Para poder editar el Precio y el Descuento, se debe habilitar esta opción en el Perfil de POS.
1. Es necesario establecer un almacén por defecto para poder completar la transacción. Si se definió un almacén en el Producto y en el Perfil, se dará preferencia al del perfil.
1. Nótese que se debe tener Productos en el Almacén para poder venderlos. Si los Productos no están disponibles, aparecerá un punto rojo en el recuadro del mismo advirtiéndolo.

  ![POS Screen](/docs/assets/img/accounts/pos-screen.png)
  
8. Luego de añadir los Productos deseados al Carrito de Compras, hacer click en "Pago".
1. Seleccionar el Método de pago y validar, se solicitará confirmación para validar la factura.
1. Se puede imprimir la Factura POS.
  ![POS Cycle](/docs/assets/img/accounts/pos-cycle.gif)
  
Luego de que la factura es validada, se puede imprimir o enviar por correo electrónico al Cliente.


### 2.2 Agregar un Producto al carrito
En el dispositivo POS existen dos formas de seleccionar un Producto. Una es haciendo click en la imagen del producto y otra es mediante el código de barra/número de serie.

* **Seleccionar producto**: hacer click en la imagen del producto hará que se agregue al carrito. El carrito es el área en el que se prepara la compra y permite editar información del producto, ajustar impuestos y agregar descuentos.

* **Código de barra/Número de serie**: el Código de barra/Número de serie es una representación de la información del producto que puede ser leído por una máquina. Ingresar este código en el campo que se muestra en la imagen hará que se agregue automáticamente el producto al carrito.

<img class="screenshot" alt="POS Item" src="{{docs_base_url}}/assets/img/accounts/pos-item.png">

> Tip: para cambiar la cantidad de un Producto, ingresar el valor deseado en el campo "Cantidad" que aparecerá al hacer click sobre el producto del carrito.

Si se tiene muchos productos resulta más práctico usar el campo de búsqueda ingresando el nombre del producto.

### 2.3  Quitar un Producto del carrito
Existen dos formas de quitar un producto del carrito:
1. Seleccionar el producto en el carrito y hacer click en el botón Quitar

    <img class="screenshot" alt="POS Item" src="{{docs_base_url}}/assets/img/accounts/pos_deleted_item.gif">

2. Ingresar Cantidad: 0.

### 2.4 Cambio

El POS calcula el monto extra pagado por el Cliente, el cual le será devuelto desde la cuenta de efectivo. El usuario debe establecer la Cuenta para monto de cambio en el Perfil.

<img class="screenshot" alt="POS Payment" src="{{docs_base_url}}/assets/img/accounts/change-amount.png">

### 2.5 Write off Amount
If you are writing off certain amount. For example when you receive extra cash as a result of not having exact denomination of change, check on ‘Write off Outstanding Amount’ and set the Account.

Outstanding amount can be write off from the POS, user has to enter the amount under Write Off field on the payment screen.

For example, here bill amount is 2,310, but the Customer paid 2,300, then the amount written off will be 10.
<img class="screenshot" alt="POS Payment" src="{{docs_base_url}}/assets/img/accounts/write-off.png">

System books the Write Off amount into the General Ledger account which has selected on the POS Profile.

### 2.6 Selección del Perfil de POS

Change the POS Profile via:
> Menu > Change POS Profile

Select the Company and then choose the POS Profile from the list. You can also set the newly selected POS profile as the default for the Company.

<img class="screenshot" alt="Change POS Profile" src="{{docs_base_url}}/assets/img/accounts/Change-POS-Profile.png">

## 3. Funcionalidades

### 3.1 Crear un nuevo Cliente
En el POS, los usuarios pueden seleccionar un Cliente existente o crear uno nuevo. También se puede agregar detalles a los Clientes, como correo electrónico, número de teléfono, etc.

<img class="screenshot" alt="POS Customer" src="{{docs_base_url}}/assets/img/accounts/pos-customer.gif">

### 3.4 Entradas contables (Balance general) de un Punto de venta:

Débitos:

  * Cliente (total)
  * Banco/Efectivo (pago)

Créditos:

  * Ingreso (neto total, menos los impuestos de cada Producto)
  * Impuesto (monto a pagar al gobierno)
  * Cliente (pago)
  * Desajuste (opcional)
  * Cuenta para monto de cambio (opcional)

Para ver las entradas luego de validar la [Factura de venta](/docs/user/manual/es/accounts/sales-invoice), hacer click en **Mostrar Libro Mayor**.

### 3.5 Correo electrónico

Los usuarios pueden enviar correos desde el POS, luego de validar una Factura, haciendo click en "Enviar correo electrónico".

<img class="screenshot" alt="POS Payment" src="{{docs_base_url}}/assets/img/accounts/pos-email.png">

El correo se envía al Cliente con la factura adjunta.

### 3.6 Comprobante de cierre de POS

Al final del día, el cajero puede cerrar el POS creando un Comprobante de cierre de POS.
Hacer click en el menú y seleccionar "Cierre el POS". Seleccionar el período, el Perfil de POS y el usuario utilizado para registrar todas las ventas.

For closing shift wise or cashier wise, use the [POS Cashier Closing](/docs/user/manual/en/accounts/pos-cashier-closing).

<img class="screenshot" alt="POS Payment" src="{{docs_base_url}}/assets/img/accounts/pos-closing-voucher.png">

Enter the collected amount for each mode of payment. If you notice any difference between the system amount and the actual physical cash collected, create a Difference Posting.

### 4. Temas relacionados
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Orden de compra](/docs/user/manual/es/buying/purchase-order)
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Solicitud de pago](/docs/user/manual/es/accounts/payment-request)
