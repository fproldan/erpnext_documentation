<!--add breadcrumbs-->

# Importación de Datos

**La Herramienta de Importación de Datos permite importar registros desde archivos CSV/Excel.**

La Herramienta de Importación de Datos es una forma simple de cargar (o editar) datos masivos (específicamente datos maestros) en el sistema.

Para empezar a importar datos ir a:

> Inicio > Configuración > Datos > Importación de Datos

O ir al Documento que se desea importar y hacer click en Menú > Importar:

<img alt="Start Import" class="screenshot" src="/docs/assets/img/setup/data-import/task-menu-import.png">

Antes de utilizar Importación de Datos **asegurarse** de tener todos los datos listos.

## 1. Insertar Nuevos Registros

Suponiendo que se quiere importar una lista de Clientes desde el viejo sistema hacia ERPNext. El primer paso será descargar una plantilla en la cual se puedan ingresar los datos. 

### 1.1 Descargar la Plantilla

1. Ir al Listado de Clientes, click en Menú > Importar. Click en **Nuevo**.
1. Seleccionar "Insertar Nuevos Registros" en el campo "Tipo de Importación".
1. Hacer click en **Guardar**.
1. Hacer click en **Descargar Plantilla**.
1. Para insertar los nuevos registros se debería descargar la "Plantilla en blanco". Si se tienen pocos Clientes en el sistema, se puede seleccionar "5 Registros" en "Tipo de Exportación" para ver el formato en el cual se deben ingresar los datos a la plantilla. 
1. Seleccionar el Tipo de Archivo de la plantilla. 
1. Seleccionar los campos que se desee completar en detalles de Cliente.
1. Hacer click en **Exportar**.

![Download Template](/docs/assets/img/setup/data-import/download-template.gif)

### 1.2 Ingresar los Datos en la Plantilla

La plantilla descargada se verá así: 

![Blank Template](/docs/assets/img/setup/data-import/blank-template-file.png)

Abrir la plantilla descargada en una aplicación de hoja de cálculo (como Excel, Numbers, o Libre Office) e ingresar los datos bajo los encabezados de columnas como se muestra a continuación: 

![Customer Template with Data](/docs/assets/img/setup/data-import/customer-template-with-data.png)

Ahora guardar la plantilla como un archivo de Excel o Comma Separated Values (CSV).

> Se pueden dejar las columnas de ID en blanco al insertar los nuevos registros. 

Al importar esta plantilla, cada fila será un registro de Cliente en el sistema.  


### 1.3 Importar la Plantilla

1. Luego de actualizar el archivo de la plantilla, ir al formulario de Importación de Datos y adjuntar el archivo haciendo click en el botón **Adjuntar**.
1. Seleccionar el archivo de la plantilla y hacer click en **Subir**.
1. Luego de que la carga sea exitosa, hacer click en **Comenzar la importación**.

![Upload Template File](/docs/assets/img/setup/data-import/upload-template-file.png)

Si hay algún error en la plantilla, se mostrará en la sección "Errores y advertencias de la importación". Los problemas se categorizarán por Fila o Columna, con su número, para que puedan ser rastreados fácilmente en la plantilla y resueltos. Se deberán resolver todos los problemas para poder importar los datos. 

![Import Warnings](/docs/assets/img/setup/data-import/import-warnings.png)

Luego de resolver los problemas, hacer click en **Comenzar la importación** nuevamente para importar los datos. Al importar los datos de forma exitosa, se verá un registro de cada documento que haya sido creado, en la sección de Registro de Importación. 

![Import Success](/docs/assets/img/setup/data-import/import-success.png)

## 2. Actualizar Registros Existentes

Suponiendo que se quieren actualizar en el sistema los datos de Clientes de forma masiva. El primer paso es descargar la plantilla con todos los datos. 

### 2.1 Descargar la Plantilla

1. Ir al Listado de Clientes, hacer click en Menú > Importar. Hacer click en **Nuevo**.
1. Seleccionar "Actualizar registros existentes" en el campo "Tipo de Importación".
1. Hacer click en **Guardar**.
1. Hacer click en **Descargar Plantilla**.
1. Para actualizar los registros existentes, se deben exportar los registros desde el sistema con el campo ID y los campos que se deseen actualizar. Se pueden elegir Todos los Registros o Registros Filtrados de acuerdo con el caso. 
1. Seleccionar los campos que se deseen actualizar para los Clientes.
1. Hacer click en **Exportar**.

### 2.2 Actualizar Datos en la Plantilla

La plantilla descargada se verá así: 

