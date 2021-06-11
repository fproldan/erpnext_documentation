# Regla de ubicación

**Una Regla de ubicación define una estrategia para asignar los productos entrantes en los almacenes correspondientes.**

Una Regla de ubicación define una relación única de Producto-Almacén, en la que se tiene en cuenta la capacidad del almacén y se determina una cierta prioridad.

En **Recibos de compra** y **Entradas de inventario** (Recepción y Transferencia de materiales), se aplican las Reglas de ubicación y los Productos son auto-asignados a los **Almacenes** en base a la estrategia definida.

Esto es particularmente útil para administrar la capacidad en almacenes grandes con múltiples ubicaciones.

Para acceder a la Regla de ubicación ir a:

> Inicio > Almacén > Transacciones de Inventario > Regla de ubicación

## 1. Prerrequisitos

Antes de crear y usar una Regla de ubicación se recomienda crear lo siguiente:

- [Producto](/docs/user/manual/es/stock/item)
- [Almacén](/docs/user/manual/es/stock/warehouse)

## 2. Creación de una Regla de ubicación

1. Ir al listado de Regla de ubicación y hacer click en Nuevo.
 <img class='screenshot' alt='Unsaved Pick List' src='{{docs_base_url}}/assets/img/stock/unsaved-putaway-rule.png'>

2. Elegir la Compañía y el Producto.
1. Selecionar el Almacén para el cual aplica esta regla.
1. Definir la Capacidad. También se puede seleccionar la UOM si se desea usar una diferente. La Capacidad en Stock UOM se completará automáticamente.
 <img class='screenshot' alt='Unsaved Pick List' src='{{docs_base_url}}/assets/img/stock/multi-uom-putaway-rule.png'>

5. Ingresar la Prioridad, la cual puede ir de 1 en adelante, siendo 1 la mayor prioridad.
6. Guardar.
 <img class='screenshot' alt='Unsaved Pick List' src='{{docs_base_url}}/assets/img/stock/saved-putaway-rule.png'>

Es posible Desactivar luego las Reglas creadas.

Cada Regla es una combinación única de Producto-Almacén.

## 3. Estrategia de las Reglas de ubicación

1. La estrategia se basa principalmente en la **Capacidad** y la **Prioridad**.
1. Los Almacenes serán asignados automáticamente hasta que no tengan más capacidad libre.
1. Primero se tendrán en consideración la prioridad, luego el espacio libre. Si dos Reglas poseen la misma prioridad, se usará la que disponga de mayor espacio libre.
1. Si ya no se posee espacio libre en ningún Almacén, el sistema mostrará un mensaje advirtiéndolo.

## 4. Funcionamiento

Como se mencionó anteriormente, las Reglas de ubicación son aplicadas en la creación de un **Recibo de compra** o una **Entrada de inventario** (Recepción o Transferencia de Material).

Tildar la opción **Aplicar Regla de ubicación** asignará los Productos en los Almacenes en base a las reglas existentes.
 <img class='screenshot' alt='Apply Putaway Rule checkbox' src='{{docs_base_url}}/assets/img/stock/apply-putaway-rule.png'>

Las Reglas también vuelven a aplicarse al guardar el documento si la opción está tildada.

Ejemplo:

1. En este caso se genera una Orden de compra con 5 botellas (60 Nos) de agua mineral.
 <img class='screenshot' alt='Purchase Order' src='{{docs_base_url}}/assets/img/stock/po-putaway-demo.png'>

2. Existen dos Reglas de ubicación, cada una con capacidad menor a 4 botellas (48 Nos). Una posee mayor prioridad que la otra.
  <img class='screenshot' alt='Active Putaway Rules List' src='{{docs_base_url}}/assets/img/stock/active-putaway-rules-list.png'>

3. Un Recibo de compra es creado para dicha Orden.

4. Al tildar **Aplicar Regla de ubicación**, la fila de 5 botellas es dividida y asignada de acuerdo a las reglas.
 <img class='screenshot' alt='Putaway Rules applied in a Purchase Receipt' src='{{docs_base_url}}/assets/img/stock/pr-putaway-apply.gif'>

5. Primero, 4 de las 5 botellas con acomodadas en el Almacén 'Finished Goods'. Al quedar ese Almacén sin espacio libre, se asigna el resto (1 botella) al Almacén 'Stores'.

## 5. Resumen de capacidad de almacenes

Este reporte muestra el nivel de capacidad de cada Almacén.

Solo se muestran Almacenes con Reglas de ubicación. El botón **Editar Capacidad** permite editar la capacidad definida en la Regla de ubicación.

 <img class='screenshot' alt='Warehouse Capacity Summary' src='{{docs_base_url}}/assets/img/stock/warehouse-capacity-summary.png'>


## 6. Tipos de aplicación de las Reglas de ubicación

### 6.1. Ubicación directa

1. El ejemplo anterior explica la **Ubicación directa**.
1. Esto esto es, básicamente, asignar directamente el inventario entrante a ciertos Almacenes en base a la estrategia establecida.
1. Esto puede realizarse fácilmente desde un Recibo de compra.

### 6.2. Ubicación indirecta (combinada)

1. El inventario es normalmente recibido primero en almacenes **temporarios**.
1. Desde aquí es enviado a una ubicación apropiada en el Almacén.
1. Esto se conoce como Ubicación **indirecta o combinada**.
1. Para simular esto en el sistema, se puede crear un Recibo de compra común, sin aplicar ninguna regla.
1. Desde aquí, se puede crear una Entrada de inventario (transferencia de material), donde sí se aplicará la Regla de ubicación.

## 7. Temas relacionados

1. [Recibo de compra](/docs/user/manual/es/stock/purchase-receipt)
1. [Entrada de inventario](/docs/user/manual/es/stock/stock-entry)
