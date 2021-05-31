# Certificado de AFIP

Para acceder a un web service de AFIP, la aplicación debe presentar un certificado de seguridad (autenticación de usuario) expedido por AFIP, que determina quién está accediendo al web service. En consecuencia, para utilizar facturación electrónica en DiamoERP se debe generar y guardar un certificado de AFIP.
A continuación, se indica cómo generarlo, para lo cual será necesaria la asistencia del contador de la compañía. Para mayor información, hacer click [aquí](https://www.afip.gob.ar/ws/documentacion/certificados.asp). 

Para acceder a Certificados ir a:

> Inicio > Contabilidad > Configuración Factura Electrónica > Certificado


## 1. Creación de Certificado de AFIP

1. Ir al listado de Certificados y hacer click en "Agregar Certificado AFIP".
2. La mayoría de los campos deberían aparecer autocompletados si se ingresó previamente la información correspondiente en la Compañía. 
3. Haciendo click en *Guardar* y luego en *Crear Pedido de Certificado*, el sistema generará un Pedido CSR, el que deberá ser descargado y proporcionado al contador para que, con ese archivo, genere el Certificado Público desde la página de AFIP. 
4. Se deberá ingresar nuevamente en el Certificado y completar el campo de *Certificado Público* con el proporcionado por el contador.
5. Guardar nuevamente y luego *Aplicar Certificado*. 


## 2. Características

### 2. 1. Nuevo certificado AFIP

Cuando se desee generar un nuevo certificado de AFIP, la información de la Compañía aparecerá cargada por defecto. Deberá completarse un *Alias* para el certificado, así como el campo *Tipo de Conexión AFIP*. En el caso de que se trate de un certificado para testing (de prueba), el campo a completar será Homologación. **Esto permitirá que el sistema conecte con el web service de AFIP pero no validará las transacciones,** lo cual permite, por ejemplo, hacer facturas "de prueba" durante las etapas de implementación sin que las mismas impacten a nivel fiscal. En caso de que sea un certificado para transaccionar, deberá completarse Producción. **En este caso todas las operaciones que se cursen serán informadas en el momento a AFIP.**

### 2. 2. Pedido CSR

El Pedido CSR deberá ser descargado y proporcionado al contador para que éste pueda generar el Certificado Público a través de la página de AFIP.

### 2. 3. Certificado Público

Obtenido el Certificado Público desde la página de AFIP, se deberá completar el mismo en el campo en blanco en el Certificado Público del sistema. **Se recomienda abrir el archivo con un editor de texto plano (por ejemplo, Block de Notas) y copiar y pegar el contenido en la celda de DiamoERP correspondiente a *Certificado Público*.** Luego se deberá hacer click en *Guardar*, y posteriormente *Aplicar Certificado*.

### 2. 4. Conexión con AFIP

Una vez configurado el Certificado, para asegurarse de que la conexión con AFIP es correcta, se puede ingresar a una nueva [Factura de Venta](docs/user/manual/es/accounts/sales-invoice), elegir un [Punto de venta](docs/user/manual/es/accounts/punto-de-venta) electrónico (si no se cuenta con uno se deberá crearlo) y hacer click en *AFIP > Comprobar Conexión*. Si el sistema arroja un mensaje de éxito, la conexión ha funcionado correctamente.





