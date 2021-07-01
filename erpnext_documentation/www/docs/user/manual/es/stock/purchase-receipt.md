<!-- add-breadcrumbs -->
# Recibo de Compra

**Los Recibos de Compra se realizan cuando se aceptan Productos del Proveedor, generalmente desde una Orden de Compra.**

También se pueden aceptar los Recibos de Compra de forma directa sin necesidad de una Orden de Compra. Para hacer esto, configurar el campo Orden de Compra Requerida como "No" en la Configuración de Compras. 

Para acceder al listado de Recibo de Compra, ir a:
> Inicio > Almacén > Transacciones de Inventario > Recibo de Compra

![Purchase Receipt flow](/docs/assets/img/stock/purchase-receipt-flow.png)

## 1. Prerrequisitos
Antes de crear y utilizar un Recibo de Compra se recomienda crear lo siguiente: 

* [Orden de Compra](/docs/user/manual/es/buying/purchase-order)

## 2. Creación de un Recibo de Compra
Un Recibo de Compra es generalmente creado desde una [Orden de Compra](/docs/user/manual/es/buying/purchase-order). En la Orden de Compra, hacer click en Crear > Recibo de Compra.

Para crear un Recibo de Compra de forma _manual_ (no recomendado), seguir los siguientes pasos:

1. Ir al listado de Recibo de Compra y hacer click en Nuevo. 
1. El nombre del Proveedor y los Productos pueden obtenerse desde la Orden de Compra haciendo click en "Obtener productos de > Orden de Compra".
1. Se puede configurar el Almacén Aceptado para todos los productos en este Recibo de Compra. Si esto está configurado en la Orden de Compra, se tomará desde allí. 
1. En el caso de que algún Producto sea defectuoso, configurar el Almacén a donde se enviarán esos Productos. 
1. Seleccionar el Producto e ingresar la cantidad en la tabla.
1. El Precio será obtenido y el Importe será calculado automáticamente.
1. Se puede expandir la fila de productos para cambiar el Almacén de Aceptados para un Producto.
1. Guardar y Validar.

    <img class="screenshot" alt="Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-receipt.png">

También se puede agregar una "Nota de Entrega del Proveedor" al Recibo de Compra si el Proveedor agregó algunas observaciones.
Utilizando la opción "Editar fecha y hora de envío" se puede editar la fecha y hora del Recibo de Compra. De forma predeterminada, la fecha y hora se establecerán cuando se hace click en el botón Nuevo. 

Es una devolución: tildar esta opción si se están devolviendo Productos que no fueron aceptados en el Almacén. 

### 2.1 Estados

Estos son los estados en que puede encontrarse un Recibo de Compra:

* **Borrador**: Se guarda un borrador pero todavía no se envía al sistema.
* **Por Facturar**: Pendiente de facturación a través de una [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice).
* **Completado**: Enviada y con todos los Productos recibidos.
* **Devolución emitida**: Todos los productos fueron devueltos. 
* **Cancelado**: Recibo de Compra cancelado.
* **Cerrado**: El fin del estado Cerrado es administrar el cierre definitivo del Recibo de Compra. Por ejemplo, se pidió 20 unidades de producto pero se cierra en 15. Por ende las otras 5 unidades no serán recibidas ni facturadas. 

## 3. Características
### 3.1 Divisa y Lista de Precios
En esta sección se muestra la moneda del Recibo de Compra, la cual se obtiene de la Orden de Compra. Los precios de los productos serán obtenidos de la Lista de Precios. Si se selecciona "Ignorar la Regla de precios", las reglas establecidas en Contabilidad > Regla de precios, no se tendrán en consideración.

Como el Producto que ingresa afecta el valor del inventario, es importante convertirlo a la moneda de base si es que se pidió en otra moneda. Para esto, se deberá actualizar el  Cambio de Divisa. 

Para saber más sobre Listas de Precios, hacer click [aquí](/docs/user/manual/es/stock/price-lists).

### 3.2 Detalles de Almacén
Los siguientes Almacenes configurados se aplicarán a todos los Productos de la tabla de Productos del Recibo de Compra. Se pueden cambiar los Almacenes para Productos individuales a través de la tabla. 

* **Almacén de Aceptados**: Este es el Almacén en el cual se aceptarán y guardarán los productos entrantes. Usualmente, se trata del Almacén de "Almacenamiento". 
* **Almacén de Rechazados:** Este es el Almacén en el que se guardarán los Productos rechazados que eran defectuosos o no cumplían con los estándares de calidad. 

#### Subcontratación

* **Materias primas consumidas**: En caso de subcontratar, seleccionar "Si" para consumir las Materias Primas del proveedor. Para saber más respecto a subcontrataciones [click aquí](/docs/user/manual/en/manufacturing/subcontracting).

