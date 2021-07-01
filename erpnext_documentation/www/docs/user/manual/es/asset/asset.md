<!-- add-breadcrumbs -->
# Activos

**Un Activo es cualquier Producto de valor que posea una Empresa.**

Ejemplos de Activos son muebles, computadoras, teléfonos celulares, impresoras, autos, etc. Los activos pueden ser alquilados para ser utilizados por los empleados de una Empresa. 

En ERPNext, el registro de Activos es el centro de la administración de activos fijos. Todas las transacciones relacionadas con Activos como compras, ventas, depreciaciones, descartes, movimientos, o mantenimientos serán administradas desde el registro de Activos.  

Para acceder al listado de Activos ir a: 
> Inicio > Bienes > Bienes > Activo

## 1. Prerrequisitos

Antes de crear y utilizar Activos, se recomienda crear lo siguiente:

* [Producto](/docs/user/manual/es/stock/item) con "Es activo fijo" habilitado
* [Categoría de Activos](/docs/user/manual/es/asset/asset-category)

## 2. Tipos de Activos

Antes de crear un Activo, es necesario entender los tipos de activos presentes en ERPNext.

Hay dos situaciones posibles al crear un registro para activos. El activo puede ser uno existente que haya sido comprado anteriormente y que ya puede haber sufrido algún tipo de depreciación parcial, o puede ser un producto recientemente adquirido.

### 2.1 Activo Existente

Para un activo existente, se puede crear el registro de activo de forma directa haciendo click en el campo "Es Activo Existente". En este caso, también es necesario ingresar el monto de depreciación ya registrado y el número de depreciaciones registradas. De acuerdo con lo anterior, el sistema creará un cronograma para la depreciación restante.

<img class="screenshot" alt="Existing Asset" src="{{docs_base_url}}/assets/img/asset/existing-asset.png">

### 2.2 Activo Nuevo

Para activos nuevos, no se puede crear el registro de forma directa, sino que se debe realizar un Recibo/Factura de Compra para el mismo. 

Al comprar nuevos activos, se crea un ID para el mismo cuando se realiza el Recibo de Compra. Al validar el Recibo de Compra de un Activo, se verá un mensaje como el siguiente "Activo AST00003 creado". Esto solo sucederá si se ha seleccionado la casilla "Es Activo Fijo" al crear el Producto.

Cuando se compran nuevos activos, los mismos pueden ser creados de forma automática cuando se realiza un Recibo de Compra, si se encuentra seleccionada la casilla "Crear Activos Automáticamente desde Compra" en la función Producto del Activo. Al validar el Recibo de Compra para un Activo, se verá un mensaje como el siguiente "5 Activos creados para Teléfono de Oficina". Si no se desea crear activos de forma automática, luego de enviar el Recibo de Compra se deberá crear el Activo de forma manual y vincular el Recibo de Compra al mismo.

<img class="screenshot" alt="Asset" src="{{docs_base_url}}/assets/img/asset/asset.png">

Luego de enviar un Recibo/Factura de Compra para el Ítem, en caso de una creación automática de activos, se creará un número de registros de Activos en etapa Borrador. Luego se puede ir a esos Activos y enviarlos.

Para saber más visitar la página [Comprando un Activo](/docs/user/manual/es/asset/purchasing-an-asset).

## 3. Creación de un Activo en forma manual

Antes de crear un Activo, se deberá generar un Producto con la opción "Es Activo Fijo" tildada y realizar un Recibo/Factura de Compra para dicho producto. Tener en cuenta que se deberá crear un número determinado de Activos de acuerdo con la cantidad especificada en el documento de Compra. 

Se debe asignar una Categoría de Activo a ese Producto. Y luego de eso, se podrá crear el Activo. 

1. Ir al listado de Activos y hacer click en Nuevo.
1. Ingresar un nombre para el activo.
1. Seleccionar el Código de Porducto, el Nombre del Producto y la Categoría de Activo será obtenida de forma automática.  
1. Seleccionar quién es el Propietario del activo, es decir, Compañía, Proveedor o Cliente.
1. Seleccionar la Compañía/Proveedor/Cliente.
1. Seleccionar el Recibo/Factura de Compra. La Fecha de Compra y el Importe Bruto de Compra de la misma serán obtenidos automáticamente.
1. Seleccionar una Ubicación. Por ejemplo: Oficina de Rafaela. Esto será obtenido de forma automática si fue especificado en la tabla de productos del Recibo de Compra.  
1. Ingresar una Fecha disponible para usar, para marcar la fecha a partir de la cual el Activo estará disponible para ser usado. El monto de depreciación del primer período se calculará desde esta fecha.  
1. Hacer click en la opción "Es Activo Existente" si se está registrando un activo existente.
1. Guardar y validar. 

### 3.1 Opciones Adicionales al crear un Activo

1. **Código de Producto**: Un Producto para el Activo debe ser un producto que no mantenga existencias de inventario, se debe hacer click en el campo "Es Activo". 
    <img class="screenshot" alt="Asset Item" src="{{docs_base_url}}/assets/img/asset/asset-item.png">
