<!-- add-breadcrumbs -->
# Proyecto

**Un Proyecto es un trabajo planeado que ha sido diseñado para obtener información respecto a algo, para producir algo nuevo o para mejorar algo.**

En ERPNext, un Proyecto tiene un amplio alcance y por ende puede ser dividido en tareas. Cuestiones como diseñar, generar prototipos, probar, enviar, etc, se convierten en tareas del proyecto. 

Mientras cada tarea dentro de un Proyecto puede ser asignada a un individuo o a un grupo de individuos, la asignación también puede hacerse a un nivel de proyecto. 

Estas Tareas pueden crearse desde un Proyecto en sí o también una [Tarea](/docs/user/manual/en/projects/tasks.html) puede crearse de forma separada.

Para acceder a Proyectos ir a:

> Inicio > Proyectos > Proyectos > Proyecto

<img class="screenshot" alt="Project" src="{{docs_base_url}}//assets/img/project/projects-project-intro.png">

## 1. Creación de un Proyecto

  1. Ir al listado de Proyecto y hacer click en Nuevo.
  2. Añadir los siguientes detalles:
      * **Nombre del Proyecto**: Título del Proyecto.
      * **Estado**: El estado predeterminado de un Proyecto será "Abierto", el cual luego puede cambiarse a "Completado" o "Cancelado".
      * **Fecha prevista de finalización**: Ingresar la fecha en la cual se planea terminar el proyecto.
  3. Guardar.

### 1.1 Opciones Adicionales al crear un Proyecto

  1. **Desde Plantilla**: Si se cuenta con una [Plantilla de Proyecto](/docs/user/manual/es/projects/project-template), se puede elegir crear el proyecto utilizandola. 
  2. **Fecha prevista de inicio**: Si se posee una línea temporal fijada para el proyecto, se pueden definir tanto la "Fecha prevista de inicio" y la "Fecha prevista de finalización" en el formulario.
  3. **Tipo de Proyecto**: Se pueden clasificar los proyectos en diferentes [tipos](/docs/user/manual/es/projects/project-type), por ejemplo, Internos o Externos. 
  4. **Prioridad**: Se puede seleccionar el nivel de prioridad del Proyecto de acuerdo a qué tan crucial sea. También se pueden añadir más niveles de prioridad. 
  5. **Departamento**: Si el proyecto proviene de o pertenece a un [Departamento](/docs/user/manual/en/human-resources/department) de la compañía, se puede indicar en este campo.
  6. **Está Activo**: se puede cambiar el valor de Si/No en etapas posteriores. 
  7. **% Método completado**: Se puede rastrear el % de finalización del proyecto en base a uno de estos tres métodos **Manual, Finalización de Tareas, Progreso de Tareas y Peso de Tareas**. 
  
  <img class="screenshot" alt="Project 2" src="{{docs_base_url}}/assets/img/project/project-proj.png">

 Algunos ejemplos de cómo se calcula el Porcentaje de Finalización en base a Tareas: 

  | Proyecto     | Actividad    | % Progreso     | Peso     | Estado      |
  |:-----------:|:------------:|:--------------:|:----------:|:----------:|
  | SC001       | Construir    | 100            | 0.4        | Completa   |
  | SC001       | Operar       | 100            | 0.2        | Completa   |
  | SC001       | Transferir   | 50             | 0.2        | Abierta    |

  | Método              | Fórmula                                            | Cálculo                   | % Finalización de Tareas     |
  |:-------------------:|:--------------------------------------------------:|:----------------------------------:|:--------------------:|
  | **Manual**          | -                                                  |-                                    | Manual              |
  | **Finalización de Tareas** | Tareas Finalizadas / Número Total de Tareas  | 2/3                                 | 66.66               |
  | **Progreso de Tareas** | Suma % Progreso de las Tareas / N° Total de Tareas| (100+100+50)/3                | 83.33               |
  | **Peso de Tareas** | Suma de (Peso de Tareas * % Progreso)           | (0.4 * 100 + 0.2 * 100 + 0.2 * 50)| 70                   |


**Observación:** Si el peso total de las Tareas no es 100, entonces el resultado calculado se dividirá por el peso total.
Por ejemplo, si el peso total de las tareas es 70, entonces el porcentaje de finalización será = (70/0.8)% = 87.5%.


## 2. Características

### 2.1. Detalles del Cliente, Usuarios y Observaciones