### 3.3 Tabla de Productos

* **Código de Barra**: Se puede rastrear Productos utilizando [códigos de barra](/docs/user/manual/es/stock/articles/track-items-using-barcode).

* **Escanear Código de Barra**: Se pueden añadir Productos a la tabla de Productos al escanear sus códigos de barra si se cuenta con un lector de código de barra. Para aprender a rastrearlos click [aquí](/docs/user/manual/es/stock/articles/track-items-using-barcode)

* El Código de Producto, el nombre, descripción, Imagen y Fabricante serán obtenidos desde el Producto.

* **Recibidos y Aceptados**: Configurar la cantidad recibida, aceptada y rechazada. La UOM se obtiene desde el Producto. Se deberá actualizar el "Factor de Conversión de UOM" si la Orden de Compra para un Producto está en una Unidad de Medida (UOM) diferente que la de almacenamiento (UOM de existencias). 

    ![Purchase Receipt Items table](/docs/assets/img/stock/purchase-receipt-item.png)

* **Precio**: El Precio será tomado desde la [Lista de Precios](/docs/user/manual/es/stock/price-lists), si se hubiere configurado ahí, y se calculará el Importe total.  

* **Plantilla de Impuesto de Producto**: Se puede configurar una Plantilla de Impuesto de Producto para aplicar un Impuesto específico a este Producto en particular. Para saber más, visitar [esta página](/docs/user/manual/es/accounts/item-tax-template).

* Si hubiesen sido configurados allí, los Detalles de Peso del Producto por unidad y Peso en UOM serán tomados del Producto.

* **Almacén y Referencia**: Se pueden configurar los Almacenes para productos aceptados y rechazados, así como también añadir una Inspección de Calidad. Ver la sección siguiente. 

* **Número de Serie, Número de Lote y Lista de Materiales (BOM)**: Si el Producto es seriado o está en lotes, se deberá introducir el Número de serie y el Número de Lote en la tabla de Productos.  Se pueden ingresar múltiples Números de Serie en un sola fila (cada uno en una línea distinta) y se deberá ingresar tantas veces el Números de Serie como la cantidad de producto a comprar/vender. 

    Hay campos separados para ingresar los Números de Serie de Productos aceptados y rechazados. El Número de Lote también puede configurarse si, por ejemplo, se está almacenando un lote de fármacos.

    El tildar la opción "Permitir tasa de valoración cero" permitirá enviar el Recibo de Compra inclusive si el Valor del producto es 0. Esto puede deberse a que el producto es una muestra o a un acuerdo mutuo con el Proveedor. 

* En esta parte se puede relacionar el pedido a una Lista de Materiales si el producto está siendo [subcontratado](/docs/user/manual/en/manufacturing/subcontracting). Al relacionar la Lista de Materiales se afectará la Cuenta de Inventario, es decir: las existencias de materias primas serán deducidas del Almacén del Proveedor. 

    **Observación**: El Producto debe estar seriado o en lote para que estas características funcionen. Si el Producto esta seriado, aparecerá una ventana emergente donde se pueden ingresar los Números de Serie. 

* Las Dimensiones Contables ayudan a identificar cada transacción con diferentes Dimensiones sin la necesidad de crear nuevos Centros de Costos. Para esto, primero se deben crear las [Dimensiones Contables](/docs/user/manual/es/accounts/accounting-dimensions).

* Salto de Página creará un salto de página justo antes de este producto al imprimir.

### 3.4 Registrar Inspecciones de Calidad
Si para algunos Productos es obligatorio registrar Operaciones de Calidad (si esto fue establecido en el Producto), se deberá actualizar el campo "Inspección de Calidad". El sistema solo permitirá validar el Recibo de Compra si se actualiza la "Inspección de Calidad". 

