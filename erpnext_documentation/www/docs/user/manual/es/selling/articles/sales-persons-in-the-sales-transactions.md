<!-- add-breadcrumbs -->
# Vendedores en Operaciones de Venta

En ERPNext, los Vendedores se encuentran en un [esquema de árbol](/docs/user/manual/es/setting-up/articles/managing-tree-structure-masters.html). Los Vendedores pueden ser seleccionados en todas las operaciones de venta.

Los Vendedores también pueden vincularse con los Clientes. Al seleccionar un Cliente en una transacción, los Vendedores vinculados con el mismo serán asignados a las operaciones de venta.

<img class="screenshot" alt="Sales Person Customer" src="{{docs_base_url}}/assets/img/articles/sales-person-transaction-1.png">

#### Margen del Vendedor

Si dos o más vendedores están trabajando de forma conjunta en una orden, debe establecerse el margen (%) de cada uno.

<img class="screenshot" alt="Sales Person Order" src="{{docs_base_url}}/assets/img/articles/sales-person-transaction-2.png">

Al guardar la transacción, de acuerdo al Total Neto y el Margen (%) se calculará el `Margen al Total Neto` para cada Vendedor.

<div class=well> El total de % de Margen para todos los Vendedores debe ser del 100%. Si se selecciona solo un Vendedor, entonces el % de Margen será 100%.</div>

#### Informe de Transacciones del Vendedor

Para ver este informe ir a:

> Ventas > Reportes clave > Resumen de transacciones por vendedor

Este informe puede generarse basado en Orden de Venta, Nota de Entrega y Factura de Venta. Mostrará el monto total de venta realizado por un empleado. 

<img class="screenshot" alt="Sales Person Report" src="{{docs_base_url}}/assets/img/articles/sales-person-transaction-3.png">

#### Comisión del Vendedor

ERPNext solo muestra el total de venta realizado por un Vendedor. Si se le ofrece comisión a dicho Vendedor debería añadirse a los Vendedores como Socios de ventas en ERPNext. Para Socios de ventas se puede definir la Comisión (%). Al seleccionar Socios de ventas en Operaciones de Venta, de acuerdo al Total Neto, también se calcula el Monto de la Comisión. Se pueden ver los informes de comisión de Socios de ventas en:
> Contabilidad > Informes > Comisiones de socios de ventas
