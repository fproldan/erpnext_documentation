# Producto

**Un Producto es un bien o servicio ofrecido por una empresa**

El término Producto también se aplica a materias primas o componentes de productos que todavía deben ser manufacturados (antes de poder ser vendidos a los clientes). ERPNext permite administrar todo tipo de productos como materias primas, sub-productos, productos finales, variantes de productos y servicios. 

ERPNext está optimizado para el manejo de ventas y compras a través de productos. Si se ofrecen servicios, se puede crear un Producto por cada servicio que se ofrece. Completar la sección de Producto es muy importante para una implementación exitosa de ERPNext.

Para acceder al listado de Producto ir a:
> Inicio > Almacén > Productos y Precios > Producto

## 1. Prerrequisitos
Antes de crear y utilizar un Producto se recomienda crear lo siguiente: 

* [Grupo de Productos](/docs/user/manual/es/stock/item-group)
* [Almacén](/docs/user/manual/es/stock/warehouse)
* Se requiere una Unidad de Medida

## 2. Creación de un Producto
1. Ir al listado de Producto y hacer click en Nuevo.
2. Ingresar un Código de Producto, el nombre se completará automáticamente con el Código de Producto al hacer click en el campo Nombre de Producto.
3. Seleccionar un Grupo de Productos
4. Ingresar el Stock de apertura y el Precio de venta estándar.
5. Guardar.
  ![Producto Guardado](/docs/assets/img/stock/item-saved.png)

