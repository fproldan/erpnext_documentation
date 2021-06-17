<!-- add-breadcrumbs -->
# Comprar en Diferentes Unidades de Medida (UOM)

Cada producto tiene su propia Unidad de Medida (UOM) de almacenamiento asociada. Por ejemplo, la UOM de lapiceras puede ser Unidades y la arena puede ser guardada en kilos. Sin embargo, cuando realizamos un pedido a un Proveedor, la UOM de un producto puede cambiar. Por ejemplo, podemos pedirle al Proveedor 1 kit/caja de Lapiceras, o, un camión de arena. Al crear la transacción de compra, se puede cambiar la UOM de Compra para un producto. 

### Situación:

El Producto "Lapicera" se almacena en Unidades pero se compra en Cajas. De esta forma, se realiza una Orden de Compra por Lapiceras en Cajas. 

#### Paso 1: Editar la UOM en la Orden de Compra

En la Orden de Compra se verán dos campos UOM.

- UOM
- UOM de Almacenamiento

En ambos campos, la UOM de un producto será obtenida de forma predeterminada. Se deberá editar el campo UOM, y seleccionar UOM de Compra (en este caso, la Caja). Actualizar la UOM de Compra mas que nada sirve de referencia al proveedor. En el formato de impresión se verá la cantidad de producto en la UOM de Compra. 

<img alt="Item Purchase UoM" class="screenshot" src="{{docs_base_url}}/assets/img/articles/editing-uom-in-po.gif">

#### Paso 2: Actualizar los Factores de Conversión

Si se reciben 20 unidades de Lapiceras en una Caja, el Factor de Conversión será 20.

<img alt="Item Conversion Factor" class="screenshot" src="{{docs_base_url}}/assets/img/articles/po-conversion-factor.png">

De acuerdo con la Cantidad y el Factor de Conversión, se calculará la cantidad en la UOM de Inventario. Si se compra solo una Caja, entocnes la cantidad en UOM de inventario será configurada como 20.

<img alt="Purchase Qty in Default UoM" class="screenshot" src="{{docs_base_url}}/assets/img/articles/po-qty-in-stock-uom.png">

### Actualización del Inventario de Existencias

Sin respetar la UOM de Compra seleccionada, la actualización del inventario de existencias se realizará en la UOM predeterminada de un producto. Por ende, es importante que el factor de conversión sea ingresado correctamente al comprar productos en diferentes UOM. 

<img alt="Print Format in Purchase UoM" class="screenshot" src="{{docs_base_url}}/assets/img/articles/po-stock-uom-ledger.png">

### Configurar Factor de Conversión de un Producto

En el Producto, dentro de la sección Compra, se pueden ennumerar todas las UOM de compra posibles para un producto, junto con su respectivo Factor de Conversión UOM. 

<img alt="Purchase UoM master" class="screenshot" src="{{docs_base_url}}/assets/img/articles/item-purchase-uom-conversion.png">

<!-- markdown -->
