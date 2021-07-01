<!-- add-breadcrumbs -->
# Valor Actual de Secuencias e identificadores

Secuencias e identificadores permite definir prefijos para nombrar documentos. Por ejemplo, si una Orden de Venta tiene prefijo "SO", entonces la serie será generada de la siguiente forma SO-00001, SO-00002... y así sucesivamente. Hacer click [aquí](/docs/user/manual/es/setting-up/settings/naming-series.html) para aprender a editar los Nombres de Serie para transacciones/documentos en ERPNext.

### 1. Configuración del Valor Actual

La función de Nombres de Serie también ofrece una herramienta donde se puede configurar el Valor Actual para un prefijo específico. Esto generalmente resulta necesario si se está empezando a utilizar ERPNext, y se cuenta con transacciones viejas en el sistema anterior, y se desea que la serie de número inicie donde terminó en el sistema anterior. Consideremos una situación para entender mejor esto.  

Por ejemplo, se cuenta con 322 Órdenes de Venta creadas en el sistema anterior, siendo SO00322 el Id. más alto de las Órdenes de Venta. En  ERPNext, se necesita que la primera Orden de Venta sea numerada a partir de #323 cuando sea guardada. Para habilitar esto, se debe configurar el Valor Actual para las series de SO utilizando los pasos mostrados a continuación.

#### Ir a la Herramienta de Nombres de Serie

`Configuración > Sistema > Nombres de Serie`

#### Actualizar la Sección Series

<img alt="Update Series Section" class="screenshot" src="{{docs_base_url}}/assets/img/articles/current-no-1.png">

#### Seleccionar Prefijo

Considerando la situación, el prefijo para la Orden de Venta sería "SO".

<img alt="Series Prefix" class="screenshot" src="{{docs_base_url}}/assets/img/articles/current-no-2.png">

#### Valor Actual

Si actualmente se cuenta con 12 Ordenes de Venta creadas en la cuenta, entonces el valor actual actualizado será de 12. Se puede editar el Valor Actual a 322, y luego hacer click en Actualizar Número de Serie.

<img alt="Series Current Value" class="screenshot" src="{{docs_base_url}}/assets/img/articles/current-no-3.png">

Con esta configuración, se contará con una numeración para las Nuevas Ordenes de Venta a partir de #323.

### 2. Error Debido A Número de Serie 

Si se recibe un error de Nombre Duplicado al guardar una transacción, por ejemplo, si al guardar el Precio de un Producto, se recibe un error que dice: 

`Nombre Duplicado Precio de Producto RFD/00016`

Este mensaje de error indica que cuando se está guardando el Precio de Producto, el sistema está tratando de asignar "RFD/00016" al registro de ese Precio de Producto. Pero se encuentra con que el Precio de Producto con esa ID ya existe en el sistema. 

Este error puede aparecer porque el Valor Actual para la Serie/Prefijo del Precio de Producto está distorsionado y no sincronizado con el real Valor Actual. Mientras que el Valor actual real para el Precio de Producto puede ser 20 (o cualquier número mayor a 16), alguien ha configurado el Valor Actual para la serie en 15.

Para confirmar el Valor Actual real para una Serie en particular, se debería visitar los informes para el documento en cuestión (Precio de Producto en este caso), y verificar el ID del Precio de Producto con el valor más alto. 

Suponiendo que se encuentra que el real Valor Actual para el Precio de Producto es 22, entonces se va a Nombres de Serie, y se configura el Valor actual para el Prefijo/Serie del Precio de Producto en 22, y se actualiza el Número de Serie. 

Estas instrucciones son aplicables para todos los documentos en ERPNext para los cuales el usuario puede personalizar Series y su Valor Actual.

Considérese otra situación para entender mejor esto. Al asignar un documento a otro usuario, el mensaje de error dice:

`Nombre duplicado Tarea Pendiente TDI00014286`

Esto indica que el Valor Actual para la Serie/Prefijo de las Tareas Pendientes (TDI) ha sido distorsionado. Se deberán seguir los siguientes pasos para corregir el valor para el Valor Actual del prefijo TDI.

1. Ver el informe de Tareas Pendientes para ver el valor más alto del id de Tareas Pendientes. 
1. Configuración >> Configuraciones >> Nombres de Serie
1. Ver sección B de Actualizar Series
1. Seleccionar Prefijo para Tareas Pendientes "TDI"
1. Asegurarse de que el número más alto para Tareas Pendientes es actualizado como Valor Actual en Nombres de Serie. Si no, corregir el Valor Actual, y hacer click en "Actualizar Numeración de Serie". 

<!-- markdown -->
