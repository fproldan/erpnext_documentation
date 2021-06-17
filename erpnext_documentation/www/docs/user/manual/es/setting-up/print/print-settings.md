<!-- add-breadcrumbs -->
# Ajustes de Impresión

**En Ajustes de Impresión se pueden definir las preferencias a la hora de imprimir como Tamaño de Papel, tamaño predeterminado del texto, si se quiere exportar como PDF o HTML, etc.**

Como ERPNext es una aplicación de navegador, el comando de impresión se ejecuta desde el que se esté utilizando.

Para editar las Ajustes de Impresión ir a:
> Inicio > Configuración > Ajustes de Impresión

<img class="screenshot" alt="Print Settings" src="{{docs_base_url}}/assets/img/setup/print/print-settings.png">

Hay varias configuraciones disponibles en Ajustes de impresión. 

## 1. Configuraciones de PDF

### 1.1 Enviar impresión como PDF

Cuando se envía un documento (como Orden/Factura de Venta) desde ERPNext, el mismo es enviado en formato PDF o HTML. De forma predeterminada, el archivo es enviado en PDF. Si se desea enviar un documento en formato HTML, destildar la opción "Enviar impresión como PDF".

### 1.2 Repetir encabezado y pie de página en PDF

El membrete es una función donde se pueden definir los Encabezados y Pies de Página estándar, que serán añadidos al Formato de Impresión del Documento. Si esta propiedad se encuentra habilitada, el Encabezado y Pie de Página se añadirá a cada página. Si no se desea lo anterior, destildar esta opción. 

### 1.3 Tamaño de Página PDF

El tamaño de página predeterminado para imprimir páginas de PDF es A4; pero se puede cambiar a tamaño membrete.

## 2. Configuración de Página

### 2.1 Imprimir con membrete

Tildar esta opción hará que se seleccione de forma automática el Membrete al imprimir un documento. Tener en cuenta que se debe configurar el Membrete como predeterminado o seleccionar uno en las transacciones para que aparezca en la vista de impresión. 

### 2.2 Impresión compacta de Productos

En transacciones como Ordenes/Facturas de venta, hay una tabla que detalla los productos comprados o vendidos. Tiene muchas columnas como Nombre del Producto, Descripción, UOM, Monto de Tarifa, etc. Si hay muchas columnas en la tabla de Producto, el Formato de Impresión puede verse un poco abarrotado. Se puede mejorar la vista de la tabla permitiendo la Impresión compacta de los Productos.

De acuerdo con esta configuración, solo habrá cuatro columnas en el Formato de Impresión: Descripción, Cantidad, Precio e Importe. 

Los valores de otras columnas (como nombre, descripción, imagen, números de serie, etc.) se encuentran concatenados en la columna Descripción.

Cuando esta casilla no está seleccionada, el formato de impresión se ve así:
![Incompact Print Format Settings](/docs/assets/img/setup/print/incompact-print.png)

Así se ve la Impresión compacta de los Productos:
![Compact Print Format Settings](/docs/assets/img/setup/print/compact-print.png)

### 2.3 Permitir Impresión para Borrador

Los documentos (principalmente las transacciones) tienen dos etapas de autenticación, Guardar y Validar. Los documentos guardados son el primer borrador y no están validados en el sistema. Por esto, la impresión está restringida para documentos en estado Validado. Sin embargo, si se desea permitir a los usuarios imprimir documentos en la etapa Borrador, tildar esta casilla. 

### 2.4 Agregar "Borrador" en el encabezado al imprimir dichos documentos

Habilitar esta configuración para imprimir un "Borrador" en Formato de Impresión, indica que el documento compartido todavía no está completamente autenticado. 

### 2.5 Permitir salto de página dentro de las tablas

Si la descripción de un producto ocupa más que el espacio usual de una página, entonces habilitar esta configuración dividirá el detalles del producto en dos páginas. De esta forma, se insertará un salto de página en la Descripción del Producto, y el resto de los detalles serán llevados a la siguiente página.  

### 2.6 Permitir Impresión para Cancelado

Las transacciones canceladas son aquellas que no impactan en los informes. Si se desea permitir la impresión para transacciones canceladas, habilitar esta configuración. Una transacción puede ser cancelada sólo luego de ser validada.

### 2.7 Imprimir impuestos con importe nulo

En las transacciones de compra y venta, se pueden aplicar muchos impuestos sobre el producto. De forma predeterminada, el formato de impresión solo muestra los impuestos con algún monto calculado. Si se desea también imprimir el impuesto que no fue aplicado y tiene monto cero, habilitar esta configuración. 

## 3. Servidor de Impresión

Se puede Habilitar Servidor de Impresión tildando esta opción y completando la IP y el puerto del Servidor. Luego, se debe elegir la impresora predeterminada.

Antes de habilitar esta función se debe instalar la biblioteca `pycups`.

Puede ser necesario instalar primero la biblioteca `cups` sino se encuentra en el sistema.

Para Debian OS Family:

`sudo apt-get install libcups2-dev`

Para Red Hat OS Family:

`sudo yum install cups-libs`

Luego de lo anterior, instalar `pycups` en el env utilizando el comando:

`./env/bin/pip install pycups`

Esto se ejecuta desde el directorio `frappe-bench`.

## 4. Impresión en bruto

Se puede habilitar la impresión en bruto y utilizar impresoras térmicas. Hacer click aquí para saber más sobre [Impresión en bruto.](/docs/user/manual/es/setting-up/print/raw-printing)

### 5. Temas Relacionados
1. [Formato de Impresión](/docs/user/manual/es/setting-up/print/print-format)
1. [Estilo de Impresión](/docs/user/manual/es/setting-up/print/print-style)
1. [Encabezado de Impresión](/docs/user/manual/es/setting-up/print/print-headings)
