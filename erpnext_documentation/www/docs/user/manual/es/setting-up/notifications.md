<!-- add-breadcrumbs -->
# Notificación

**Se pueden configurar diversas notificaciones en el sistema para recibir recordatorios de actividades importantes.**

1. La fecha de finalización de una Tarea.
2. Fecha de Entrega Esperada de una Orden de Venta.
3. Fecha de Pago Esperada.
4. Recordatorio de seguimiento.
5. Si se recibe o envía una Orden mayor a un valor en particular.
6. Notificación de Vencimiento para un Contrato.
7. Finalización/Cambio de Estado de una Tarea.

Para acceder a la configuración de notificaciones ir a:

> Inicio > Configuración > Notificaciones de Correo Electrónico > Notificación

## 1. Configuración de una Alerta

Para Configurar una Notificación:

1. Seleccionar el Tipo de Documento sobre el cual se desean recibir notificaciones de cambios.
2. Definir qué eventos se quieren ver en el campo "Enviar alerta en". Los eventos son: 
    - Nuevo: Cuando se crea un nuevo documento del tipo seleccionado.
    - Guardar/Validar/Cancelar: Cuando un documento del tipo seleccionado es guardado, validado, o cancelado. 
    - Días Antes/Días Después: Activar esta alerta **Días antes o despues** de la **Fecha de Referencia**. Esto puede ser útil para recordar fechas de vencimiento por venir o para realizar seguimientos sobre ciertas iniciativas o cotizaciones. 
    - Cambios de Valor: Cuando cambia un valor en particular en el tipo de documento seleccionado.
    - Método: Envía notificaciones cuando se activa un método específico. Ejemplo: before_insert.
    - Personalizar: Envía una notificación a una [Cuenta de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-account) seleccionada.
3. Configurar Condiciones adicionales de ser necesario.
4. Definir los receptores del alerta. Pueden ser un campo en el documento o una lista de Direcciones de Correo Electrónico fijadas. 
5. Redactar el mensaje.
1. Guardar.


### 1.1 Configurar un Asunto

