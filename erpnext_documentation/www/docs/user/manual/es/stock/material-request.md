<!-- add-breadcrumbs -->
# Solicitud de Materiales

**Una Solicitud de Materiales es un documento simple que identifica el requerimiento de un cierto conjunto de Productos (productos o servicios) por un motivo en particular.**

Una Solicitud de Material puede tener los siguientes objetivos:

* **Compra**: Si el material pedido debe ser comprado.
* **Transferencia de Material**: Si el material pedido debe ser pasado de un Almacén a otro. 
* **Expedición de Material**: Si el material pedido debe ser expedido para algún objetivo como fabricación.
* **Manufacturar:** Si el material pedido debe ser producido.
* **Proporcionado por el cliente**: Si el material pedido será provisto por un Cliente. Para saber más respecto a esto visitar la página [Productos Provistos por un Cliente](/docs/user/manual/es/manufacturing/articles/customer-provided-items).

<img class="screenshot" alt="Material Request" src="{{docs_base_url}}/assets/img/buying/material-request-flowchart.png">

Para acceder al listado de Solicitud de Material ir a:
> Inicio > Almacén > Transacciones de Inventario > Solicitud de Materiales

## 1. Creación de una Solicitud de Materiales
1. Ir al listado de Solicitud de Materiales y hacer click en Nuevo.
2. Completar el campo "Solicitado para".
3. Seleccionar uno de los objetivos mencionados anteriormente.
4. Se pueden tomar Productos desde Listas de Materiales, Ordenes de Venta o Paquetes de Productos. 
  ![MR fetch from](/docs/assets/img/stock/mr-fetch-from.png)
5. Seleccionar el Producto y configurar la cantidad.
6. Seleccionar el Almacén para el cual los productos son pedidos.
7. En esta tabla, se puede cambiar el "Solicitado para" para Productos individuales.
8. Guardar y Validar.

### 1.1 Formas alternativas de crear una Solicitud de Materiales
Una Solicitud de Materiales puede generarse automáticamente:

* Desde una [Orden de Venta](/docs/user/manual/es/selling/sales-order).
* Cuando la Cantidad Proyectada de un Producto en Almacén alcanza un nivel particular.
* Desde el [Plan de Producción](/docs/user/manual/es/manufacturing/production-plan) para planificar las actividades de fabricación.

Si los Productos son de inventario, también se debe mencionar el Almacén a donde se espera que los mismos sean enviados. Esto ayuda a controlar la [Cantidad Proyectada](/docs/user/manual/en/stock/projected-quantity) para este Producto.

> Información: La Solicitud de Materiales no es obligatoria. Es ideal si se cuenta con compras centralizadas, para poder recolectar esta información de varias oficinas.

### 1.2 Estados

Los estados en que puede encontrarse una Solicitud de Material son:

* **Borrador**: Un borrador está guardado pero todavía no fue enviado al sistema.
* **Validado**: El documento es enviado al sistema.
* **Suspendido**: Si no se requieren más materiales, la Solicitud de Material puede ser suspendida. 
* **Cancelado**: Los materiales no son necesarios y, por ende, se cancela el pedido.
* **Pendiente**: La Compra/Fabricación está pendiente para completar la Solicitud de Material. 
* **Parcialmente ordenado**: Ordenes de Compra para algunos Productos de la Solicitud de Materiales fueron hechas y otras están pendientes.
* **Ordenado**: Todos los Productos en la Solicitud de Materiales fueron pedidos a través de Ordenes de Compra.
* **Emitido**: Los materiales son distribuídos utilizando la Entrada de inventario de Expedición de Material. 
* **Transferido**: Los materiales requeridos son transferidos de un Almacén a otro utilizando Entrada de Inventario. 
* **Recibido**: Los materiales fueron pedidos y recibidos en el Almacén utilizando un Recibo de Compra. 

## 2. Características
### 2.1 Tabla de Productos
* **Código de Barra**: Se puede rastrear Productos utilizando [códigos de barra](/docs/user/manual/es/stock/articles/track-items-using-barcode).

* El Código de Producto, el nombre, descripción, Imagen y Fabricante serán obtenidos desde el Producto.

* **Escanear Código de Barra**: Se pueden añadir Productos a la tabla de Productos al escanear sus códigos de barra si se cuenta con un lector de código de barra. Para aprender a rastrearlos click [aquí](/docs/user/manual/es/stock/articles/track-items-using-barcode)

* La UOM, el Factor de Conversión, y el Monto serán obtenidos. Se cambia el Almacén para el cuál se realiza la Solicitud de material. 

* Detalles contables como la Cuenta de Gastos y Dimensiones Contables pueden ser configurados para los Productos. 

* Salto de Página creará un salto de página justo antes de este producto al imprimir.

### 2.2 Almacenes
* **Establecer Almacén de destino**: De forma opcional, se puede configurar el Almacén a donde llegarán los Productos pedidos. Esto será incluido en el campo "Almacén de destino" en las filas de la tabla de Productos. 

### 2.3 Detalles de Impresión
#### Membrete
Se pueden imprimir las Solicitud de Materiales en papel con el membrete de la empresa. Hacer click [aquí](/docs/user/manual/es/setting-up/print/letter-head) para saber más.

#### Encabezado
Los encabezados de las Solicitudes de material pueden ser modificados al imprimir el documento. Se puede hacer esto seleccionandolo en **Encabezado**. Para crear nuevos Encabezados ir a: Inicio > Configuraciones > Impresión > Encabezados. Leer más [aquí](/docs/user/manual/es/setting-up/print/print-headings).

### 2.4 Términos y Condiciones
En operaciones de Compra/Venta puede haber ciertas bases y condiciones que rigen la forma en que el proveedor vende bienes o servicios al cliente. Se pueden aplicar Términos y Condiciones a las transacciones y estos aparecerán en el documento impreso. Para saber más respecto a Términos y Condiciones, hacer click [aquí](/docs/user/manual/es/setting-up/print/terms-and-conditions)

### 2.5 Luego de Validar
Se pueden crear los siguientes documentos:

* [Solicitud de Cotización](/docs/user/manual/es/buying/request-for-quotation)
* [Orden de Compra](/docs/user/manual/es/buying/purchase-order)
* [Cotización de Proveedor](/docs/user/manual/es/buying/supplier-quotation)

<img class="screenshot" alt="Material Request" src="{{docs_base_url}}/assets/img/stock/material-request.png">


### 2.6 Generar Solicitud de Materiales Automáticamente

Las Solicitudes de Materiales pueden ser generadas automáticamente al habilitar la configuración en [Configuración de Inventario](/docs/user/manual/es/stock/stock-settings#9-automatic-material-request) y establecer el nivel en el [Producto](/docs/user/manual/es/stock/item#34-automatic-reordering). Cuando el nivel de existencias caiga por debajo de una cierta cantidad, al configurar un pedido automático, se generará automáticamente una Solicitud de materiales para el Producto.

## 3. Temas Relacionados
1. [Producto](/docs/user/manual/es/stock/item)
1. [Creación Automática de Solicitud de Materiales](/docs/user/manual/es/stock/articles/auto-creation-of-material-request)
1. [Lista de Selección](/docs/user/manual/es/stock/pick-list#23-create-pick-list-from-material-request)
1. [Solicitud de Cotización](/docs/user/manual/es/buying/request-for-quotation)
1. [Orden de Compra](/docs/user/manual/es/buying/purchase-order)
1. [Cotización de Proveedor](/docs/user/manual/es/buying/supplier-quotation)
