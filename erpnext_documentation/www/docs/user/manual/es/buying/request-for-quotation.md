<!-- add-breadcrumbs -->
# Solicitud de Cotización

**Una Solicitud de Cotización es un documento que envía una empresa a uno o más proveedores pidiendo una cotización para determinados productos.**

![Buying Flow](/docs/assets/img/buying/buying_flow_rfq.png)

Para acceder a Solicitud de Cotización ir a:
> Inicio > Compras > Compras > Solicitud de Cotización

## 1. Prerrequisitos
Antes de crear y utilizar una Solicitud de Cotización, se aconseja crear lo siguiente:

* [Proveedor](/docs/user/manual/es/buying/supplier)
* [Producto](/docs/user/manual/es/stock/item)

## 2. Creación de una Solicitud de Cotización
1. Ir al listado de Solicitud de Cotización y hacer click en Nuevo.
2. Ingresar la Fecha.
3. Elegir el proveedor al cual se enviará la Solicitud de Cotización.
4. En la siguiente tabla, ingresar los productos, la cantidad y el almacén de destino al cual se enviarán los productos.
1. El Almacén puede dejarse en blanco si el campo "Mantener Existencias" está deshabilitado para el producto.
5. Guardar y Validar.

Una Solicitud de Cotización también puede crearse desde una Solicitud de Material validada. Una vez que se crea la Solicitud de Cotización, se puede imprimir y enviar el PDF que tendrá todos los detalles relevantes y recibir la respuesta mediante correo electrónico. También se puede recibir la respuesta (Cotización del Proveedor) desde el mismo ERPNext, ver sección _3.1 Cotización de Proveedor por Usuario_. Sin embargo, si se trata de una gran cantidad de productos, el proveedor puede estar más cómodo con una planilla de Excel, etc. 

## 3. Características

### 3.1 Obtener Productos Desde

Los productos en la tabla de productos pueden ser obtenidos desde otros documentos. Las opciones son: Solicitud de Material, Oportunidad y Posible Proveedor. 

* **Solicitud de Material**: Los Productos se obtendrán desde la Solicitud de Material validada que se seleccione. Una Solicitud de Material puede buscarse con algunas palabras y también puede seleccionarse un rango de fechas para filtrarlas. 

* **Oportunidad**: Los Productos pueden obtenerse desde una Oportunidad guardada. Aquí también puede seleccionarse un rango de fechas. 

* **Posible Proveedor**: Seleccionar un Posible Proveedor. Entonces, si ya se tiene alguna Solicitud de Material realizada para este proveedor, los productos se obtendrán de allí. 

### 3.2 Obtener Proveedores

En vez de ingresar los proveedores en la tabla de forma manual, también se puede obtenerlos utilizando este botón. Cuando se hace click en el botón Obtener Proveedores, se verá un campo "Obtener Proveedores por". Hay dos opciones para obtener proveedores: por etiquetas o por grupos. 

* **A Través de Etiquetas**: Ir a "Etiqueta" a través de la barra de búsqueda. Anteriormente se deben haber creado y asignado las etiquetas al DocType del Proveedor en el módulo de Compras. Luego se puede seleccionar por Etiqueta y obtener el proveedor. Al hacer click en "Añadir Proveedores", se obtendrán los proveedores que coincidan con las etiquetas seleccionadas. 

* **A Través de Grupos**: Seleccionar "Grupo de Proveedores" y elegir el grupo de proveedores desde el cual se desea añadir proveedores. Por ejemplo, si se selecciona Hardware, todos los proveedores de hardware serán añadidos, de forma tal que se pueda recibir una cotización de todos ellos. 

En la tabla de Proveedores, al expandir una fila, se verá la opción "Descargar PDF" la cual abrirá el PDF de la Solicitud de Cotización. 

### 3.3 Enlace a solicitudes de material

Al hacer click en **Herramientas > Enlace a solicitudes de material**, se vinculará la Solicitud de Cotización a Solicitudes de material disponibles. Los productos deberían ser los mismos en ambas solicitudes.

### 3.4 Vista previa del correo electrónico

En la sección "Detalles de correo electrónico" de una Solicitud en borrador se puede armar y previsualizar el correo que se enviará al proveedor.

![Email Details Section]({{docs_base_url}}/assets/img/buying/email-details-section.png)

Ingresar cualquier mensaje adicional en el campo "Mensaje para los Proveedores". Esta campo puede ser autocompletado usando una "Plantilla de Correo Electrónico".

También se puede agregar un saludo y el Asunto del correo. Al hacer click en el botón "Vista previa del correo electrónico" se podrá ver cómo será el correo que se enviará al proveedor.

![Preview Email]({{docs_base_url}}/assets/img/buying/email-preview.png)

### 3.5 Términos y Condiciones

