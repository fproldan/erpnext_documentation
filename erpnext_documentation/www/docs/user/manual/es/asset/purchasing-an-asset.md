# Compra de un Activo

Para comprar un nuevo activo:

1. Crear una Categoría de Activo.
1. Crear un Producto relacionado con la opción "Es Activo Fijo".
1. También se puede habilitar la opción "Crear Activos Automáticamente al Comprar" para crear los activos de forma automática. (Opcional)

  <img class="screenshot" alt="Purchasing Asset" src="{{docs_base_url}}/assets/img/asset/asset-auto-create-on-purchase.png">

4. Luego, deberá seguirse el [ciclo de compra](/docs/user/manual/es/buying/purchase-order) para comprar un activo.
1. Ingresar la Ubicación del Activo en la tabla de Productos del [Recibo de Compra](/docs/user/manual/es/stock/purchase-receipt) o [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice) a través de la cual se recibe el producto.
1. Al validar un Recibo de Compra, si está tildada la opción de creación automática, se crearán los registros de Activo automáticamente. Luego pueden ingresarse manualmente otros detalles en el Activo. 

<img class="screenshot" alt="Purchasing Asset" src="{{docs_base_url}}/assets/img/asset/asset-purchase-receipt.png">

Se generarán nuevos registros contables al validar el Recibo si la Contabilidad de Capital en Proceso de Trabajo está habilitada en la Categoría del activo comprado.

<img class="screenshot" alt="Asset" src="{{docs_base_url}}/assets/img/asset/asset-purchase-receipt-gl-entries.png">

Aquí se puede notar que, en vez de debitar la cuenta de activo correspondiente, se debitó la cuenta Capital en Proceso de Trabajo. Esto se debe a que el activo acaba de ser comprado y todavía no está disponible para ser utilizado. Hasta que el activo esté disponible para ser utilizado, el valor se mantendrá en esta cuenta. El día en que esté disponible para uso, se acreditará la cuenta de capital y se debitará la cuenta correspondiente al activo.

En el caso de que la opción "Contabilidad de Capital en Proceso de Trabajo" esté deshabilitada en la Categoría de Activo, el registro del recibo se realizará contra las cuentas de activo correspondientes configuradas en la Categoría de Activo. 

ERPNext también utiliza la cuenta temporal "Activo Recibido pero no Facturado" (una cuenta del pasivo) que se acredita al validar el registro del Recibo de Compra. Luego, al validar la Factura de Compra, esta cuenta se debita/revierte.

#### Temas Relacionados
1. [Activo](/docs/user/manual/es/asset/asset)
1. [Recibo de Compra](/docs/user/manual/es/stock/purchase-receipt)
1. [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice)
