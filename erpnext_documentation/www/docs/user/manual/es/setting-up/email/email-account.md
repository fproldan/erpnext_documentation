<!-- add-breadcrumbs -->
# Cuenta de Correo Electrónico

**Se puede sincronizar la Cuenta de Correo Electrónico para enviar y recibir emails desde ERPNext.**

En ERPNext se pueden administrar muchas Cuentas de Correo Electrónico entrantes y salientes. Tiene que haber por lo menos una cuenta predeterminada de entrantes y una de salientes. Si se utiliza la nube de ERPNext, la cuenta de correos salientes es configurada por el implementador.

Para acceder a Cuentas de Correo Electrónico ir a:
> Inicio > Configuración > Notificaciones de Correo Electrónico > Cuenta de Correo Electrónico

## 1. Prerrequisitos

Antes de crear una Cuenta de Correo Electrónico, se necesita un [Dominio de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-domain). Sin embargo, se puede saltear este paso si se utiliza alguno de los servicios listados [aquí](/docs/user/manual/es/setting-up/email/email-inbox#2-create-an-email-domain).

## 2. Creación de una Cuenta de Correo Electrónico

1. Ir al listado de Cuenta de Correo Electrónico y hacer click en Nueva.
1. Ingresar la dirección de correo con el dominio. Los [Dominios](/docs/user/manual/es/setting-up/email/email-domain) deben estar creados para poder crear la cuenta.
    No se necesita crear un dominio si se está sincronizando un email de ciertos proveedores, como se listan [aquí](/docs/user/manual/es/setting-up/email/email-inbox#2-create-an-email-domain).
1. Ingresar la contraseña de la cuenta de correo.
1. Guardar.
Si las credenciales son correctas, se sincronizará la cuenta. 

> Observación: Para algunos servicios como Gmail, puede ser necesario editar las configuraciones para permitir aplicaciones menos seguras. 

### 2.1 Opciones adicionales al crear una Cuenta de Correo Electrónico

1. **Utilizar ID de acceso de correo electrónico diferente**: Sirve para utilizar un email de inicio de sesión y contraseña alternativos para acceder a esta cuenta. Por ejemplo, si se cuenta con el email notificaciones@ejemplo.com y se quiere que los usuarios accedan a este correo electrónico desde un ID alternativo, se deberá tildar esta opción. Los receptores del email verán la cuenta notificaciones@ejemplo.com como la cuenta desde la cual se envió el mail. 
1. **Esperando contraseña**: Si se está creando esta cuenta en nombre de alguien y la contraseña es desconocida, seleccionar esta casilla de verificación. Cuando el otro usuario inicie sesión, se le pedirá ingresar la contraseña. 
1. **Use la codificación ASCII para la contraseña**: Seleccionar esto llevará a utilizar codificación ASCII para la contraseña. 

## 3. Configuración de la Cuenta de Correo Electrónico

### 3.1 Cuentas de Correo Electrónico Predeterminadas

ERPNext creará, de forma predeterminada, plantillas para muchas cuentas de email. No todas están habilitadas. Para habilitarlas se deben configurar detalles válidos para la cuenta de email.  

Hay dos tipos de cuentas de email, salientes y entrantes. La cuentas de email salientes utilizan un servicio SMTP para enviar emails y los mismos son recuperados desde la bandeja de entrada utilizando IMAP o POP. La mayoría de los proveedores de email como Gmail, Outlook, o Yahoo proveen estos servicios.

<img class="screenshot" alt="Defining Criteria" src="{{docs_base_url}}/assets/img/setup/email/email-account-list.png">

### 3.2 Cuenta de Correos Electrónicos Entrantes

Para configurar una Cuenta de Correo Electrónico entrante, hacer click en el campo **Habilitar correos entrantes** y editar las configuraciones POP3, si se está utilizando un servicio de email popular, las mismas ya estarán preconfiguradas. 

<img class="screenshot" alt="Incoming EMail" src="{{docs_base_url}}/assets/img/setup/email/email-account-incoming.png">

Se encuentran disponibles las siguientes opciones para emails entrantes:

* **Usar IMAP**
* **Utilizar SSL**
* **Límite para Adjunto (MB)**
* **Entrante predeterminado**: Si se encuentra seleccionada, todas las respuestas a la empresa (ej: respuestas@empresa.com) se recibirán en esta cuenta.
* **Opción de Sincronización de Correos**: se puede configurar para sincronizar todos los correos electrónicos o solo los no vistos. 
* **Conteo de sincronización inicial**: Número de correos a sincronizar la primera vez.

#### Anexar Correos Electrónicos a Documentos

Esta característica crea documentos cuando un correo electrónico se envía a una cuenta en particular. Por ejemplo, se puede anexar asistencia@ejemplo.com al doctype Ticket. Al hacer esto, cada vez que un email es enviado a asistencia@ejemplo.com, el sitema creará un Ticket para el mismo. De forma similar, si se vincula trabajos@ejemplo.com, cuando se envíen correos a trabajos@ejemplo.com, se creará un documento de Solicitante de Empleo.

Tildar la opción "Habilitar la vinculación automática en documentos", vinculará los correos a documentos. Para saber más hacer click [aquí](/docs/user/manual/es/setting-up/email/linking-emails-to-document).

### 3.3 Notificación para mensajes sin responder

Si se desea que ERPNext notifique de un correo que está sin responder por un período de tiempo determinado, entonces se puede configurar **Notificar si permanece sin responder**. Aquí se puede configurar el número de minutos de espera antes de enviar notificaciones, y a dónde enviarlas. 

<img class="screenshot" alt="Incoming EMail" src="{{docs_base_url}}/assets/img/setup/email/email-account-unreplied.png">

#### Configurar condiciones para importaciones de Correo Electrónico 

Las Cuentas de Correo Electrónico permiten configurar condiciones de acuerdo con los datos de los mails entrantes. El email será importado a ERPNext solo si todas las condiciones son ciertas. Por ejemplo, si se quiere importar un email siempre y cuando el asunto sea "Email Importante", se ingresa doc.asunto == "Email Importante" en el cuadro de texto de condiciones. También se pueden configurar condiciones más complejas combinándolas, como se muestra en la siguiente captura de pantalla.

<img class="screenshot" alt="Incoming EMail Conditions" src="{{docs_base_url}}/assets/img/setup/email/email-account-incoming-conditions.png">

### 3.4 Cuenta de Correos Electrónicos Salientes

Todos los emails enviados desde el sistema, ya sea desde el usuario a un contacto, a través de notificaciones o a través de emails de transacciones, serán enviados desde una Cuenta de Correos Electrónicos Salientes. 

Para configurar una Cuenta de Correo Electrónico saliente, hacer click en el campo **Habilitar correos salientes** y editar las configuraciones del servidor SMTP, si se está utilizando un servicio de email popular, las mismas ya estarán preconfiguradas.

<img class="screenshot" alt="Outgoing EMail" src="{{docs_base_url}}/assets/img/setup/email/email-account-sending.png">

Se encuentran disponibles las siguientes opciones para correos salientes:

* **Utilizar TLS**
* **Puerto**
* **Deshabilitar autenticación del servidor SMTP**
* **Agregar Firma**: La firma predeterminada se adjuntará al final de cada email. 
* **Saliente predeterminado**: Las notificaciones y los emails enviados masivamente, serán enviados desde este servidor saliente.
* **Utilizar siempre la dirección de correo electrónico de la cuenta como remitente**: La dirección de email de esta cuenta será mencionada como emisora para correos salientes.
* **Incluir opción para darse de baja**: Enviar un link para dar la baja de correos enviados desde esta dirección. 
* **Seguir el estado del Correo Electrónico**: Rastrear si el email ha sido leído por el receptor. Observar que, si se está enviando a muchos destinatarios, con que uno solo de ellos abra el correo, ya será considerado "Abierto". 
* **Agregar correos electrónicos a la carpeta de enviados**: Si se usan servidores personalizados como Zimbra o CPanel, SMTP no adjuntará los emails a la Carpeta de Enviados. Habilitar esta opción asegurará que todos los emails son explícitamente adjuntados a la Carpeta de Enviados de la cuenta de email.
* **Usar SSL para saliente**: Usar SSL como estándar para mails salientes. El puerto predeterminados es el 465.
* * **Habilitar Respuesta Automática**: Si se encuentra habilitada esta opción, ingresar un mensaje automático de respuesta.

## 4. Manejo de respuestas

En ERPNext cuando se envía un email a un contacto, como un cliente, el emisor será el usuario que envió el email. En la propiedad **Responder A**, la Dirección de Correo Electrónico será la de la cuenta entrante (como `respuestas@empresa.com`). ERPNext extraerá automáticamente estos emails de la cuenta entrante y los etiquetará a la comunicación relevante. 

> **Observación para auto implementación:** Para emails salientes, se debe configurar el propio servidor SMTP o registrarse con un servicio basado en SMTP, como mandrill.com o sendgrid.com, que permiten el envío de un mayor número de emails transaccionales. Los servicios de email Regulares como Gmail, restringirán los envíos a un número limitado de emails por día. 

Si se encuentran errores al configurar la cuenta de email, referirse a esta [página](/docs/user/manual/es/setting-up/articles/email-error).

## 5. Temas Relacionados
1. [Bandeja de Entrada de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-inbox)
1. [Boletín de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-digest)
1. [Informes de Correo Electrónico Automáticos](/docs/user/manual/es/setting-up/email/auto-email-reports)
1. [Envío de Correos Electrónicos](/docs/user/manual/es/setting-up/email/sending-email)
1. [Dominio de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-domain)
