<!-- add-breadcrumbs -->
# Nota de Entrega

**Una Nota de Entrega se realiza cuando se envía un cargamento desde el Almacén de la Empresa hacia el Cliente.**

Normalmente, se envía una copia de la Nota de Entrega con el transportista. La Nota de Entrega contiene la lista de Productos que se envían en el cargamento y actualiza el inventario. La Nota de Entrega es un paso opcional y puede crearse una Factura de Venta directamente desde una Orden de Venta. 

Para acceder al listado de Nota de Entrega ir a:
> Inicio > Almacén > Transacciones de Inventario > Nota de Entrega

![Delivery Note flow](/docs/assets/img/stock/delivery-note-flow.png)

## 1. Prerrequisitos
Antes de crear y utilizar una Nota de Entrega se recomienda crear lo siguiente:

* [Orden de Venta](/docs/user/manual/es/selling/sales-order)

## 2. Creación de una Nota de Entrega
La creación de Nota de Entrega es muy similar al Recibo de Compra. Generalmente se crea desde una Orden de Venta validada (que todavía no fue enviada al cliente) al hacer click en Crear > Nota de Entrega.

Para crear una Nota de Entrega de forma _manual_ (no recomendado), seguir los siguientes pasos:

1. Ir al listado de Nota de Entrega y hacer click en Nuevo.
1. Los detalles del Producto y del Cliente pueden ser tomados desde la Orden de Venta haciendo click en "Obtener Productos de > Orden de Venta".
1. La UOM y los Precios serán tomados automáticamente.
1. Guardar y Validar.

    <img class="screenshot" alt="Delivery Note" src="{{docs_base_url}}/assets/img/stock/delivery-note.png">

Si la Nota de Entrega es creada desde la Orden de Venta, se tomará desde allí toda la información respecto a Productos no enviados y otros detalles. 

También se puede editar la fecha y hora de contabilización de la Nota de Entrega. De forma predeterminada, las mismas se establecerán en el día y la hora en que se crea la Nota de Entrega. 

### 2.1 Estados

Estos son los estados en que puede encontrarse una Nota de Entrega:

* **Borrador**: Se guarda un borrador pero todavía no se envía al sistema.
* **Pendiente de Facturación**: Pendiente de facturación a través de una [Factura de Venta](/docs/user/manual/es/accounts/sales-invoice).
* **Completa**: Validada y con todos los Productos enviados. 
* **Cancelada**: Nota de Entrega cancelada.
* **Cerrada**: El fin del estado Cerrado es administrar el cierre definitivo de la Nota de Entrega. Por ejemplo, el Cliente pidió 20 unidades de producto pero se cierra en 15, por ende las otras 5 unidades no serán enviadas ni facturadas. 

### 2.2 Envíos Parciales

Cuando se crea una Nota de Entrega desde una Orden de Venta, las cantidades pueden cambiarse. De forma que, si la Orden de Venta contiene 10 Productos a ser enviados, y solo se envía 5 esta semana y los restantes la semana que viene, entonces se puedan crear dos Notas de Entrega en dos semanas. 

## 3. Acciones Relacionadas
### 3.1 Detalles de la Orden de Compra del Cliente
Aquí se puede ingresar el número de Orden de Compra del Cliente a fin de tenerla como referencia. 

### 3.2 Dirección y Contacto
* **Dirección de Envío**: La dirección del Cliente a donde serán enviados los Productos. 
* **Persona de Contacto**: Si el cliente es una organización, agregar la Persona de Contacto en este campo. 

[Contactos](/docs/user/manual/es/CRM/contact) y [Direcciones](/docs/user/manual/es/CRM/address) se almacenan por separado para que se puedan adjuntar muchos Contactos o Direcciones al cliente.

### 3.3 Divisa y Lista de Precios
En esta sección se puede configurar la moneda en la cual se enviará la Nota de Entrega. Esto generalmente se obtiene, si fue configurado, de la Orden de Venta. Si se configura una Lista de Precios, los precios de los productos serán tomados de allí. Si se selecciona "Ignorar la Regla de precios", las Reglas establecidas en Contabilidad > Reglas de precios, serán ignoradas.

