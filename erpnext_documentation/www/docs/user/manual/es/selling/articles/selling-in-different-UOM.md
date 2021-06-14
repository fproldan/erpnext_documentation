<!-- add-breadcrumbs -->
# Vender en Diferentes Unidades de Medida (UOM)
 
Una unidad de medida (UOM) de precio de venta es la UOM con la que se da un precio a los productos. Se puede tener muchas UOM de precio de venta por cualquier artículo en inventario. Sin embargo, para vender al cliente, la UOM para un artículo puede cambiar. 
 
Por ejemplo, una lapicera puede guardarse en depósito en unidades, pero se vende en Cajas. Por ende se realizará la Orden de Venta por Lapiceras en Caja. 
 
### Paso 1: En los Productos, bajo la sección Unidad de Medida se pueden enumerar todas las posibles UOM para un producto, con su Factor de Conversión de UOM. Actualizar los Factores de Conversión de UOM. 
Si en una caja hay 10 unidades de Lapiceras, entonces el Factor de Conversión de UOM es 10. 

<img class="screenshot" alt="Item Unit of Measure" src="{{docs_base_url}}/assets/img/selling/Item-UOM.png">


### Paso 2: En la Orden de Venta, se encuentran dos campos UOM 

- UOM
- UOM del almacén

En ambos campos, la UOM de un producto será obtenida de forma preestablecida. Se deberá editar el campo UOM, y seleccionar UOM de Venta (en este caso, la Caja). Actualizar la UOM de venta mas que nada sirve de referencia al Cliente. En el formato de impresión se verá la cantidad de producto en la UOM de Venta. 

<img class="screenshot" alt="Sale order Unit of Measure" src="{{docs_base_url}}/assets/img/selling/Sale-Order-UOM.png">
 
De acuerdo a la cantidad y al Factor de Conversión, la cantidad se calculará en la UOM de existencias de un producto. Si solo se vende una Caja, entonces la cantidad de acuerdo a la UOM de existencias será establecida como 10. 
 
 
### Actualización del Mayor de Inventarios
 
Sin importar la UOM de Venta seleccionada en la Orden de Venta, la actualización del Mayor de Inventarios se realizará en la UOM predeterminada de un producto. Por ende, es importante que el factor de conversión sea ingresado correctamente al vender productos en diferentes UOM. 

<img class="screenshot" alt="Stock report in UOM" src="{{docs_base_url}}/assets/img/selling/stock ledger for as STOCK-UOM.png">
