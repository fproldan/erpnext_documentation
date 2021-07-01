<!-- add-breadcrumbs -->

# Procesamiento de Estados de cuentas

**Procesamiento de Estados de cuentas es una herramienta que ayuda a enviar Estados de cuentas (Balance general) y de Antigüedad (resumen de Cuentas por cobrar) en formato PDF a los Clientes de forma masiva por medio de correo electrónico de forma periódica ya sea manual o automáticamente.**

Esta funcionalidad es útil si se desea enviar actualizaciones por correo electrónico a Clientes de forma periódica respecto a sus transaciciones (como Facturas de venta). El PDF adjunto que se envía para cada Cliente contiene detalles como la fecha de contabilidad de la factura, el número de la Factura de venta, detalles del débito y el crédito, etc. relevantes sobre su contabilidad.

El propósito de esta funcionalidad es recordar a varios clientes que tienen facturas impagas.

Para acceder a la lista de **Procesamiento de Estados de cuentas** se puede buscar en la barra de navegación o ir a:

> Inicio > Contabilidad > Herramientas > Procesamiento de Estados de cuentas

## 1. Prerrequisitos

1. La herramienta utiliza las direcciones de correo de los clientes para enviarles los reportes. Si no se encuentra este dato en el Contacto del Cliente la herramienta no permitirá seleccionar dicho Cliente, por lo que es importante asegurarse de que los siguientes datos están completos.

    - Correo Electrónico de Facturación del Cliente: este dato es obligatorio y puede definirse en el [Contacto del Cliente](/docs/user/manual/es/CRM/contact#1-how-to-create-a-contact) tildando la opción "Es contacto de facturación".
    - Correo electrónico de contacto principal del Cliente: no es obligatorio a menos que se tilde la opción "Enviar a contacto principal".

2. Configurar la Cuenta de correo electrónico con la opción "Habilitar correos salientes". Más información al respecto [aquí](/docs/user/manual/es/setting-up/email/email-account).


## 2. Creación de una entrada de Procesamiento de Estados de cuentas

1. Ir a la lista de "Procesamiento de Estados de cuentas" y hacer click en Nuevo.

2. Ingresar un nombre para la entrada, para referencia futura.

3. Establecer los filtros para los estados que serán enviados a los Clientes.
    
    - Los filtros "Desde la fecha" y "Hasta la fecha" se ocultarán y auto-completarán al tildar la opción "Habilitar correo electrónico automático".
    - "Proyecto" y "Centro de costos" son [campos de opción múltiple](/docs/user/manual/en/customize-erpnext/articles/table-multiselect-field), es decir, que se puede seleccionar más de uno en cada filtro.

    <img class="screenshot" src="{{docs_base_url}}/assets/img/accounts/psoa-name_and_filters.png">
    
4. En la sección "Clientes" se debe seleccionar uno por cada fila de la tabla y se traerán sus direcciones de correo primaria y de facturación. 

    - El campo "Seleccionar clientes por" permite traer Clientes de forma masiva agrupandolos por "Categoría de Cliente", "Territorio", "Socio de ventas" y "Persona de ventas". Luego de seleccionar la opción deseada se debe hacer click en el botón "Obtener clientes". 
    - En agrupaciones de árbol como "Territorio", "Persona de ventas" y "Categoría de Cliente" también se considerarán los Clientes que posean los valores hoja de estas estructuras. Por lo que si se elige "Argentina" como territorio, serán seleccionados todos los clientes con ese valor y los que tengan valores ubicados bajo esta rama del árbol.
    - La opción "Enviar a contacto principal" enviará el estado de cuentas a la dirección de correo primaria de los Clientes además de a la de facturación.

    <img class="screenshot" src="{{docs_base_url}}/assets/img/accounts/psoa-customers.png"><br>

5. En la sección "Preferencias de impresión" se pueden configurar los aspectos:

    - Orientación del PDF, ya sea "Horizontal" o "Vertical".
    - Si se desea o no ver el reporte de antigüedad (resumen de Cuentas por cobrar) el cual muestra el importe de "envejecimiento" de comprobantes (como Facturas de venta) de los últimos 30/60/90/120 días, basándose en la "Fecha de pago" o la "Fecha de contabilidad".

    <img class="screenshot" src="{{docs_base_url}}/assets/img/accounts/psoa-print.png">

6. En la sección "Configuración de Correo Electrónico" se puede configurar cómo se quiere enviar el correo. Hay dos subsecciones:

    <img class="screenshot" src="{{docs_base_url}}/assets/img/accounts/psoa-auto-email.png">
    
    - Al seleccionar "Habilitar correo electrónico automático" aparecerán opciones para enviar los reportes de forma periódica.
     - Se puede determinar la "Frecuencia" con la cual se enviarán los correos luego de la "Fecha de inicio". Las opciones son "Semanal", "Mensual" y "Trimestral".
     - También se puede seleccionar la "Duración del filtro (meses)". Por ejemplo, si se configura en 3, se enviarán los reportes de los últimos tres meses contando desde la fecha actual (es decir, en la que el correo es enviado).
    - Estos correos no son enviados de inmediato, sino a medianoche con un proceso en segundo plano.
    - Después de esto se pueden completar los campos "Asunto", "CC para" y "Cuerpo". Si no se completan, se usarán datos predefinidos.
    
    <img class="screenshot" src="{{docs_base_url}}/assets/img/accounts/psoa-email-default-content.png">

7. Guardar.

Si se configuró el envío automático entonces se deberá esperar a que se ejecute, sino se debe hacer click en el botón "Enviar correo electrónico".

## 3. Funcionalidades

### 3.1 Descargar PDF consolidado de todos los Clientes

Al crear una entrada, se ve un botón "Descargar" el cual permite ver el reporte de todos los Clientes. Se puede usar para revisar antes de enviar.

### 3.2 Enviar correos manualmente

Al crear una entrada, se ve un botón "Enviar correo electronico" con el cual los correos son puestos en cola en los trabajos en segundo plano, cuyo progreso se puede chequear ingresando a "Correos electrónicos en cola". Esto se puede realizar incluso si se tildó la opción "Habilitar correo electrónico automático".

<img class="screenshot" src="{{docs_base_url}}/assets/img/accounts/psoa-buttons.png">

### 3.3 Uso de valores dinámicos en el asunto y cuerpo del correo

Se puede usar etiquetas para aplicar estos valores dinámicos desde:

- El Cliente al cual se enviarán los correos, usando la palabra clave "customer" 
- Cualquier campo seleccionado en el Procesamiento de Estados de cuentas usando la palabra clave "doc"
- Cualquier método en [`frappe.utils`](https://github.com/frappe/frappe/blob/develop/frappe/utils/__init__.py) usando la palabra clave "frappe"

Pueden ser usados como se muestra a continuación:

<img class="screenshot" src="{{docs_base_url}}/assets/img/accounts/psoa-template.png">

Correo:

<img class="screenshot" src="{{docs_base_url}}/assets/img/accounts/psoa-email.png">

Reporte en PDF:

<img class="screenshot" src="{{docs_base_url}}/assets/img/accounts/psoa-report.png">

## 4. Temas relacionados
1. [Configuración de una cuenta de correo electrónico](/docs/user/manual/es/setting-up/email/email-account)
1. [Creación de Contacto de Cliente](/docs/user/manual/es/CRM/contact#1-how-to-create-a-contact)
1. [Contacto](/docs/user/manual/es/CRM/contact)
