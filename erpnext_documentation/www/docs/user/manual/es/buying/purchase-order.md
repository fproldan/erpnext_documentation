<!-- add-breadcrumbs -->
# Orden de Compra

**Una Orden de Compra es un contrato vinculante con el Proveedor, al cual se le promete comprar una serie de productos bajo ciertas condiciones.**

Es similar a la Orden de Venta pero en vez de enviarla a un sujeto externo, se la mantiene para registros internos. 

> Inicio > Compras > Compras > Orden de Compra

![Buying Flow](/docs/assets/img/buying/buying_flow_po.png)

## 1. Prerrequisitos
Antes de crear y utilizar una Orden de Compra se recomienda crear lo siguiente:

* [Proveedor](/docs/user/manual/es/buying/supplier)
* [Producto](/docs/user/manual/es/stock/item)


## 2. Creación de una Orden de Compra

Una Orden de Compra puede crearse automáticamente desde una Solicitud de Material o una Cotización de Proveedor.

1. Ir al listado de Orden de Compra y hacer click en Nuevo.
1. Seleccionar el Proveedor, y la fecha en que se requieren los productos.
1. En la tabla de productos, seleccionar el producto por código, se puede cambiar el "pedido para fecha" para cada producto. 
1. Configurar la cantidad y el precio será obtenido automáticamente si está configurado en el Producto. 
1. Configurar Impuestos.
1. Guardar y Validar.
    <img class="screenshot" alt="Purchase Order" src="{{docs_base_url}}/assets/img/buying/purchase-order.png">

### 2.1 Configurar Almacenes

* **Configurar Almacén de Destino**: De forma opcional, se puede configurar un Almacén de destino predeterminado a donde se enviarán los Productos comprados. Esto será obtenido en las filas de la tabla de Productos.

### 2.2 Obtener Productos desde Solicitudes de Material Abiertas

Los Productos pueden ser ingresados en la Orden de Compra automáticamente desde [Solicitudes de Material](/docs/user/manual/es/stock/material-request) abiertas. Para que esto funcione se deben seguir los siguientes pasos:

1. Seleccionar un Proveedor en la Orden de Compra.
1. Configurar el Proveedor predeterminado en el Producto en el campo correspondiente dentro de [Valores Predeterminados de Ventas, Compras y Contabilidad](/docs/user/manual/es/stock/item#39-item-defaults).
1. La [Solicitud de Material](/docs/user/manual/es/stock/material-request) debe ser de tipo "Compra".
1. Hacer click en el botón **Obtener productos de solicitudes de materiales abiertas** debajo del nombre del Proveedor. En ese momento aparecerá un diálogo con Solicitudes de Materiales con Productos en los cuales el Proveedor predeterminado es el mismo que el seleccionado en la Orden de Compra. Al seleccionar la Solicitud de Material y hacer click en **Obtener Productos**, estos serán tomados desde la misma.
 
<img class="screenshot" alt="Get Items from Open Material Requests" src="{{docs_base_url}}/assets/img/buying/get-items-from-open-mr.png">

> **Observación:** El botón **Obtener productos de solicitudes de materiales abiertas** es visible siempre y cuando la tabla de Productos esté vacía. 

## 3. Características

### 3.1 Dirección y Contacto

* **Dirección de proveedor**: La Dirección de Facturación del Proveedor.
* **Dirección de Envío**: La dirección de envío del Proveedor desde la cual estará enviando los productos. 
* Dirección, Dirección de Envío, Contacto, Correo electrónico de contacto serán obtenidas si se guardan en el Proveedor.


### 3.2 Divisa y Lista de Precios

Se puede seleccionar la moneda en la cual se guardará la orden de compra. Si se configura una Lista de Precios, los precios de los productos serán obtenidos desde allí. Si se selecciona "Ignorar reglas de precios" las Reglas de precios configuradas en Contabilidad > Reglas de precios, serán ignoradas.

Para saber más sobre Listas de Precios, hacer click [aquí](/docs/user/manual/es/stock/price-lists).

Para saber sobre manejo de transacciones en múltiples monedas, hacer click [aquí](/docs/user/manual/es/accounts/articles/managing-transactions-in-multiple-currency).

### 3.3 Subcontratación o "Suministro de materia prima". 

Configurar la opción "Suministro de materia prima" es útil para subcontrataciones donde se provee las materias primas para fabricar un producto. Para saber más, visitar la página [Subcontratación](/docs/user/manual/en/manufacturing/subcontracting).

### 3.4 Tabla de Productos

* **Escanear Código de Barras**: Se pueden añadir Productos a la tabla de Productos al escanear sus códigos de barra si se cuenta con un lector de código de barra. Para aprender a rastrearlos hacer click [aquí](/docs/user/manual/es/stock/articles/track-items-using-barcode)

* **Cantidad y Precio**: Al seleccionar el código de Producto, se obtendrán su nombre, descripción y UOM. El "Factor de Conversión UOM" se configurará de forma predeterminada en 1, se puede cambiar dependiendo de la UOM recibida del vendedor (más información al respecto en la próxima sección). 

    El "Precio de la lista de precios" será obtenido si se configura una tarifa de Compra Estándar. El "Precio de la última compra" muestra el precio del producto de la última Orden de Compra. Si fue configurado, el Precio se obtendrá desde el producto. Se puede adjuntar una Plantilla de Impuestos de Producto para aplicar una tasa impositiva específica al producto. 

* **Pesos del Producto** se obtendrá si fue configurado en el Producto, sino, se debe ingresar de forma manual. 

* **Almacén**: El Almacén a donde se entregarán los productos; será completado automáticamente si fue configurado en el campo "Asignar Almacén Destino". Tildando la opción "Contra la Orden general" puede vinsularse a una determinada [Orden general](/docs/user/manual/es/selling/blanket-order). También pueden vincularse un "Proyecto" y una "Lista de Materiales" para rastrear su progreso. 

* "Cantidad de acuerdo a la UOM predeterminada" mostrará las existencias actuales de acuerdo con la UOM configurada en el producto. La "Cantidad recibida" se acualizará cuando los productos sean facturados. 

* **Detalles de Contabilidad**: Esta sección se completa de forma automática para una Orden de compra. La "Cuenta de Gastos" es aquella contra la cual se factura la Orden de Compra y el Centro de Costo es la cuenta a la cual se carga la Orden de Compra.

Fecha "Solicitado para" en cada Producto: Si se esperan envíos por partes, el Proveedor sabrá qué cantidad enviar en cada fecha. Esto ayudará a prevenir un sobre abastecimiento. También ayudará a controlar qué tanto cumple el Proveedor los plazos. 

### 3.5 Materias Primas Suministradas

Esta sección aparece si se selecciona "Sí" en el campo "Suministro de materia prima". En la tabla se deben seleccionar los Productos provistos al Proveedor para el proceso subcontratado.

* **Establecer almacén de reserva**: en la [Subcontratación](/docs/user/manual/es/manufacturing/subcontracting), las materias primas se pueden reservar en un almacén diferente. Al seleccionarlo en este campo se lo usará para completar automáticamente las filas de Productos de la tabla de materias primas.

#### Tabla de materias primas

* **Cantidad Pedida**: El número de Productos requerido para completar la subcontratación de la forma especificada en la [Lista de Materiales](/docs/user/manual/es/manufacturing/bill-of-materials).
* **Cantidad Suministrada**: Esto se actualizará cuando se creen las Entradas de Inventario para transferir materiales al Almacén del Proveedor desde el Almacén de Reserva utilizando el botón **Transferir**.

    ![Subcontract Transfer Material](/docs/assets/img/buying/subcontract-transfer-materials.gif)

### 3.6 Conversión de UOM de Compra y UOM de Inventario

En la Orden de Compra, se puede cambiar la UOM de acuerdo con los requerimientos de inventario.

Por ejemplo, si se compró la materia prima en grandes cantidades con una UOM - Cajas, y se desea convertirla en UOM - Unidades, se puede realizar esto al crear la Orden de Compra. 

1. Configurar la UOM como unidades en el producto. Tener en cuenta que la UOM configurada en el Producto es la UOM de inventario. 
2. En la Orden de Compra mencionar la UOM como Caja. (Debido a que el material va a llegar en Cajas)
3. En la sección Almacén y Referencia, la UOM será obtenida automáticamente y será Unidades (desde el formulario de Producto):

 <img class="screenshot" alt="Purchase Order - UOM" src="{{docs_base_url}}/assets/img/buying/purchase-order-uom.png">

4. Mencionar el factor de conversión de UOM. Por ejemplo, (1); si una caja tiene 1 kilo. 
5. Tener en cuenta que la cantidad de existencias será actualizada de acuerdo con lo anterior. 

 <img class="screenshot" alt="Purchase Order - UOM" src="{{docs_base_url}}/assets/img/buying/po-stock-uom.png">

### 3.7 Impuestos y cargos

Si el Proveedor va a cobrar cargos o impuestos adicionales como gastos de envío o de seguro, los mismos pueden ser añadidos aquí. Esto ayudará a registrar los costos con más facilidad y precisión. A su vez, si alguno de estos gastos aumenta el valor del producto, también habrá que mencionarlos en la tabla de Impuestos. 

Visitar la página de [Plantilla de Impuestos (Compra)](/docs/user/manual/es/buying/purchase-taxes-and-charges-template) para saber más respecto a impuestos.

El total de impuestos y cargos se verá debajo de la tabla.

Para añadir impuestos de forma automática a través de una [Categoría de impuestos](/docs/user/manual/es/accounts/tax-category).

Para lograr una valuación precisa, es necesario asegurarse de ingresar todos los impuestos y cargos correctamente en la tabla correspondiente. 

#### Regla de Envío

Una Regla de Envío ayuda a determinar el costo de enviar un producto. El costo tenderá a aumentar a medida que la distancia de envío sea mayor. Para saber más, vistar la sección [Regla de Envío](/docs/user/manual/es/selling/shipping-rule).

<img class="screenshot" alt="Purchase Order Taxes" src="{{docs_base_url}}/assets/img/buying/po-taxes.png">

Por ejemplo, se compran Productos que valen X y se venden por 1,3X. Por ende el Cliente paga 1,3 veces el impuesto que el vendedor paga al Proveedor. Como ya se pagó impuestos al Proveedor por X, lo que se debe al Estado es solo 0.3 de impuestos. 

Esto puede ser rastreado fácilmente en ERPNext, ya que, cada impuesto principal es también una Cuenta. Idealmente, se deben crear dos Cuentas para cada tipo de IVA que se pague y colecte, “IVA-X de Compra” (activo) y “IVA-X de Venta” (pasivo), o algo similar que cumpla la misma función.

### 3.8 Descuento Adicional

Además de ofrecer descuentos por producto, esta sección permite sumar un descuento al total de la Orden de compra. Este descuento puede ser aplicado al importe total, es decir, con impuestos incluidos, o al importe neto, es decir, sin incluir impuestos y otros cargos. El descuento adicional puede aplicarse como monto o porcentaje. 

Para más detalles leer [Aplicar descuento](/docs/user/manual/es/selling/articles/applying-discount).

### 3.9 Términos de Pago

A veces el pago no se realiza en una sola cuota. Dependiendo del acuerdo, la mitad puede abonarse antes del envío y la otra mitad al recibir los productos o servicios. En esta sección, se puede añadir una plantilla de Términos de Pago o insertar los mismos de forma manual. 

Para saber más respecto a Términos de Pago hacer click [aquí](/docs/user/manual/es/accounts/payment-terms).

### 3.10 Términos y Condiciones

En operaciones de Compra/Venta puede haber ciertas bases y condiciones que rigen la forma en que el proveedor vende bienes o servicios al cliente. Se pueden aplicar los Términos y Condiciones a las transacciones y éstos aparecerán en el documento impreso. Para saber más respecto a Términos y Condiciones, hacer click [aquí](/docs/user/manual/es/setting-up/print/terms-and-conditions)

### 3.11 Ajustes de Impresión
#### Membrete
Se pueden imprimir los pedidos de cotización/orden de compra en papel con el membrete de la empresa. Más información [aquí](/docs/user/manual/es/setting-up/print/letter-head).

"Agrupar productos iguales", agrupará los productos iguales que se hayan sumado muchas veces a la tabla de Producto. Esto puede verse al imprimir.

#### Encabezado
Los títulos de los documentos pueden ser modificados. Leer más [aquí](/docs/user/manual/es/setting-up/print/print-headings).

El Descuento Adicional del vendedor, los Términos de Pago, los Términos y Condiciones pueden registrarse en la Orden de Compra.

### 3.12 Más Información
Esta sección muestra el estado de la Orden de Compra, porcentaje de productos recibidos y porcentaje de productos facturados. Si es una Orden entre Empresas, la Orden de Venta puede ser vinculada aquí. 

### 3.13 Luego de Validar
Una vez que se "Valida" la Orden de Compra, se pueden generar acciones como estas:

* Se puede Añadir, Actualizar y Borrar Productos en la Orden de Compra haciendo click en el botón **Actualizar Productos**. De cualquier forma, no se puede borrar productos que ya hayan sido recibidos.

* Estado: Luego de validada se puede mantener una Orden de Compra o Cerrarla. 

* Crear: De una Orden de Compra validada, se puede crear lo siguiente: 

    * [Recibo de Compra](/docs/user/manual/es/stock/purchase-receipt) - Un recibo que indica que se recibieron los Productos.
    * [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice) - Una factura para la Orden de Compra.
    * [Entrada de Pago](/docs/user/manual/es/accounts/payment-entry) - Un registro que indica que el pago de la orden de compra ha sido realizado. 
    * [Asiento Contable](/docs/user/manual/es/accounts/journal-entry) - Se crea un Asiento en el Libro Mayor.

    ![Purchase Order post submitting](/docs/assets/img/buying/po-after-submit.png)

### 4. Temas Relacionados
1. [Solicitud de Cotización](/docs/user/manual/es/buying/request-for-quotation)
1. [Plantilla de Impuestos (compra)](/docs/user/manual/es/buying/purchase-taxes-and-charges-template)
1. [Comprar en Diferentes Unidades](/docs/user/manual/es/buying/articles/purchasing-in-different-unit)
1. [Corregir Orden de Compra validada](/docs/user/manual/es/buying/articles/amending-purchase-order-after-submit)
