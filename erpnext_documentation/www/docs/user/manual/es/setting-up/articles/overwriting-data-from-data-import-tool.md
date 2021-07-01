<!-- add-breadcrumbs -->
# Sobrescribir Datos usando la Herramienta de Importación de Datos

La Herramienta de Importación de Datos permite importar documentos (como clientes, Proveedores, Ordenes, Facturas, etc) desde un archivo Excel/CSV hacia ERPNext. Esa misma herramienta puede utilizarse para sobrescribir valores en esos documentos existentes. 

Sobrescribir Datos usando la Herramienta de Importación de Datos solo funciona para las transacciones guardadas, no para las validadas. 

Digamos que hay un número de productos para los cuales se necesita sobrescribir el Grupo de Productos. A continuación están los pasos para sobrescribir Grupos de Productos para Productos existentes. 

## Paso 1: Descargar Plantilla

La plantilla utilizada para sobrescribir datos será la misma que la utilizada para importar nuevos productos. Por ende, el primer paso es descargar la plantilla.

> Inicio >  Configuraciones  > Datos > Importación de Datos

Como los productos a ser sobrescritos ya estarán disponibles en el sistema, al descargar la plantilla, hacer click en "Descargar con datos" para obtener todos los productos existentes en la plantilla. 

<img alt="Download Template" class="screenshot" src="{{docs_base_url}}/assets/img/articles/overwrite-1.gif">
    
## Paso 2: Preparar Datos

Ingresar un nuevo valor en la columna de Grupo de Productos para un producto. Como Grupo de Producto es un documento en sí mismo, es necesario asegurarse que el Grupo de Productos ingresado en el archivo de hoja de cálculo ya existe. 

<img alt="Update Values" class="screenshot" src="{{docs_base_url}}/assets/img/articles/overwrite-2.png">

Como solo se está sobrescribiendo el Grupo de Productos, las columnas obligatorias serán las siguientes: 

1. Columna A (ya que tiene los valores principales de la plantilla)
1. Nombre (Columna B)
1. Grupo de Productos

Las columnas de otros campos que no tendrán ningún impacto pueden ser eliminadas, incluso si son obligatorias. Esto se aplica solo para sobrescritura, no al importar nuevos registros. 

## Paso 3: Cargar Plantilla

Luego de actualizar los Grupos de Productos en la hoja de cálculo, volver a la Herramienta de Importación de Datos en ERPNext. Buscar y seleccionar el archivo/plantilla que tiene los datos a ser sobrescritos.

<img alt="Browse template" class="screenshot" src="{{docs_base_url}}/assets/img/articles/overwrite-3.gif">

## Paso 4: Subir

Al hacer click en Importar, el Grupo de Productos será reemplazado.

<img alt="Upload" class="screenshot" src="{{docs_base_url}}/assets/img/articles/overwrite-4.png">

Si la validación de los valores falla, entonces se indicará el número de fila de la hoja de cálculo para el cual falló la validación y se requiere corrección. En ese caso, se deberá corregir el valor en esa fila de la hoja de cálculo, y luego importar el mismo archivo nuevamente. Si la validación falla incluso para una sola fila, ninguno de los registros son importados/sobrescritos. 

<!-- markdown -->