![Customer Template for Update](/docs/assets/img/setup/data-import/customer-template-for-update.png)

Después de cambiar los valores deseados, guardar la plantilla como un archivo de Excel o CSV.

> Al exportar registros para actualizarlos, es necesario asegurarse que la columna ID es exportada y no es editada. Los valores en la columna ID son utilizados para identificar los registros en el sistema. Se pueden actualizar los valores en las otras columnas pero no en la columna ID.

### 2.3 Importar la Plantilla

Seguir los pasos mostrados en la sección [Importar la Plantilla](#13-importing-the-template) explicada más arriba.

## 3. Importar Registros Secundarios

Los Datos son almacenados en ERPNext en tablas como hojas de cálculo con columnas y filas de datos. Cada formulario como Orden de Venta tiene muchos campos como Cliente, Empresa, etc. También tiene tablas como la tabla de productos, tabla de impuestos, etc. En la Importación de Datos, el conjunto de campos en la Orden de Venta es tratado como la tabla principal y las filas en el interior de la tabla secundaria (tabla de productos = se tratan como tabla secundaria para la importación de datos. 

Cada formulario en ERPNext puede tener muchas tablas secundarias asociadas a él. Las tablas secundarias son vinculadas a las tablas principales y se implementan cuando hay muchos valores para alguna propiedad. Por ejemplo, un Producto puede tener muchos precios, una Factura de Venta muchos productos, Impuestos, etc.

Al exportar un documento con tablas secundarias, por ejemplo, cada fila secundaria aparecerá en una fila separada pero será asociada con una sola fila principal. Los valores subsecuentes en las columnas principales permanecerán en blanco. Es necesario asegurar que este orden no se rompa al importarlas a través de Importación de Datos. 

![Child Table Export](/docs/assets/img/setup/data-import/child-table-export.png)

## 4. Opciones de Importación

### 4.1 Importar desde Google Sheets

También se pueden importar datos desde Google Sheets. Importar la plantilla en Google Sheets e ingresar los datos. Es necesario asegurarse que el archivo de Google Sheets esté configurado como público. Se puede probar esto abriendo la URL de Google Sheets en una ventana de incógnito.

![Google Sheets](/docs/assets/img/setup/data-import/google-sheets.png)

![Import via Google Sheets](/docs/assets/img/setup/data-import/import-via-google-sheets.png)

### 4.2 Validar luego de importar

En ERPNext los tipos de documentos son principalmente dos - maestros y transacciones. Los maestros son registros como Cliente y Tarea, que sólo pueden ser guardados pero no validados. Las transacciones como Orden de Venta, Factura de Compra, etc, son documentos que pueden ser guardados y validados. 

Al seleccionar un tipo de documento validable para importar, se puede hacer click en **Validar luego de importar** para que se valide automáticamente. 

### 4.3 No Enviar Correos Electrónicos

Suponiendo que se creó una [Notificación](/docs/user/manual/es/setting-up/notifications) en el sistema y que, cada vez que se crea una Iniciativa, se envía un Correo Electrónico. Ahora, si se están importando de forma masiva, se enviarán muchos correos electrónicos, lo cuál puede no ser deseado. Desde aquí, se podrá deshabilitar esa opción para evitar enviar dichos correos electrónicos.

## 5. Observaciones Adicionales

### 5.1 Limite de Carga

No hay un límite concreto en cuanto al número de registros que pueden importarse. Sin embargo, se recomienda cargar sólo unos miles de registros por vez. Si se importan números muy grandes de registros (como por ejemplo 50.000), el sistema puede volverse muy lento para aquellos usuarios que lo estén utilizando. 

### 5.2 Archivos CSV

Un archivo CSV (Comma Separated Value) es un archivo de datos que se puede subir a ERPNext para actualizar varios datos. Cualquier archivo de hoja de cálculo desde aplicaciones famosas 
de hojas de cálculo como MS Excel u Open Office Spreadsheet puede ser guardado como archivo CSV.

Si se está utilizando Microsoft Excel y se están usando caracteres no ingleses, asegurarse de guardar el archivo codificado como UTF-8.

Para versiones más antiguas de Excel, no hay una forma clara de guardar como UTF-8. Por ende, es necesario guardar el archivo como CSV, luego abrirlo en Block de Notas, y luego guardarlo como "UTF-8" (O actualizar la versión de Excel)

## 6. Temas Relacionados

1. [Importador de Plan de Cuentas](/docs/user/manual/es/setting-up/chart-of-accounts-importer)
1. [Exportación de Datos](/docs/user/manual/es/setting-up/data/data-export)
