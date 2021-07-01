<!-- add-breadcrumbs -->
# Cotización

**Una cotización es un costo estimado de los productos/servicios que se le ofrecen al cliente actual o futuro.** 

Durante una venta, un cliente puede pedir una nota de los productos o servicios que se le están ofreciendo junto con los precios y otras condiciones del acuerdo. A esto puede llamársele "Propuesta", "Presupuesto", "Factura Proforma" o **Cotización**.

Para acceder al listado de Cotización, ir a: 
> Inicio > Comercialización > Ventas > Cotización

Un flujo de ventas promedio tiene el siguiente formato:

<img class="screenshot" alt="Make Quotation from Opportunity" src="{{docs_base_url}}/assets/img/selling/selling-flow-quo.png">

Una cotización incluye detalles como:

  * El destinatario de la cotización
  * Los productos y cantidades ofrecidos
  * Los precios a los cuales se ofrecen dichos productos
  * Los impuestos que pueden aplicarse
  * Otros gastos (como transporte, seguros), si los hubiere 
  * Vigencia del contrato
  * Tiempo de entrega
  * Otras condiciones

> Consejo: Las imagenes generan un impacto positivo en las Cotizaciones. Se recomienda siempre adjuntar imágenes de los productos. 


## 1. Prerrequisitos
Antes de crear y utilizar una Cotización, se recomienda crear lo siguiente: 

* [Cliente](/docs/user/manual/en/CRM/customer)
* [Iniciativa](/docs/user/manual/en/CRM/lead)
* [Producto](/docs/user/manual/en/stock/item)

## 2. Creación de una Cotización
1. Ir al listado de Cotización y hacer click en "Nuevo". 
2. Seleccionar si la cotización es para un Cliente o una Iniciativa en el campo "Cotizar a". 
3. Escribir el nombre del Cliente/Iniciativa.
1. Seleccionar una fecha de vencimiento, después de la cual el monto cotizado será considerado inválido. 
1. El Tipo de orden puede ser Ventas, Mantenimiento, o Carrito de Compras. Este último es sólo para compras online y no está pensado para ser creado de esta forma. 
4. Agregar los productos y sus cantidades en la tabla de productos, sus precios serán obtenidos automáticamente desde el listado de precios. También se pueden seleccionar productos desde una Oportunidad haciendo click en "Obtener productos de > Oportunidad". 
5. Agregar impuestos y otros cargos adicionales si los hubiera. 
6. Guardar.

También se puede crear una Cotización desde una Oportunidad, como se muestra a continuación.

<img class="screenshot" alt="Make Quotation from Opportunity" src="{{docs_base_url}}/assets/img/selling/make-quote-from-opp.png">

## 3. Características

### 3.1 Dirección y contacto
En esta sección hay cuatro campos:

* **Dirección del cliente:** Este es el domicilio de facturación del cliente
* **Dirección de envío:** Domicilio a donde serán enviados los productos
* **Persona de contacto:** Si el cliente es una organización, en este campo se anota la persona a contactar. 
* **Territorio:** Lugar a donde pertenece el cliente. La configuración predeterminada es "Todos los territorios". 

### 3.2 Divisa y listas de precios
Se puede seleccionar la moneda en la cual se arma la cotización u orden de venta. Si se configura una Lista de Precios, los precios de los productos serán obtenidos desde allí. Si se selecciona "Ignorar la Regla de precios" las reglas establecidas en Contabilidad > Reglas de precios, serán ignoradas. 

Para saber más sobre Listas de Precios hacer click [aquí](/docs/user/manual/es/stock/price-lists).

Para saber sobre manejo de transacciones en múltiples monedas hacer click [aquí](/docs/user/manual/en/accounts/articles/managing-transactions-in-multiple-currency).

### 3.3 Tabla de productos
Cada fila de la tabla puede expandirse haciendo click en Edit. 

* Al seleccionar Código de Producto, los siguientes conceptos serán añadidos automáticamente: nombre del producto, descripción, imágenes si las hubiera, cantidad predeterminada como 1 y precio. Se pueden añadir descuentos en la sección de Descuento y Margen. 
* Desde **Descuentos y Márgenes** se pueden añadir márgenes de ganancia u otorgar un descuento. Ambos pueden configurarse como monto fijo o porcentaje. El precio final será mostrado debajo, en la sección Precio. Se puede crear una Plantilla de Impuestos específicamente para un producto. 
* **Detalles del peso del Producto** serán obtenidos si fueron cargados en el producto.
* En **Almacén y referencias**, el almacén será seleccionado desde el producto, este es el almacén donde se encuentran presentes los productos.
* En **Planificación** se puede ver la cantidad proyectada y la cantidad actual de un producto. Para saber más sobre estos campos, hacer click [aquí](/docs/user/manual/es/stock/projected-quantity). Haciendo click en el botón "Balance de inventario", se accede a un doctype donde se puede generar un informe de las existencias del producto. 
* **Carrito de compras**, "Notas adicionales" para transacciones via web. Las observaciones del producto serán obtenidas cuando se agregue a través del carrito de compras.
* **Salto de página** Creará un salto de página arriba del producto al imprimir. 

* En esta tabla se pueden insertar filas abajo y arriba, duplicar, mover, o borrar filas.

* Consejo: La tabla de productos también puede ser descargada en formato CSV y subida a otra transacción.

