<!-- add-breadcrumbs -->
# Pagos adelantados

**Pagos realizados por el Cliente/Proveedor antes del envío de la factura son considerados Pagos adelantados.**

Generalmente, el pago adelantado se realiza en casos de importes elevados. Por ejemplo, en el caso de que un Cliente ordene un mueble de lujo cuyo precio es de $24.000 y se le pide que pague por adelantado una determinada suma antes de que se inicie la confección de dicho producto.

En ERPNext, el pago adelantado se registra por medio de una Entrada de pago. Si existe una Orden de venta, se puede crear directamente una Entrada de pago por el monto del adelanto. O sino, se puede crear una Entrada de pago independiente para el Cliente. De la misma forma se pueden crear Entradas de pago para Proveedores por medio de Ordenes de compra.

![PE from SO](/docs/assets/img/accounts/advance-payment-1.png)

> Nota: si el pago no está vinculado a una factura, se lo considera como un pago adelantado. Los pagos adelantados se ven reflejados en las Cuentas a cobrar y reportes de pagos.

## 1. Prerequisitos
Para crear un pago adelantado, se necesita tener previamente creado lo siguiente:

* Entidad (Cliente/Proveedor)
* Cuenta de pago (Banco o Efectivo)

## 2. Creación de Pagos adelantados
Una vez que se validan las Ordenes de venta o compra, aparece la opción para crear un Pago contra la misma. También se puede crear una nueva Entrada de pago y manualmente seleccionar los valores correspondientes (como entidad y cuentas de pago). A continuación se listan los pasos para la creación de Pagos adelantados contra Ordenes de venta.

1. Ir a la Orden de venta y hacer click en **Crear > Pago**.
1. Seleccionar/tildar las cuentas.
1. Guardar y validar.


Cualquier Entrada de pago que no está vinculada a una factura es considerada como pago adelantado.

Si el Cliente pagó $5.000 en efectivo como adelanto, esto será registrado como una entrada de crédito contra la cuenta a cobrar del cliente. Para balancear esto (según el sistema contable de doble entrada), se debitarán $5.000 de la cuenta de efectivo de la compañía.

### 2.2 Asignación de Pagos adelantados en la factura

Al crear una factura, se debe chequear si existe un Pago adelantado para esa entidad.

<img class="screenshot" alt="Advace Payment" src="{{docs_base_url}}/assets/img/accounts/advance-payment-3.png">

Al hacer click en el botón **Obtener anticipos recibidos** serán traídas a la factura las Entradas de pago de la entidad. Luego, se puede asignar el monto del anticipo contra la factura. La asignación reducirá el monto pendiente de la factura de forma inmediata.

Guardar y validar la Factura de venta.

### 3. Temas relacionados
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Asiento contable](/docs/user/manual/es/accounts/journal-entry)
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
