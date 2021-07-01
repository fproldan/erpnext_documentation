# Plantilla de Correo Electrónico

Cada correo enviado es diferente, pero algunos pueden estar estandarizados y se los conoce como Plantilla de Correo Electrónico o Respuesta Estándar. 

Para acceder al listado de Plantilla de Correo Electrónico ir a:
> Inicio > Configuración > Notificaciones de Correo Electrónico > Plantilla de Correo Electrónico

## 1. Creación de una Plantilla de Correo Electrónico

1. Ir al listado de Plantilla de Correo Electrónico y hacer click en Nuevo.
1. Ingresar un Nombre para esta Plantilla de Correo Electrónico.
1. Ingresar un Asunto para esta Plantilla de Correo Electrónico.
1. Respuesta es el contenido estándar del correo que será parte de esta plantilla. 
1. Guardar.

<img class="screenshot" alt="Email Template" src="{{docs_base_url}}/assets/img/setup/email/email-template-example.png">

**DocType Asociado:** (opcional) El DocType asociado con esta plantilla.

### 1.1 Uso de la Plantilla de Correo Electrónico

Se puede utilizar esta Plantilla de Correo Electrónico en los que se envían desde ERPNext en campo "CC, BCC & Plantilla de Correo Electrónico" de la sección correo del documento. ERPNext tomará el asunto y la respuesta de acuerdo con la plantilla seleccionada. 

Se puede seleccionar una plantilla por defecto para cada document desde [Personalizar formulario](/docs/user/manual/es/customize-erpnext/customize-form).

### 1.2 Obtención de los nombres de los campos

Los nombres de los campos que pueden usarse en la plantilla son los del documento desde el cual se está enviando el correo. Se pueden encontrar los campos de cada documento a través de Personalización > Personalización de formularios > Personalizar Formulario y seleccionando el tipo de documento (ej: Orden de Venta)

### 1.3 Plantillas

Las plantillas son compiladas utilizando Jinja. Para aprender más respecto a Jinja, visitar esta [página](https://jinja.palletsprojects.com/en/2.10.x/).

## 2. Temas Relacionados
1. [Cuenta de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-account)
1. [Bandeja de Entrada de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-inbox)