La cantidad total, el importe y el peso neto de todos los productos se verán al final de la tabla de productos. El importe que se verá aquí no incluirá impuestos. 

### 3.4 Impuestos y cargos
Para sumar impuestos a la Cotización se puede seleccionar una [Plantilla de impuestos (ventas)](/docs/user/manual/es/selling/sales-taxes-and-charges-template) o añadir los impuestos de forma manual en la tabla de Impuestos y cargos sobre ventas.

El total de impuestos y gastos se verá al final de la tabla. Haciendo click en Detalle de Impuestos se pueden ver todos los componentes y montos. 

<img class="screenshot" alt="Taxes in Quotation" src="{{docs_base_url}}/assets/img/selling/quotation-taxes.png">

Para añadir impuestos de forma automática a través de una Categoría de impuestos, visitar [esta página](/docs/user/manual/es/accounts/tax-category).

Después de guardar la Cotización aparece en el desplegable de Acciones el botón **Calcular percepciones**, mediante el cual se pueden agregar automáticamente en esta tabla los impuestos de percepción que correpsondan para el Cliente en particular. Para más información al respecto visitar [Configuración de Percepciones](/docs/user/manual/es/accounts/configuracion-de-percepciones).

#### Regla de Envío
Una Regla de Envío ayuda a determinar el costo de enviar un producto. El costo tenderá a aumentar a medida que la distancia de envío sea mayor. Para saber más, vistar la sección [Regla de Envío](/docs/user/manual/es/selling/shipping-rule).

### 3.5 Descuento adicional y código de cupón
Además de ofrecer descuentos por producto, esta sección permite sumar un descuento al total de la cotización. Este descuento puede ser aplicado al importe total, es decir, con impuestos incluidos, o al importe neto, es decir, sin incluir impuestos y otros gastos. El descuento adicional puede aplicarse como monto o porcentaje. 

Para más detalles, leer [Aplicar descuento].(/docs/user/manual/en/selling/articles/applying-discount)

### 3.6 Términos de pago
A veces el pago no se realiza en una sola cuota. Dependiendo del acuerdo, la mitad puede abonarse antes del envío y la otra mitad al recibir los productos o servicios. En esta sección, se puede añadir una plantilla de Condiciones de Pago o ingresar los mismos de forma manual. 

<img class="screenshot" alt="Payment Terms in Quotation" src="{{docs_base_url}}/assets/img/selling/quotation-payment-terms.png">

Para saber más respecto a Condiciones de Pago, [click aquí](/docs/user/manual/en/accounts/payment-terms).

### 3.7 Términos y Condiciones
En operaciones de Compra/Venta puede haber ciertas bases y condiciones que rigen la forma en que el proveedor vende bienes o servicios al cliente. Se pueden aplicar las Bases y Condiciones a las transacciones y éstas aparecerán en el documento impreso. Para saber más respecto a Bases y Condiciones, [click aquí](/docs/user/manual/en/setting-up/print/terms-and-conditions)

### 3.8 Ajustes de Impresión
#### Membrete
Las cotizaciones u órdenes de venta pueden ser impresas en papel con el membrete de la empresa. Leer más  [aquí](/docs/user/manual/en/setting-up/print/letter-head).

"Agrupar productos" sirve para agrupar productos iguales que hayan sido añadidos más de una vez en la tabla de productos. Esto se puede ver al imprimir. 

#### Imprimir Encabezado
Las Cotizaciones también pueden ser denominadas "Factura Proforma" o "Propuesta".
Esto puede hacerse seleccionando **Encabezado de Impresión**. Para crear nuevos encabezados ir a: Inicio > Configuración > Impresión > Encabezado de Impresión. Leer más [aquí](/docs/user/manual/en/setting-up/print/print-headings).

### 3.9 Más información
* **Campaña:** Puede asociarse una campaña de ventas a la cotización. Un grupo de cotizaciones puede ser parte de una campaña de ventas. 
* **Referencia:** Si la cotización es para un potencial cliente, sus datos pueden obtenerse desde la Fuente de Potenciales Clientes tanto desde una campaña, un proveedor, exhibición, etc. Si se quiere cotizar a un cliente actual, seleccionar Cliente Actual.
* **Cotización de Proveedor:** Una Cotización de Proveedor puede ser asociada a fin de poder compararla con la cotización actual al cliente. Al hacer eso, se puede tener una idea de la ganancia o pérdida de la venta. 

### 4. Validación de la Cotización
Una Cotización es una transacción "validable". Cuando se hace click en Guardar se guarda un borrador, cuando se hace click en Validar se guarda de forma definitiva. Como esta Cotización está pensada para ser enviada a un Cliente o Iniciativa, la misma debe ser cerrada a fin de que no se puedan hacer cambios luego de su envío. 

Al validarla, se puede crear una Orden de Venta o Suscripción desde la Cotización utilizando el botón Crear. En el panel que se encuentra en la parte de arriba, se puede ir a la Orden de Venta asociada a esa Cotización. En caso de que la venta no se concrete, se puede configurar la Cotización como perdida haciendo click en el botón Establecer como perdido.

<img class="screenshot" alt="Submitted Quotation" src="{{docs_base_url}}/assets/img/selling/submitted-quotation.png">

### 5. Temas relacionados
1. [Aplicar descuentos](/docs/user/manual/es/selling/articles/applying-discount)
