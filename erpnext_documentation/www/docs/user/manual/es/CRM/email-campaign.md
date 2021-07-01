<!-- add-breadcrumbs -->
# Campaña Vía Correo Electrónico

**Una Campaña Vía Correo Electrónico es un conjunto de emails enviados a clientes potenciales o contactos de acuerdo a un cronograma en particular.**

Las Campañas Vía Correo Electónico siguen siendo una de las formas más efectivas de llegar a los Clientes, Contactos o Cliente Potenciales y mantenerlos involucrados. Por ejemplo, se puede configurar una Campaña Vía Correo Electrónico para hacer llegar el producto a los clientes, usando cada mail para revelar un aspecto interesante del mismo.  

Para crear una Campaña Vía Correo Electrónico ir a:

 > Inicio > CRM > Campaña > Campaña Vía Correo Electrónico

## 1. Prerrequisitos

Antes de crear y utilizar una Campaña Vía Correo Electrónico primero debe crearse lo siguiente: 

* [Campaña](/docs/user/manual/es/CRM/campaign)
* [Cliente Potencial](/docs/user/manual/es/CRM/lead) o [Contacto](/docs/user/manual/es/CRM/contact) o [Grupo de Email](/docs/user/manual/es/CRM/email_group)

## 2. Creación de una Campaña Vía Correo Electrónico

1. Ir al listado de Campaña Vía Correo Electrónico y hacer click en Nueva.
2. Seleccionar la [Campaña](/docs/user/manual/es/CRM/campaign) para la cual se desea configurar una Campaña Vía Correo Electrónico.
3. Configurar la "Fecha de Inicio" para la Campaña Vía Correo Electrónico.
4. En "Campaña Vía Correo Electrónico Para", seleccionar si se quiere armar la Campaña para un cliente Potencial, un Contacto o para un Grupo de Email para enviar a muchos contactos.
5. En "Receptor", seleccionar el Cliente Potencial, Contacto o Grupo de Email respectivo para el cuál se desea iniciar la Campaña Vía Correo Electrónico.
6. En "Emisor", seleccionar el usuario del sistema que será emisior de los correos electrónicos. 
7. Guardar

    <img class="screenshot" alt="Email Campaign" src="{{docs_base_url}}/assets/img/crm/email-campaign.png">

La Campaña Vía Correo Electrónico mostrada anteriormente es para la siguiente Campaña: 

    <img class="screenshot" alt="Campaign Schedule" src="{{docs_base_url}}/assets/img/crm/campaign-email-schedule.png">

**Observación**: El campo **Enviar Luego De (días)** presente en la sección Campaña especifica el día en el cuál se enviará el mail, de acuerdo con la **Fecha de Inicio** de la **Campaña Vía Correo Electrónico**. Observar la "Fecha de finalización" en la Campaña Vía Correo Electrónico mostrada más arriba. Es "26-07-2019", la cuál es 4 días luego de la  "Fecha de inicio", "22-07-2029", debido a que el cronograma de la Campaña termina en el día numero 4.

### 2.1 Creación de múltiples Campañas Vía Correo Electrónico para una Campaña

También se pueden crear nuevas Campañas Vía Correo Electrónico para Clientes Potenciales o Contactos para la misma Campaña a través del Tablero de Campaña.

1. Ir a la Campaña para la cuál se desean crear las Campañas Vía Correo Electrónico.
2. Hacer click en el + frente a Campañas Vía Correo Electrónico para crear una Nueva Campaña Vía Correo Electrónico para la Campaña. 

    <img class="screenshot" alt="Email Campaigns from Dashboard" src="{{docs_base_url}}/assets/img/crm/email-campaigns-from-dash.png">

## 3. Características

### 3.1 Comunicación Vinculada 

Cuando se envían los mails a los respectivos clientes potenciales o contactos, la Comunicación se vincula con el documento de la Campaña Vía Correo Electrónico. Se pueden ver todos los correos electrónicos enviados en el documento. 

<img class="screenshot" alt="Linked Communication" src="{{docs_base_url}}/assets/img/crm/email-campaign-linked-comm.png">

### 3.2 Darse de baja de Campañas Vía Correo Electrónico

Si un cliente potencial o contacto no quiere seguir recibiendo correos electrónicos respecto a una campaña, puede darse de baja de la campaña vía correo electrónico haciendo click en el link de baja enviado junto con el mail. 

<img class="screenshot" alt="Unsubscribe link" src="{{docs_base_url}}/assets/img/crm/unsubscribe-link.png">

Cuando un cliente potencial o contacto se da de baja, el estado del documento de la Campaña Vía Correo Electrónico cambia a "Dada de Baja".

<img class="screenshot" alt="Unsubscribed" src="{{docs_base_url}}/assets/img/crm/email-campaign-unsubscribed.png">

### 3.3 Utilizar los campos Cliente Potencial o Contacto en la Plantilla de Email. 

 La Plantilla de Email tiene el contexto del documento que se ha especificado en el campo "Campaña vía Correo Electrónico Para". Si se desea mostrar los campos de los documentos de Cliente Potencial o Contacto en la Plantilla de Email se deberá usar `doc.nombredelcampo` para ello.
 Por ejemplo, si "Campaña vía Correo Electrónico Para" es "Contacto", se puede mencionar el "nombre" del Contacto en `doc.nombre` en la Plantilla de Email como se muestra a continuación:

<img class="screenshot" alt="Email Template Document" src="{{docs_base_url}}/assets/img/crm/email-template-doc.png">

De esta forma, los correos electrónicos enviados se verán asi: 

<img class="screenshot" alt="Email Campaign Doc Data" src="{{docs_base_url}}/assets/img/crm/email-campaign-doc-data.png">

### 3.4 Estado

El Estado indica en que estado se encuentra la Campaña vía Correo Electrónico, y puede ser: 

- **Programada**: Cuando la Campaña vía Correo Electrónico no ha empezado pero está programada en una "Fecha de Inicio" futura.
- **En Proceso**: La campaña figurará como "En Proceso" entre la "Fecha de Inicio" y la "Fecha de Finalización" de la campaña.
- **Completa**: Luego de la "Fecha de Finalización" de la campaña, el estado será modificado a "Completa".
- **Dada de Baja**: Cuando el Cliente Potencial o Contacto se da de baja de la Campaña.

    <img class="screenshot" alt="Email Campaign Status" src="{{docs_base_url}}/assets/img/crm/email-campaign-status.png">

## 4. Temas Relacionados
1. [Campaña](/docs/user/manual/es/CRM/campaign)
1. [Iniciativa](/docs/user/manual/es/CRM/lead)
1. [Contacto](/docs/user/manual/es/CRM/contact)
