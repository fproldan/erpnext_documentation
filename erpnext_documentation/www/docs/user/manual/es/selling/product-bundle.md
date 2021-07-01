<!-- add-breadcrumbs -->
# Paquete de Productos

**Un Paquete de Productos es un documento donde se puede crear una lista de productos existentes que se agrupan y se venden en conjunto (o paquete).** 

Por ejemplo, cuando se vende un teléfono celular, es necesario también entregar en conjunto con el mismo, el cargador, cable USB y tarjeta SIM y por ende, es necesario que las existencias de los mismos se vean afectadas. 
Para tener en cuenta lo anterior, se puede crear un Paquete de Productos para el producto principal, es decir, teléfono celular. Luego, es necesario armar la lista de los productos a entregar, es decir, el teléfono celular + cargador + cable + tarjeta SIM, estos productos serán llamados "Productos Secundarios". 

Un Paquete de Productos puede ser visto, desde el punto de vista de la venta, como una "Lista de Materiales".

A continuación se encuentran los pasos necesarios para crear un Paquete de Productos y utilizarlo en las transacciones de venta. 

Para acceder a Paquete de Productos ir a: 
> Inicio > Ventas > Productos y Precios > Paquete de Productos

## 1. Prerrequisitos
Antes de crear y utilizar un Paquete de Productos se recomienda crear lo siguiente:

* [Producto](/docs/user/manual/es/stock/item)

## 2. Creación de un Paquete de Productos
1. Ir al listado de Paquete de Productos y hacer click en Nuevo. 
2. Seleccionar el Producto Principal, crear uno si no fue creado. Asegurarse de no seleccionar la opción Mantener Stock al crear el Producto principal. Por ejemplo: Vajilla. 
3. Ingresar un precio para el producto principal, éste será utilizado cuando se realice una transacción. 
4. Se puede también escribir una descripción para uso interno. 
5. Ingresar en la tabla de productos los que componen el paquete junto con sus cantidades. 
6. Guardar.
<img class="screenshot" alt="Product Bundle" src="{{docs_base_url}}/assets/img/selling/product-bundle.png">

### 2.1 Seleccionar Producto principal

En el Paquete de Productos hay dos secciones. El "Producto Principal" y la lista de productos (Productos Secundarios).

El "Producto Principal" debe ser visto más bien como un producto contenedor o virtual y no como un producto físico. 
El "Producto Principal" debe ser un <b>producto sin existencias</b>. Para crear un <b>producto sin existencias</b> se debe destildar la opción "Mantener Stock" en el Formulario de Producto. 
Es un producto sin existencias porque no se mantienen existencias para el mismo, sino solo para los "Productos Secundarios". 
Si se quiere mantener existencias para el Producto Principal entonces se debe crear un Listado de Materiales (LdM) y empaquetarlos utilizando las Transacciones de Ingreso de Existencias. 

### 2.2 Seleccionar Productos Secundarios

En la Tabla de Productos se ingresarán todos los productos secundarios para los cuales se mantienen existencias y que serán enviados al cliente.
Recordar: El "Producto Principal" es solo virtual, con lo cual el mismo (en nuestro ejemplo de arriba, teléfono celular) también debe incluirse en el listado de Productos Secundarios (o de Lote). 

## 3. Características
### 3.1 Paquete de Productos en Transacciones de Venta 

Al realizar Transacciones de Venta (Factura de Venta, Orden de Venta, Nota de Entrega) el Producto Principal será seleccionado en la tabla principal de productos. 

<img class="screenshot" alt="Product Bundle" src="{{docs_base_url}}/assets/img/selling/product-bundle.gif">

Al seleccionar el Producto Principal en la tabla principal de productos, sus productos secundarios serán tomados en la Tabla de Lista de Envío de la transacción. Si el producto secundario es seriado, se podrá especificar su número de serie en la lista de envío. Al enviar la transacción, el sistema reducirá el nivel de existencias de los productos secundarios en el almacén especificado en la tabla de Lista de Envío. 

<div class="well"><b>Use Product Bundle to Manage Offers/Schemes:</b>
<br>
Esto fue descubierto cuando un cliente, que se dedicaba a la venta de productos nutricionales, solicitó una función que permita administrar ofertas como "Comprar uno y llevar uno gratis". Para eso, creó un producto sin existencias que fue utilizado como Producto Principal. En la descripción del producto ingresó los detalles de la oferta con la imagen del producto mostrando la misma. El producto a la venta fue seleccionado como Producto Paquete donde la cantidad era dos. Por ende, cada vez que se vendía una unidad del Producto Principal bajo esta oferta, el sistema deducía dos unidades del producto en el Almacén.</div>

### 4. Temas relacionados
1. [Producto](/docs/user/manual/es/stock/item)
