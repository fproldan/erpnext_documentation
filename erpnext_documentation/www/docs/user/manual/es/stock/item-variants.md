<!-- add-breadcrumbs -->
# Variantes de Productos

**Una Variante de Producto es una versión de un Producto con diferentes atributos, como tamaños o colores.**

Considérese que el Producto es una remera y viene en diferentes tamaños (pequeño, medio, grande) y colores (rojo, azul, verde). En ERPNext la remera será considerada como una plantilla de Producto y cada una de las variaciones será una Variante de Producto. 

Así se va a vender una remera _azul_ en tamaño _pequeño_ y no sólo una remera. Las Variantes de Producto permiten tratar a las versiones _pequeña_, _mediana_, y _grande_ de una remera como variaciones del Producto: "remera".

Sin variantes de Productos, se debería tratar a las versiones _pequeña_, _mediana_ y _grande_ de una remera como tres Productos separados. 

## 1. Utilización de Variantes de Productos

Las Variantes pueden basarse en dos cosas:

1. Atributos de Producto
2. Fabricantes

> Observación: Una vez creada la plantilla de un producto, cada vez que se actualiza esta plantilla, se actualizan todas las variantes. 

### 1.1 Creación de la Plantilla de Variante de Producto 

1. Para utilizar Variantes de Producto en ERPNext se debe crear un Producto y tildar la opción "Posee Variantes" en la sección Variantes. 

2. El Producto entonces pasará a ser una "Plantilla". Dicha Plantilla ya no es idéntica a un "Producto" regular. Por ejemplo, la misma no puede ser usada de forma directa en ninguna transacción (Orden de Ventas, Nota de Entrega, Factura de Compra).
 
3. Solo las Variantes del Producto (remera _azul_ en talle _pequeño)_ pueden ser usadas de forma práctica. Por ende, sería ideal decidir si un Producto "Posee Variantes" o no, directamente al crearlo. 
    <img class="screenshot" alt="Has Variants" src="{{docs_base_url}}/assets/img/stock/item-has-variants.png">

4. Al seleccionar "Posee Variantes" aparecerá una tabla. En la misma es necesario especificar los atributos de las variantes para el Producto. En caso de que el atributo tenga Valores Numéricos, se puede especificar el rango y crear intervalos en base a los valores de crecimiento. 
    <img class="screenshot" alt="Valid Attributes" src="{{docs_base_url}}/assets/img/stock/item-attributes.png">
> Observación: No se puede realizar transacciones utilizando una "Plantilla".

### 1.2 Variantes de Producto de acuerdo con los Atributos del Producto

Para crear "Variantes de Producto" en relación a una "Plantilla" hacer click en "Crear". Desde ahí, elegir si se desea crear una única variante o muchas. Si se selecciona Variante individual, desde uno o más atributos sólo se creará un Producto. Al elegir Múltiples variantes, se seleccionarán los atributos y se crearán muchos Productos. Por ejemplo, si se elige Color: Rojo, Verde y Talle: Pequeño, Mediano, Grande, se crearán 6 variantes. 

Crear muchas variantes en ERPNext:

<img class="screenshot" alt="Make Variants" src="{{docs_base_url}}/assets/img/stock/make-multiple-variants.png">

Para aprender más respecto a cómo configurar atributos ir a [Atributos de Producto](/docs/user/manual/es/stock/item-attribute)

### 1.3 Variantes de Producto de acuerdo a Fabricantes 

Para configurar variantes de acuerdo a Fabricantes, seleccionar "Fabricante" en el campo "Variante basada en" de la plantilla de Producto. 
En este caso, para crear variantes, hacer click en Crear > Crear Variante. El sistema pedirá que se seleccione un Fabricante. También se puede incluir un Número de Pieza de Fabricante. 

<img class='screenshot' alt='Setup Item Variant by Manufacturer' src='{{docs_base_url}}/assets/img/stock/select-mfg-for-variant.png'>

El nombre de la variante se basará en el nombre (ID) del Producto que conforma la plantilla, sumando un sufijo numérico. Por ejemplo: "Destornillador" tendrá como variante "Destornillador-1". 

## 2. Actualizar las Variantes de Producto en base a la Plantilla
Ir a: **Inicio > Almacén > Productos y Precios > Configuraciones de Variantes de Producto**. Los campos mostrados aquí serán copiados también en las variantes. De forma predeterminada, se mostrarán todos los campos, borrar cualquier fila que no se quiera actualizar desde la plantilla del producto hacia las variantes. 

## 3. Temas Relacionados
1. [Grupos de Producto](/docs/user/manual/es/stock/item-group)
1. [Atributos de Productos](/docs/user/manual/es/stock/item-attribute)
1. [Precio de Producto](/docs/user/manual/es/stock/item-price)
1. [Codificación de Producto](/docs/user/manual/es/stock/articles/item-codification)
