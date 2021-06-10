<!-- add-breadcrumbs -->
# Orden de Venta

**Una Orden de Venta es la confirmación de un pedido del cliente.**

Usualmente es un contrato vinculante con el Cliente. Una vez que este confirma la Cotización, se la puede convertir en una Orden de Venta.

<img class="screenshot" alt="Make Quotation from Opportunity" src="{{docs_base_url}}/assets/img/selling/selling-flow-so.png">

Para acceder a Orden de Venta ir a:
> Inicio > Ventas > Ventas > Orden de Venta

## 1. Prerrequisitos

Antes de crear y utilizar una Orden de Venta se recomienda crear lo siguiente: 

* [Cliente](/docs/user/manual/es/CRM/customer)
* [Producto](/docs/user/manual/es/stock/item)

## 2. Creación de una Orden de venta

1. Ir al listado de Orden de Venta y hacer click en Nuevo.
1. Seleccionar el Cliente
1. Configurar la "Fecha de entrega" (se aplica a todo el pedido).
1. En Tipo de Orden se puede establecer si se trata de una Orden de Venta, una Orden de Mantenimiento, o si proviene de una operación online [Carrito de compras](/docs/user/manual/en/website/shopping-cart) desde el sitio web. La configuración predeterminada la va a establecer como "Ventas".
1. En la sección "Orden de Compra del Cliente" se puede agregar el número de Orden de Compra u otros detalles que puedan ser útiles como referencia. 
1. Añadir los productos y cantidades a ser enviados en la tabla correspondiente. Si los precios de los productos ya fueron configurados, el campo Precio se completará automáticamente. Si no, es necesario introducir los precios de los productos manualmente. También se puede modificar la tarifa completada automáticamente en caso de que deban hacerse cambios en su valor. 
1. Hacer click en "Guardar" para guardar un borrador de la Orden de Venta. 
1. Si se hace click en "Validar", la Orden de Venta será almacenada definitivamente en el Sistema. 

### 2.1 Otras formas de crear una Orden de Venta

1. También se puede crear una Orden de Venta desde una Cotización que haya sido enviada haciendo click en el boton "Crear" que se encuentra arriba a la derecha.

  <img class="screenshot" alt="Make Sales Order from Quotation" src="{{docs_base_url}}/assets/img/selling/make-SO-from-quote.png">

1. O se puede crear una nueva Orden de Venta y extraer detalles de una Cotización. 

  <img class="screenshot" alt="Make Sales Order from Quotation" src="{{docs_base_url}}/assets/img/selling/so-from-quote.gif">

Para permitir Reglas de precios por clientes, (el "Cliente A" paga $1,00 por el "Producto 1", pero el "Cliente B" paga $1,25 por el mismo producto) hay que tildar la opción "Permitir al Usuario Editar Lista de Precios en Transacción" en [Configuración de Venta](/docs/user/manual/es/selling/selling-settings). Esto permite guardar el precio por producto específico para cada cliente cuando se cambia un precio en la Orden de Venta. 

## 3. Características

### 3.1 Divisa y Lista de Precios

Se puede seleccionar la moneda en la cual se arma la cotización u orden de venta. Si se configura una Lista de Precios, los precios de los productos serán obtenidos desde allí. Si se selecciona "Ignorar Regla de precios" las [Reglas de precios](/docs/user/manual/es/accounts/pricing-rule) establecidas en Contabilidad > Reglas de precios, serán ignoradas.

Para saber más sobre Listas de Precios, hacer click [aquí](/docs/user/manual/es/stock/price-lists).

Para saber sobre manejo de transacciones en múltiples monedas, hacer click [aquí](/docs/user/manual/es/accounts/articles/managing-transactions-in-multiple-currency).

### 3.1 Establecer Almacén de Origen

Si se posee stock de productos en múltiples almacenes, configurar uno de origen en esta sección va a ocasionar que todos los productos de la tabla de productos sean extraídos desde ese almacén. Debe haber existencias disponibles en el "Almacén de Origen" que se está seleccionando. Esta opción va a modificar el "Almacén Predeterminado" establecido en el producto.

