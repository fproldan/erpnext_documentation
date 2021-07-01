<!-- add-breadcrumbs -->
# Calendario

**El Calendario es una Herramienta que permite crear, compartir y realizar un seguimiento de eventos en la cuenta ERPNext.**

En el calendario se puede tener una vista de Días, Semanas o Meses.

![Calendar](/docs/assets/img/using-erpnext/using-calender-1.png)

Para acceder al calendario ir a:

> Inicio > Herramientas > Calendario

## 1. Creación de Eventos en un Calendario

1. Ir al Calendario y hacer click en Nuevo.
2. Ingresar el Tema y Fecha de Inicio del evento.
3. Guardar.

![Calendar](/docs/assets/img/using-erpnext/using-calender-2.gif)

De forma alternativa también se puede crear un evento desde la 'Vista por Días' del Calendario. Esta vista está dividida en varios compartimientos a lo largo del día. Se puede seleccionar el compartimiento para el inicio del evento, ingresar el tema y arrastrarlo hasta la hora de finalización del evento. 

![Calendar](/docs/assets/img/using-erpnext/using-calender-3.gif)

### 1.1. Evento Basado en una Iniciativa 

En el formulario de Iniciativa hay un campo llamado Siguiente contacto por y Siguiente fecha de contacto. Una vez especificados estos datos, se creará automáticamente un evento para ese Usuario en la fecha y horario establecidos. 

![Calendar](/docs/assets/img/using-erpnext/using-calender-4.png)

### 1.2. Evento Basado en Tarjetas de Trabajo

Por cada Tarjeta de Trabajo creada para un Usuario en la cuenta ERPNext, se creará un evento correspondiente en el calendario.

![Calendar](/docs/assets/img/using-erpnext/using-calender-job-card.png)

### 1.3. Cumpleaños

Un Evento de Cumpleaños se crea de acuerdo con la Fecha de Nacimiento especificada en la función Empleados. 

### 1.4. Eventos Recurrentes

Hay varios eventos que ocurren de forma regular en las empresas en intervalos periódicos. En ERPNext, se pueden crear eventos de este estilo habilitando la propiedad 'Repetir este Evento' para cada uno de ellos. 

Al hacer esto, se pedirá ingresar la periodicidad del evento en el campo 'Repetir En'. Esto podría ser diariamente, mensualmente, semanalmente o Anualmente. 

También se puede ingresar el último día de la repetición en el campo 'Repetir Hasta'. En el caso de repeticiones infinitas, se puede elegir dejar este campo en blanco. 

![Calendar](/docs/assets/img/using-erpnext/using-calender-5.gif)

### 1.5. Recordatorios de Eventos

Hay dos formas en que se puede recibir un recordatorio para un evento vía correo electrónico. 

1. Habilitar Recordatorio en el Evento

 En la función Evento, hacer click en la casilla de verificación "Enviar un recordatorio por correo electrónico en la mañana" generará un notificación que se enviará por correo electrónico a todos los participantes del evento.

 ![Calendar](/docs/assets/img/using-erpnext/using-calender-6.png)

2. Crear Resumen de Correo Electrónico

 Para obtener recordatorios de eventos por correo electrónico, se debería crear un Resumen de Correo Electrónico para los Eventos del Calendario. 

 El Resumen de Correo Electrónico puede configurarse desde:

 > Configuración > Correo Electrónico > Resumen de Correo Electrónico

 ![Calendar](/docs/assets/img/using-erpnext/using-calender-7.png)

{siguiente}
