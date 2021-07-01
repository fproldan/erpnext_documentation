<!-- add-breadcrumbs -->
# Orden de pago

**Una Orden de pago es un documento interno usado para registrar pagos múltiples a Proveedores.**

En grandes corporaciones, la decisión de realizar pagos a Proveedores es llevada a cabo por alguien como el Gestor de compras. La acción de crear los pagos es realizada por un Contador. 

La Orden de pago es la comunicación entre el Gestor de compras y el Contador mediante la cual se notifica que se debe proceder con el pago.

En ERPNext, usando la Orden de pago, se pueden agrupar múltiples Solicitudes de pago creadas contra un mismo Proveedor.

## 1. Prerrequisitos
Antes de crear y usar la Orden de pago, se recomienda crear lo siguiente:

1. [Orden de compra](/docs/user/manual/es/buying/purchase-order)

 o

1. [Factura de compra](/docs/user/manual/es/accounts/purchase-invoice)

## 2. Creación de una Orden de pago
1. Ir al listado de Orden de pago y hacer click en Nuevo.
1. Seleccionar la cuenta de banco de la Compañía.
1. Hacer click en el botón **Obtener desde** y seleccionar Solicitud de pago. Aplicar los filtros necesarios y seleccionar las Solicitudes de pago.
 ![Payment Order Fetch](/docs/assets/img/accounts/payment-order-fetch.png)
4. Las solicitudes de pago serán traídas a la Orden de pago.
 ![Payment Order Fetch](/docs/assets/img/accounts/payment-order.png)
5. Guardar y validar. Aparecerá un botón para crear Entradas de pago de forma masiva.
 ![Payment Order Fetch](/docs/assets/img/accounts/payment-order-submit.png)