### 3.2 Tabla de Productos

* **Fechas de entrega para cada producto**: Si hay muchos productos, establecer una fecha de entrega en la primera fila hará que la misma sea copiada a las filas de abajo, si éstas están en blanco. Si no se configuran en su totalidad, hay que configurarlas desde la parte de arriba de la Orden de Venta. 

    Una Orden de Venta muestra el monto facturado, la tasa de valuación, y la ganancia bruta en la tabla de productos cuando se hace click en Edit para expandir una fila. 

    También se pueden sumar productos en la tabla de productos escaneando sus códigos de barra si se cuenta con un lector de código de barras. Aprender a usar códigos de barras para rastrear productos [aquí](/docs/user/manual/es/stock/articles/track-items-using-barcode)

* **Almacén de entrega**: Este es el almacén desde el cual se extraerán los productos para ser enviados al cliente.

* **Envío triangulado**: Esta es una situación en la cual no se cuenta con existencias de los productos sino que se los envía directamente al cliente desde el proveedor. Para permitir el envío triangulado de un producto tildar la opción "Proveedor envía a cliente". Al hacer esto, la opción Almacén de Envío desaparecerá. Seleccionar el proveedor en el campo "Proveedores". 

    Además, si se crea una Orden de Compra desde esta Orden de Venta, se creará para el proveedor seleccionado y solo para los productos válidos para envío triangulado. 

* **Planificación**: Para saber respecto a los campos de planificación hacer click [aquí](/docs/user/manual/es/stock/projected-quantity).

