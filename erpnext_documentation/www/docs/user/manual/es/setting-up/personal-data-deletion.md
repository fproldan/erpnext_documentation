<!--add breadcrumbs-->
# Eliminación de Datos Personales

Como parte del cumplimiento de GDPR, ERPNext tiene Eliminación de Datos Personales.

La herramienta de eliminación de datos personales permite al usuario anonimizar todos los datos personalmente indentificables, que el mismo ha generado utilizando ERPNext. Es decir, los datos personalmente identificables serán aleatorizados. Esto incluye datos personales de la cuenta de usuario como: nombre de usuario, nombre completo, fecha de nacimiento, números de teléfono, número de teléfono celular, ubicación, intereses, biografía, firma digital, Dirección de correo electrónico, Contacto, Dirección, Comunicación, etc. También incluye los datos de Iniciativas y Oportunidades, los detalles que se hayan guardado como números de teléfono, números de teléfono celular, fax, sitio web, y nombre.

Sin embargo, esto excluye datos que sean requeridos legalmente para mantener un negocio. 

## 1. Solicitud de Eliminación de Datos de Usuario

1. Para comenzar a borrar datos personalmente identificables, se debe ingresar a [nombre-instancia]/request-to-delete-data (ejemplo: ejemplo.erpnext.com/request-to-delete-data) en el campo URL.

    <img class="screenshot" alt="Request Data Webform" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/request-to-delete-data-webform.png">

2. Ingresar el correo electrónico asociado con la cuenta ERPNext. Luego de enviar el pedido, se recibirá una respuesta de éxito.

    <img class="screenshot" alt="Deletion Request Success" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/deletion-request-success.png">

3. Esto enviará un correo con un enlace de verificación para borrar datos, a la dirección asociada con el usuario. 

    <img class="screenshot" alt="Verification Email" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/verification-email.png">

4. Cuando el usuario hace click en el enlace de verificación se muestra un mensaje de confirmación. 
    
    <img class="screenshot" alt="Confirmed Verification" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/confirmed-verification.png">

## 2. Eliminación de datos personales del usuario 

El pedido para eliminar datos es registrado en el doctype "Solicitud de Eliminación de Datos Personales".

<img class="screenshot" alt="Personal Data Download Request Doctype" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/personal-data-deletion-request-doctype.png">

Este doctype posee tres estados para completar el proceso de eliminación de datos del usuario.

### 2.1 Verificación Pendiente

Este estado indica que el usuario ha slicitado la eliminación de datos a través del formulario web. Sin embargo, la verificación de este pedido está pendiente. Buscar Solicitud de Eliminación de Datos Personales desde la barra de búsqueda.

<img class="screenshot" alt="Pending Verification" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/pending-verification.png">

### 2.2 Aprobación Pendiente

Esto indica que el usuario ha verificado el pedido vía email. Esto habilita la opción de "Eliminar Datos" para los Administradores de Sistema. 

<img class="screenshot" alt="Pending Approval" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/pending-approval.png">

### 2.3 Eliminado

Esto indica que el Administrador de Sistema ha hecho click en el botón "Eliminar Datos". Esto significa que los datos personalmente identificables del usuario han sido anonimizados. 

<img class="screenshot" alt="Deleted User" src="{{docs_base_url}}/assets/img/setup/personal-data-deletion-request/deleted-user.png">

## 3. Temas Relacionados
1. [Descarga de Datos Personales](/docs/user/manual/es/setting-up/personal-data-download)

