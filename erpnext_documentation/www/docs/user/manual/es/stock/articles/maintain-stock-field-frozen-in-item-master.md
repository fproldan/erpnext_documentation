<!-- add-breadcrumbs -->
# Bloquear campo "Mantener Stock" en el Producto

En el producto, se podrá verificar que los siguientes campos estén bloqueados.

1. Mantener Stock
1. Posee Número de Lote
1. Posee Número de Serie

<img alt="Item Field Frozen" class="screenshot" src="{{docs_base_url}}/assets/img/articles/maintain-stock-1.png">

Para un producto, una vez que se creó una Entrada de inventario, los valores de estos campos serán congelados/bloqueados. Esto es así para prevenir que el usuario modifique el valor lo cual podría llevar a un desfasaje entre las existencias reales del producto, y el nivel de existencias en el sistema. 

Para el producto seriado, como el nivel de existencias se calcula de acuerdo a la cantidad de Números de Serie presentes, configurar este producto como no seriado a mitad de camino rompería la sincronización, y el nivel de existencias mostrado en el informe no sería exacto, por ende, el campo de Posee Número de Serie es congelado. 

Para que estos campos vuelvan a ser editables, se deben borrar todas las transacciones de existencias realizadas para este producto. Para el caso del Producto Seriado y en Lote también se debe borrar el registro de Número de Serie y Número de Lote para este producto. 

<!-- markdown -->
