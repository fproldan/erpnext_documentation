<!-- add-breadcrumbs -->
# Registro de horas

**Un Registro de horas almacena el tiempo invertido por un empleado en completar cada tarea.**

El Registro de horas también puede utilizarse para calcular lo que se debe facturar por cada empleado, para calcular sus salarios o registrar la contribución de un empleado hacia un Proyecto o Tarea. 

En ERPNext, un Registro de horas puede tener una cuenta de un empleado en particular que se encuentre trabajando en muchas Tareas o Proyectos, en un formato tabular.

<img class="screenshot" alt="Timesheet" src="{{docs_base_url}}/assets/img/project/projects-timesheet.png">

Para acceder al Registro de horas ir a:

> Inicio > Proyectos > Seguimiento de Tiempo > Registro de horas

## 1. Creación de un Registro de horas

  1. Ir al listado de Registro de horas y hacer click en Nueva.
  2. Ingresar el nombre de la Compañía y el Código de Empleado.
  3. Añadir los siguientes detalles al campo "Registro de horas".
      * **Tipo de Actividad**: Añadir el tipo de actividad para el cual se ha credo el Registro de horas.
      * **Desde**: Ingresar la fecha y hora en la cual se inició el trabajo.
      * **Horas**: Ingresar el número de horas para las cuales se creó este Registro de horas. Un Registro de horas también puede ser utilizado para el trabajo de muchos días.
      * **Proyecto**: Si este mismo Registro de horas debe ser relacionado a un Proyecto en particular, se puede añadir el nombre del Proyecto aquí.
      * **Factura**: Esta casilla debe ser seleccionada si este Registro de horas en particular es facturable. 
  4. Hacer click en "Agregar Fila" para añadir más de estos registros.
  5. Guardar.
  6. Luego de guardar el Registro de horas de acuerdo con los detalles ingresados en los diferentes Registros de horas, la Fecha de Inicio, Fecha de Finalización y el Total de Horas Trabajadas se actualizarán automáticamente. Hacer click en Validar. 

### 1.1. De forma alternativa, un Registro de horas también puede crearse desde una Tarea de la siguiente forma:

  1. Ir a la Tarea para la cuál se desea crear el Registro de horas.
  2. Ir a "Registro de horas" dentro de la sección Actividad del tablero. El ícono más '+' que se encuentra aquí redirige a la página de creación de Registro de horas. 
  3. Seguir los pasos para crear un Registro de horas.

  <img class="screenshot" alt="Timesheet" src="{{docs_base_url}}/assets/img/project/projects-timesheet-from-task.gif">

### 1.2. Temporizador en Registro de horas

**Puede utilizarse un temporizador para registrar el tiempo real utilizado por un empleado para finalizar una actividad en particular en un Registro de horas.**

#### 1.2.1. Pasos para iniciar un Temporizador:

- En un Registro de horas, al hacer click en **Iniciar Temporizador** aparecerá un diálogo que solicitará que se ingresen los siguientes detalles:
    * **Tipo de Actividad**: La Actividad para la cual se registra el Tiempo.
    * **Proyecto**: El Proyecto para el cual se está creando el Registro de horas.
    * **Tarea**: La Tarea para la cual se está registrando el tiempo en el Registro de horas. 
    * **Horas Esperadas**: Ingresar el número de horas en que se espera terminar la Tarea.

<img class="screenshot" alt="Timer in Progress" src="{{docs_base_url}}/assets/img/project/projects-timer-in-timesheet.gif">

- Una vez que se haya completado la Tarea, hacer click en Completado. Se creará una nueva entrada en el Registro correspondiente y las horas serán almacenadas en la Tabla de Tiempo. 

- Si el tiempo excede las "Horas Esperadas", aparecerá un mensaje de alerta.

<img class="screenshot" alt="Timer Exceeded" src="{{docs_base_url}}/assets/img/project/projects-timer-time-exceed.png">


### 1.3. Opciones Adicionales al crear un Registro de horas

Al expandir la fila del Registro de horas pueden ingresarse los siguientes detalles:

   * **Horas Esperadas**: Ingresar el tiempo tentativo requerido para completar las Tareas en los Registros de horas.
   * **Hasta**: Ingresar la fecha y hora en la cuál se completó el trabajo. 
   * **Completado**: Debe seleccionarse esta caja si la Tarea se ha completado en el momento de enviar el Registro de horas.
   * **Tarea**: Si este Registro de horas debe ser relacionado a alguna Tarea en particular, puede hacerse aquí. 
   * **Horas Facturables**: El número de horas que se cobrarán al cliente por este Registro de horas.  
   * **Tarifa de Facturación**: La tarifa según la cual se le cobrará al cliente por este trabajo.
   * **Tarifa de Costo**: Este es el costo real del trabajo realizado. Se toma desde el costo de la actividad (por empleado) o del tipo de actividad, y puede ser editado. 
   * **Monto de Facturación**: El monto de facturación se calcula de forma automática en base al número de horas facturables y la Tarifa de Facturación. 
   * **Monto de Costo**: El monto de costo se calcula automáticamente de acuerdo con el número de horas y la tarifa de costo. 
   
   <img class="screenshot" alt="Timesheet" src="{{docs_base_url}}/assets/img/project/projects-time-sheet-expansion.png">

## 2. Características

### 2.1 Detalles de Facturación

* **Total de Horas Facturables**: Con base en el Registro de horas, se tomará automáticamente el Total de Horas Facturables. 
* **Monto Total Facturable**: Con base en el Registro de horas, se tomará automáticamente el Monto Total Facturable. 
* **Total de Horas Facturadas**: Una vez que se valida el Registro de horas, se dará la opción de crear una Factura de Ventas desde el mismo. El número de horas que se cobrará al cliente se obtendrá aquí y, una vez que la Factura de Venta es enviada, se obtendrá el Total de Horas Facturadas.
* **Monto Total Facturado**: De forma similar a cómo se obtiene el Total de Horas Facturadas, se obtendrá el Monto Total Facturado. 
* **Monto Total de Costo**: Con base en el Registro de horas, el Monto Total de Costo se etiquetará aquí, de acuerdo con lo que haya sido especificado por el Empleado.
* **Procentaje Monto Facturado**: Una vez validado el Registro de horas, y creada la [Factura de Venta](/docs/user/manual/es/projects/sales-invoice-from-timesheet) desde el Registro de horas, el porcentaje del Monto Total Facturable que haya sido efectivamente facturado en el Monto Total Facturado se calcula y se refleja aquí.

<img class="screenshot" alt="Timesheet" src="{{docs_base_url}}/assets/img/project/projects-timesheet-billing-details.png">

## 3. Luego de Guardar el Registro de horas
 
Una vez que se guarda y valida un Registro de horas, los detalles como Tarifa de Facturación y Tarifa de Costo son bloqueadas y no pueden cambiarse. Además, pueden crearse los siguientes documentos.

 * [Factura de Venta](/docs/user/manual/es/projects/sales-invoice-from-timesheet) 
 * [Recibo de Sueldo](/docs/user/manual/es/projects/salary-slip-from-timesheet)

