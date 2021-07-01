<!-- add-breadcrumbs -->
# Nombrar usando Número de Serie

Los Números de Serie son valores únicos asignados a cada unidad de un producto. Los Números de Serie ayudan a rastrear los detalles de garantía y vencimiento de un producto. Generalmente los productos seriados son de gran valor como máquinas, computadoras y equipos costosos.

Para que un producto sea seriado, ir al producto y hacer click en la casilla **Posee Número de Serie**.

Hay dos formas de generar un Número de Serie en ERPNext.

### 1. Seriar productos de compra

Si los productos comprados son recibidos con Números de Serie aplicados por OEM (Fabricante de Equipo Original), se puede seguir el mismo Número de serie en ERPNext. Al crear el Recibo de Compra, se debe escanear o ingresar de forma manual el Número de Serie para un producto. Al validar el Recibo de Compra, los Números de Serie serán creados en la base de datos como Números de Serie proporcionados para un producto.  Si se utiliza el Número de Serie OEM, entonces en el producto, el Prefijo no debería ser mencionado para seriar. En el caso de este escenario, el campo Prefijo debería ser dejado en blanco. 

Si los productos recibidos ya tienen un Número de Serie, simplemente se escanea ese código de barra para ingresar el Número de Serie en el Recibo de Compra. Hacer click [aquí](https://frappe.io/blog/management/using-barcodes-to-ease-data-entry) para aprender más sobre este tema. 

El validar el Recibo de Compra o el ingreso de existencias para el producto seriado, los Números de Serie serán generados automáticamente. 

<img alt="Serial Nos Entry" class="screenshot" src="{{docs_base_url}}/assets/img/articles/serial-naming-1.png">

Los números de serie generados serán actualizados para cada producto

<img alt="Serial Nos Created" class="screenshot" src="{{docs_base_url}}/assets/img/articles/serial-naming-2.png">

### 2. Seriar productos manufacturados

Para seriar productos manufacturados, se pueden definir Series para la generación de Números de Serie en el Producto. Siguiendo a esas series, el sistema creará nuevos Números de Serie por producto cuando se realice una entrada de su Producción. 

#### 2.1 Serie de Números de Serie

Cuando un producto está configurado como seriado, permitirá mencionar una Serie para el mismo

<img alt="Serial Nos Created" class="screenshot" src="{{docs_base_url}}/assets/img/articles/serial-naming-3.png">

#### 2.2 Entrada de Producción para Producto Seriado

Al validar una entrada de producción para fabricar un producto, el sistema generará automáticamente Números de Serie, siguiendo las Series especificadas en el Producto. 

<img alt="Serial Nos Created" class="screenshot" src="{{docs_base_url}}/assets/img/articles/serial-naming-4.png">

<!-- markdown -->