Los otros campos de la tabla de productos son similares a lo explicado en [Cotización](/docs/user/manual/es/selling/quotation#23-the-items-table).

### 3.3 Lista de Embalaje

Está asociada a los [Paquetes de productos](/docs/user/manual/es/selling/product-bundle) y solo aparece cuando la transacción involucra un paquete de productos. 

La tabla de "Lista de Embalaje" se actualizará de forma automática cuando se guarde la Orden de Venta. Si algún producto es un Paquete de Productos, entonces la "Lista de Embalaje" va a estar compuesta por el listado detallado de los productos.

Se deberá seleccionar un Almacén de entrega incluso para un producto perteneciente a un paquete de productos, este almacén luego será actualizado en los productos de la Lista de Embalaje. Se puede cambiar el almacén, el número de serie y lote en los productos de la lista de embalaje en el caso de que los productos dentro del paquete de productos provengan de distintos almacenes.

Una Lista de Embalaje tiene la siguiente apariencia:

<img class="screenshot" alt="Packing List" src="{{docs_base_url}}/assets/img/selling/so-packing-list.png">

### 3.4 Impuestos y cargos
Para sumar impuestos a la Orden de venta se puede seleccionar una [Plantilla de impuestos (venta)](/docs/user/manual/es/selling/sales-taxes-and-charges-template) o añadir los impuestos de forma manual en la tabla de Impuestos y cargos.

El total de impuestos se verá al final de la tabla. Haciendo click en Disolución de Impuestos se pueden ver todos los componentes y montos. 

<img class="screenshot" alt="Taxes in Quotation" src="{{docs_base_url}}/assets/img/selling/sales-order-taxes.png">

Después de guardar la Orden de venta aparece en el desplegable de Acciones el botón **Calcular percepciones**, mediante el cual se pueden agregar automáticamente en esta tabla los impuestos de percepción que correpsondan para el Cliente en particular. Para más información al respecto visitar [Configuración de Percepciones](/docs/user/manual/es/accounts/configuracion-de-percepciones).

#### Regla de Envío
Una Regla de Envío ayuda a determinar el costo de enviar un producto. Este tenderá a aumentar a medida que la distancia de envío sea mayor. Para saber más, vistar la sección [Regla de Envío](/docs/user/manual/es/selling/shipping-rule).

Si se selecciona una Categoría de Impuestos, la plantilla y la tabla de impuestos se completarán automáticamente. Para saber más visitar [esta página](/docs/user/manual/es/accounts/tax-category).

### 3.5 Descuentos Adicionales
Además de ofrecer descuentos por producto, esta sección permite sumar un descuento al total de la Orden de venta. Este descuento puede ser aplicado al importe total, es decir, con impuestos incluidos, o al importe neto, es decir, sin incluir impuestos y otros cargos. El descuento adicional puede aplicarse como monto o porcentaje. 

Para más detalles, leer [Aplicar descuento](/docs/user/manual/es/selling/articles/applying-discount).

### 3.6 Términos de Pago
A veces el pago no se realiza en una sola cuota. Dependiendo del acuerdo, la mitad puede abonarse antes del envío y la otra mitad al recibir los productos o servicios. En esta sección se puede añadir una plantilla de Términos de Pago o insertar los mismos de forma manual. 

Para saber más respecto a Términos de Pago, hacer click [aquí](/docs/user/manual/es/accounts/payment-terms).

### 3.7 Términos y Condiciones
En operaciones de Compra/Venta puede haber ciertas bases y condiciones que rigen la forma en que el proveedor vende bienes o servicios al cliente. Se pueden aplicar Términos y Condiciones a las transacciones y estos aparecerán en el documento impreso. Para saber más respecto a Términos y Condiciones hacer click [aquí](/docs/user/manual/es/setting-up/print/terms-and-conditions)

### 3.8 Ajustes de Impresión
#### Membrete
Las Cotizaciones u Ordenes de venta pueden ser impresas en papel con el membrete de la empresa. Leer más [aquí](/docs/user/manual/es/setting-up/print/letter-head).

#### Encabezado
Esto puede cambiarse seleccionando un **Encabezado**. Para crear nuevos encabezados ir a: Inicio > Configuración > Impresión > Encabezado. Más información [aquí](/docs/user/manual/es/setting-up/print/print-headings).

"Agrupar productos iguales" sirve para agrupar productos que hayan sido añadidos más de una vez en la tabla de productos. Esto se puede ver al imprimir.

### 3.9 Más información
* **Campaña:** Una campaña de ventas puede ser asociada a la Orden de venta. Un grupo de Ordenes puede ser parte de una campaña de ventas.
* **Referencia:** Si la Orden de venta es para un potencial cliente, sus datos pueden obtenerse desde la Fuente de la Iniciativa tanto desde una campaña, un proveedor, exhibición, etc. Si se quiere cotizar a un cliente actual, seleccionar Cliente Actual.
* **Referencia de pedido entre empresas**: Si dos empresas son parte de la misma organización o tienen una relación principal-secundaria, se puede asociar una Orden de Compra a esta Orden de Venta. Leer más sobre facturación entre empresas [aquí](/docs/user/manual/es/accounts/inter-company-invoices).
* **Proyecto**: Si la Orden de Venta es parte de un Proyecto se puede asociar en esta sección y por ende, el progreso del Proyecto será actualizado.

### 3.10 Estado de Facturación y Entrega

* **Estado**: El estado de la Orden de Venta puede ser Borrador, en Espera, para Entregar y Facturar, para Facturar, para Entregar, Completa, Cancelada o Cerrada. 
* **Porcentaje Facturado y Entregado**: El porcentaje del monto facturado y los productos entregados de la Orden de Venta. 

### 3.11 Comisión
Si la venta se dio a través de un Socio de ventas, se pueden sumar los detalles de su comisión aquí. Se ingresa la tasa de comisión y su monto se verá debajo. 

### 3.12 Equipo de Ventas
**Vendedores:** ERPNext permite añadir a todos los vendedores que hayan trabajado en este trato. Se puede cambiar el porcentaje de contribución de cada uno y calcular cuántos incentivos se ganaron con esta transacción. 

<img class="screenshot" alt="Sales Team in Sales Order" src="{{docs_base_url}}/assets/img/selling/so-sales-team.png">

### 3.13 Sección de Repetición Automática
Repetir automáticamente Ordenes de Venta es como una suscripción. Se debe seleccionar una fecha desde y una fecha hasta. Seleccionar la Repetición Automática creada. Para saber más sobre repeticiones automáticas [click aquí](/docs/user/manual/es/automation/auto-repeat).

### 3.14 Luego de Validar
La Orden de Venta es una transacción "Validable". Acciones posteriores (como confeccionar una Nota de Entrega) solo podrán ejecutarse luego de "Validar" la Orden de Venta.

Una vez que se "Valida" la Orden de Venta, se pueden realizar las siguientes acciones desde la misma: 

* Se pueden Agregar, Actualizar y Borrar productos de la Orden de Venta haciendo click en el botón **Actualizar Productos**. Sin embargo, no se pueden borrar productos que ya fueron entregados o que tienen Ordenes de trabajo asignadas.

* Estado: Luego de validada, se puede mantener la Orden de Venta o Cerrarla.

* Crear: Se puede crear lo siguiente desde una Orden de Venta validada:

    * Nota de Entrega - Para registrar un envío. También se puede hacer una Nota de Entrega para productos seleccionados de acuerdo a la fecha de entrega.
    * Orden de Trabajo - Iniciar una Orden de Trabajo con las materias primas. 
    * Factura de Venta - Facturar la Orden
    * Solicitud de Material - Pedir materiales de los cuales ya no haya existencias. 
    * Solicitud de Materias Primas - Pedir las materias primas necesarias para la manufactura.
    * Proyecto - Crear un proyecto basado en la Orden de Venta.
    * Suscripción - Repetir de forma automática una Orden de Venta, es decir, realizar una suscripción. .
    * Solicitud de Pago - Solicitar el Pago de la Orden. 
    * Pago - Registrar el pago de la Orden de Venta. 

Estas acciones también pueden verse en la parte de arriba del Tablero. También se puede realizar un Asiento contable basado en la Orden de Venta desde el tablero. 

<img class="screenshot" alt="Actions from Submitted Sales Order" src="{{docs_base_url}}/assets/img/selling/submit-so.png">

### 3.15 Orden de Venta con Tipo de Orden "Mantenimiento" 
Cuando el "Tipo de Orden" de la Orden de Venta es "Mantenimiento" es necesario seguir estos pasos: 

1. Ingresar Moneda, Lista de Precios y detalles de Productos. 
2. Mencionar impuestos y otra información.
3. Guardar y validar el formulario.
4. Una vez que el formulario fue validado, el botón Crear dará las siguientes opciones que son específicas a la Orden de Venta de tipo mantenimiento:

    i) Visita de Mantenimiento
    ii) Cronograma de Mantenimiento.

  ![Orden de Venta de Tipo Mantenimiento](/docs/assets/img/selling/so-maintenance.png)

> **Nota 1:**
Al clickear en el botón Acción y seleccionar "Visita de Mantenimiento" se puede llenar el formulario de visita de forma directa. Los detalles de la Orden de Venta serán obtenidos directamente.

> **Nota 2:**
Al hacer click en el botón Acción y seleccionar "Cronograma de Mantenimiento" se pueden completar los detalles del cronograma. Los detalles de la Orden de Venta serán obtenidos directamente. 

> **Nota 3:**
Al hacer click en el botón "Factura" se puede realizar una Factura por los servicios. Los detalles de la Orden de Venta serán obtenidos directamente. 

### 4. Temas relacionados
1. [Cotización](/docs/user/manual/es/selling/quotation)
1. [Cerrar Orden de Venta](/docs/user/manual/es/selling/articles/close-sales-order)
1. [Corregir Orden de Venta luego de ser validada](/docs/user/manual/es/selling/articles/amending-sales-order-after-submit)
1. [Lista de Selección de Productos](/docs/user/manual/es/stock/pick-list#21-create-pick-list-from-sales-order)
