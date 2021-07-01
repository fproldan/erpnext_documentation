<!-- add-breadcrumbs -->
# Secuencias e identificadores

**Los documentos y transacciones pueden ser identificados utilizando prefijos en forma de nombres de serie.**

ERPNext permite crear prefijos para los documentos, y cada prefijo forma su propia serie. Por ejemplo, una serie con el prefijo INV12#### tendrá como números INV120001, INV120002, y así sucesivamente.

Se pueden tener varias series para cada transacción. Por ejemplo, pueden generarse los prefijos o identificadores mostrados a continuación para Factura de Venta: 

* ACC-SINV-.YYYY.-
* SINV12####
* SALESINV-00####

Se puede definir o seleccionar el patrón de Secuencias e identificadores desde:

> Inicio > Configuración > Secuencias e identificadores

## 1. Configuración de Secuencias e identificadores para Documentos

1. Seleccionar el tipo de transacción para el cual se desea crear la serie. El sistema mostrará las secuencias actuales en el cuadro de texto.  
2. Editar la serie de acuerdo a lo que se requiera, con prefijos únicos para cada una de ellas.
  El primer prefijo será el predeterminado. Cada nuevo prefijo de Secuencias e identificadores debe ser añadido en una nueva fila. La secuencia añadida estará disponible en el documento. 
  ![Multiple naming series](/docs/assets/img/setup/settings/multiple-naming-series.gif)
  
3. Si se desea que el usuario seleccione de forma explícita una serie en vez de la predeterminada, tildar la opción "El usuario deberá elegir siempre".

1. También se puede actualizar el punto de inicio de una secuencia seleccionando el prefijo e ingresando el valor actual, en la sección "Definir Secuencia". 

1. Hacer click en el botón Actualizar para actualizar la Secuencia para el documento seleccionado. 

> Observación: Para ver las Secuencias añadidas recientemente, hacer click en Menú > Recargar.

## 2. Año Financiero en Secuencias e identificadores

También se puede mostrar el año financiero en las Secuencias. De forma predeterminada, si se ingresa "YYYY", tomará el año actual. Para configurar secuencias basadas en el año fiscal ingresar algo como 'ACC-SINV-.19-20.-' donde 19-20 es el Año Fiscal Actual. Es común tener series separadas para cada año financiero. 

Como puede verse en la siguiente captura de pantalla de una Factura de Venta, se encuentra mencionado el año 2019: 

![Fiscal year in Naming Series](/docs/assets/img/setup/settings/year-naming-series.png)


## 3. Actualizar el valor actual para Secuencias e identificadores existentes

Se puede cambiar el número inicial/actual de una secuencia existente. 

1. En la sección Definir Secuencia, seleccionar el prefijo al cual se le cambiará la numeración. 
1. El valor actual será obtenido y mostrado.
1. Cambiar la secuencia numérica inicial/actual de ser necesario. 
1. Hacer click en "Actualizar número de serie".

Por ejemplo, si el número de serie actual de una Orden de Venta es 16, y se desea volver a empezar o configurarlo como 50, ingresar 0 o 50 dependiendo del caso. Cualquier nueva Orden de Venta creada empezará desde el número de secuencia nuevo. 

Para saber más sobre esto, [visitar este artículo](/docs/user/manual/es/setting-up/articles/naming-series-current-value).

> Consejo: Se puede tener una serie separada para cada tipo de Cliente o para cada una de las tiendas minoristas. 

## 4. Utilizar Valores de Campos en Secuencias e identificadores

Algunas empresas prefieren utilizar "códigos-cortos" para proveedores, es decir, WN para la empresa "Web Notes", que luego puede ser utilizada en nombres de serie para una identificación más rápida.  
 
Por ejemplo:

    Un campo personalizado "ID de Vendedor" se crea en el Documento: Proveedor.
    Luego en Nombres de Serie, se permite algo como
        PO-.YY.MM.-.idde_vendedor.-.####
        Resultando en "PO-1503-WN-00001"

## 5. Temas Relacionados
1. [Renombrar en Grupo](/docs/user/manual/es/setting-up/settings/bulk-rename)
