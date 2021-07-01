<!-- add-breadcrumbs -->
# Tareas


**En ERPNext, una lista de Tareas es una herramienta simple donde se pueden definir actividades a realizar. La Lista de Tareas enumerará todas las actividades asignadas a una persona, ya sea por otras o por ella misma.**

![ToDo](/docs/assets/img/using-erpnext/using-to-do-1.png)

Una lista de Tareas también se crea automáticamente cuando se asigna un Documento a una persona. Ver [Creación Automática de Tareas](/docs/user/manual/es/using-erpnext/articles/todo-auto-creation)

Para acceder a Tareas ir a

> Inicio > Herramientas > Tareas

## 1. Creación de una Lista de Tareas

1. Ir al listado de Tareas y hacer click en nuevo.
2. Eso llevará a una Entrada Rápida para Tareas, donde se requerirá ingresar la descripción de las Tareas.
3. Guardar.

 ![ToDo](/docs/assets/img/using-erpnext/using-to-do-2.gif)

> Observación: Al crear una lista de Tareas utilizando una Entrada Rápida, la misma se asignará de forma predeterminada al usuario creador. Para evitar esto, y asignarla a otros usuarios, es necesario editar la Lista de Tareas en la Página Completa. 

### Notificación de Tareas

Al crear una lista de Tareas, el usuario al cual la misma ha sido asignada será notificado. 

![ToDo](/docs/assets/img/using-erpnext/using-todo-notification.png)

### 1.1. Opciones adicionales al crear Tareas

1. **Estado**: Se puede definir el estado de las Tareas. Al crearla, el estado predeterminado será "Abierta". El usuario puede cambiarla a "Cerrada" cuando las tareas se hayan completado. 
2. **Prioridad**: Se puede definir la Prioridad de esta tarea como Baja, Media o Alta. 
3. **Color**: Se puede asignar un color a cada una de las Tareas. Por ejemplo, al crear una Tarea como recordatorio semanal para enviar informes, se le puede asignar el color Violeta, mientras que a todas las Tareas personales se les puede asignar el color Amarillo. 
4. **Fecha de Vencimiento**: Se puede ingresar una Fecha de Vencimiento a todas las Tareas. 
5. **Asignado a**: Se puede usar este campo en los casos en que se asignen Tareas a otros usuarios de ERPNext.

 ![ToDo](/docs/assets/img/using-erpnext/using-to-do-3.png)

### 1.2. Referencias

Cada Documento en ERPNext tiene una opción denominada "Asignar A" en la barra lateral. Al utilizar esta opción, cualquier Documento puede ser asignado a un usuario. En este caso se le asignarán al usuario Tareas de forma simultánea. 

1. **Tipo de Referencia**: Cuando una lista de Tareas es creada desde otro documento, como una Tarea o un Asunto, el Tipo de Documento de Referencia se vincula aquí a la lista de Tareas. También se puede elegir ingresar un Tipo de Documento de Referencia de forma manual. 
2. **Nombre de Referencia**: Al ser asignado a través de otro DocType, el nombre del DocType de Referencia también se vincula aquí. 
3. **Asignación Por**: Al ser asignado una Lista de Tareas a través de otro Tipo de Documento, la persona que realiza la asignación también es etiquetada. 

 ![ToDo](/docs/assets/img/using-erpnext/using-to-do-4.png)

## 2. Estados de Tareas
Las Tareas tienen 3 estados, cada uno describe el estado actual de una tarea.

* **Abierta**: Una lista de Tareas, al ser creada, es configurada de forma predeterminada como Abierta.
* **Cerrada**: Cuando se completa una actividad, la lista de Tareas puede ser marcada como "Cerrada", "Resuelta" o "Completa". A su vez, en condiciones como Asunto Resuelto o Tarea Completa, la lista de Tareas es cerrada de forma automática. También puede ser Reabierta de ser necesario.  
* **Cancelada**: Cuando se elimina la asignación de un usuario a una lista de Tareas/Tarea/Asunto, la lista de Tareas vinculada a ese documento es "Cancelada" automáticamente.

 ![ToDo](/docs/assets/img/using-erpnext/using-to-do-5.png)


{siguiente}
