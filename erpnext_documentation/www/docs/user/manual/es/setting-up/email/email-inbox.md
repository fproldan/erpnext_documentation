<!-- add-breadcrumbs -->
# Bandeja de Entrada

**Una vez que se agrega una Cuenta de Correo Electrónico se podrá acceder a su bandeja de entrada.**

Administrar un negocio incluye muchos intercambios de correos con partes como Clientes y Proveedores y miembros dentro de la empresa. La funcionalidad de Bandeja de Entrada permite concentrar todos los emails de negocios en la cuenta ERPNext. Habilitar el acceso a correos de negocios con otros detalles de transacciones convierte a ERPNext en una única plataforma que permite acceder a toda la información de negocios en un solo lugar.

En ERPNext, se puede configurar una Bandeja de Entrada para cada Usuario de Sistema. A continuación se encuentran detallados los pasos para configurar la Bandeja de Entrada para un Usuario. 

## 1. Usuario

Se puede configurar cada Bandeja de Entrada solo para un Usuario de Sistema. De esta forma, es necesario asegurarse que se han añadido todos los trabajadores como Usuarios y que se les han asignado los permisos requeridos. 

Más información sobre la creación de usuarios [aquí](/docs/user/manual/es/setting-up/users-and-permissions/adding-users).

## 2. Dominio de Correo Electrónico

El Dominio de Correo Electrónico para los siguientes Servicios está disponible de forma predeterminada y se puede proceder directamente a crear una [Cuenta de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-account). Más información respecto a la creación de un Dominio de Correo Electrónico [aquí](/docs/user/manual/es/setting-up/email/email-domain).

* **Gmail**
* **Yahoo**
* **Sparkpost**
* **SendGrid**
* **Outlook.com**
* **Yandex.mail**

<img class="screenshot" alt="Email Service" src="{{docs_base_url}}/assets/img/setup/email/email-service.png">

Para poder enviar y recibir correos en la cuenta ERPNext desde otros servicios de email (como WebMail o Gmail), se deberá configurar un Dominio de Correo Electrónico. Aquí, los detalles de acceso como Dirección SMTP, Número de Puerto, detalles de direcciones IMAP/POP3, son capturados. Si alguna vez se ha configurado un email local (como Outlook), el Dominio de Correo Electrónico requiere que se ingresen los detalles de forma similar. 

Para añadir un nuevo Dominio de Correo Electrónico ir a:

> Inicio > Configuración > Notificaciones de Correo Electrónico > Dominio de Correo Electrónico > Nuevo

<img class="screenshot" alt="Email Domain" src="{{docs_base_url}}/assets/img/setup/email/email-domain.png">

Aprender más sobre Dominio de Correo Electrónico [aquí](/docs/user/manual/es/setting-up/email/email-domain). Una vez configurado un Dominio de Correo Electrónico para el Servicio, se utilizará para crear Cuentas de Correo Electrónico para todos los Usuarios en la cuenta ERPNext. 

## 3. Cuenta de Correo Electrónico

Crear una Cuenta de Correo Electrónico basada en el ID de Correo Electrónico del Usuario. Para cada Usuario cuya cuenta de correo deba ser integrado con ERPNext, debe crearse una Cuenta de Correo Electrónico. 

Si se está creando una Cuenta de Correo Electrónico para un colega sin conocer su contraseña, seleccionar el campo "Esperando Contraseña". De acuerdo con esta configuración, un Usuario (para el cual se crea la Cuenta) recibirá una notificación para ingresar la contraseña del correo al acceder a su cuenta ERPNext.

<img class="screenshot" alt="Email Password" src="{{docs_base_url}}/assets/img/setup/email/email-password.png">

> Si se está creando una Cuenta de Correo Electrónico para la Bandeja de Entrada de un Usuario, entonces dejar el campo "Adjuntar a" en blanco.

Para más detalles sobre cómo configurar una Cuenta de Correo Electrónico, [click aquí](/docs/user/manual/es/setting-up/email/email-account).

## 4. Vincular Cuenta de Correo Electrónico con el Usuario

Una vez que se crea una Cuenta de Correo Electrónico para un Usuario, seleccionarla en el Usuario. Esto asegurará que los emails obtenidos de ese ID de Correo Electrónico solo serán accesibles para ese usuario en la cuenta ERPNext.

<img class="screenshot" alt="Email User Link" src="{{docs_base_url}}/assets/img/setup/email/email-user-link.png">

Se pueden vincular muchos correos a un solo usuario. 

## 5. Utilizar Bandeja de Entrada de Correo Electrónico

Si se ha configurado correctamente una Bandeja de Entrada de Correo Electrónico como se explicó anteriormente, entonces en el inicio de sesión de un Usuario, se verá el ícono de Bandeja de Entrada. Esto llevará al usuario a la Bandeja de Entrada de Correo Electrónico dentro de la cuenta ERPNext. Todos los Correo Electrónico recibidos en esa cuenta serán tomados y enlistados en la vista de Bandeja de Entrada. El Usuario podrá abrirlos y realizar distintas acciones sobre ellos.

### 5.1 Carpetas

En ERPNext, se pueden vincular muchas Cuentas de Correo Electrónico con un solo Usuario. Para cambiar a la Bandeja de Entrada de otra cuenta y acceder a otras carpetas como Enviados, Spam, Papelera, hacer click en la opción Bandeja de Entrada en la barra lateral. 

<img class="screenshot" alt="Email Folders" src="{{docs_base_url}}/assets/img/setup/email/email-folders.png">

### 5.2 Acciones

Se pueden realizar varias acciones sobre los correos en la bandeja de entrada como Responder, Reenviar, Marcar como Spam o Eliminar.

<img class="screenshot" alt="Email Actions" src="{{docs_base_url}}/assets/img/setup/email/email-actions.png">

### 5.3 Vincular

Se puede vincular un email a un documento como Asunto, Iniciativa, Oportunidad, etc, de acuerdo con el contexto del correo. Seleccionar el tipo de documento y el documento al cual vincular el email.

<img class="screenshot" alt="Make from Email" src="{{docs_base_url}}/assets/img/setup/email/make-from-email.png">

### 6. Temas Relacionados
1. [Cuenta de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-account)
1. [Enviar Correo Electrónico](/docs/user/manual/es/setting-up/email/sending-email)
1. [Dominio de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-domain)
