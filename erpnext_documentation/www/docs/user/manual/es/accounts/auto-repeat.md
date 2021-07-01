<!-- add-breadcrumbs -->
# Repetición automática

La Repetición automática ayuda a crear ciertos documentos de forma automática en un determinado período de tiempo.


Por ejemplo: en el caso de que se realice el seguimiento de gastos diferidos para ciertos productos. Esto requiere que se cree el mismo Asiento contable todos los meses para acreditar en la cuenta de Gastos diferidos y debitar en la de Gastos. Para esto se puede crear el primer Asiento contable de forma manual y después crear una repetición automática para ese documento.

Para acceder a la Repetición automática, ir a:
> Inicio > Configuración > Automation > Repetición automática

## 1. Configuración de la repetición automática

### 1.1 Configurar la repetición automática
1. Ir al listado de Repetición automática y hacer click en Nuevo.
2. Seleccionar el Tipo de Documento de Referencia, como Asiento contable, Factura de venta, etc.
3. Seleccionar el Documento de referencia. Este es el docmuento específico que se desea repetir.
4. Definir la Fecha de inicio y la Fecha Final (opcional).
   Si no se selecciona una Fecha Final, se crearán documentos de forma indefinida, hasta que la repetición sea deshabilitada.
5. Establecer la frecuencia para la creacion de los documentos (Diario, Semanal, Mensual, Trimestral, Semestral, Anual).
6. Guardar.

### 1.2 Configurar la repetición automática desde el documento
También se puede activar la repetición automática haciendo click en la opción **Repetir** dentro de **Menú**.

**Nota**: si un documento ya está en repetición automática, la opción Repetir ya no estará disponible.

<img class="screenshot" alt="Allow Auto Repeat" src="/docs/assets/img/automation/repeat-option.png">

Una vez que se hace click en Repetir, aparecerá un cuadro donde se deberá completar los datos y hacer click en Guardar.

<img class="screenshot" alt="Auto Repeat Prompt" src="/docs/assets/img/automation/auto-repeat-prompt.png">

## 2. Características

### 2.1 Notificar por Email
Si se desea notificar a ciertos contactos cuando los documentos son creados, se puede tildar la opción "Notificar por Email" en la sección Notificación. Así se enviará el documento generado automáticamente a las direcciones de correo electrónico especificadas. Los campos que se deben completar se explican a continuación:

- **Destinatarios**: aquí se definen las direcciones de correo a las cuales se notificará.
- **Obtener Contactos**: este botón traerá los contactos vinculados al documento para el cual se creó la repetición automática y completará el campo Destinatarios.
- **Plantilla**: se puede seleccionar una plantilla para el email, con la cual se completará automáticamente el Asunto y el Mensaje.
- **Asunto**: asunto del correo (ejemplo: Factura creada exitosamente).
- **Mensaje**: mensaje del email.
- **Vista previa**: con este botón se podrá ver una vista preliminar del correo.
- **Formatos de Impresión**: seleccionar un formato de impresión para definir el diseño del correo que se enviará al Cliente.

> **Nota**: si el documento que se configura para Repetición automática necesita validación, asegurarse de tildar la opción "Permitir la impresión de borradores" en [Ajustes de impresión](/docs/user/manual/es/setting-up/print/print-settings) para poder realizar el envío por correo del documento. Si esta opción no está habilitada, se notificará sobre la creación pero sin el documento adjunto.

### 2.2 Repetir en un día específico
Si la frecuencia es Mensual, Trimestral, Semestral o Anual, entonces se crearán documentos en el mismo día que la "Fecha de inicio" de la repetición. Si se desea crear documentos en otro día, se puede configurar siguiendo los siguientes pasos:

- **Repetir el día**: día del mes en el cual se deberá crear el documento. Por ejemplo, si la frecuencia es mensual y en este campo se ingresa 7, entonces el documento se generará el día 7 de cada mes.
- **Repetir el último día del mes**: esta opción está disponible ya que el último día de cada mes no siempre es el mismo. Por ejemplo, en año bisiesto el último día de Febrero es el 29, cuando el resto del tiempo es el 28. Si se tilda esta opción, los documentos se crearán en el úlimo día correspondiente de cada mes.

### 2.3 Tablero
Se puede ver el cronograma de repetición automática en el tablero de cada repetición. Si no se especifica una Fecha final el cronograma mostrará solo la próxima fecha.

<img class="screenshot" alt="Allow Auto Dashboard" src="/docs/assets/img/automation/auto-repeat-dashboard.png">

### 2.4 Frecuencia de repetición en la barra lateral
Cuando un documento está en Repetición automática se puede ver la frecuencia de repetición en la barra lateral del mismo.
Se puede hacer click en el estado para ver los documentos repetidos vinculados.

<img class="screenshot" alt="Auto Repeat Frequency" src="/docs/assets/img/automation/auto-repeat-frequency.png">

### 2.5 Deshabilitar la Repetición automática
Si se tilda esta opción se detendrá la creación de documentos y se desvinculará la Repetición automática del documento de Referencia.
