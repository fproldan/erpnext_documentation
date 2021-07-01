<!-- add-breadcrumbs -->
# Errores de Correo electrónico

En ERPNext, se puede personalizar la Pasarela de Enlace de Entrada y Salida. Al guardar una Cuenta de Correo electrónico, ERPNext intenta establecer una conexión con la pasarela de enlace de email. Si la cuenta ERPNext logra conectarse, entonces la Cuenta de Correo electrónico se guarda exitosamente. Si no, puede ser que se reciba un error como se muestra a continuación.  

<img class="screenshot" alt="Email Error" src="{{docs_base_url}}/assets/img/articles/email-error.png">

Esto indica que, utilizando las credenciales de inicio de sesión y otros detalles de la pasarela de enlace de email provistos en la Cuenta de Correo electrónico, ERPNext no puede conectarse con el servidor de email. En este punto es necesario asegurarse de haber ingresado credenciales de correo válidas para la Pasarela de Enlace de Email. Una vez configurada la Cuenta de Correo electrónico exitosamente, se deberá poder enviar y recibir emails sin problema desde la cuenta ERPNext.

Observación: La cuenta ERPNext está conectada de forma predeterminada con un servidor de correo de ERPNext. Si no se desea usar otro servidor, se pueden enviar correos utilizando el servidor de ERPNext, sin que se requiera ninguna configuración en la Cuenta de Correo electrónico. 