En operaciones de Compra/Venta puede haber ciertas bases y condiciones que rigen la forma en que el proveedor vende bienes o servicios al cliente. Se pueden aplicar los Términos y Condiciones a las transacciones y éstas aparecerán en el documento impreso. Para saber más respecto a Términos y Condiciones, [click aquí](/docs/user/manual/es/setting-up/print/terms-and-conditions)

### 3.6 Ajustes de impresión
#### Membrete
Se pueden imprimir los pedidos de cotización/orden de compra en papel con el [membrete](/docs/user/manual/es/setting-up/print/letter-head) de la empresa.

"Agrupar productos iguales", agrupará los productos iguales que se hayan sumado muchas veces a la tabla de Producto. Esto puede verse al imprimir.

#### Encabezado
Los títulos de los documentos pueden ser modificados. Leer más [aquí](/docs/user/manual/en/setting-up/print/print-headings).

## 4. Creación de una Cotización de Proveedor luego de una Solicitud 
Luego de crear una Solicitud de Cotización, hay dos formas de generar una Cotización de Proveedor desde la Solicitud de Cotización. 

### 4.1 Cotización de Proveedor por Usuario

1. Abrir Solicitud de Cotización y hacer click en **Cotización de Proveedor > Crear**.

    ![Supplier Quotation from RFQ]({{docs_base_url}}/assets/img/buying/make-supplier-quotation-from-rfq.png)

2. Seleccionar el Proveedor, y hacer click en el proveedor nuevamente. En esta página hacer click en el + que se encuentra al lado de "Cotización de Proveedor". Se abrirá una nueva página de Cotización de Proveedor, el usuario debe ingresar la cantidad, el precio y validarla.

    ![Supplier Quotation from Supplier]({{docs_base_url}}/assets/img/buying/supplier-quotation-from-sup.png)
    
### 4.2 Cotización de Proveedor por Proveedor

1. Si se crea un [Contacto](/docs/user/manual/es/CRM/contact) para el Proveedor y se asocia a una dirección de correo electrónico, los detalles de Contacto y la dirección serán obtenidos al seleccionar el Proveedor. Crear un Contacto y correo si todavía no se encuentran presentes. 

2. Hacer click en el botón "Enviar correos electrónicos a proveedores".

    **Si la cuenta de Proveedor no está presente**: El sistema creará una cuenta de Proveedor y enviará los detalles al Proveedor. El proveedor deberá hacer click en el link (Actualización de Contraseña) presente en el correo. Luego de actualizar la contraseña, el Proveedor puede acceder a su portal con el formulario de Solicitud de Cotización. El Proveedor será creado como Usuario de Sitio Web. 

    ![Supplier email if account not present]({{docs_base_url}}/assets/img/buying/supplier-password-update-link.png)
    
    **Si la cuenta de Proveedor está presente**: El sistema le enviará el link de Solicitud de Cotización al Proveedor, el mismo tendrá que ingresar utilizando sus credenciales para ver el formulario de Solicitud de Cotización en el portal. 

    ![Supplier email if account present]({{docs_base_url}}/assets/img/buying/send-rfq-link.png)

3. De cualquier forma, cuando el Proveedor ingresa, se le mostrará la siguiente pantalla. Desde aquí pueden enviar la cotización:

    ![Supplier Quotation Screen]({{docs_base_url}}/assets/img/buying/rfq-supplier-quotation.png)

    El proveedor debe ingresar el monto y las notas (términos de pago) en el formulario y hacer click en validar. En la sección de Cotización estarán visibles las cotizaciones anteriores. 

4. Al validar, el sistema creará la Cotización de Proveedor (en modo borrador) contra el proveedor. El usuario debe revisar la Cotización de Proveedor y validarla. Cuando todos los Productos de la Solicitud de Cotización hayan sido cotizados por un Proveedor, el estado de la cotización será actualizado a "Recibido" en la tabla de "Solicitud de Cotización" del Proveedor. 

    ![RFQ status after supplier quote]({{docs_base_url}}/assets/img/buying/rfq-supplier-quoted.png)

## 5. Sin Cotización del Proveedor

Si un Proveedor indica que no enviará una cotización para los productos, esto puede señalarse en el documento de Solicitud de Cotización haciendo click en la casilla "Sin Cotización" luego de que la Solicitud de Cotización haya sido enviada. La casilla de Sin Cotización puede ser vista al expandir la fila de un Proveedor haciendo click en Edit. 

![No Quote from Supplier]({{docs_base_url}}/assets/img/buying/no-quote-supplier.png)

Para saber respecto a crear una Cotización de Proveedor hacer [click aquí](/docs/user/manual/es/buying/supplier-quotation).

### 6. Temas Relacionados
1. [Orden de Compra](/docs/user/manual/es/buying/purchase-order)
1. [Proveedor](/docs/user/manual/es/buying/supplier)
1. [Cotización del Proveedor](/docs/user/manual/es/buying/supplier-quotation)
1. [Cotización](/docs/user/manual/es/selling/quotation)
1. [Solicitud de Material](/docs/user/manual/es/stock/material-request)
