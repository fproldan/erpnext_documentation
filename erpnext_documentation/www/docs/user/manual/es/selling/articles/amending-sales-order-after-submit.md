<!-- add-breadcrumbs -->
# Corregir Orden de Venta validada
El Precio y la Cantidad pueden ser modificados luego de validar la Orden de Venta utilizando el botón `Actualizar Productos`.

<img alt="Update Items" class="screenshot" src="{{docs_base_url}}/assets/img/articles/so-update-items.png">

Para actualizar el precio y la cantidad en una Orden de Venta validada, hacer click en el botón `Actualizar Productos`. Al hacer eso aparecerá una ventana de diálogo que permitirá realizar el cambio. 

<img alt="Update Items" class="screenshot" src="{{docs_base_url}}/assets/img/articles/so-update-items-rate-and-qty.gif">

Tener en cuenta las siguientes validaciones y posibilidades de aplicación: 

- La función de Actualización revisa si la Orden de Venta posee Nota de Entrega y Factura de Venta.
- La cantidad solo puede ser actualizada para Ordenes de Venta que no han sido entregadas o que cuentan con una Nota de Entrega Parcial. Para Ordenes de Venta con Notas de Entrega completas, la cantidad no puede actualizarse. 
- El precio puede actualizarse para Ordenes de Venta que aún no han sido facturadas o que han sido parcialmente facturadas. Para Ordenes de Venta con Factura de Venta validada, no puede ser actualizado. 
