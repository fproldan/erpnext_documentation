# Regla de ubicación

**Una Regla de ubicación define una estrategia para asignar los productos entrantes en los almacenes correspondientes.**

Una Regla de ubicación define una relación única de Producto-Almacén, en la que se tiene en cuenta la capacidad del almacén y se determina una cierta prioridad.

En **Recibos de compra** y **Entradas de inventario** (Recepción y Transferencia de materiales), se aplican las Reglas de ubicación y los Productos son auto-asignados a los **Almacenes** en base a la estrategia definida.

This is particularly useful for capacity management in large warehouses with multiple locations.

To access a Putaway Rule, go to:

> Home > Stock > Stock Transactions > Putaway Rule
## 1. Prerequisites

Before creating and using a Putaway Rule, it is advised that you create the following first:

- [Stock Item](/docs/user/manual/en/stock/item)
- [Warehouse](/docs/user/manual/en/stock/warehouse)

## 2. How to create a Putaway Rule

1. Go to the Putaway Rule list, click on New.
 <img class='screenshot' alt='Unsaved Pick List' src='{{docs_base_url}}/assets/img/stock/unsaved-putaway-rule.png'>

1. Set the Company and Select an Item.
1. Set the Warehouse on which this rule is applicable.
1. Set the Capacity. You can also select a UOM if you want to set the Capacity in a different UOM. The Capacity in Stock UOM will be set automatically.
 <img class='screenshot' alt='Unsaved Pick List' src='{{docs_base_url}}/assets/img/stock/multi-uom-putaway-rule.png'>

1. Set the Priority. This can begin from 1 onwards, 1 being the highest priority.
1. Save.
 <img class='screenshot' alt='Unsaved Pick List' src='{{docs_base_url}}/assets/img/stock/saved-putaway-rule.png'>

1. You can additionally Disable a Putaway Rule as well.

The rule is unique to each Item-Warehouse combination.

## 3. How Putaway is strategized
1. Here the strategy is purely based on **Capacity** and **Priority**.
1. Warehouses will be auto-assigned until they reach full capacity.
1. Priority will be considered first. Followed by free space. If two rules have the same priority, the rule with more free space available will be assigned.
1. If you are running at full capacity (no free space in any Warehouse), ERPNext will let you know.


## 4. How does it work

As mentioned above the Putaway Rules are applied on the creation of a **Purchase Receipt** from a **Purchase Order**. Let us see that in action:

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