Luego de habilitar los Criterios de Inspección para Compra en el [Formulario de Producto](/docs/user/manual/es/stock/item#216-inspection-criteria) y de adjuntar allí una Plantilla de Inspección de Calidad, las Inspecciones de Calidad pueden ser registradas en Recibos de Compra.

Para saber más visitar la página [Inspección de Calidad](/docs/user/manual/es/stock/quality-inspection).

![Quality Inspection](/docs/assets/img/stock/quality-inspection.png)


### 3.5 Materias Primas Consumidas
* La tabla de **Productos Consumidos** contiene las Materias Primas consumidas por el Proveedor para poder recibir el Producto Final. 
* El botón **Ver Existencias Actuales** tomará las existencias actuales de Productos Consumidos desde el Depósito del Proveedor.
    <img class="screenshot" alt="Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-receipt-consumed-items.png">

### 3.6 Impuestos y cargos sobre compras
Los Impuestos y cargos serán tomados desde la [Orden de Compra](/docs/user/manual/es/buying/purchase-order).

Visitar la página de [Plantilla de Impuestos (Compra)](/docs/user/manual/es/buying/purchase-taxes-and-charges-template) para saber más sobre impuestos.

El total de Impuestos y cargos será mostrado debajo de la tabla. 

Para añadir impuestos de forma automática a través de una Categoría de Impuesto, visitar [esta página](/docs/user/manual/es/accounts/tax-category).

Asegurarse de añadir correctamente todos los impuestos en la tabla de Impuestos y cargos para una valoración precisa. 

#### Regla de Envío
Una Regla de Envío ayuda a determinar el costo de enviar un producto. El costo tenderá a aumentar a medida que la distancia de envío sea mayor. Para saber más, vistar la sección [Regla de Envío](/docs/user/manual/es/selling/shipping-rule).


### 3.7 Descuentos Adicionales
En esta sección puede configurarse cualquier descuento adicional a aplicar a toda la orden. 
Leer [Aplicar Descuento](/docs/user/manual/es/selling/articles/applying-discount) para más detalles.

### 3.8 Más información
El estado del Recibo de Compra se muestra aquí y en la partesuperior del documento. Los distintos estados son: Borrador, Pendiente de Facturar, Completo, Cancelado y Cerrado. Esta sección también muestra el Procentaje facturado, es decir, el porcentaje del monto para el cual se han creado [Facturas de Venta](/docs/user/manual/es/accounts/sales-invoice).

### 3.9 Ajustes de Impresión

#### Membrete
Se pueden imprimir los Recibos de Compra en papel con el membrete de la empresa. Saber más [aquí](/docs/user/manual/es/setting-up/print/letter-head).

"Agrupar productos iguales", agrupará los productos iguales que se hayan sumado muchas veces a la tabla de Producto. Esto puede verse al imprimir.

#### Encabezado
Los encabezados de los Recibos de Compra pueden ser modificados al imprimir el documento seleccionando el correspondiente en **Encabezado**. Para crear nuevos Encabezados ir a: Inicio > Configuraciones > Impresión > Encabezados. Leer más [aquí](/docs/user/manual/es/setting-up/print/print-headings).

### 3.10 Luego de Validar

Se crea un ingreso a la Cuenta de Inventario por cada Producto, agregando el mismo al Almacén por la "Cantidad Aceptada". Si hay productos rechazados, se creará también un ingreso a la Cuenta de Inventario por cada Rechazo. La "Cantidad Pendiente" es actualizada en la Orden
de Compra.

Luego de validar el Recibo de Compra, pueden crearse los siguientes documentos:

* [Devolución de Compra](/docs/user/manual/es/stock/purchase-return)
* [Entrada de Inventario](/docs/user/manual/es/stock/stock-entry)
* [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice)
* [Retener Stock de Muestra](/docs/user/manual/es/stock/retain-sample-stock)

![Purchase Receipt submit](/docs/assets/img/stock/purchase-receipt-submit.png)

### 3.11 Devolver una Orden de Compra
Una vez recibida la Orden de Compra utilizando un Recibo de Compra, se puede crear una devolución en caso de que deban devolverse Productos al [Proveedor](/docs/user/manual/es/buying/supplier). Para saber más, visitar la página [Devolución de Compra](/docs/user/manual/es/stock/purchase-return).

### 3.12 Saltear Recibo de Compra

Si no se quiere crear un Recibo de Compra luego de realizada una Orden de Compra, y se desea pasar directamente a una Factura de Compra, habilitar esta opción en [Configuración de Compras](/docs/user/manual/es/buying/buying-settings#23-purchase-receipt-required).

* * *

#### Cambiar el valor de los Productos luego del Recibo de Compra:

A veces algunos gastos que suman al total de los Productos comprados se conocen luego de un tiempo. Un ejemplo común de esto es, si los Productos son importados, solo se conocerán los Aranceles Aduaneros y otros gastos cuando el "Despachante de Aduana" envíe su factura. Si se quiere sumar estos costos a los bienes comprados se debe utilizar el [Comprobante de Costo en Destino](/docs/user/manual/es/stock/landed-cost-voucher), ya que representa los gastos que se pagan cuando los Productos llegan a su destino. 

## 4. Temas Relacionados
1. [Nota de Entrega](/docs/user/manual/es/stock/delivery-note)
1. [Orden de Compra](/docs/user/manual/es/buying/purchase-order)
1. [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice)
1. [Proveedor](/docs/user/manual/es/buying/supplier)
1. [Comprobante de Costo en Destino](/docs/user/manual/es/stock/landed-cost-voucher)
