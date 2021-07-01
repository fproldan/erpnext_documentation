# Lista de picking (picking list)

**Una Lista de picking es un documento que indica qué productos deben ser quitados del inventario para completar Ordenes.**

Esto resulta especialmente útil para empresas con grandes cantidades de inventario, volúmenes de orden o clientes comprando muchas unidades de mantenimiento de existencias (SKU).
La Lista de picking establece el Almacén donde un Producto está disponible en términos FIFO (primero que ingresa, primero que sale).
La Selección del Almacén para un producto en lote es diferente. En el caso de productos en lote, se selecciona el Almacén en el cual el lote está más cerca de la fecha de vencimiento. 

Para acceder al listado de Lista de picking ir a:

> Inicio > Almacén > Transacciones de Inventario > Lista de picking

## 1. Prerrequisitos

Antes de crear y utilizar una Lista de picking se recomienda crear lo siguiente: 

- [Producto](/docs/user/manual/es/stock/item)
- [Almacén](/docs/user/manual/es/stock/warehouse)

## 2. Creación de una Lista de picking

1. Ir al listado de Lista de picking y hacer click en Nuevo.
 <img class='screenshot' alt='Unsaved Pick List' src='{{docs_base_url}}/assets/img/stock/pick-list-unsaved-doc.png'>

1. Configurar la Compañía
1. Seleccionar el Propósito de la Lista de picking. Las opciones son las siguientes:  

   - **Entrega:** Esta opción permitirá añadir Productos desde una Orden de Venta para enviar. Luego de validar la Lista de picking, puede crearse una nueva Nota de Entrega desde el Almacén del cual se seleccionaron los productos. 

   - **Transferencia de Material para Fabricación:** Esto permitirá seleccionar una Orden de Trabajo desde la cual se presentarán las materias primas para elegir. Se puede seleccionar el número de productos finales para los cuales se eligen las materias primas. Luego de elegir las cantidades se puede crear una Entrada de Inventario para los productos seleccionados, es decir, materias primas.

   - **Transferencia de Material:** Esto permitirá seleccionar una Solicitud de Materiales para el cual se desea elegir productos. Luego de realizada la selección, se puede crear una Entrada de Inventario para los productos elegidos. 

1. Añadir el Producto y la cantidad que se quiere seleccionar en la tabla de Ubicaciones de Productos. Hacer click en **Obtener ubicaciones de productos** para obtener el Almacén y otros detalles para cada Producto. 

1. **Almacén principal:** Si se selecciona un Almacén principal, solo los Almacenes que se encuentran dentro del mismo serán sugeridos. 

1. **Obtener ubicaciones de productos:** Una vez que se eligieron los productos, se puede hacer click en el botón **Obtener ubicaciones de productos** para poder seleccionar el Almacén para cada producto. Como el Almacén será obtenido de forma automática si se elige un Producto desde cualquier documento de referencia, este botón puede resultar útil para añadir manualmente Productos adicionales o cambiar la cantidad de productos Existentes en la tabla de Ubicaciones de Productos.  

1. **Ubicaciones de Productos:** Este campo tendrá toda la información respecto a la ubicación del producto (Almacén), Número de serie para productos seriados y Número de lote para productos en lote. 
 <img class='screenshot' alt='Item Locations' src='{{docs_base_url}}/assets/img/stock/pick-list-item-locations.png'>

 Si los productos poseen Números de Serie, la fila de Productos se verá de la siguiente forma:
 <img class='screenshot' alt='Item Location Detail' src='{{docs_base_url}}/assets/img/stock/pick-list-item-location-detail.png'>

7. Guardar y Validar.
 <img class='screenshot' alt='Submitted Pick List' src='{{docs_base_url}}/assets/img/stock/pick-list-submitted-doc.png'>

### 2.1 Creación de una Lista de picking desde Orden de Venta

