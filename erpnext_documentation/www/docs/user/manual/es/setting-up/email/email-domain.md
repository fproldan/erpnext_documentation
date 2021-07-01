<!-- add-breadcrumbs -->
# Dominio de Correo Electrónico

**Un Dominio de Correo Electrónico es el nombre de la red/servicio que se está utilizando para la cuenta de correo electrónico.**

Se puede ir directamente a la creación de una [Cuenta de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-account) si se está utilizando alguno de los servicios enlistados [aquí](/docs/user/manual/es/setting-up/email/email-inbox#2-create-an-email-domain).

Se puede configurar el Dominio de Correo Electrónico en ERPNext para una fácil configuración de todas las Cuentas de Correo Electrónico. Para encontrar las configuraciones de Dominio de Correo Electrónico ir a:

> Inicio > Configuración > Notificaciones de Correo Electrónico > Dominio de Correo Electrónico

**¿Cúal es mi Dominio de Correo Electrónico?:** Puede ser que se haya comprado un servicio de Correo Electrónico al proveedor de internet o al proveedor de servicio de IT. Por ejemplo, si se accede al buzón con una URL como esta http://mail.empresa.com, entonces empresa.com es el dominio de email.

Si se quiere enviar y recibir mails en la cuenta ERPNext, se debe configurar correctamente un dominio de correo electrónico. Se puede estar utilizando servicios gratuitos de mail como Gmail o Yahoo. En este caso, no se necesita crear un dominio, simplemente se debe seleccionar el proveedor de servicio del listado. Sin embargo, quizás sea necesario permitir el acceso de ERPNext a la cuenta Gmail.

ERPNext crea una plantilla de dominio de Correo Electrónico utilizando ejemplo.com para referencia. Se deberá ingresar el nuevo dominio si se lo quiere usar en la cuenta ERPNext.

<img class="screenshot" alt="Email Domain" src="{{docs_base_url}}/assets/img/setup/email/email-domain.png">

## 1. Creación de un Dominio de Correo Electrónico
1. Ir al listado de Dominio de Correo Electrónico y hacer click en Nuevo.
1. Ingresar la Dirección de correo electrónico de ejemplo. Aquí es donde se ingresa la dirección de correo de la empresa. Por ejemplo si el ID de correo electrónico es empresa@nombredelaempresa.com, eso es lo que se debería ingresar.
1. Servidor de Correo Electrónico. Esta es la URL del servidor de mail o del servicio de email que se ha comprado. Por ejemplo, puede ser mail.empresa.com o imap.empresa.com. 
1. Usar IMAP. IMAP y POP son dos servicios utilizados por la mayoría de servidores para correos electrónicos entrantes. Si el servidor de Correo Electrónico de la empresa permite IMAP para emails entrantes, tildar esta opción. 
1. Utilizar SSL. Si el servidor de email de la empresa usa comunicación SSL (Secure Socket Layer) se deberá tildar esta opción. 

    **¿Tiene la empresa SSL?:** Puede ser que la empresa haya comprado un certificado SSL del proveedor de servicios de IT, y puede ser que hayan instalado SSL para el servidor de email. Si se utiliza 'https' al acceder al servidor de correos electrónicos desde el navegador, entonces puede ser que la empresa cuente con una configuración SSL.

1. Usar SSL para saliente. Si el servidor de correo usa SSL para salientes, tildar esta opción para usar SSL de forma explícita para emails salientes. El puerto predeterminado es 465.

1. Agregar correos electrónicos a la carpeta de enviados. Si no se están utilizando servidores provistos por Gmail u otros servicios similares, puede ser necesario tildar esta opción para añadir todos los correos salientes a la bandeja de entrada de la cuenta de email. (Recomendado para servidores de email como Zimbra y CPanel).

1. Límite Adjunto (MB). Se puede limitar el tamaño de los archivos adjuntos en emails enviados desde ERPNext.

1. El Servidor SMTP es el servicio de correos electrónicos salientes del servidor. 

1. Seleccionar el campo Usar TLS si el servidor SMTP admite TLS para seguridad.

1. Puerto. El servicio SMTP usualmente se configura en el puerto 25. Si el servidor de email está configurado en un número de puerto distinto, se puede configurar aquí. 

### 1.1 Luego de guardar el dominio

Luego de hacer click en guardar, éstas configuraciones son validadas por ERPNext y el Dominio de Correo Electrónico es guardado. A veces esto toma algunos segundos así que es posible que haya que esperar. Este dominio de correo estará luego disponible en un menú desplegable llamado Dominio, en la pantalla de Cuentas de Correo Electrónico. 

![Email domain in email account](/docs/assets/img/setup/email/email-domain1.png)

#### ¿Se ingresó todo pero no se puede configurar el Dominio de Correo Electrónico?

Si se han ingresado y verificado todas las configuraciones explicadas anteriormente pero todavía no se logra configurar el Dominio de Correo Electrónico, se puede contactar con soporte de ERPNext, dentro de la cuenta, para recibir ayuda. 

### 2. Temas Relacionados
1. [Cuenta de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-account)
1. [Bandeja de Entrada de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-inbox)