Para saber más sobre Listas de Precios, [click aquí](/docs/user/manual/es/stock/price-lists).

Para saber respecto a administrar transacciones en distintas monedas, hacer click [aquí](/docs/user/manual/es/accounts/articles/managing-transactions-in-multiple-currency).

### 3.4 Almacenes

* **Establecer Almacén de Origen**: Desde aquí provendrán los Productos a ser enviados al Cliente. 
* **Almacén Destino**: En un escenario de ventas típico, el Producto existe en el Almacén y llega al Cliente. Sin embargo, si se desea retener stock de muestra, se debe ingresar un Almacén en este campo. 

### 3.5 Tabla de Productos
* **Código de Barra**: Se puede rastrear Productos utilizando [Códigos de Barra](/docs/user/manual/en/stock/articles/track-items-using-barcode).

* El Código de Producto, el nombre, descripción, Imagen y Fabricante serán obtenidos desde el [Producto](/docs/user/manual/es/stock/item).

* **Escanear Código de Barra**: Se pueden añadir Productos a la tabla de Productos al escanear sus códigos de barra si se cuenta con el lector correspondiente. Para aprender a rastrearlos click [aquí](/docs/user/manual/es/stock/articles/track-items-using-barcode)

* **Descuento y Margen**: Se pueden aplicar descuentos sobre productos individuales en forma de porcentaje  o el monto total del Producto. Leer [Aplicar Descuento](/docs/user/manual/es/selling/articles/applying-discount) para más detalles.

* **Precio**: El Precio será tomado desde la [Lista de Precios](/docs/user/manual/es/stock/price-lists), si se hubiere configurado ahí, y se calculará el Importe total.

* **Plantilla de Impuesto de Producto**: Se puede configurar una Plantilla de Impuesto de Producto para aplicar un Impuesto específico a este Producto en particular. Para saber más, visitar [esta página](/docs/user/manual/es/accounts/item-tax-template).

* Si hubiesen sido configurados allí, los Detalles de Peso del Producto por unidad y Peso en UOM serán tomados del Producto.

* **Almacén y Referencia**: Se muestra el Almacén desde el cual se envían los Productos al Cliente. A su vez, si la Nota de Entrega se creó de la siguiente forma "Orden de Venta > Nota de Entrega", también se mostrará la Orden de Venta. 

* **Número de Serie y Número de Lote**: Si el Producto es seriado o está en lotes, se deberá introducir el [Número de Serie](/docs/user/manual/es/stock/serial-no) y [Número de Lote](/docs/user/manual/es/stock/batch) en la tabla de Productos. Se pueden ingresar múltiples Números de Serie en un sola fila (cada uno en una línea distinta) y se deberá ingresar tantas veces el Número de Serie como la cantidad de producto a comprar/vender. 

    Se mostrarán la "Cantidad disponible en el Almacén", la "Cantidad de lotes disponibles en el Almacén" y la "Cantidad Instalada". Para saber más respecto a instalación, visitar la página [Nota de Instalación](/docs/user/manual/es/stock/installation-note).

    **Observación**: El Producto debe estar seriado o en lote para que estas características funcionen. Si el Producto está seriado, aparecerá una ventana emergente donde se pueden ingresar los Números de Serie. 

* La Cuenta de Gastos es la cuenta desde la cual se debitará el monto. Si se selecciona "Permitir tasa de valoración cero", se permitirá validar la Nota de Entrega inclusive si la Valoración del Producto es 0. Esto puede ser porque se trate de una muestra de un producto o por un acuerdo con el Proveedor.  

* Las Dimensiones Contables ayudan a identificar cada transacción con diferentes Dimensiones sin la necesidad de crear nuevos Centros de Costos. Para esto, primero se deben crear las Dimensiones Contables, para saber más, visitar [esta página](/docs/user/manual/es/accounts/accounting-dimensions).

* **Salto de Página** creará un salto de página justo antes de este producto al imprimir.

