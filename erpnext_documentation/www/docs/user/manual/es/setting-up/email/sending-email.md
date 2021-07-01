<!-- add-breadcrumbs -->
# Envío de Correos Electrónicos desde cualquier Documento

En ERPNext se puede enviar cualquier documento por correo (como adjunto en PDF), haciendo click en Menú > Correo Electrónico.

<img class="screenshot" alt="Send Email" src="{{docs_base_url}}/assets/img/setup/email/send-email.gif">

**Observación:** Se debe contar con [Cuentas de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-account) salientes configuradas para esto.

Luego de hacer click en enviar, el correo se añade a la lista para enviar. Se encontrará en el estado Enviando hasta que sea Enviado. El estado del correo se ve en la lista, si el envío falla, se puede enviar haciendo click en Enviar Ahora. 

![Email Queue](/docs/assets/img/setup/email/email-queue.png)

Se encuentran disponibles las siguientes opciones al enviar un Correo Electrónico.

* **CC**: copia del correo. Útil cuando se desea mantener a alguien en el hilo de la conversación pero no se busca dirigir el mismo a ellos específicamente. 
* **BCC**: copia oculta, es similar a CC pero las otras personas presentes en el hilo no pueden ver que el correo electrónico también fue enviado a quienes están en BCC. Esto resulta útil para esconder ciertas direcciones de correo electrónico si se está enviando a muchas personas que no necesariamente se conocen.
* **Plantilla de Correo Electrónico**: Se pueden crear plantillas preestablecidas para enviar respuestas estándar. Las Plantillas de Correo Electrónico ya están disponibles en el sistema para Notificación de Envío, Notificación de Estado de Licencia, y Notificación de Aprobación de Licencia. 
* **Enviarme una copia**: se enviará una copia a la dirección de correo emisora. Esto resulta útil para asegurar que haya sido enviado sin errores.
* **Enviar confirmación de lectura**: Si se selecciona esta casilla, se recibirá una notificación si el receptor leyó el correo. En caso de muchos receptores, inclusive si solo uno lo leyó, se recibirá la notificación. 
* **Adjuntar impresión del documento**: Adjuntar PDF del documento que se está enviando. 
* **Seleccionar adjuntos**: Cualquier otro archivo adjunto adicional puede ser añadido aquí.

Los dos campos siguientes aparecen en la pantalla de impresión: 

![Email Print Options](/docs/assets/img/setup/email/email-print-options.png)

* **Seleccionar formato de impresión**: El formato de impresión del documento. Más información al respecto [aquí](/docs/user/manual/es/setting-up/print/print-format).
* **Seleccionar idioma**: El idioma en el cual se generará el PDF.

### Temas Relacionados
1. [Dominio de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-domain)
1. [Cuenta de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-account)
1. [Bandeja de Entrada de Correo Electrónico](/docs/user/manual/es/setting-up/email/email-inbox)
