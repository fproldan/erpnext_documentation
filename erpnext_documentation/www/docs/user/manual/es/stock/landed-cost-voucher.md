<!-- add-breadcrumbs -->
# Comprobante de Costo de Destino

**Costo en Destino es el costo final total que requiere un producto para llegar hasta la puerta del comprador.**

El Costo en Destino incluye los costos originales del producto, todos los gastos de envío, derechos de aduana, impuestos, seguros, costos de conversión de monedas, etc. Puede que todos estos componentes no se apliquen en cada envío, pero los costos relevantes deben ser considerados como parte del costo en destino.

> Para entender mejor el costo en destino, considérese el siguiente ejemplo. Se necesita un lavarropa para la casa. Antes de comprar, se realizan averiguaciones para encontrar el mejor precio. En este proceso, se puede encontrar un mejor precio en un negocio que se encuentra lejos de casa. Sin embargo, si se va a comprar en ese negocio, también se debe considerar el costo de envío. El costo total, con envío incluído, puede ser mayor al que se consigue en un negocio más cercano. En ese caso, se eligirá comprar en el negocio más cercano, ya que el costo en destino del producto será más barato. 

De forma similar, al hacer negocios, es crucial identificar el costo en destino para un Producto, debido a que ayuda a decidir el costo de venta de ese producto e impacta en las ganancias de la empresa. Por ende, todos los gastos de costo en destino deberían ser incluidos en la tarifa de valoración del Producto.

De acuerdo con un estudio realizado por [Third-Party Logistics](http://www.3plstudy.com/), solo un 45% de los encuestados utilizan el Costo en Destino minuciosamente. Los principales motivos para no utilizar el Costo en Destino son: falta de información necesaria (49%), falta de herramientas adecuadas (48%), tiempo insuficiente (31%), y desconocimiento respecto a cómo aplicar costo en destino (27%).

Para acceder al listado de Comprobante de Costo en Destino ir a:
> Inicio > Almacén > Herramientas > Comprobante de Costo en Destino

## 1. Prerrequisitos
Antes de crear y utilizar un Comprobante de Costo en Destino se recomienda crear lo siguiente: 

* [Recibo de Compra](/docs/user/manual/es/stock/purchase-receipt)

    O

* [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice)


## 2. Creación de un Comprobante de Costo en Destino

1. Ir al listado de Comprobante de Costo en Destino y hacer click en Nuevo.
1. Seleccionar el tipo de Documento Comprobante, sea Factura de Compra o Recibo. Se pueden seleccionar muchos documentos. 
1. Seleccionar la Factura o Recibo específico. El nombre del proveedor y el Total se obtendrán automáticamente. 
1. Hacer click en el botón Obtener productos para traer los detalles de producto desde la Factura o Recibo de Compra. 
1. Seleccionar si la Distribución de cargos se hará de acuerdo con cantidad, importe o si se hará manualmente. 
1. Ingresar la Cuenta de Gastos y el Importe para los Cargos Aplicables en la tabla de Impuestos y cargos. El monto se distribuirá de forma equitativa de acuerdo con la cantidad o importe, según lo que se seleccionó anteriormente.  
1. Guardar y Validar.

    <img class="screenshot" alt="Landed Cost Voucher" src="{{docs_base_url}}/assets/img/stock/landed-cost-voucher.png">


En el documento se pueden seleccionar muchas Facturas/Recibos de compra y obtener todos los productos desde esos Recibos de Compra. Luego se deben ingresar los gastos aplicables, en la tabla de "Impuestos y cargos". Se puede borrar fácilmente un producto, si los gastos adicionales no se aplican al mismo. 

Los gastos sumados son distribuidos de forma proporcional entre todos los productos, de acuerdo con el monto o cantidad. Si se seleccionó en base al monto, el Producto con el mayor valor recibirá una mayor proporción de los gastos. En el caso de cantidad, el Producto con mayor cantidad recibirá la mayoría de los gastos, y los otros Productos recibirán montos menores. Esto se muestra en la siguiente captura de pantalla. 

<img class="screenshot" alt="Landed Cost Voucher" src="{{docs_base_url}}/assets/img/stock/landed-cost-distribution.png">

## 3. Acciones Relacionadas
### 3.1 Añadir Costo en Destino al Recibo de Compra

En ERPNext, al crear el Recibo de Compra, se pueden sumar gastos relacionados al costo en destino en la tabla de "Impuestos y cargos". Esos gastos deberían ser ingresados como "Valuación y Total" o "Valuación" en el campo "Considerar impuestos o cargos por". Aquellos gastos que son pagaderos al mismo Proveedor del cual se obtienen los productos deberían ser catalogados como "Valuación y Total". En cambio, si los gastos son a pagar a un tercero, deberían ser catalogados como "Valuación". Al validar el Recibo de Compra, el sistema calculará el costo en destino de todos los productos, teniendo en cuenta esos gastos. El costo en destino será considerado al calcular la Tarifa de Valoración del producto (de acuerdo con los métodos FIFO o Promedio Móvil). 

Pero, en realidad, al crear un Recibo de Compra puede que no conozcamos todos los gastos que se aplicarán para el costo en destino. El transportista puede enviar su factura luego de 1 mes, pero no tiene sentido esperar tanto para generar el Recibo de Compra. Las empresas que importan productos o partes, pagan grandes montos en Derechos Aduaneros. Y, generalmente, la factura del Departamento de Aduana llega despúes de un tiempo. Es en estos casos en que el Comprobante de Costo en Destino es de gran utilidad, ya que permite añadir esos gastos adicionales en una fecha posterior y actualizar el costo en destino de los productos comprados. 

### 3.2 Luego de validar

1. Se recalcula la Tarifa de Valoración de los productos de acuerdo con el nuevo costo en destino. 

3. Si se utiliza "Inventario Perpetuo", el sistema realizará registros contables generales para corregir el balance de Existencias Disponibles. Debitará (aumentará) la "cuenta depósito" correspondiente y acreeditará (disminuirá) la **Cuenta de Gastos** mencionada en la tabla de Impuestos y cargos. Si los productos ya fueron enviados, el Costo de Productos Vendidos ya ha sido registrado de acuerdo con la tarifa de valoración anterior. Es decir, que se volverán a publicar los registros contables generales para todos los registros futuros de productos asociados, para corregir ese valor.

### 4. Temas Relacionados
1. [Hoja de ruta](/docs/user/manual/es/stock/delivery-trip)
1. [Recibo de Compra](/docs/user/manual/es/stock/purchase-receipt)