Se pueden recuperar los datos de un campo en particular utilizando `doc.[nombrede_campo]`. Para utilizarlo en el asunto/mensaje, es necesario rodearlo con `{% raw %}{{ }}{% endraw %}`. Estas se llaman etiquetas [Jinja](http://jinja.pocoo.org/). Por ejemplo, para obtener el nombre de un documento, se utiliza `{% raw %}{{ nombrede.documento }}{% endraw %}`. El siguiente ejemplo envía un email al guardar una Tarea con el Asunto de "TAREA#### ha sido creada"

<img class="screenshot" alt="Setting Subject" src="{{docs_base_url}}/assets/img/setup/notifications/email-alert-subject.png">

### 1.2 Configurar Condiciones

Las Notificaciones permiten configurar condiciones de acuerdo con los datos del campo en los documentos. Por ejemplo, si se quiere recibir un correo si una Iniciativa ha sido guardada con un estado de "Interesado", se ingresa `doc.estado == "Interesado" en el cuadro de texto de condiciones. También se pueden configurar condiciones más complejas combinándolas. 

<img class="screenshot" alt="Setting Condition" src="{{docs_base_url}}/assets/img/setup/notifications/email-alert-condition.png">

El ejemplo mostrado arriba enviará una Notificación cuando una Tarea sea guardada con el estado de "Abierta" y la "Fecha de Finalización Esperada" para la tarea sea la misma, o una fecha anterior, a la fecha en la que ha sido guardada. 


### 1.3 Configurar un Mensaje

Se pueden utilizar tanto etiquetas Jinja (`{% raw %}{{ doc.[field_name] }}{% endraw %}`) como HTML en el cuadro de texto del mensaje.

    {% raw %}<h3>Orden Vencida</h3>

    <p> La transacción {{ nombrede.documento }} ha excedido la Fecha de Vencimiento. Por favor, realizar las acciones necesarias.</p>

    <!-- mostrar último comentario -->
    {% if comments %}
    Último comentario: {{ comments[-1].comment }} by {{ comments[-1].by }}
    {% endif %}

    <h4>Details</h4>

    <ul>
    <li>Cliente: {{ doc.cliente }}
    <li>Monto: {{ doc.monto_total }}
    </ul>{% endraw %}


### 1.4 Establecer propiedad después de la Alerta

A veces, para asegurarse que la Notificación no sea enviada varias veces, se puede definir una propiedad personalizada (a través de Personalizar Formulario) como "Notificación Enviada" y luego configurar esta propiedad luego de que el alerta es enviada, seleccionando una opción en el campo **Establecer propiedad después de la Alerta**.

Luego se puede usar esto como condición en las reglas de **Condición** para garantizar que los emails no se envíen muchas veces

<img class="screenshot" alt="Setting Property in Notification" src="{{docs_base_url}}/assets/img/setup/notifications/email-alert-subject.png">

### 1.5 Ejemplo

1. Definir los Criterios
    <img class="screenshot" alt="Defining Criteria" src="{{docs_base_url}}/assets/img/setup/notifications/email-alert-1.png">

1. Configurar los Receptores y el Mensaje
    <img class="screenshot" alt="Set Message" src="{{docs_base_url}}/assets/img/setup/notifications/email-alert-2.png">


---

## 2. Notificaciones Slack

Si se prefiere que las notificaciones sean enviadas a un canal Slack dedicado a esto, también se puede elegir la opción "Slack" en las opciones de canal y seleccionar la URL de Slack Webhook correspondiente.

### 2.1 URL de Slack Webhook

Una URL de Slack webhook es una URL que lleva directamente a un canal Slack.

Para generar URLs webhook, se debe crear una nueva Aplicación Slack:

1. Ir a https://api.slack.com/slack-apps.
2. Hacer click en "Crear una Aplicación Slack".
    <img class="screenshot" alt="Set Message" src="{{docs_base_url}}/assets/img/setup/notifications/slack_notification_1.png">

3. Dar un nombre a la Aplicación y elegir el área de trabajo adecuada. 
    Una vez que la aplicación fue creada, ir a la sección "Webhooks Entrantes" y añadir un nuevo Webhook al Área de Trabajo.
    <img class="screenshot" alt="Set Message" src="{{docs_base_url}}/assets/img/setup/notifications/slack_notification_2.png">

4. Copiar el link creado, volver a ERPNext y utilizarlo para crear una nueva URL de Slack Webhook en Integraciones > URL de Slack Webhook.
    <img class="screenshot" alt="Set Message" src="{{docs_base_url}}/assets/img/setup/notifications/slack_notification_3.png">

5. Seleccionar Slack y el canal Slack, en los campos Slack y canal Slack, dentro de la notificación


### 2.2 Formato de Mensaje

A diferencia de los mensajes de Email, Slack no permite el formato HTML.

En cambio, se puede utilizar formato markdown [Documentación Slack](https://get.slack.help/hc/en-us/articles/202288908-Format-your-messages)

Ejemplo:
    {% raw %}
    *Orden Vencida*

    Transacción {{ nombre.documento }} ha excedido la Fecha de Vencimiento. Por favor, realizar las acciones necesarias.


    {% if comments %}
    Último Comentario: {{ comments[-1].comment }} by {{ comments[-1].by }}
    {% endif %}

    *Detalles*

    â€¢ Cliente: {{ doc.cliente }}
    â€¢ Monto: {{ doc.total_general }}
    {% endraw %}

<img class="screenshot" alt="Set Message" src="{{docs_base_url}}/assets/img/setup/notifications/slack_notification_4.png">


---

## 3. Notificaciones de Sistema

ERPNext cuenta con Notificaciones de Sistema para **Asignaciones**, **menciones**, **documentos compartidos**, y **Puntos de Energía**. Estas notificaciones se muestran en el menú desplegable de notificaciones en la esquina superior derecha de la barra de navegación.

También hay un canal adicional para enviar alertas - **Notificaciones de Sistema**:

<img class="screenshot" alt="Notifications Dropdown" src="{{docs_base_url}}/assets/img/setup/notifications/system-notifications-channel.png">

Elegir este canal enviará una notificación de sistema cuando se active una alerta, en vez de un Email o una notificación Slack. 

<img class="screenshot" height=400 alt="Notifications Dropdown" src="{{docs_base_url}}/assets/img/setup/notifications/system-notification.png">

Al hacer click en la notificación se accede al documento de **Registro de Notificaciones** que contiene el asunto y mensaje configurados así como también el archivo adjunto, si Adjuntar Impresión está configurada: 

<img class="screenshot" alt="Notifications Dropdown" src="{{docs_base_url}}/assets/img/setup/notifications/notification-log.png">

Si se requieren tanto alertas por Email/Slack como Notificaciones de Sistema, el canal principal puede ser Email o Slack y esta opción puede ser seleccionada:

<img class="screenshot" alt="Notifications Dropdown" src="{{docs_base_url}}/assets/img/setup/notifications/send-system-notification.png">

## 4. WhatsApp

Es posible enviar alertas mediante **WhatsApp**:
<img class="screenshot" alt="Notifications WhatsApp Channel" src="{{docs_base_url}}/assets/img/setup/notifications/twilio-channel.png">

Si se prefiere que las notificaciones sean enviadas a un número de WhatsApp, se puede elegir la opción "WhatsApp" en las opciones de canal y seleccionar el Número Twilio apropiado. Los Números Twilio pueden ser añadidos a las configuraciones Twilio en Frappe. Los mensajes de WhatsApp solo pueden ser enviados a números que tengan códigos de país en ellos.

<img class="screenshot" alt="Twilio Settings" src="{{docs_base_url}}/assets/img/setup/notifications/twilio-settings.png">

### 4.1 Configuraciones Twilio

Para programar las configuraciones Twilio, primero se necesita obtener las credenciales Twilio de las configuraciones de la Cuenta Twilio. Solo pueden añadirse aquellos números de teléfono que hayan sido activados en la Cuenta Twilio con acceso a WhatsApp.
<img class="screenshot" alt="Twilio Credentials" src="{{docs_base_url}}/assets/img/setup/notifications/twilio-credentials.png">

### 4.2 Formato de Mensaje

WhatsApp solo permite a sus usuarios enviar a los clientes plantillas de mensaje que han sido preaprobadas por ellos. De no cumplirse esto, pueden imponerse restricciones sobre la cuenta Twilio.
<img class="screenshot" alt="Pre Approved Message Template" src="{{docs_base_url}}/assets/img/setup/notifications/twilio-pre-approved-message.png">


## 5. SMS

Finalmente, se pueden enviar notificaciones por **SMS**:
<img class="screenshot" alt="SMS Channel" src="{{docs_base_url}}/assets/img/setup/notifications/sms-notification-channel.png">

Para utilizar este canal, se deberán completar los [Ajustes de SMS](/docs/user/manual/es/setting-up/sms-setting).


## 6. Temas Relacionados
1. [Ajustes de SMS](/docs/user/manual/es/setting-up/sms-setting)
1. [Seguimiento de Documento](/docs/user/manual/es/setting-up/email/document-follow)
