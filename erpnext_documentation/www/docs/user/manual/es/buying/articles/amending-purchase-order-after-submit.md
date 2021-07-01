<!-- add-breadcrumbs -->
# Corregir Orden de Compra validada
Luego de haber validado la Orden de Compra, el Precio y la Cantidad establecidos en la misma pueden ser corregidos utilizando el botón "Actualizar productos". 

<img alt="Update Items" class="screenshot" src="{{docs_base_url}}/assets/img/articles/po-update-items.png">

Para Actualizar Precio y Cantidad en una Orden de Compra validada, hacer click en el botón "Actualizar productos". Aparecerá una ventana emergente que permitirá realizar el cambio. 

<img alt="Update Items" class="screenshot" src="{{docs_base_url}}/assets/img/articles/po-update-items-rate-and-qty.gif">

Por favor, tener en cuenta la siguientes validaciones y casos de uso: 

- Las Funciones de Actualización controlan si la Orden de Compra tiene Recibo de Compra y Factura de Compra. 
- La Cantidad puede ser actualizada para una Orden de Compra no recibida o parcialmente recibida. No puede actualizarse para Orden de Compra con un Recibo de Compra completo. 
- El Precio puede actualizarse para Ordenes de Compra no facturadas o parcialmente facturadas. No puede actualizarse para Ordenes de Compra con una Factura de Compra ya validada. 
