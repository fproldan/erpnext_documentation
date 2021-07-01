<!-- add-breadcrumbs -->
# Configurar Autenticación de Dos Factores

## Habilitar Autenticación de Dos Factores (2FA)

Especificar lo siguiente en Configuración del Sistema

* El método de validación OTP (Aplicación OTP = TOTP utilizando Identificador Suave o Fuerte, mientras que, Email/SMS = HOTP utilizando Email o SMS
* El tiempo de expiración para el Código QR Code en el servidor, si se especifica la Aplicación OTP
* El Nombre de Emisor OTP.

<img alt="Enable Two Factor Auth" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-1.png">


Al activar 2FA desde configuración, también se activa para el Rol "Todos". De esta forma, todos los usuarios, incluyendo el Administrador, deberán realizar una autenticación de segundo nivel con un identificador. Si no se tilda la opción "Autenticación de Dos Factores" en el rol "Todos", y se la habilita en otros roles, la obligatoriedad de iniciar sesión con un identificador puede ser limitada a ciertos roles. 2FA no se aplica a inicios de sesión de Usuarios de Sitio Web e inicio de sesión vía API.

<img alt="Role Enable Two Factor Auth" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-2.png">

Si se utiliza la autenticación vía SMS, asegurarse que las configuraciones de SMS están actualizadas

<img alt="SMS Settings" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-3.png">

Si se utiliza Correo electrónico, asegurarse que las configuraciones de la Cuenta de correo saliente están actualizadas

<img alt="Email Settings" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-4.png">

Cuando el nuevo usuario intenta iniciar sesión por primera vez en un sistema que tiene habilitada la autenticación de dos factores y que tiene seleccionada la autenticación vía Aplicación OTP, se le enviará un correo electrónico que contiene el link al Código QR.

<img alt="Email Notify Two Factor" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-5.png">
<img alt="QR Code Page" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-6.png">

Escanear el Código QR con una aplicación de autenticación como Google Authenticator, registra el acceso para el usuario y automáticamente empieza a generar identificadores que pueden utilizarse para iniciar sesión. 

<img alt="Two Factor Scan App" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor_app.jpeg">

Si se utiliza Correo electrónico/SMS como método de autenticación, también se recibirán notificaciones.

<img alt="Email and SMS" class="screenshot" src="{{docs_base_url}}/assets/img/articles/twofactor/twofactor-8.png">
