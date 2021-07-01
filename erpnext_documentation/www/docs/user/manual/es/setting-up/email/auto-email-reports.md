<!-- add-breadcrumbs -->
# Reporte Automático por Correo Electrónico

**Los Reportes Automáticos por Correo Electrónico envían informes para el documento seleccionado.**

Se pueden configurar los **Reportes Automáticos por Correo Electrónico** para enviar informes en intervalos regulares. Estos deben ser informes guardados, de cualquier tipo (Generador de Informes, Script o Informe de Consultas).

Los Reportes Automáticos por Correo Electrónico pueden encontrarse en:

> Inicio > Configuración > Notificaciones de Correo Electrónico > Reporte Automático por Correo Electrónico

## 1. Creación de un Reporte Automático por Correo Electrónico

1. Ir al listado de Reporte Automático por Correo Electrónico y hacer click en Nuevo.
1. Seleccionar el Reporte para el cual se desean generar los correos.
1. Seleccionar el usuario para el cual se quiere crear este informe (se aplicarán los permisos para este usuario).
1. Configurar la Dirección de Correo Electrónico a la cual se desea enviar el informe y la frecuencia del mismo. Los Correos Electrónicos se enviarán a medianoche. La fecha se repetirá en caso de una frecuencia semanal/mensual/anual. Por ejemplo, si la fecha seleccionada es 7 y la frecuencia es mensual, el correo se enviará el día 7 de cada mes.  

 <img class="screenshot" alt="With Filters" src="{{docs_base_url}}/assets/img/setup/email/auto-email-2.png">
 
5. Guardar.

Se puede probar el informe haciendo click en "Descargar" o "Enviar Ahora". Aquí hay un ejemplo del email que se recibirá para un informe de libro mayor:

<img class="screenshot" alt="Report by Email" src="{{docs_base_url}}/assets/img/setup/email/auto-email-4.png">

## 2. Características

### 2.1 Filtrar datos

* **Enviar sólo si hay algún dato**: Si se encuentra habilitada, los emails no se enviarán si no hay datos en el reporte. 
* **Solo enviar registros actualizados en las últimas X horas**: Si se configura en 24, el correo contendrá solo registros actualizados en las últimas 24 horas. 
* **Número de Filas**: El número de filas a ser enviadas en el correo. El máximo es 500. 

### 2.2 Filtros de informe

Si el informe tiene filtros, éstos serán visibles. Hacer click en la tabla para editarla:

<img class="screenshot" alt="Edit Filters" src="{{docs_base_url}}/assets/img/setup/email/auto-email-3.png">

Por ejemplo, si el correo es para el informe "Resumen de Facturación del Proyecto" seleccionar el Proyecto. El rango de fechas aquí es el del "Resumen de Facturación del Proyecto".

### 2.3 Mensaje

También puede añadirse un mensaje para que sea enviado con el informe. Por ejemplo, "Éste es tu Resumen mensual de Facturación del Proyecto:"

También puede cambiarse el formato de archivo en el cual se crea el informe. Las opciones disponibles son HTML, XLSX, y CSV.

### 2. Temas Relacionados
1. [Boletín de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-digest)
1. [Seguimiento de Documentos](/docs/user/manual/es/setting-up/email/document-follow)