1. **Custodio**: El empleado al que se da/asigna el activo.
1. **Departamento**: El área del Custodio.
1. **Es Activo Existente**: tildar esta opción si ya se contaba con el activo, es decir, si no fue comprado recientemente. El activo también puede provenir del Año Fiscal anterior. Los activos existentes que están parcial o totalmente depreciados también pueden ser creados o mantenidos para futuras referencias. 
1. **Depreciación Acumulada Inicial**: El monto acumulado de depreciación que ya ha sido registrado para un activo existente.
1. **Cantidad de Depreciaciones Registradas**: Ingresar el número de depreciaciones que ya han sido registradas para un activo existente. 
1. **Valor Actual (Luego de la Depreciación)**: En el caso de estar creando un registro de un activo existente que ya ha sido parcial/totalmente depreciado, mencionar el valor actual del activo. En el caso de un activo nuevo, mencionar el valor de compra, o dejar en blanco.
1. **Siguiente Fecha de Depreciación**: Mencionar la fecha en que se registrará la siguiente depreciación, incluso si es la primera. Si el activo es existente y la depreciación ya ha sido completada, dejar en blanco. 
1. **Calcular Depreciación**: Habilitar esta casilla de verificación para calcular la depreciación de los Activos. 
1. **Permitir Depreciación Mensual**: Habilitar esta casilla de verificación para distribuir el monto de la depreciación en los 12 meses del año. Los registros de depreciación se realizarán todos los meses en la fecha indicada como Fecha de Inicio de la Depreciación. Por ejemplo, si la Fecha de Disponibilidad de Uso es el 22 de noviembre de 2019 y la Fecha de Inicio de la Depreciación es el 31 de marzo de 2020, la primera depreciación se realizará el 30 de noviembre de 2019, la segunda el 31 de diciembre de 2019 y así sucesivamente. El montó se distribuirá de acuerdo con los días que quedan hasta la próxima depreciación. 

## 4. Características

### 4.1 Depreciación

* **Frecuencia de la Depreciación (Meses)**: El número de meses entre depreciaciones.
* **Número Total de Depreciaciones**: El número total de depreciaciones a lo largo de la vida útil del Activo. En el caso de activos existentes que ya están parcialmente depreciados, mencionar el número de depreciaciones pendientes. Por ejemplo, si se configura la frecuencia como 12 meses y el número de depreciaciones como 3, se registrará una depreciación cada 12 meses durante 3 años. 
* **Método de Depreciación**:
    - **Línea Recta**: Este método distribuye el costo del activo fijo de forma constante a lo largo de su vida útil.
    - **Saldo doblemente decreciente**: Un método acelerado de depreciación, resulta en una mayor depreciación en los primeros años de uso.
    - **Valor Escrito**: En este método, el porcentaje de depreciación es fijo pero se aplica en el valor actual del activo, obtenido luego de cada depreciación.
    - **Manual**: En este método se puede definir manualmente la Fecha Programada y el Monto de Depreciación para cada período.
    Para conocer más detalles respecto a Depreciación de Activos, [visitar esta página](/docs/user/manual/es/asset/asset-depreciation).
* **Fecha de Inicio de la Depreciación**: La fecha a partir de la cual comenzará el registro de la depreciación. 
* **Valor Esperado Luego de Vida Útil**: La Vida Útil es el período de tiempo durante el cuál la empresa espera que ese activo sea productivo. Luego de ese período, el activo es descartado o vendido. En caso de ser vendido, mencionar el valor estimado aquí. Este valor también se conocer como Valor de Rescate, Valor de Descarte o Valor Residual. 
* **Tasa de Depreciación**: La misma se calculará en base al monto ingresado en valor esperado luego de vida útil. 


### 4.2 Cronograma de Depreciación

Al registrar depreciaciones de este Activo, la sección de Cronograma de Depreciación será visible. 
Esta tabla tiene columnas para Libro de finanzas, Fecha Programada, Monto de Depreciación, Monto Depreciado, y Asiento contable. 
![Depreciation Schedule](/docs/assets/img/asset/asset-depreciation.png)

### 4.3 Detalles del Seguro
Si se ha tomado un Seguro para el Activo que se está registrando, se pueden almacenar los siguientes detalles del mismo:

* Número de Póliza
* Asegurador
* Valor Asegurado
* Fecha de Inicio del Seguro
* Fecha de Finalización del Seguro
* Seguro a Todo Riesgo

### 4.4 Registros Contables
Al enviar un activo, la cuenta "Obras de Capital en Proceso" será acreditada y la cuenta de activo relacionada al activo en cuestión será debitada. El envío solo es posible luego de ingresar la "Fecha de Disponibilidad de Uso". Si la "Fecha de Disponibilidad de Uso" es una fecha futura, el registro contable se realizará de forma automática en esa fecha a través del planificador.

### 4.5 Mantenimiento
Hacer click en la casilla Requiere Manteniemiento permite registrar el Manteinimiento del Activo. Para saber más visitar la página [Mantenimiento de Activos](/docs/user/manual/es/asset/asset-maintenance).

### 4.6 Luego de Validar
Una vez que se crea un Activo, se verán las opciones para transferir, descartar o vender el activo. Desde el botón Crear se puede ajustar el valor del mismo o realizar un registro de depreciación. 

![Asset Submit](/docs/assets/img/asset/asset-submit.png)

### 5. Temas Relacionados
1. [Mantenimiento de Activos](/docs/user/manual/es/asset/asset-maintenance)
1. [Movimiento de Activos](/docs/user/manual/es/asset/asset-movement)
1. [Recibo de Compra](/docs/user/manual/es/stock/purchase-receipt)
1. [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice)
