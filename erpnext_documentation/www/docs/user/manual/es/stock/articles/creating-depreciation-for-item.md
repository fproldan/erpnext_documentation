<!-- add-breadcrumbs -->
# Crear Amortización para Producto

A continuación se detalla el paso a paso de la creación de la amortización para un Activo Fijo que fue comprado y almacenado en un almacén 
Esto se puede hacer a través de una entrada de [Conciliación de Inventario](/docs/user/manual/es/stock/opening-stock).

#### Paso 1:

Completar las columnas pertinentes en el archivo Adjunto: 

- **Código de Producto** que debe ser amortizado
- **Almacén** en el que está almacenado el producto.
- **Cantidad** Dejar columna en blanco
- **Valoración** el valor del producto después de la amortización. 

<img alt="reorder level" class="screenshot" src="{{docs_base_url}}/assets/img/articles/fixed-asset-dep-1.gif">

Luego de actualizar la valuación para un producto, volver a Conciliación de Inventarios y subir el archivo .csv. 

#### Paso 2:

Seleccionar la Cuenta de Gastos para la amortización en **Cuenta de Diferencias**. El valor registrado en la cuenta de amortización será la diferencia entre la vieja y la nueva valoración del activo fijo, la cual será el monto en que el bien se depreció. 

<img alt="reorder level" class="screenshot" src="{{docs_base_url}}/assets/img/articles/fixed-asset-dep-2.png">
