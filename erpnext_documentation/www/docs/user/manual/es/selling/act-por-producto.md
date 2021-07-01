# Actualización de Precios por Producto

La actualización de precios por producto es una utilidad que permite generar masivamente nuevos Precios de los Productos seleccionados en todas las listas de precios donde aparezcan en base a un porcentaje deseado, el cual se aplicará a los últimos precios vigentes.

### Creación de una Actualización de Precio por Producto

1. Ir a *Inicio > Ventas > Actualización de Precios > Actualizacion de Precio por Producto* y hacer click en Nuevo.
2. Ingresar el porcentaje por el cual se desea actualizar los precios. El valor del mismo debe ir sin el símbolo de porcentaje (%).
3. Se puede elegir si los precios van a ser redondeados tras la modificación tildando la opción "Redondear precios". También se puede elegir con qué fecha "Válido desde" se van a crear los precios.
4. Seleccionar los productos cuyos precios se desea actualizar. Como es posible que se desee actualizar una gran cantidad de productos existen las siguientes opciones:
    * **Obtener desde**: se pueden traer los productos con determinada Categoría, Marca, Almacén o Proveedor.
    * **Añadir Multiple**: este botón se encuentra en la esquina inferior izquierda de la tabla de productos y permite seleccionar productos de una manera más rápida mediante una ventana emergente.
    * **Descargar/Subir**: estos dos botones se encuentran en la esquina inferior derecha de la tabla de productos y permiten descargar y cargar datos en formato CSV. Recordar que los datos a cargar deben tener un orden especifico, por lo que, para realizarlo, primero se deberá descargar el CSV plantilla con el botón Descargar (preferiblemente teniendo la tabla vacía).
    * **Vaciar tabla**: este botón se encuentra al lado del de **Obtener desde** y, si bien no es para cargar datos, sí lo es para corregir errores. Lo que hace es vaciar la tabla de productos rápidamente (especialmente pensado para casos con una cantidad elevada de productos).
6. Después de comprobar que todos los datos sean correctos, se debe Guardar y Validar.

Como la actualización se ejecuta mediante una tarea, el proceso puede tardar un tiempo, por lo que al validarse el documento posee el Estado: Procesando.

Una vez que la tarea finaliza, pasa a Estado: Procesado. Los Precios de producto generados poseen un enlace al documento que los generó, por lo que se puede filtrar el listado de precios por cada Actualización.

Si hubo algún problema el estado se muestra como Error y el detalle del mismo aparece como un comentario dentro del documento. En el caso de que ocurra un error, no se genera ningún precio, de forma que al solucionar el problema que ocasionaba el error se puede volver a intentar la actualización de todos los precios.

### Revertir actualización

Si se desea revertir una actualización de lista de precios es posible hacerlo cancelando el documento validado. Así, todos los precios generados por el mismo serán borrados del sistema.
