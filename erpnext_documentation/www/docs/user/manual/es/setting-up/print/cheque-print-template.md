<!-- add-breadcrumbs -->
# Plantilla de Impresión de Cheques

**La Plantilla de impresión de cheques permite definir plantillas para cheques bancarios.**

Los Negocios implican la realización de pagos a varias partes, como proveedores o empleados. Los pagos pueden hacerse de varias formas como efectivo, transferencia bancaria o cheque. Si se realiza un pago mediante cheque, se puede crear un Formato de Impresión para imprimir Cheques desde ERPNext, en base a la Entrada de Pago.

Para acceder a la Plantilla de Impresión de Cheques ir a: 
> Inicio > Contabilidad > Plantilla de impresión de cheques

Utilizando la Plantilla de impresión de cheques se puede generar un nuevo Formato de Impresión para cheques. Se creará en base al formato de cheque provisto por el banco.  

Un cheque de muestra:

<img class="screenshot" alt="Sample Cheque" src="{{docs_base_url}}/assets/img/setup/print/sample-cheque.jpg">


## 1. Creación de una Plantilla de impresión de cheques
1. Ir al listado de Plantilla de impresión de cheques y hacer click en Nueva.
1. Se puede configurar la posición de varios ítems en el cheque.
1. Guardar.

En la Plantilla de Impresión de Cheques, para cada valor (como Pagador, Fecha), se proveen las coordenadas exactas en base a dónde debería figurar ese valor en el cheque. La coordenadas se dan en centímetros. A continuación se encuentra una represetación de la estructura: 

<img class="screenshot" alt="Sample Cheque" src="{{docs_base_url}}/assets/img/setup/print/cheque-1.png">

### 1.1 Nuevo Formato a Través de Escaneo

Para acelerar la creación de nuevos formatos de impresión de cheques, se puede subir una imagen escaneada del cheque. Tomando en cuenta dicha imagen, el sistema actualiza las coordenadas automáticamente para cada valor como nombre de parte, monto, fecha, monto en palabras, etc. 

### 1.2 Nuevo Formato de Impresión Manual

Si la vista previa es correcta, hacer click en el botón **Crear Formato de Impresión**. De acuerdo con los valores provistos por la Plantilla de Impresión de Cheques, el sistema generará automáticamente un script HTML para el Formato de Impresión del Cheque.

Se pueden proveer coordenadas de forma manual para cada valor, de acuerdo a dónde se desee que se encuentre impreso en el cheque y personalizar con HTML/CSS.

#### Vista Previa
De acuerdo con la coordenadas provistas para todos los valores, se dará una vista previa para mostrar cómo se imprimirán los valores en el cheque. 

<img class="screenshot" alt="Sample Cheque" src="{{docs_base_url}}/assets/img/setup/print/cheque-2.png">

### 1.3 Impresión de Cheques

El nuevo formato de impresión generado para el cheque será visible en la Entrada de Pago. Luego de crearla se podrán imprimir los detalles de la transacción en el cheque. 
<img class="screenshot" alt="Sample Cheque" src="{{docs_base_url}}/assets/img/setup/print/cheque-3.gif">

### 2. Temas Relacionados
1. [Plantilla de Dirección](/docs/user/manual/es/setting-up/print/address-template)
1. [Plantilla de Términos y Condiciones](/docs/user/manual/es/setting-up/print/terms-and-conditions)
