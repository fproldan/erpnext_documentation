# Configuraciones de Twitter

Las configuraciones relacionadas a Twitter como OAuth pueden configurarse aquí. ERPNext necesita acceder a la API a través de la cuál se comparte utilizando el Protocolo de Autenticación de OAuth 2.0.

## 1.  Configuración de la Aplicación Twitter

Se debe tener la aplicación Twitter para la empresa. ERPNext interactúa con esta aplicación para compartir los Tweets.

### 1.1 Creación de Twitter Developer App

Crear la Aplicación a través del siguiente link `https://developer.twitter.com/` y verificar que la Aplicación tenga permiso de acceso para **Leer y Escribir**.
![Twitter App Permission](/docs/assets/img/crm/twitter-app-permission.png)

### 1.2. Configuración de la URL Callback
1. Seleccionar la aplicación e ir a **Detalles de Aplicación**.
2. Luego ir a **Editar** y hacer click en **Editar Detalles**.
3. Añadir la URL del sitio web de la empresa en **URLs de Callback** de la siguiente forma:
`https://{yoursite}/api/method/erpnext.crm.doctype.twitter_settings.twitter_settings.callback`
4. Hacer click en **Guardar** para realizar los cambios.  

![Twitter App Callback URL](/docs/assets/img/crm/twitter-callback-url.png)


## 2. Configuraciones de Twitter

Para acceder a las Configuraciones de Twitter:
> Inicio > CRM > Configuraciones > Configuraciones de Twitter

![Twitter Settings](/docs/assets/img/crm/twitter-settings.png)

### 2.1 Clave API y Clave Secreta de API

Para obtener la **Clave de API** y la **Clave Secreta de API** desde la cuenta de Twitter Developer ir a:
> `https://developer.twitter.com/` > Mis Aplicaciones > `{Your App}` > Claves y Autenticaciones

![Twitter Keys Tokens](/docs/assets/img/crm/twitter-key-token.png)

Una vez que se guarda el documento llenando la **Clave de API** y la **Clave Secreta de API** se redirigirá a la página de inicio de sesión de Twitter, en la cual, al proveer las credenciales válidas de Twitter y hacer click en **Autorizar aplicación**, el usuario aprueba el pedido de la aplicación para acceder a sus datos de usuario e interactuar con Twitter.
![Twitter Authorize App](/docs/assets/img/crm/twitter-authorize-app.png)

{siguiente}