1. Ir a una [Orden de Venta](/docs/user/manual/es/selling/sales-order).
1. Hacer click en el botón **Crear** en la parte superior derecha del formulario y luego hacer click en la opción **Lista de picking**.
1. Una vez que se elige Lista de picking, toda la información requerida será obtenida desde la Orden de Venta. 
1. Se debería poder ver la Tabla de Ubicación de Productos con los Almacenes seleccionados para cada Producto. 
1. Guardar este documento, el cual podrá ser utilizado para seleccionar existencias por la persona que realiza esta actividad. 
1. Validar el documento una vez que se finalizó la selección de productos y que las cantidades seleccionadas de producto fueron actualizadas en el documento. 

**Consejo:** Se puede crear una Lista de picking para muchas Ordenes de Venta del mismo Cliente. Hacer click en Obtener Productos y seleccionar la Orden de Venta. 

> **Observaciones:**
>
> - La Lista de picking solo puede ser creada para Ordenes de Venta que tienen Productos pendientes de envío.
> - Una **Nota de Entrega** puede ser creada solo si la Lista de picking es validada.

### 2.2 Creación de una Lista de picking desde Orden de Trabajo

1. Ir a una [Orden de Trabajo](/docs/user/manual/es/manufacturing/work-order).
1. Hacer click en el botón **Crear lista de picking**.
1. Se verá el cuadro de diálogo pidiendo la cantidad de Productos Finales. Este es un campo requerido para calcular la cantidad de materias primas necesarias para fabricar la cantidad ingresada de Productos Finales. 
<img class='screenshot' alt='Dialog For qty' src='{{docs_base_url}}/assets/img/stock/pick-list-dialog-for-qty.png'>

4. Se debería poder ver la tabla de Ubicación de Productos con el Almacén seleccionado para cada materia prima. 
1. Guadar este documento el cual luego podrá ser remitido a la persona que seleccionará los productos. 
1. Validar el documento una vez que se terminó de seleccionar los productos y el producto seleccionado se haya actualizado correctamente en el documento. 

> **Observaciones:**
>
> - La Lista de picking solo puede ser creada para Ordenes de Trabajo que se encuentran en el estado de "No Iniciadas" o "En Curso".
> - Una **Entrada de Inventario** puede crearse solo luego de que la Lista de picking sea validada. 

### 2.3 Creación de una Lista de picking desde Solicitud de Material

1. Ir a [Solicitud de Material](/docs/user/manual/es/stock/material-request).
1. Hacer click en el botón **Crear** y luego click en la opción **Lista de picking**.
1. Se debería poder ver la tabla de Ubicación de Productos con el Almacén seleccionado para cada producto en la Solicitud de Material.
1. Guadar este documento el cual luego podrá ser remitido a la persona que seleccionará los productos. 
1. Validar el documento una vez que se terminó de seleccionar los productos y el producto seleccionado se haya actualizado correctamente en el documento.

> **Observaciones:**
>
> - Solo las Solicitudes de Material de tipo "Transferencia de Material" pueden ser utilizadas para crear Listas de picking. 
> - Una **Entrada de Inventario** de tipo "Transferencia de Material" puede ser creada luego de que la Lista de picking haya sido validada. 

## 3. Características

### 3.1. Actualizar stock actual

Si una Lista de picking está desactualizada, puede haber un cambio en la disponibilidad de existencias para el momento en que se crea una Nota de Entrega o Entrada de Inventario desde la misma. Hacer click en **Actualizar stock actual**, actualizará las cantidades y almacenes en la tabla de Ubicaciones de Productos.

> **Observaciones:** Este botón es visible siempre y cuando no haya Notas de Entrega o Entradas de Inventario creados desde esa Lista de picking. 

## 4. Temas Relacionados

1. [Orden de Venta](/docs/user/manual/es/selling/sales-order)
1. [Orden de Trabajo](/docs/user/manual/es/manufacturing/work-order)
1. [Solicitud de Material](/docs/user/manual/es/stock/material-request)
