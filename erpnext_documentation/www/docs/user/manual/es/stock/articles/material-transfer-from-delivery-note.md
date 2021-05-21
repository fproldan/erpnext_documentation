<!-- add-breadcrumbs -->
# Transferencia de Material desde Nota de Entrega 

En ERPNext, se puede crear una entrada de Transferencia de Material desde un documento de [Entrada de Inventario](/docs/user/manual/es/stock/stock-entry). Sin embargo, hay algunos escenarios en la Transferencia de Materiales donde debe ser presentada como Nota de Entrega y Recibo de Compra. 

## Transferencia de Material desde Nota de Entrega

### Situaciones

1. Uno de los ejemplos es cuando se transfiere un Material desde un almacén hacia un sitio de proyecto, sin embargo, debe presentárselo como Nota de Entrega al cliente. 

2. A su vez, hay requerimientos estatutarios donde se debe aplicar impuestos a cada Transferencia de Material. Esta situación es más fácil administrar en una transacción como Nota de Entrega que como Entrada de inventarios. 

Considerando estas situaciones, se sumó la posibilidad de Transferencia de Material a las Notas de Entrega. A continuación se encuentran los pasos a seguir para utilizar Nota de Entrega para crear una entrada de Transferencia de Material.  

### Pasos

#### Habilitar Almacén de Cliente

El documento Nota de Entrega tiene un campo escondido denominado Almacén de Cliente. Se puede habilitar desde [Configuración de Inventario](/docs/user/manual/es/stock/stock-settings) al tildar "Permitir Transferencia de material desde la Nota de entrega a la Factura de venta". 

<img class="screenshot" alt="Delivery Note Material Transfer" src="{{docs_base_url}}/assets/img/stock/customer-warehouse.png">

### Seleccionar Almacenes

Al crear una Nota de Entrega para Transferencia de Material, seleccionar Almacén de origen para un producto en el campo correspondiente.

En el campo Almacén del Ciente, seleccionar el Almacén al cual el Material va a ser transferido o elegir un Almacén de destino. 

<img class="screenshot" alt="Delivery Note Material Transfer" src="{{docs_base_url}}/assets/img/stock/customer-warehouse-2.png">

Al validar una Nota de Entrega, las existencias del producto serán deducidas desde el "Almacén de Origen" y sumadas al "Almacén del Ciente". 

## Transferencia de Material desde Recibo de Compra

### Situaciones

Hay algunos requerimientos estatutarios donde deben aplicarse impuestos a cada Tansferencia de Material. Es por eso que es más facil administrar una situación como esta en una transacción como Recibo de Compra que en Entrada de inventario, debido a que no pueden aplicarse impuestos a Entradas de inventario. 

A continuación se encuentran los pasos para utilizar un Recibo de Compra para crear una entrada de Transferencia de Material. 

### Pasos

#### Habilitar Almacén delProveedor

Similar al Almacén del Ciente mencionado más arriba, el primer paso es habilitar el Almacén de Proveedor desde [Configuraciones de Inventario](/docs/user/manual/en/stock/stock-settings) como fue mostrado anteriormente. 

<img class="screenshot" alt="Delivery Note Material Transfer" src="{{docs_base_url}}/assets/img/stock/supplier-warehouse-enable.png">

### Seleccionar Almacenes

Al crear un Recibo de Compra para una Transferencia de Material seleccionar, para un producto, el almacén objetivo en el campo Almacén Aceptado. 

En el Almacén del Proveedor, seleccionar un Almacén desde donde será transferido el material.

<img class="screenshot" alt="Delivery Note Material Transfer" src="{{docs_base_url}}/assets/img/stock/supplier-warehouse.png">

Al validar el Recibo de Compra, las existencias del producto se descontarán del "Almacén del Proveedor" y se sumarán al "Almacén Aceptado". 
