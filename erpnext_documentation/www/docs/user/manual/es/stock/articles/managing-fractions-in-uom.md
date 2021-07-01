<!-- add-breadcrumbs -->
# Administrar Fracciones en UOM

UOM significa Unidad de Medida. Algunos ejemplos de UOM son Números o Unidades, Kilos, Litros, Metros, Caja, Cartón, etc. 

Hay pocas UOM que no pueden tener valores decimales. Por ejemplo, si se tiene televisores como productos, con números como UOM, no se puede tener 1.5 númereos de televisión, o 3,7 números de equipos de computación. El valor de cantidad para estos productos tiene que ser un número entero.

Se puede configurar si una UOM particular puede tener valor en decimales o no. De forma predeterminada, los valores decimales se permitirán para todas las UOM. Para restringir el uso de decimales o de valores en fracción para cualquier UOM se deben seguir los siguientes pasos. 

#### Listado de UOM

Para acceder al listado de UOM ir a:

> Almacén > Configuración > Unidad de Medida

Del listado de UOM seleccionar aquella a la que se le restringirá el uso de decimales. Para el siguiente ejemplo se eligió Números. 

#### Configurar

En la función UOM, se encontrará un campo llamado "Debe ser un número entero". Tildar esta opción para restringir al usuario el uso de decimales en el campo cantidad para el producto que utilice esta UOM. 

<img alt="UoM Must be Whole No" class="screenshot" src="{{docs_base_url}}/assets/img/articles/uom-fraction-1.png">

#### Validación

Al crear la transacción, si se ingresa un valor en fracción para aquellos productos cuya UOM tiene el campo "Debe ser un número entero" seleccionado, se mostrará un mensaje de error como el siguiente:

`La cantidad no puede ser una fracción #`

<img alt="UoM Validation Message" class="screenshot" src="{{docs_base_url}}/assets/img/articles/uom-fraction-2.png">


<!-- markdown -->
