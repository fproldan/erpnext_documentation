<!-- add-breadcrumbs -->
# Actualización masiva

**La Actualización masiva permite actualizar un campo en particular de un DocType para todos los documentos.**

Para acceder a Actualización masiva ir a:
> Inicio > Configuración > Datos > Actualización masiva

Considérese un caso en que se cuenta con 20 cotizaciones en las cuales se ha seleccionado "Todos los Territorios" y ahora se quiere cambiar el territorio a un país específico. En vez de actualizar las cotizaciones individuales de forma manual, se puede utilizar la Actualización masiva para actualizar las 20 Cotizaciones a la vez.  

Para hacer esto:
1. Ir a Actualización masiva.
1. Seleccionar el Tipo de Documento, como Cotización.
1. Seleccionar el campo a actualizar, como territorio.
1. Ingresar un nuevo valor **válido** para que sea actualizado.
1. Ingresar cualquier condición aplicable, por ejemplo, estado="Borrador" solo afectará a documentos en estado Borrador.
1. Seleccionar el límite, es decir, el número de documentos (Cotizaciones) a actualizar.
1. Hacer click en Actualizar.

    ![Bulk Update](/docs/assets/img/setup/bulk-update.png)

> Observación: Sólo se pueden actualizar campos que puedan ser actualizados normalmente en una etapa en particular. Por ejemplo, la fecha de validez hasta, no puede ser actualizada para Cotizaciones validadas. 

### Temas Relacionados
1. [Renombrar en Grupo](/docs/user/manual/es/setting-up/settings/bulk-rename)