* **Cliente**: Si un Proyecto está siendo llevado a cabo para un Cliente en particular, los detalles pueden ser ingresados aquí. 
* **Orden de Venta**: Si un Proyecto está basado en una [Orden de Venta](/docs/user/manual/es/selling/sales-order) de un Cliente, se pueden obtener los detalles aquí. Esto permitirá actualizar al Cliente respecto al Progreso del proyecto de acuerdo con la Orden de Venta emitida. 
* **Usuarios**: Se pueden añadir [usuarios del sitio web](/docs/user/manual/es/setting-up/users-and-permissions/adding-users) para darles acceso a este Proyecto. Por ejemplo, se puede añadir al cliente como Usuario del Sitio Web para permitirle acceder al proyecto a fin de monitorear el progreso y/o realizar aportes/comentarios. De forma similar, un Proveedor o un Empleado por Contrato/Freelancer que esté involucrado en el proyecto, puede ser añadido como usuario.  

  Además, se puede expandir la ventana y seleccionar si se desea enviar un Correo Electrónico de Bienvenida a algún usuario en particular o darles derechos para Visualizar Adjuntos. 

  Se puede aprender más respecto a permitir a usuarios ver proyectos [aquí](/docs/user/manual/es/projects/project-customer-portal).

* **Notas**: Se pueden añadir observaciones adicionales al proyecto. 

  <img class="screenshot" alt="Project - Costing" src="{{docs_base_url}}/assets/img/project/projects-customer-users-notes.png">

### 2.2. Fechas de Inicio y Finalización

* **Fecha de inicio real**: Marca el Inicio Real del proyecto, rastreado a través de Registro de Horas, la Fecha y Hora Real de Inicio del Proyecto serán registradas de forma automática.  
* **Fecha de finalización real**: Marca la Finalización Real del proyecto, rastreada a través de las últimas actualizaciones de los Registro de Horas, la Fecha y Hora Reales de Finalización del proyecto serán registradas de forma automática. Para saber más respecto a Registro de Horas hacer click [aquí](/docs/user/manual/es/projects/timesheets/).

  <img class="screenshot" alt="Project - Costing" src="{{docs_base_url}}/assets/img/project/projects-start-time-end-time.png">

### 2.3. Cálculo de Costos y Facturación

* **Costo Estimado**: Ingresar el Costo Estimado del Proyecto.
* **Monto Total de Ventas**: Si ya se ha vinculado el Proyecto con una Orden de Venta, el Monto Total de la Orden de Venta será completado automáticamente aquí. 
* **Monto Total de Costos**: El sistema tomará automáticamente el Monto Total de Costos desde todos los Registro de Horas vinculados a este proyecto. 
* **Monto Total Facturable**: El sistema tomará automáticamente el Monto Total Facturable desde todos los Registro de Horas vinculados a este proyecto. 
* **Total Reembolso**: De acuerdo con los gastos reclamados por un [Empleado](/docs/user/manual/es/human-resources/employee) para la finalización de un Proyecto, se calculará automáticamente el Total de Reembolso.
* **Monto Total Facturado**: El Monto Total Facturado se completa de forma automática en el sistema utilizando la Factura de Venta creada desde la Orden de Venta. 
* **Costo Total de Compra**: El Costo Total de Compra de un Proyecto es el costo tomado desde las Facturas de Compra, que se crean desde Órdenes de Compra enviadas para la provisión de Materiales requeridos para un Proyecto. 
* **Costo Total del Material Consumido**: Utilizando las Entradas de inventario realizadas de acuerdo con el requerimiento de Materiales en el proyecto, se captura el Costo Total de Material Consumido.


### 2.4. Margen

* **Margen Bruto**: El Margen Bruto será el margen existente entre el Monto Total de Costo y el Monto Total Facturado.

  **Margen Bruto = (Monto Total de Ventas + Monto Total Facturable) - Monto Total de Costos + Monto Total Facturable + Total de Gastos Reclamados + Costos Totales de Compra + Costo Total de Material Consumido)**

* **Margen Bruto %**: El porcentaje del Monto Total Facturado gastado en el Monto Total de Costo resulta en el % Bruto.

  **((Monto Total de Ventas + Monto Total Facturable) - Monto Total de Costos + Monto Total Facturable + Total de Gastos Reclamados + Costos Totales de Compra + Costo Total de Material Consumido) / Monto Total de Ventas)* 100**

  <img class="screenshot" alt="Project - Costing" src="{{docs_base_url}}/assets/img/project/projects-costing-and-billing.png">

### 2.5. Monitorear el Progreso

Al habilitar la opción "Rastrear Progreso" haciendo click en la casilla de verificación, se permitirá añadir detalles de monitoreo al proyecto. Se enviará un informe respecto del progreso del proyecto a todos sectores involucrados en el proyecto.

* **Lista de festividades**: Se puede seleccionar la [Lista de festividades](/docs/user/manual/es/human-resources/holiday-list) para la compañía. Esto permitirá obtener los Informes de Progreso solo en los Días Laborales. 
* **Frecuencia**: Se puede configurar la frecuencia con la cuál se desea obtener los informes. Puede ser configurado por hora, dos veces al día o de forma semanal. 

  <img class="screenshot" alt="Project - Costing" src="{{docs_base_url}}/assets/img/project/projects-monitor-progress.png">

## 3. Temas Relacionados
  1. [Tarea](/docs/user/manual/es/projects/tasks)
  2. [Tipo de Proyecto](/docs/user/manual/es/projects/project-type)
  3. [Plantilla de Proyecto](/docs/user/manual/es/projects/project-template)
