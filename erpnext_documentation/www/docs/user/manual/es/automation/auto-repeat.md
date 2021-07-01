<!-- add-breadcrumbs -->
# Repetición Automática

La función de Repetición Automática permite crear ciertos documentos de forma automática en un determinado período de tiempo. 

Se puede Personalizar cualquier Formulario para hacer que los documentos sean **repetibles**.

Por Ejemplo: Asumamos que se utiliza el sistema de gasto diferido para algunos ítems. Se debe crear el mismo Asiento de Libro Diario todos los meses para acreditar la cuenta de Gasto Diferido y debitar la Cuenta de Gastos. Se puede crear el primer Asiento de forma manual para esto, y luego crear una transacción de repetición automática para el mismo. 

Para acceder a Repetición Automática, ir a:
> Inicio > Configuraciones > Automatización > Repetición Automática

## 1. Cómo Configurar Repetición Automática

### 1.1 Personalizar el Formulario
1. Ir a: **Inicio > Personalización > Personalización de Formulario > Personalizar Formulario**.
2. Seleccionar el formulario en el cuál se desea permitir la creación de documentos repetibles.
3. Hacer click en 'Permitir Repetición Automática' para permitir la creación de documentos repetibles para ese Formulario. Esto es necesario para que el tipo de documento sea visible en el campo de Documento de Referencia en el doctype de Repetición Automática.

  <img class="screenshot" alt="Allow Auto Repeat" src="/docs/assets/img/automation/allow-auto-repeat.png">

### 1.2 Configurar Repetición Automática
1. Ir a **Inicio > Configuraciones > Automatización > Repetición Automática > Nueva**.
2. Seleccionar el Tipo de Documento de Referencia, como Asiento de Libro Diario, Factura de Venta, etc. 
3. Seleccionar el Documento de Referencia. Este es el documento individual que se desea repetir. 
4. Configurar la Fecha de Inicio y de Finalización (opcional). 
   Si la Fecha de Finalización no está especificada, se crearán documentos recurrentes, salvo que se desactive la Repetición Automática. 
5. Configurar la Frecuencia para la creación de documentos repetibles.
   (Diaria, Semanal, Mensual, Cuatrimestral, Semestral, Anual).
6. Guardar.

### 1.3 Configurar Repetición Automática desde el documento
También se puede poner a un documento en Repetición Automática haciendo click en la opción **Repetir** del **Menú** en la Barra de Herramientas.

**Observación**: Si un documento ya está en Repetición Automática, la opción Repetir no estará disponible. 

<img class="screenshot" alt="Allow Auto Repeat" src="/docs/assets/img/automation/repeat-option.png">

Una vez que se hace click en Repetir, aparecerá una ventana para la Repetición Automática. Completar los detalles y hacer click en Guardar. 

<img class="screenshot" alt="Auto Repeat Prompt" src="/docs/assets/img/automation/auto-repeat-prompt.png">

## 2. Características

### 2.1 Notificar Vía Email
Si se quiere notificar a ciertos contactos cada vez que se crean los documentos recurrentes, se puede hacer click en 'Notificar Vía Email' en la sección Notificación de la Repetición Automática. Esto enviará los documentos recurrentes generados automáticamente a las Direcciones de Email especificadas. Los campos para esto mismo se explican a continuación:

- **Receptores**: Define los IDs de Email de los receptores para los emails de creación de documentos recurrentes. 
- **Obtener Contactos**: Este botón obtendrá los contactos vinculados al documento que está configurado en Repetición Automática y completará el campo de Receptores con los mismos. 
- **Plantilla**: Se puede elegir una Plantilla de Email para el email. Esto completará los campos de Asunto y Mensaje. 
- **Asunto**: Asunto para el Email (ejemplo: creación exitosa de Tarea Pendiente Recurrente).
- **Mensaje**: Mensaje a enviar en el Email.
- **Vista Previa del Mensaje**: Este botón mostrará una vista previa del mensaje.
- **Formato de Impresión**: Seleccionar un formato de impresión para definir la vista del documento que deberá ser enviado vía email al cliente.  

> **Observación**: Si el documento para el cuál se está configurando la Repetición Automática es enviable, es necesario asegurarse que el campo  "Permitir Impresión de Borrador" esté habilitado en las [Configuraciones de Impresión](/docs/user/manual/en/setting-up/print/print-settings) para recibir el nuevo documento recurrente en la Notificación Vía Email de la Repetición Automática. Si esto no se encuentra habilitado, se enviará notificación respecto a la creación del documento recurrente, pero sin el documento. 

### 2.2 Repetir en un día en Particular
Si la frecuencia está configurada como Mensual, Cuatrimestral, Semestral o Anual, entonces se crearán los documentos recurrentes en los meses respectivos en el mismo día que la 'Fecha de Inicio' de la Repetición Automática. Si se desea crear documentos recurrentes en otros días, esto puede configurarse de la siguiente manera:

- **Repetir en Día**: Día del mes en el cuál se creará el documento recurrente. Por ejemplo, si la frecuencia es Mensual y se ingresa el 7, entonces el documento recurrente será generado en el día 7 de cada mes. 
- **Repetir en el Último Día del Mes**: Esta opción está disponible debido a que el último día de cada mes es diferente. Por ejemplo, en un año bisiesto, el último día de Febrero es el 29, y sino, es el 28. Si se hace click en esta opción, se crearán los documentos recurrentes en el último día de los meses respectivos. 

### 2.3 Tablero
Se puede ver el cronograma de la Repetición Automática en el Tablero de la Repetición Automática de Documentos. Si no se especifica una Fecha de Finalización, el cronograma solo mostrará la Próxima Fecha Programada.

<img class="screenshot" alt="Allow Auto Dashboard" src="/docs/assets/img/automation/auto-repeat-dashboard.png">

### 2.4 Frecuencia de la Repetición Automática en la barra lateral 
Cuando un documento se programa para Repetición Automática, se puede ver la frecuencia de la misma en la barra lateral. 
Se puede hacer click en el estado para ver el documento en Repetición Automática. 

<img class="screenshot" alt="Auto Repeat Frequency" src="/docs/assets/img/automation/auto-repeat-frequency.png">

### 2.5 Desactivar Repetición Automática
Si se hace click en este campo, se dejarán de crear esos documentos recurrentes y se desvinculará el documento en Repetición Automática del campo de Documento de Referencia.
