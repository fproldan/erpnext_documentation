<!--add breadcrumbs-->
# Descarga de Datos Personales

Como parte de cumplimiento de GDPR, ERPNext cuenta con la funcionalidad de Descarga de Datos Personales.

La herramienta de descarga de datos personales permite a un usuario descargar automáticamente todos los datos personales que se han generado utilizando ERPNext. Esto incluye datos personalmente identificables de la cuenta de usuario como: nombre de usuario, nombre completo, fecha de nacimiento, números de teléfono, número de teléfono celular, ubicación, intereses, biografía, firma digital, Dirección de correo electrónico, Contacto, Dirección, Comunicación, etc. También incluye los datos de Iniciativas y Oportunidades, los detalles que se hayan guardado como números de teléfono, números de teléfono celular, fax, sitio web, y nombre. 
## 1. Solicitud de Desacarga de Datos de Usuario

1. Para comenzar la descarga de datos, el usuario debe estar **conectado** e ingresar a [nombre-instancia]/request-data (ejemplo: erpnext.com/request-data) en el campo URL.

    <img class="screenshot" alt="Request Data" src="{{docs_base_url}}/assets/img/setup/personal-data-download-request/request-data-webform.png">

2. Luego de enviar el pedido, se recibirá una respuesta de éxito.
    
    <img class="screenshot" alt="Request Data" src="{{docs_base_url}}/assets/img/setup/personal-data-download-request/download-request-succes.png">

3. Esto enviará un email con un link de descarga de los datos a la dirección de correo asociada con el usuario. 
    
    <img class="screenshot" alt="Download Data Email" src="{{docs_base_url}}/assets/img/setup/personal-data-download-request/download-data-email.png">

El archivo disponible para descarga estará en formato JSON.

## 2. DocType de Solicitud de Descarga de Datos Personales

Este pedido también está registrado en el DocType "Pedido de Descarga de Datos Personales", el archivo-link que es enviado al usuario vía email, también está adjuntado al doc. Buscar Solicitud de Descarga de Datos Personales en la barra de búsqueda. 

<img class="screenshot" alt="Personal Data Download Request Doctype" src="{{docs_base_url}}/assets/img/setup/personal-data-download-request/personal-data-download-request-doctype.png">

## 3. Temas Relacionados
1. [Eliminación de Datos Personales](/docs/user/manual/es/setting-up/personal-data-deletion)
