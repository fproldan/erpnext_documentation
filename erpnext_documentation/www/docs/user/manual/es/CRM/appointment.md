# Cita

**Una cita es un encuentro preacordado entre un Cliente Potencial y un Empleado de la Empresa.**

El tipo de documento Cita puede ser utilizado para programar y administrar las interacciones con una [Iniciativa](/docs/user/manual/es/CRM/lead) o con una [Oportunidad](/docs/user/manual/es/CRM/opportunity). 

Para acceder al listado Cita ir a:
> Inicio > CRM > Flujo de Venta > Cita

## 1. Prerrequisitos

1. [Configuraciones de Reserva de Cita](/docs/user/manual/es/CRM/appointment-booking-settings)
2. [Lista de Feriados](/docs/user/manual/es/human-resources/holiday-list)
3. [Empleado](/docs/user/manual/es/human-resources/employee)
4. [Cliente Potencial](/docs/user/manual/es/CRM/lead)
5. [Correo Electrónico](/docs/user/manual/es/setting-up/email/email-account)

## 2. Creación de una Cita

1. Ir al listado de Citas y hacer click en Nueva
2. Seleccionar el día y hora acordados para la cita
3. Ingresar los detalles del cliente
4. En documentos vinculados, si ya se creó una Iniciativa para el Cliente, se puede configurar aquí. De otra forma, el sistema creará automáticamente una nueva iniciativa con los detalles del cliente ingresados en el paso anterior. 
5. Guardar.
 ![New Appointment](/docs/assets/img/crm/new-appointment.png)

### 2.1 Creación desde el sitio web

Los Clientes/Clientes Potenciales pueden generar una cita utilizando la página web `yoursitename.com/book_appointment`. 

Primero deben ingresar una fecha y hora.
![Appointment Webform](/docs/assets/img/crm/appointment-webform.png)

Luego, añadir más detalles:
![Appointment Details](/docs/assets/img/crm/appointment-details.png)

Se comparará el correo electrónico del cliente con clientes potenciales en el sistema y si se encuentra una coincidencia, se vincula con el documento.
Si no se encuentran clientes potenciales, la cita se marca como "No Verificada" y se envía un correo electrónico al cliente para confirmar su dirección de mail. 

## 3. Características

### 3.1 Autoasignar

Las citas se asignan automáticamente a empleados de acuerdo con la lista `Agentes` en [Configuraciones de Reserva de Cita](/docs/user/manual/en/CRM/appointment-booking-settings). El agente con el menor número de asignaciones en el día de la cita y que esté libre en la hora establecida, es asignado a la cita. 

### 3.2 Confirmación de Correo Electrónico

Si no hay un cliente potencial en el sistema que coincida, se enviará un correo electrónico a la dirección de correo ingresada en la cita para confirmar que dicha dirección sea válida. Al realizar la confirmación, se creará un nuevo Cliente Potencial en el sistema junto con la Cita.
