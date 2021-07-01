<!-- add-breadcrumbs -->
# Creación Automática de Tareas

Cada Documento en ERPNext tiene una opción denominada 'Asignar A' en la barra lateral. Al utilizar esta opción, cualquier Documento puede ser asignado a un usuario. Automáticamente se le asignará a ese usuario una Tarea. 

![ToDo Auto Creation](/docs/assets/img/using-erpnext/using-todo-auto-assign-1.gif)

Bajo esas condiciones, los tres estados de Tareas se definen de acuerdo con las actualizaciones en la asignación. 

Consideremos una situación en la cuál se asigna una Tarea a través de un Asunto. Digamos que hay dos niveles de Asistencia en la empresa: L1 y L2 y cada nuevo ticket de asistencia es considerado perteneciente al L1 y por ende se asigna a miembros relevantes del equipo. En este caso, los estados de Tareas variarían de la siguiente forma:  

1. **Abierto**: Cuando se crea un asunto y se asigna a un miembro del equipo de asistencia L1.
2. **Cerrado**: El miembro del equipo L1 identifica el asunto y lo resuelve. 
3. **Cancelado**: El miembro del equipo L1 identifica el asunto como una situación a ser tratada por el nivel de asistencia L2 y se lo asigna a un miembro relevante de ese equipo. 

## Reabrir Asignaciones Cerradas

En el mismo caso que el anterior, digamos que el ticket de asistencia fue marcado como cerrado por un miembro del equipo L1. Sin embargo, el Asunto es reabierto si el ticket es reabierto, o si hubo alguna actividad sobre este asunto.

De forma simultánea, las Tareas asociadas al Ticket de Asistencia también serán reabiertas.

![ToDo](/docs/assets/img/using-erpnext/using-to-do-6.png)
