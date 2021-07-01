<!-- add-breadcrumbs -->
# Vinculación de Correos Electrónicos a Documentos

**Un correo electrónico puede vincularse a múltiples documentos en ERPNext.**

Esto puede hacerse de las siguientes dos maneras:

- Incorporación de Correo Electrónico en Contacto, Cliente, Proveedor.
- Vinculación Automática de Correo Electrónico.

## 1. Incorporación de Correo Electrónico para Cliente y Proveedor

La Incorporación de Correo Electrónico se realiza en Contacto, Cliente, y Proveedor. Todos los correos enviados o recibidos de un Contacto pueden ser vistos en la Línea de Tiempo de ese contacto, así como también en la Línea de Tiempo del Cliente o Proveedor vinculados con ese Contacto. Para incorporar Correos Electrónicos, hacer lo siguiente: 

1. En un Contacto, añadir Links para el Cliente o Proveedor respectivamente.

    <img class="screenshot" alt="Add Customer/Supplier in Contact" src="{{docs_base_url}}/assets/img/setup/email/contact-link.png">

1. Ahora bien, cuando un Correo Electrónico es enviado a o recibido del Contacto asociado con el Cliente o Proveedor, ese correo se vincula al Cliente o Proveedor mencionado en la sección Enlaces del Contacto. 

    <img class="screenshot" alt="With Filters" src="{{docs_base_url}}/assets/img/setup/email/email_aggregation.gif">

## 2. Vinculación Automática de Correo Electrónico a un Documento

La Vinculación Automática de Correos Electrónicos relaciona un Correo al Documento especificado en la Dirección de Correo Electrónico única, generada por el sistema para un documento. Si un correo es enviado o recibido utilizando esa Dirección de Correo Electrónico única, el sistema lo vinculará al Documento. 

1. Habilitar la Vinculación Automática de Correo Electrónico en la Cuenta de Correo Electrónico. Esta funcionalidad puede utilizarse únicamente con una Cuenta de Correo Electrónico a la vez. 

    <img class="screenshot" alt="Add Customer/Supplier in Contact" src="{{docs_base_url}}/assets/img/setup/email/enable_email_link.png">

1. Una vez que esta funcionalidad está habilitada, se verá un ID de Correo Electrónico único, el cual fue generado utilizando el ID mencionado en la Cuenta. 

1. Ahora se puede copiar el ID de Correo Electrónico haciendo click sobre el mismo, así como también enviar o recibir correos utilizando el ID de Correo Electrónico único. Si un correo contiene este ID de Correo Electrónico único, ya sea en la sección Receptores, CC o BCC, el sistema vinculará ese Correo Electrónico al Documento especificado. 

    <img class="screenshot" alt="Add Customer/Supplier in Contact" src="{{docs_base_url}}/assets/img/setup/email/email_link.gif">

### 3. Temas Relacionados
1. [Reporte de Correo Electrónico Automático](/docs/user/manual/es/setting-up/email/auto-email-reports)
1. [Enviar Correo Electrónico desde cualquier Documento](/docs/user/manual/es/setting-up/email/sending-email)
1. [Seguimiento de Documento](/docs/user/manual/es/setting-up/email/document-follow)
