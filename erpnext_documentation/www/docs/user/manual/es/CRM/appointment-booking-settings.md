# Configuraciones de Reserva de Turno

Se puede encontrar toda la configuración relacionada con la reserva de citas en la Configuración de Reserva de Turnos.

![Appointment Booking Settings](/docs/assets/img/crm/appointment-booking-settings.png)

## 1. Permitir la programación de Turnos 

Esta casilla de verificación permitirá programar turnos y también habilitará la función `/programar_turno` para los usarios del sitio web (es decir los clientes). Los clientes accederán a una vista de portal. Para saber más visitar la [Página de Turnos](/docs/user/manual/es/CRM/appointment)

## 2. Detalles de Agente

En esta sección se pueden añadir detalles de agentes, como sus horarios de trabajo y vacaciones.

### 2.1  Disponibilidad Horaria

Aquí se puede configurar el horario en que los agentes estarán disponibles para asistir a una cita. Esto se configura por día de la semana. Cada fila representa un bloque continuo de tiempo, se pueden realizar muchos registros para cada día de la semana. 

Por ejemplo, si los agentes trabajan de Lunes a Viernes de 9 am a 5 pm pero tienen un descanso para el almuerzo a la 1:30 pm el cual dura media hora, se deberán crear dos registros, uno para cada día. Uno desde 9 am hasta 1:30 pm y otro desde las 2 pm hasta las 5 pm.

### 2.2 Agentes

Esta es la lista de agentes que serán **autoasignados** a turnos. El número de turnos que pueden existir en una franja horaria también depende del número de empleados en la lista. 

### 2.3 Lista de Feriados

Se puede vincular una (lista de feriados)[https://erpnext.com/docs/user/manual/en/human-resources/holiday-list] aquí para aplicar al calendario de turnos. Si el día es un feriado, reservar un turno en esa fecha no será posible. 

## 3. Detalles de Turno

Esta sección contiene detalles sobre los turnos en sí.

### 3.1 Duración de Turno en Minutos

La duración del turno en minutos. Esto se utiliza para calcular las franjas horarias para turnos en el portal web. Cambiar esto no afectará los turnos que fueron creados con anterioridad al cambio.

### 3.2 Notificar vía correo electrónico

Al habilitar esta casilla se enviará un mail a todos los participantes de la cita, es decir, el empleado y el cliente, en el día del mismo. Habilitar o deshabilitar esta casilla no afectará a los turnos creados antes del cambio. 

### 3.3 Número de días de antelación con el cuál se puede pedir un turno

Este es el máximo número de días de anticipación con que puede crearse el turno. Si la Lista de Feriados provista anteriormente termina antes de la fecha calculada usando este número, la programación de turnos terminará al mismo tiempo que la lista de feriados. 


## 4. Configuraciones de Éxito

### 4.1 URL de Redireccionamiento en caso de Éxito 

Esta es la URL a la cuál será redirigido el usuario al crear exitosamente un turno a través del portal Web. Este redireccionamiento no ocurrirá al crear turnos desde el Escritorio UI.
Dejar en blanco para redirigir al incio. Esto es relativo a la URL del sitio web, por ejemplo "Acerca De" redirigirá a "https://yoursitename.com/about"
