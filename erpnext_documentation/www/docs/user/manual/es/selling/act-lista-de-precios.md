# Actualización de Lista de Precios

La actualización de precios por lista de precios es una utilidad que permite generar nuevos Precios de productos de las listas seleccionadas en base a un porcentaje deseado, el cual se aplicará a los precios existentes.


## Creación de una Actualización de Lista de Precio

1. Ir a *Inicio > Ventas > Actualización de Precios > Actualizacion de Lista de Precio* y hacer click en Nuevo.
2. Ingresar el porcentaje por el cual se desea actualizar los precios. El valor del mismo debe ir sin el símbolo de porcentaje (%).
3. Se puede elegir si los precios van a ser redondeados tras la modificación tildando la opción "Redondear precios".
4. Seleccionar las listas de precios que se desea actualizar. Para esto existen botones que permiten traer las lista de precios de ventas, las de compras o todas las habilitadas en el sistema.
5. Después de comprobar que todos los datos sean correctos, se debe Guardar y Validar.

Como la actualización se ejecuta mediante una tarea, el proceso puede tardar un tiempo, por lo que al validarse el documento posee el Estado: Procesando.

Una vez que la tarea finaliza, pasa a Estado: Procesado. Los Precios de producto generados poseen un enlace al documento que los generó, por lo que se puede filtrar el listado de precios por cada actualización.

Si hubo algún problema el estado se muestra como Error y el detalle del mismo aparece como un comentario dentro del documento. En el caso de que ocurra un error, no se genera ningún precio, de forma que al solucionar el problema que ocasionaba el error se puede volver a intentar la actualización de todos los precios.

## Revertir actualización

Si se desea revertir una actualización de lista de precios es posible hacerlo cancelando el documento validado. Así, todos los precios generados por el mismo serán borrados del sistema.