### 2.1 Propiedades del Producto

  * **Nombre del Producto:** Es el nombre real del producto o servicio. 
  
  * **Código del Producto:** El Código de Producto es una forma simple de identificar el Producto. Si hay pocos Productos, se recomienda que el Código de Producto y el Nombre sean el mismo. De esta forma los nuevos usuarios pueden reconocer y actualizar más facilmente los detalles de Productos en todas las transacciones. En caso de haber muchos productos con nombres largos y listas de cientos de productos, es aconsejable codificarlos. Para entender cómo codificar productos ir a [Codificación de Productos](/docs/user/manual/es/stock/articles/item-codification). También se puede generar un Código de Producto en base a una [Secuencia](/docs/user/manual/es/setting-up/settings/naming-series) seleccionando esta opción en [Configuración de inventarios](/docs/user/manual/es/stock/stock-settings#1-item-naming-by).
  
  * **Grupo de Productos:** El Grupo de Productos se utiliza para clasificar un producto de acuerdo a diferentes criterios como productos, materias primas, servicios, subproductos, bienes de consumo o todos los grupos de productos. Crear un Grupo de Productos predeterminado en el listado de Grupo de Productos en Configuración > Grupo de Productos y preseleccionar la opción mientras se completan los detalles del Nuevo Producto en [Grupo de Productos](/docs/user/manual/es/stock/item-group). Los Grupos de Productos pueden ser subproductos, materias primas, etc o también pueden basarse en lo que necesite el negocio. 
  
  * **Unidad de Medida predeterminada:** Esta es la unidad de medida predeterminada que se utilizará para el producto. Puede ser unidades, kilos, metros, etc. Se pueden almacenar todas las Unidades de Medidas que necesite un producto en Configuración > Datos Principales > UOM. Estas pueden ser preseleccionadas al completar el Nuevo Producto utilizando el signo % para que aparezca una ventana emergente con el listado de UOM. Para más detalles, visitar la página [UOM](/docs/user/manual/en/stock/uom).

### 2.2 Opciones al crear un Producto
* **Deshabilitado**: Si se desactiva un Producto, este no podrá ser seleccionado en ninguna transacción.

* **Permitir Producto Alternativo**: A veces, al fabricar un producto final, puede suceder que algunos materiales específicos no estén disponibles. Si se habilita esta opción, se puede crear y seleccionar un producto alternativo del listado de Productos Alternativos. Para saber más, visitar la página [Producto Alternativo](/docs/user/manual/es/manufacturing/item-alternative).

* **Mantener Stock:** Si se mantienen existencias de este Producto en el Inventario, ERPNext realizará una Entrada de Inventario para cada transacción de este producto. Asegurarse de no seleccionar esta opción cuando se crea un Producto sin stock (fabricación contra pedido/contruir) o un servicio.

* **Incluir producto en fabricación**: Esto es para materias primas que serán utilizadas para crear productos finales. Si el Producto es un servicio adicional como "lavado" que será usado en la Lista de Materiales, deshabilitar esta opción. 

* **Tasa de valoración**: Hay dos opciones para valuar las existencias de productos. FIFO (Primero que ingresa - Primero que sale) y Promedio Móvil. Para entender en detalles esta seccion ir a [Valoración, FIFO y Promedio Móvil](/docs/user/manual/es/stock/articles/item-valuation-fifo-and-moving-average).

* **Precio de venta estándar**: Al *crear* un Producto, ingresar un valor en este campo creará automáticamente un [Precio de Producto](/docs/user/manual/es/stock/item-price) en la base de datos. Ingresar un valor luego de que el Producto ha sido guardado no funcionará. En este caso, el Precio de Producto será creado desde cualquier transacción con el producto. Es el valor al cual se venderá el producto. Será obtenido de las Ordenes de Venta y Facturas de Venta. 

* **Es Activo Fijo**: Hacer click en esta casilla de verificación si este producto es un Activo de la empresa. Ver el módulo de [Activos](/docs/user/manual/es/asset) para saber más. 

* **Creación automática de activos en la compra**: Si un Producto es un Activo de la Empresa, tildar esta opción si se desea crear un activo automáticamente al comprar este producto durante el [Ciclo de Compra](/docs/user/manual/es/buying/purchase-order). Para saber más ver la Página de [Activos](/docs/user/manual/es/asset/asset).

* **Porcentajes de Tolerancia**: Estas opciones sólo estarán disponibles luego de guardar el Producto. Son el porcentaje en el cual se permitirá sobre facturar y sobre entregar este Producto. Si no son configurados, se tomarán desde [Configuración de cuentas](/docs/user/manual/es/accounts/accounts-settings) y [Configuración de Inventarios](/docs/user/manual/es/stock/stock-settings#3-limit-percent) respectivamente.

* **Subir una Imagen**: Para subir una imagen como ícono que aparecerá en todas las transacciones, se debe guardar el formulario completado parcialmente. Luego de guardarlo, aparecerá el botón "Cambiar" en el ícono de Imagen. Hacer click allí, luego hacer click en Subir y cargar la imagen.  

## 3. Características

### 3.1 Marca y Descripción

* **Marca**: Si hay más de una marca, guardarlas en Almacén > Configuración > Marca y preseleccionarlas cuando se crea un Nuevo Producto.
* **Descripción**: Descripción del Producto. De forma predeterminada se tomará el Código de Producto.
  ![Marca y Descripción del Producto](/docs/assets/img/stock/item-brand-description.png)

### 3.2 Código de Barras

Pueden guardarse códigos de barra en los Productos para escanearlos y agregarlos con facilidad a las transacciones. En la tabla de Códigos de Barra se puede agregar el [código de barra escaneable](/docs/user/manual/es/stock/articles/track-items-using-barcode) de un producto. En ERPNext hay dos tipos de Código de Barra:

* **EAN**: El Número de Artículo Europeo, compuesto por 13 dígitos. El EAN es de uso internacional y es reconocido por la mayoría de los Sistemas TPV.
* **UPC**: El Código Universal de Producto es un número compuesto por 12 dígitos. El UPC generalmente se usa solo en Estados Unidos y Canadá. 

### 3.3 Inventario

* **Vida útil en Días**: Esto es para un producto de [Lote](/docs/user/manual/es/stock/batch). El número de días luego de los cuales el lote de productos será inutilizable. Por ejemplo, medicamentos. 
* **Final de vida útil**: Para un solo Producto, la fecha luego de la cual será completamente inutilizable. Es decir, no podrá usarse en transacciones y manufacturas. Por ejemplo, se utilizarán cristales de plástico para fabricar productos durante 5 años, luego de los cuales se querrá utilizar gotas de plástico. 
* **Período de garantía (en días)**: Para poder rastrear un período de garantía es necesario que el producto sea seriado. Cuando el Producto es entregado, la fecha de entrega y la de período de vencimiento se guarda en la sección de Número de Serie. A través de esa sección se puede rastrear el estado de la garantía. 

  El período de garantía es un período de tiempo en el cual el producto comprado puede ser devuelto o cambiado. 

  <img class="screenshot" alt="Item Warranty" src="{{docs_base_url}}/assets/img/stock/item-inventory.png">

* **Unidad de Medida (UOM)**: La Unidad de Medida para el Producto. Puede ser unidades, Kilos, etc. La UOM que se usa internamente puede diferir de la UOM de compra. 
* **Peso por Unidad**: El peso real de cada unidad del producto. Ejemplo: 1 kilo de galletas o 10 galletas por paquete. 
* **Tipo de Solicitud de Material predeterminado**: Cuando se cree una nueva Solicitud de Material, el campo establecido aquí será seleccionado de forma predeterminada.
* **Método de Valoración**: Seleccionar el Método de Valoración ya sea FIFO o Promedio Móvil. Para saber más sobre Métodos de Valoración hacer click [aquí](/docs/user/manual/es/stock/articles/item-valuation-fifo-and-moving-average).

### 3.4 Ordenar Automáticamente

Cuando las existencias de un producto caen por debajo de una cierta cantidad se puede configurar un pedido automático en la sección "Ordenar Automáticamente". Esto debe ser habilitado en la [Configuración de Inventarios](/docs/user/manual/es/stock/stock-settings#9-automatic-material-request). Esta función creará una [Solicitud de Materiales](/docs/user/manual/es/stock/material-request) para el producto. El usuario que posea el rol de Gerente de Compras y Gerente de Almacén será **notificado** cuando se cree la Solicitud de Material. 

* **Registro (grupo)**: En qué grupo de almacenes se revisará la cantidad del producto. 
* **Solicitud para**: Para que almacén se hace la solicitud de producto. 
* **Nivel mínimo de stock**: Cuando el producto llega a esta cantidad, se genera la solicitud. El nivel de pedido puede ser determinado en base al tiempo de espera y el promedio de consumo diario. Por ejemplo, se puede establecer el nivel de pedido de una placa madre en 10. Cuando haya solo 10 placas madres en existencia, el sistema creará una Solicitud de Material automáticamente en la cuenta de ERPNext. 
* **Cantidad mínima para ordenar**: El número de unidades a pedir de forma tal que la suma del costo de pedido y los costos de mantenimiento estén en su mínimo. La cantidad a pedir está basada en la "Cantidad mínima de la orden" especificada por el proveedor y otros factores.

  Por ejemplo, si el nivel de pedido es de 100 productos, la cantidad a pedir no necesariamente tiene que ser 100 productos. La cantidad a pedir puede ser mayor o igual al nivel de pedido. Puede depender del tiempo de espera, descuento, transporte y promedio de consumo diario. 

* **Tipo de Solicitud de Material**: El tipo de [Solicitud de Material](/docs/user/manual/es/stock/material-request) con el cual se pedirán los productos. Esto depende de si se compra el Producto, se lo fabrica o se lo transfiere entre Almacenes. 

  <img alt="Item Reorder" class="screenshot" src="{{docs_base_url}}/assets/img/stock/item-reorder.png">

> **Observación**: la Solicitud de Material se creará a las 12 de la noche dependiendo del nivel de pedido establecido. 

### 3.5 Múltiples Unidades de Medida

Se puede contar con distintas Unidades de Medidas para un mismo Producto. Si la UOM de venta predeterminada es unidades pero se recibe la mercadería en kilos, se pueden establecer UOM adicionales con su respectivo factor de conversión. Por ejemplo, 500 unidades de destornilladores = 1 kilo; entonces es necesario seleccionar kilo/litro como UOM y configurar el factor de conversión como 500. Para saber más respecto a vender en diferentes UOM, visitar [esta página](/docs/user/manual/es/selling/articles/Selling-in-different-UOM).

### 3.6 Número de serie y lote

Utilizando Números de Serie se pueden rastrear las garantías y las devoluciones. En caso de que un proveedor retire un Producto individual, el sistema de números ayuda a rastrear ese Producto individual. El sistema numérico también administra las fechas de vencimiento.

Tener en cuenta que si se vende productos de a miles, y si los mismos son muy pequeños, como lapiceras o gomas de borrar, no es necesario seriarlos. 

En ERPNext, se deberá mencionar los Números de Serie en algunas entradas contables. Si el producto no es un bien de consumo durable, si no tiene garantía ni posibilidades de ser devuelto, es bueno evitar asignar números de serie. 

<img alt="Serial No modal" class="screenshot" src="{{docs_base_url}}/assets/img/stock/serial_no_modal.gif">

Por otro lado, un grupo de productos puede ser fabricado en lotes. Esto es útil para movilizar el lote y asociar una fecha de vencimiento a cierto lote. 

* **Posee número de lote**: Si se tilda esta opción se mostrarán opciones como número de lote, fecha de vencimiento, y conservar muestra de existencias. No se puede activar esta opción si hay alguna transacción preexistente para este Producto. Si esta opción esta desactivada, se deberá ingresar manualmente los números de serie para cada transacción. 

    * **Serie de número de lote**: Prefijo que será aplicado a los números de lote. Si se configura 5x1SCR, entonces el primer lote será nombrado como 5x1SCR00001 en la primera transacción/fabricación.

    * **Crear nuevo lote automáticamente**: Si el número de lote no se menciona en las transacciones, entonces será creado automáticamente siguiendo un formato como este AAAA.00001. Si se prefiere crear los números de lote de un producto de forma manual, entonces dejar este campo en blanco. Esta configuración sobreescribe lo establecido en la Configuración de Inventarios bajo el campo "Prefijo de la Serie de Nomenclatura". Los números de lote pueden configurarse para ser generados automáticamente si se fabrican los productos o para ingresarlos manualmente si los mismos provienen de un fabricante externo. 

    * **Tiene fecha de caducidad**: Si se tilda esta opción, el número de lote será creado de acuerdo a la fecha de caducidad. Las mismas pueden ser configuradas en el Lote. 

    * **Conservar muestra**: A fin de conservar un mínimo número de existencias de un producto en forma de muestra. Para hacer esto se debe configurar un Almacén de Retención de Muestras en la Configuración de Inventarios. Para saber más, hacer click [aquí](/docs/user/manual/es/stock/retain-sample-stock).

* **Posee número de serie**: Esto es similar al número de lote, será creado cuando se realicen transacciones o manufacturas. Si se configuran los números de serie como AA, entonces un número como AA00001 será creado en la primera transacción.

> Consejo: Al ingresar el Código de Producto en la tabla de Productos, si la tabla requiere detalles de inventario, entonces dependiendo de si el producto es seriado o posee lote, se puede ingresar el número de lote o serie de forma inmediata cuando aparezca la ventana emergente.

<img alt="Batch No modal" class="screenshot" src="{{docs_base_url}}/assets/img/stock/batch_no_modal.png">

> **Observación**: Una vez que se marca un producto como seriado, en lotes o ninguno de los dos, no se puede cambiar esto luego de haber realizado una Entrada de Inventarios. 

Para saber más visitar la página [Conciliación de Inventario](/docs/user/manual/es/stock/stock-reconciliation).

### 3.7 Variantes
Una Variante de Producto es una versión diferente del Producto. Para saber más respecto a la adminsitración de variantes ver [Variantes de Producto](/docs/user/manual/es/stock/item-variants).

### 3.8 Valores Predeterminados de Ventas, Compras y Contabilidad

En esta sección se pueden definir configuraciones predeterminadas relacionadas a un producto para todas sus transacciones en toda la empresa. 

* **Almacén predeterminado:** Este es el Almacén que será seleccionado automáticamente en las transacciones para este Producto. 
* **Lista de precios predeterminada:** Tanto de venta como de compra. De la misma forma, se pueden configurar las cuentas predeterminadas de compra y venta. 
* **Proveedor predeterminado**: Si se configura un proveedor predeterminado, el mismo será seleccionado para nuevas transacciones de compra. 
* **Cuenta de gastos predeterminada:** Es la cuenta de la cual será debitado el costo del Producto. 
* **Cuenta de ingresos predeterminada:** Es la cuenta en la cual se acreditará el ingreso generado por vender el Producto. 
* **Centros de costos predeterminados:** Es utilizado para rastrear los gastos para este Producto.

  ![Item defaults](/docs/assets/img/stock/item-defaults.png)

> Consejo: Se pueden añadir más filas para múltiples empresas.

### 3.9 Detalles de compra y reabastecimiento 

* **Es un producto para compra:** Si esta opción no está tildada, no se podrá usar este producto en operaciones de compra.
* **Unidad de Medida de Compra Predeterminada**: La UOM predeterminada que será usada en las transacciones de compra. 
* **Cantidad mínima de la orden**: La cantidad mínima requerida para transacciones de compra como Ordenes de Compra. Si esto se configura, el sistema no permitirá avanzar en la operación de compra si la cantidad de producto pedida es menor que la establecida en este campo. 
* **Stock de seguridad**: El “Stock de seguridad” es utilizado en el informe "Nivel recomendado de reabastecimiento de producto". De acuerdo con el Stock de seguridad, el consumo diario promedio y el tiempo de espera, el sistema sugiere el Nivel de Pedido de un producto.

  Nivel de Pedido = Stock de seguridad + (Consumo Diario Promedio * Tiempo de Espera)
* **Precio de la última compra**: Aquí se mostrará el precio al cual se compró por última vez un producto utilizando una [Factura de Venta](/docs/user/manual/en/accounts/purchase-invoice).
* **Es producto proveído por cliente:** tildar esta opción si el producto es provisto por un cliente y recibido a través de **Entrada de Inventario: Recepción de Materiales**. Si está tildada, el campo de **Cliente** es obligatorio como el Cliente predeterminado para **Solicitud de Materiales**. Para saber más, visitar [esta página](/docs/user/manual/es/manufacturing/articles/customer-provided-items).
* **Plazo de entrega en días:** El tiempo de espera en días es el número de días que transcurren entre el pedido del producto y su llegada al Almacén.

  <img class="screenshot" alt="Purchase details" src="{{docs_base_url}}/assets/img/stock/item-purchase-details.png">

### 3.10 Detalles del Proveedor

* **Entregado por el Proveedor (Envío Triangulado)**: Si el producto será enviado directamente desde el proveedor al cliente tildar esta opción. Leer más al respecto [aquí](/docs/user/manual/es/selling/articles/drop-shipping).
* **Código de Proveedores:** Código de Rastreo del Producto definido por el Proveedor. En las transacciones de Compra al selecccionar un Producto, también se obtendrá el Número de pieza del proveedor, para referencia del mismo. Para leer más sobre esto click [aquí](/docs/user/manual/es/buying/articles/maintaining-suppliers-part-no-in-item).

  ![Detalles del Proveedor del Producto](/docs/assets/img/stock/item-supplier.png)

### 3.11 Detalles de Comercio Exterior
Si se está obteniendo el producto de otro país, se pueden incluir los detalles en esta sección. 

* **País de Origen**: El país desde donde se obtiene el producto. 
* **Número de arancel aduanero**: Se puede crear un número de arancel aduanero con una descripción para utilizarlo como referencia y para compartir con organizaciones aduaneras. Más adelante puede ser usado en las Notas de Entrega.  

### 3.12 Detalles de Venta

* **Unidad de Medida de Ventas Predeterminada**: La UOM predeterminada que será utilizada en las transacciones de venta.
* **Descuento máximo (%)**: Se puede definir el % máximo de descuento que puede aplicarse a un producto. Por ejemplo: si se configura un 20%, no puede venderse el mencionado producto con un descuento mayor al 20%.
* **Es un producto para venta**: Si esta opción no está tildada, no se podrá utilizar el producto en operaciones de venta. 

  ![Item Sales Details](/docs/assets/img/stock/item-sales.png)

### 3.13 Ingresos y Gastos Diferidos
Se puede permitir un ingreso o gasto diferido para el producto. Una vez que tilda esta opción, se verán las opciones para configurar la Cuenta de Gastos Diferidos y el número de meses a través de los cuales el ingreso/gasto es distribuido. 

Por ejemplo, considérese una membresía anual de un gimnasio, se paga por adelantado pero el servicio se otorga durante todo el año. Para el dueño del gimnasio es un ingreso diferido y para el cliente, un gasto diferido. 

  ![Deferred Revenue](/docs/assets/img/stock/deferred-revenue.png)

Ver las páginas respecto a [Ingreso Diferido](/docs/user/manual/es/accounts/deferred-revenue) para más detalles.

### 3.14 Detalles del Cliente

El Cliente puede identificar un Producto con un Código de Producto diferente. Esto es similar al [Código de Proveedor](/docs/user/manual/es/stock/item#311-supplier-details). 

* **Nombre del Cliente**: Seleccionar el cliente.
* **Categoría de Cliente**: Este campo será tomado de acuerdo al Cliente seleccionado en el campo anterior. 
* **Código de Referencia:** Un cliente puede identificar este producto con un número distinto. Se puede rastrear el Código de Producto asignado por el Cliente a este producto. Cuando se crea una Orden de Venta, se mostrará el Código de Referencia del Cliente para este Producto. 

### 3.15 Impuestos del Producto

Esta configuración solo es necesaria si un Producto en particular tiene una tasa de impuesto diferente a la definida en la cuenta estándar de impuestos. 

Se deberá crear una nueva "Plantilla de Impuesto de Producto" o elegir una existente. Por ejemplo, si se tiene una Cuenta de impuesto, "IVA 14%" y este Producto en particular está eximido de ese impuesto, entonces se selecciona "IVA 14%" en la primera columna y se configura "0" como tasa impositiva en la segunda columna. Para más detalles, visitar la página de [Plantilla de Impuesto de Producto](/docs/user/manual/es/accounts/item-tax-template). 

![Plantilla de Impuesto de Producto](/docs/assets/img/stock/item-tax-template.png)

También se puede configurar una [Categoría de impuesto](/docs/user/manual/es/accounts/tax-category) para este producto.


### 3.16 Criterios de Inspección

* **Plantilla de Inspección de Calidad**: Si se prepara una Inspección de Calidad para el Producto, se actualizará automáticamente esta plantilla de criterios en la tabla correspondiente. Ejemplos de estos criterios son: Peso, Largo, Terminación, etc.
La Inspección de Calidad puede hacerse con Vista Rápida y no es necesario ir a una página diferente para actualizar los detalles de la inspección en ERPNext.
* **Inspección requerida antes de la compra**: Si es obligatoria la realización de una inspección antes de que el producto sea comprado, es decir, antes de generar el Recibo de Compra, tildar esta opción. 
* **Inspección requerida antes de la entrega**: Si en el momento de la entrega del producto por parte del Proveedor, es decir, antes de crear la Nota de Entrega, es obligatorio realizar una inspección, tildar esta casilla.  

Para saber más respecto a Inspección de Calidad, hacer click [aquí](/docs/user/manual/es/stock/quality-inspection).

### 3.17 Manufactura

* **Lista de Materiales Predeterminada**: La [Lista de Materiales](/docs/user/manual/es/manufacturing/bill-of-materials) predeterminada que se utiliza para fabricar este Producto.
* **Suministro de materia prima para la compra**: Si se está tercerizando a un vendedor, se puede elegir proveerlos con las materias primas para fabricar el producto utilizando la Lista de Materiales predeterminada. 
* **Fabricante de producto predeterminado:** Seleccionar el Fabricante de este producto. 
* **Número de pieza del fabricante predeterminado:** Ingresar el número de pieza que el fabricante le asignó a este producto. 

  ![Item Manufacturing](/docs/assets/img/stock/item-manufacturing.png)

* Los detalles del fabricante solo aparecerán luego de haber creado un "Fabricante de Producto" desde el panel y seleccionado ese registro como predeterminado. Añadir aquí detalles para:
  * Código de Producto
  * Ingresar el nombre del Fabricante
  * Ingresar el Número de Pieza que el Fabricante utiliza para identificar este producto
  * Seleccionar "Es Predeterminado" para mostrar el fabricante y número de pieza en el registro del Producto. 

  ![Item Manufacturer](/docs/assets/img/stock/item-manufacturer.png)

### 3.18 Sitio Web

* **Mostrar en sitio web**: Seleccionar si se quiere mostrar este Producto en el Sitio Web. Una vez que se selecciona esta opción, aparecerán opciones adicionales para configurar el producto en el sitio web. Para ver el producto en el sitio web hacer click en el link "Ver en Sitio Web" arriba a la izquierda justo por encima de la imagen del producto. Visitar el [Módulo de Sitio Web](/docs/user/manual/es/website) para saber más.

  <img class="screenshot" alt="Manufaturing details" src="{{docs_base_url}}/assets/img/stock/item-manufacturing-website.png">

* **Peso**: Los Productos de mayor peso serán mostrados primeros en el sitio web. El límite para el número que se puede ingresar aquí es muy alto.
* **Presentación**: Una presentación de diapositivas puede mostrarse en la parte superior de la página. Visitar [Página de Inicio](/docs/user/manual/es/website/homepage) en el Módulo de Sitio Web para saber más. 
* **Imagen del sitio web**: Se puede adjuntar una imagen en vez de una presentación de diapositivas.
* **Almacén para el Sitio Web**: Seleccionar un Almacén existente o crear uno nuevo para transacciones en el Sitio Web. Este Almacén será diferente de los Almacenes fuera de línea. Las existencias para cualquier transacción en línea serán deducidas de los Almacenes configurados como Almacén de Sitio Web. 
* **Grupos de productos en el sitio web**: En esta tabla se pueden seleccionar [Grupos de Productos](/docs/user/manual/es/stock/item-group) existentes o crear nuevos para clasificar productos en el sitio web.
* **Establecer meta-etiquetas**: Las meta-etiquetas ayudan con las estrategias de SEO. Ver [Página Web](/docs/user/manual/en/website/web-page) para saber cómo utilizarlas.

Visitar [Sitio Web](/docs/user/manual/en/website) para entender estos temas en detalle. 

### 3.19 Especificaciones del Sito Web
Esta sección es para configurar otros detalles del Producto

* **Copiar desde Grupo:** Los detalles de "Especificaciones del Sitio Web" serán obtenidos de la configuración de un Grupo de Productos específico configurado en la sección anterior (2.17).
* **Especificaciones del sitio web**: La etiqueta y su descripción para el producto. Por ejemplo: "Garantía: 1 año".
* **Descripción del Sitio Web**: Esto aparecerá en la página del producto.
* **Contenido del sitio Web**: Se pueden crear diseños adicionales, etc. Utilizar Bootstrap 4 para mostrar en la página del producto. 

### 3.20 Detalles de publicación del Hub

Hub es un mercado gratuito en línea donde los Clientes y Proveedores pueden realizar transacciones. Si ambas partes están en ERPNext, las transacciones se dan de forma fluida. Por ejemplo, al crear una Orden de Compra, una Orden de Venta será creada para el Proveedor. Se puede visitar hub en: https://hubmarket.org.

* **Publicar en el Hub**: Elegir si se desea publicar el producto en Hub. 
* **Almacén del Hub**: Este es un Almacén separado donde guardar las existencias para las transacciones realizadas en hub.
* **Sincronizado con Hub**: Sincronizar el producto y otros detalles con hub cuando se realizan transacciones.


### 4. Temas relacionados
1. [Precio de Producto](/docs/user/manual/es/stock/item-price)
2. [Codificación de Producto](/docs/user/manual/es/stock/articles/item-codification)
3. [Variantes de Producto](/docs/user/manual/es/stock/item-variants)
4. [Grupo de Productos](/docs/user/manual/es/stock/item-group)
5. [Atributos de Producto](/docs/user/manual/es/stock/item-attribute)
6. [Valoración, FIFO y Promedio Móvil](/docs/user/manual/es/stock/articles/item-valuation-fifo-and-moving-average)
7. [Tasa de Valoración de Productos en Transacciones](/docs/user/manual/es/stock/articles/item-valuation-transactions)
8. [Campo "Mantener Stock" bloqueado en el Producto](/docs/user/manual/es/stock/articles/maintain-stock-field-frozen-in-item-master)
9. [Administrar Productos Finales Rechazados](/docs/user/manual/es/stock/articles/managing-rejected-finished-goods-items)
10. [Devolver Productos Rechazados](/docs/user/manual/es/stock/articles/return-rejected-item)
11. [Rastrear Productos utilizando Código de Barras](/docs/user/manual/es/stock/articles/track-items-using-barcode)
12. [Crear Amortización para Producto](/docs/user/manual/es/stock/articles/creating-depreciation-for-item)
13. [Nombrar usando Número de Serie](/docs/user/manual/es/stock/articles/serial-no-naming)
14. [Saldo de apertura de stock para Productos seriados y en lote](/docs/user/manual/es/stock/articles/opening-stock-balance-entry-for-serialized-and-batch-item)
15. [Número de Serie](/docs/user/manual/es/stock/serial-no)
16. [Nombrar usando Número de serie](/docs/user/manual/es/stock/articles/serial-no-naming)
