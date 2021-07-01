<!-- add-breadcrumbs -->
# Tareas

**En la administración de proyectos, una tarea es una unidad de acción o actividad que debe ser completada.**

<img class="screenshot" alt="Task" src="{{docs_base_url}}/assets/img/project/projects-task.png">

Para acceder a Tareas ir a:

> Inicio > Proyectos > Proyectos > Tarea

## 1. Creación de una Tarea

  1. Ir al listado de Tarea y hacer click en Nueva.
  2. Añadir el asunto de la Tarea.
  3. Guardar.
  
  <img class="screenshot" alt="Task" src="{{docs_base_url}}/assets/img/project/projects-task-creation-main.gif">

De forma alternativa, también puede crearse una tarea desde un Proyecto de la siguiente forma: 

  1. Ir al Proyecto para el cual se desea crear la tarea. 
  2. Ir a Tarea en la sección Proyecto del Tablero. El signo más '+' que se encuentra allí redirige a la página de creación de tareas.  
  3. Añadir el asunto de la tarea.
  4. Guardar.
  
  <img class="screenshot" alt="Task" src="{{docs_base_url}}/assets/img/project/projects-task-creation.gif">

### 1.1 Opciones adicionales al crear una Tarea

Al editar una nueva tarea, pueden añadirse los siguientes detalles:

  * **Estado**: Se puede añadir el estado del Proyecto o cambiarlo cuando sea necesario, por ejemplo de "Abierto" a "Trabajando", "Atrasado", "Pendiente de Revisión", "Completado", o "Cancelado".
  * **Proyecto**: En caso de que una tarea sea agregada de forma independiente, se puede elegir vincular la tarea a un Proyecto en particular. Si la tarea es creada desde un Proyecto, los detalles del Proyecto serán añadidos de forma automática. 
  * **Prioridad**: Se puede elegir definir la prioridad de la tarea, entre Baja, Media, Alta o Urgente. 
  * **Incidencia**: Si la tarea es una acción que deviene de una Incidencia, la misma puede ser etiquetada aquí. 
  * **Peso**: Si una tarea en particular posee determinado peso dentro de un proyecto, o no, el peso puede especificarse aquí. El peso se calcula en el Método de Porcentaje de Completitud de Tareas de acuerdo con el Peso de las Tareas.
  * **Tipo**: Si la tarea puede ser definida bajo algún Tipo de Tareas en particular como Entrenamiento de Usuario, o Demostración de Usuario, se puede ingresar el Tipo de Tarea aquí. Se puede utilizar para filtrar las tareas de acuerdo con Tipos de Tareas. 
  * **Color**: Cada tarea puede ser reconocida por un color diferente. Esto ayuda a identificar una tarea al crear los Gráficos de Gantt. 
  * **Es Grupo**: Esta opción puede ser seleccionada para indicar que una tarea es principal, y que puede ser dividida posteriormente en muchas sub tareas.
  * **Es Plantilla**: Se puede tildar esta opción para indicar que la tarea es una plantilla y que debe ser utilizada en una Plantilla de proyecto.
  * **Tarea Padre**: Si una tarea en particular es parte de un grupo de tareas, la tarea principal puede ser vinculada a la tarea desde este campo.
  
  <img class="screenshot" alt="Task" src="{{docs_base_url}}/assets/img/project/timesheet/project-task.png">

## 2. Características

### 2.1. Cronograma y detalles

* **Fecha prevista de inicio**: Se puede ingresar aquí la fecha en la cuál se espera iniciar la Tarea.
* **Fecha prevista de finalización**: Se puede ingresar aquí la fecha en la cuál se espera finalizar la Tarea.
* **Tiempo previsto**: Se puede ingresar el número de horas que se espera invertir en esta tarea.
* **% Progreso**: Se puede ingresar el Porcentaje de Progreso de una Tarea.
* **Es una meta**: Esta casilla de verificación puede seleccionarse en caso de que una tarea en particular sea una Meta en un Proyecto. 
* **Descripción de la tarea**: Se puede añadir una descripción de la tarea aquí.

  <img class="screenshot" alt="Task" src="{{docs_base_url}}/assets/img/project/projects-task-timeline.png">

### 2.2. Dependencias y Tiempo Real

* **Tareas Dependientes**: Tareas Dependientes indica que una tarea en particualar depende de otra tarea, y que la primera no puede completarse sino se completa la otra. 

  La dependencia de Tareas puede verse en el Gráfico de Gantt de la siguiente forma.

  <img class="screenshot" alt="Task" src="{{docs_base_url}}/assets/img/project/projects-task-gantt.png">

* **Fecha de inicio real**: La fecha y hora real en la cual se inicia la Tarea se registra de acuerdo con el [Registro de horas](/docs/user/manual/es/projects/timesheets/).
* **Fecha de finalización real**: La fecha y hora real en la cual se finaliza la tarea se registra aquí a través del Registro de horas.

  <img class="screenshot" alt="Task" src="{{docs_base_url}}/assets/img/project/projects-task-dependencies.png">

### 2.3. Presupuesto

* **Monto Total de Costos**: El Monto Total de Costos se obtiene de los Registros de horas validados por el usuario mientras se trabajaba en esta tarea.
* **Monto Total de Facturación**: El Monto Total que se facturará al [Cliente](/docs/user/manual/es/CRM/customer) por la realización de esta tarea se registra en este campo desde los Registros de horas. 
* **Total Reembolsos**: El Monto Total de Gastos Reclamado por un Empleado para la realización de esta Tarea se registra y refleja aquí. 

### 2.4. Más Información

* **Departamento**: Se puede ingresar el Departamento Principal para la tarea. Esto no se relaciona con el Departamento Principal de un Proyecto ya que cada tarea es llevada a cabo por un departamento distinto.
* **Compañía**: Se puede cambiar la Compañía para la cual se está realizando la Tarea. Esto puede utilizarse en casos donde una compañía realiza una Tarea para una Empresa Relacionada o para su Empresa Principal o para una Filial. 

  <img class="screenshot" alt="Task" src="{{docs_base_url}}/assets/img/project/projects-task-costing.png">

## 3. Temas Relacionados

  1. [Proyecto](/docs/user/manual/es/projects/project)
  2. [Registros de horas](/docs/user/manual/es/projects/timesheets)

{next}