### 3.6 Registrar Inspecciones de Calidad
Si para algunos Productos es obligatorio registrar Operaciones de Calidad (si esto fue establecido en el Producto), se deberá actualizar el campo "Inspección de Calidad". El sistema solo permitirá validar el Recibo de Compra si se actualiza la "Inspección de Calidad".

Luego de habilitar los Criterios de Inspección para Ventas en el [Formulario de Productos](/docs/user/manual/es/stock/item#216-inspection-criteria) y de adjuntar allí una Plantilla de Inspección de Calidad, las Inspecciones de Calidad pueden ser registradas en Notas de Entrega. 

### 3.7 Impuestos y cargos
Los Impuestos y cargos serán tomados desde la [Orden de Compra](/docs/user/manual/es/buying/purchase-order).

Visitar la página de [Plantilla de Impuestos (Venta)](/docs/user/manual/en/selling/sales-taxes-and-charges-template) para saber más de impuestos.

El total de impuestos y cargos será mostrado debajo de la tabla. 

Para añadir impuestos de forma automática a través de una Categoría de Impuesto, visitar [esta página](/docs/user/manual/es/accounts/tax-category).

Asegurarse de añadir correctamente todos los impuestos en la tabla de Impuestos y cargos para una valoración precisa.

#### Regla de envío
Una Regla de envío ayuda a determinar el costo de enviar un producto. El costo tenderá a aumentar a medida que la distancia de envío sea mayor. Para saber más, vistar la sección [Regla de envío](/docs/user/manual/es/selling/shipping-rule) page.

### 3.8 Descuentos Adicionales
En esta sección puede configurarse cualquier descuento adicional a aplicar a toda la orden. Este descuento puede basarse en el Importe Total, es decir, luego de impuestos y cargos, o en el Total Neto, es decir, antes de impuestos y cargos. El descuento adicional puede ser aplicado como porcentaje o monto. 
Leer [Aplicar Descuento](/docs/user/manual/es/selling/articles/applying-discount) para más detalles.

### 3.9 Términos y Condiciones
En operaciones de Compra/Venta puede haber ciertas bases y condiciones que rigen la forma en que el proveedor vende bienes o servicios al cliente. Se pueden aplicar los [Términos y Condiciones](/docs/user/manual/en/setting-up/print/terms-and-conditions) a las transacciones y estos aparecerán en el documento impreso.

### 3.10 Información de Transportista
Si se terceriza el transporte de los Bienes hacia su lugar de entrega, los detalles del transportista pueden ser agregados. Esto no es lo mismo que [envío triangulado](/docs/user/manual/es/selling/articles/drop-shipping).

* **Transportista**: El Proveedor que va a llevar el Producto al Cliente. El [Proveedor](/docs/user/manual/es/buying/supplier) debería estar configurado como Transportista para poder seleccionarlo aquí.
* **Conductor**: Se puede añadir aquí el conductor que manejará el medio de transporte. 

![Delivery Note Transport](/docs/assets/img/stock/delivery-note-transport.png)

Pueden registrarse los siguientes detalles:

* Distancia en kilómetros
* Método de transporte, es decir, ruta, aire, tren o barco. 

### 3.11 Más Información

La Nota de Entrega puede relacionarse a los siguientes documentos a fines de contar con información más completa: 

* [Proyecto](/docs/user/manual/es/projects/project)
* [Campaña](/docs/user/manual/es/CRM/campaign)
* [Fuente de la Iniciativa](/docs/user/manual/es/CRM/lead_source)

### 3.12 Ajustes de Impresión

#### Membrete
Se pueden imprimir las Notas de Entrega en papel con el membrete de la empresa. Saber más [aquí](/docs/user/manual/es/setting-up/print/letter-head).

"Agrupar productos iguales", agrupará los productos iguales que se hayan sumado muchas veces a la tabla de Producto. Esto puede verse al imprimir. 

#### Encabezado
Los encabezados de las Notas de Entrega pueden ser modificados al imprimir el documento. Se puede hacer esto seleccionando **Encabezado**. Para crear nuevos Encabezados de Impresión ir a: Inicio > Configuraciones > Impresión > Encabezado. Leer más [aquí](/docs/user/manual/es/setting-up/print/print-headings).

Hay opciones adicionales para poder imprimir la Nota de Entrega sin el monto, esto puede ser útil cuando el Producto tiene un valor muy alto. También, al imprimir, se pueden agrupar los Productos iguales en una fila. 

### 3.13 Estado
Aquí se muestran el estado del documento y el porcentaje de instalación. Cualquier instrucción adicional para el envío puede ser ingresada en este campo. 

### 3.14 Comisión

Si la venta fue realizada a través de algún Socio de ventas, aquí se pueden añadir los detalles de su comisión. Esto generalmente se toma desde la Orden de Venta.

### 3.15 Equipo de Ventas
**Vendedores:** ERPNext permite añadir a todos los vendedores que hayan trabajado en esta venta.

Esto generalmente se toma desde la Orden de Venta, por ejemplo: 

<img class="screenshot" alt="Sales Team in Sales Order" src="{{docs_base_url}}/assets/img/selling/so-sales-team.png">

### 3.16 Envío de Paquetes o Productos con Paquete de Productos

Si se está enviando Productos que son parte de un [Paquete de Productos](/docs/user/manual/es/selling/product-bundle), ERPNext creará automáticamente una tabla de Lista de Embalaje basada en los sub-productos de ese Producto. 

Si los Productos son seriados, entonces para el tipo de Productos del Paquete de Productos hay que actualizar el Número de Serie en la tabla de "Lista de Embalaje". 

### 3.17 Embalaje de Productos

Si se está realizando el envío a través de distintas cajas o por peso, se puede utilizar una Nota de Embalaje para dividir la Nota de Entrega en unidades más pequeñas. Para saber más respecto a Listas de Embalaje visitar [esta página](/docs/user/manual/es/stock/packing-slip).

Se pueden crear muchas Listas de Embalaje desde una Nota de Entrega y ERPNext se asegurará que las cantidades en la Lista no excedan las cantidades en la Nota. Tener en cuenta que se puede crear una Lista de Embalaje desde una Nota de Entrega solo cuando esta úlrima está en borrador. 

### 3.18 Luego de Validar

Cuando la Nota de Entrega es validada, se creará una entrada en el Mayor de inventario para cada Producto y se actualizará el inventario. 
La Cantidad Pendiente en la Orden de Venta es actualizada (si corresponde).

El Tablero mostrará las siguientes opciones: 

* [Nota de Instalación](/docs/user/manual/es/stock/installation-note)
* [Devolución de Venta](/docs/user/manual/es/stock/sales-return)
* [Hoja de ruta](/docs/user/manual/es/stock/delivery-trip)
* [Facturas de Venta](/docs/user/manual/es/accounts/sales-invoice)

![Delivery Note after submit](/docs/assets/img/stock/delivery-note-submit.png)

### 3.19 Devolución de Orden de Venta
Una vez validada la Orden de Venta utilizando una Nota de Entrega, se puede crear una devolución en caso de que el [Cliente](/docs/user/manual/es/CRM/customer) devuelva el Producto. Para saber más visitar la página [Devoluciones de Venta](/docs/user/manual/es/stock/sales-return).

### 3.20 Saltear Nota de Entrega

Si no se quiere crear una Nota de Entrega luego de realizada una Orden de Venta, y se desea pasar directamente a una Factura de Venta, habilitar esta opción en [Configuración de Venta](/docs/user/manual/es/selling/selling-settings#32-delivery-note-required).

### 4. Temas Relacionados
1. [Almacén](/docs/user/manual/es/stock/warehouse)
1. [Error de Inventario en Nota de Entrega](/docs/user/manual/es/stock/articles/delivery-note-stock-error)
1. [Transferencia de Material desde Nota de Entrega](/docs/user/manual/es/stock/articles/material-transfer-from-delivery-note)
1. [Nota de Instalación](/docs/user/manual/es/stock/installation-note)
1. [Hoja de ruta](/docs/user/manual/es/stock/delivery-trip)
