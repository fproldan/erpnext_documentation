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

1. Elegir la Compañía y el Producto.
1. Selecionar el Almacén para el cual aplica esta regla.
1. Definir la Capacidad. También se puede seleccionar la UOM si se desea usar una diferente. La Capacidad en Stock UOM se completará automáticamente.
 <img class='screenshot' alt='Unsaved Pick List' src='{{docs_base_url}}/assets/img/stock/multi-uom-putaway-rule.png'>

1. Ingresar la Prioridad, la cual puede ir de 1 en adelante, siendo 1 la mayor prioridad.
1. Guardar.
 <img class='screenshot' alt='Unsaved Pick List' src='{{docs_base_url}}/assets/img/stock/saved-putaway-rule.png'>

1. Es posible Desactivar luego las Reglas creadas.

Cada Regla es una combinación única de Producto-Almacén.

## 3. Estrategia de las Reglas de ubicación

1. La estrategia se basa principalmente en la **Capacidad** y la **Prioridad**.
1. Los Almacenes serán asignados automáticamente hasta que no tengan más capacidad libre.
1. Primero se tendrán en consideración la prioridad, luego el espacio libre. Si dos Reglas poseen la misma prioridad, se usará la que disponga de mayor espacio libre.
1. Si ya no se posee espacio libre en ningún Almacén, el sistema mostrará un mensaje advirtiéndolo.


## 4. Funcionamiento

Como se mencionó anteriormente, las Reglas de ubicación son aplicadas en la creación de un **Recibo de compra** o una **Entrada de inventario** (Recepción o Transferencia de Material).

A checkbox called **Apply Putaway Rule** will allocate items to Warehouses based on the Putaway Rules.
 <img class='screenshot' alt='Apply Putaway Rule checkbox' src='{{docs_base_url}}/assets/img/stock/apply-putaway-rule.png'>

Putaway Rules are applied on checking this checkbox. They are also re-applied on save if this checkbox is enabled.

Let us see the same in action:

1. Here is a Purchase Order with a requirement of 5 Cartons (60 Nos) of Mineral Water.
 <img class='screenshot' alt='Purchase Order' src='{{docs_base_url}}/assets/img/stock/po-putaway-demo.png'>

1. Two active Putaway Rules have been created below with capacity 4 Cartons (48 Nos) each. One has a higher priority than the other.

1. A Purchase Receipt is created from this Purchase Order.

1. On checking **Apply Putaway Rule**, one row of 5 Cartons is split and assigned according to the rules.
 <img class='screenshot' alt='Putaway Rules applied in a Purchase Receipt' src='{{docs_base_url}}/assets/img/stock/pr-putaway-apply.gif'>

1. First, 4 out of 5 Cartons are accommodated in the 'Finished Goods - UPI' Warehouse. Once this Warehouse is at capacity, it assigns the rest (1 Carton) to the 'Stores - UPI' Warehouse.

## 5. Warehouse Capacity Summary

The **Warehouse Capacity Summary** Report shows Warehouse capacities and their respective stock levels.

Only Warehouses having Putaway Rules will be listed here. The **Edit Capacity** button gives provision to edit the Putaway Rule capacity.

 <img class='screenshot' alt='Warehouse Capacity Summary' src='{{docs_base_url}}/assets/img/stock/warehouse-capacity-summary.png'>


## 6. Types of Putaway Application

### 6.1. Direct Putaway

1. The example in the previous section explains **Direct Putaway**.
1. It is, essentially, directly assigning incoming stock to certain Warehouses based on a strategy.
1. This can easily be exercised via a Purchase Receipt.

### 6.2. Indirect (Combined) Putaway

1. Stock is often received into **temporary** or **staging** Warehouses first.
1. From here it is placed into appropriate locations within the Warehouse.
1. This is called **Indirect or Combined** Putaway.
1. To simulate this within ERPNext, a simple Purchase Receipt can be created into the temporary Warehouse, without Putaway applied.
1. From here, a Stock Entry (Material Transfer) can be done, where Putaway Rules can be applied similar to Purchase Receipts.

## 7. Related Topics

1. [Purchase Receipt](/docs/user/manual/en/stock/purchase-receipt)
1. [Stock Entry](/docs/user/manual/en/stock/stock-entry)
