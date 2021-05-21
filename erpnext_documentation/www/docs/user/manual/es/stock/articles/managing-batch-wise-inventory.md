<!-- add-breadcrumbs -->
# Administrar Inventario en base a Lotes 

Un conjunto de productos que comparten las mismas propiedades y aributos puede agruparse en un solo Lote. Por ejemplo, los productos farmacéuticos son de lote, de forma tal que su fecha de fabricación y de vencimiento pueden rastrearse conjuntamente. 

Para mantener lotes de un producto determinado es necesario configurar el campo "Posee Número de Lote" como "Si" en el Producto.   

<img alt="Batch Item" class="screenshot" src="{{docs_base_url}}/assets/img/articles/batchwise-stock-1.png">

Se puede crear un nuevo Lote desde:

> Almacén > Número de serie y de lote > Lote > Nuevo

Para aprender más respecto a lotes hacer click [aquí](/docs/user/manual/es/stock/batch).

Para el Producto en Lote es obligatorio actualizar el Número de Lote en las transacciones de inventario (Recibo de Compra y Nota de Entrega).

#### Recibo de Compra

Al crear un Recibo de Compra, se debe crear un nuevo Lote o seleccionar uno existente. Un lote puede ser asociado con un Producto en Lote. 

<img alt="Batch in Purchase Receipt" class="screenshot" src="{{docs_base_url}}/assets/img/articles/batchwise-stock-2.png">

#### Nota de Entrega

Definir el Lote en la tabla de Productos de la Nota de Entrega. Si un producto en Lote es añadido dentro de un Paquete de Productos, se puede también actualizar su Número de Lote en la Lista de Embalaje. 

<img alt="Batch in Delivery Note" class="screenshot" src="{{docs_base_url}}/assets/img/articles/batchwise-stock-3.png">

#### Historial de Saldo por Lotes

Para ver el informe de inventario en base a lotes ir a: 

> Almacén > Reportes clave > Historial de Saldo por Lotes

<img alt="Batchwise Stock Balance" class="screenshot" src="{{docs_base_url}}/assets/img/articles/batchwise-stock-4.png">
