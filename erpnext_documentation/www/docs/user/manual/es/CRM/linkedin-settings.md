# Configuraciones de LinkedIn

Las configuraciones relacionadas a LinkedIn como OAuth pueden configurarse aquí. ERPNext necesita acceder a la API a través de la cuál se comparte utilizando el Protocolo de Autenticación de OAuth 2.0.

## 1. Configuración de LinkedIn Developer App

Se debe tener la aplicación LinkedIn Developer App para la empresa. ERPNext interactúa con esta aplicación para compartir los post. 

### 1.1 Creación de LinkedIn Developer App

Crear la Aplicación a través del siguiente link `https://www.linkedin.com/developers` completar todos los detalles y verificarla. La Aplicación tiene los siguientes productos.  

1. Compartir en LinkedIn
2. Iniciar Sesión con LinkedIn
3. Plataforma de Desarrollo de Marketing
![LinkedIn Developer App Product](/docs/assets/img/crm/linkedin-dev-products.png)

### 1.2 Configuración de URLs de Redireccionamiento:

1. Ir a la Aplicación LinkedIn Developers y luego a la pestaña **Auth**
2. En la sección **Configuraciones de OAuth 2.0**, agregar **URLs de Redireccionamiento**:
`https://{yoursite}/api/method/erpnext.crm.doctype.linkedin_settings.linkedin_settings.callback`
3. Hacer click en **Actualizar** para realizar los cambios. 
![LinkedIn Redirect URL](/docs/assets/img/crm/linkedin-redirect-urls.png)

## 2. Configuraciones de LinkedIn

Para acceder a las Configuraciones de LinkedIn ir a:
> Inicio > CRM > Configuraciones > Configuraciones de LinkedIn

![LinkedIn Settings](/docs/assets/img/crm/linkedin-settings.png)

### ID de la Empresa
El ID de la Empresa se consigue desde la URL de LinkedIn de la Empresa. 
![LinkedIn Company ID](/docs/assets/img/crm/linkedin-company-id.png)

### Clave de Cliente y Clave de Secreta de Cliente
Para obtener la **Clave de Cliente** y **Secreto de Cliente** de la cuenta de LinkedIn Developer ir a:
> `https://www.linkedin.com/developers/` > Mis aplicaciones > `{Your App}` > Auth

![LinkedIn Client](/docs/assets/img/crm/linkedin-client.png)

Una vez que se guarda el documento completando el **ID de la Empresa**, la **Clave de Cliente** y la **Clave de Secreta de Cliente** se redirigirá a la página de inicio de sesión de LinkedIn's, en la cual, al proveer las credenciales válidas de LinkedIn y hacer click en Autorizar, el usuario aprueba el pedido de la aplicación para acceder a sus datos de usuario e interactuar con LinkedIn en su nombre.
![Authorize LinkedIn](/docs/assets/img/crm/authorize-linkedin.jpg)

{siguiente}