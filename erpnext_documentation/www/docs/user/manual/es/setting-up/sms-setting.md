<!-- add-breadcrumbs -->
# Ajustes de SMS

**Es posible suscribirse a un proveedor SMS para enviar mensajes a números de teléfono celulares.**

Para integrar SMS en ERPNext, contactar un Proveedor de Acceso de SMS que provea HTTP API. Ellos crearán una cuenta y proporcionarán un nombre de usuario y contraseña únicos.

Para acceder a Ajustes de SMS ir a:
> Inicio > Integraciones > Configuración > Ajustes de SMS

Para programar los Ajustes de SMS en ERPNext, se debe averiguar el HTTP API (un documento que describe el método para acceder a la interfaz SMS desde otras aplicaciones). En este documento, se obtendrá una URL que es utilizada para enviar los SMS mediante una solicitud HTTP. A través de esta URL, se podrán programar los Ajustes de SMS en ERPNext.

Ejemplo de URL de Acceso de SMS:  
    
    http://instant.smses.com/web2sms.php?username=<USERNAME>&password;=<PASSWORD>&to;=<MOBILENUMBER>&sender;=<SENDERID>&message;=<MESSAGE>
    

<img class="screenshot" alt="SMS Setting 2" src="{{docs_base_url}}/assets/img/setup/sms-settings2.jpg">

> Observación: Para URL de Acceso de SMS, solo incluir la serie antes del "?".

Ejemplo: 
    
    http://instant.smses.com/web2sms.php?username=abcd&password;=abcd&to;=9900XXXXXX&sender;
    =DEMO&message;=THIS+IS+A+TEST+SMS

La URL mostrada arriba enviará SMS desde la cuenta abcd al número de teléfono celular 9900XXXXXX siendo el ID del emisor DEMO con el mensaje de "ESTE ES UN SMS DE PRUEBA".

Tener en cuenta que algunos parámetros en la URL son estáticos. Se obtendrán valores estáticos del Proveedor de SMS como nombre de usuario, contraseña, etc. Estos valores estáticos deberían ser ingresados en la tabla de Parámetros Estáticos.

<img class="screenshot" alt="SMS Setting" src="{{docs_base_url}}/assets/img/setup/sms-settings1.png">

### Temas Relacionados
1. [Cuenta de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-account)
1. [Notificaciones](/docs/user/manual/es/setting-up/notifications)
