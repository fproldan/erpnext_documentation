<!-- add-breadcrumbs -->
# Regla de Envío

La función Regla de Envío ayuda a definir reglas bajo las cuales aplicar los gastos de envío en las transacciones de venta. 

La gran mayoría de las empresas (principamente minoristas), aplican los gastos de envío de acuerdo al total de la factura. Si el valor de la factura está por encima de cierto monto, entonces el costo de envío aplicado es menor. Si el valor de la factura es menor, entonces los gastos de envío a aplicar son mayores. Se puede configurar la Regla de Envío para cumplir los requerimientos de variación en el valor del envío de acuerdo al Total Neto de la transacción de venta.

Para configurar una Regla de Envío ir a:

`Ventas > Productos y Precios > Regla de Envío`

#### Condiciones de Regla de Envío

<img alt="Shipping Rule Prices" class="screenshot"  src="{{docs_base_url}}/assets/img/articles/shipping-charges-1.png">

De acuerdo a la imagen mostrada más arriba, se puede notar que los gastos de envío se reducen a medida que el valor aumenta. Estos gastos de envío sólo se aplicarán si el total de la transacción está dentro de alguno de los rangos mencionados anteriormente. 

#### Válido para Países

Se pueden configurar los Gastos de Envío para que sean válidos para todos los países o designar uno o más Países específicos. Si se mencionan países específicos, los Gastos de Envío se aplicarán sólo si el país del cliente coincide con uno de los países mencionados en la Regla de Envío. 

<img alt="Shipping Rule " class="screenshot"  src="{{docs_base_url}}/assets/img/articles/shipping-charges-2.gif">

#### Cuenta de Envío

Si los gastos de envío son aplicados de acuerdo a una Regla de Envío, entonces será necesario agregar otros valores como Cuenta de Envío, Centro de Costos así como también añadir una fila en la tabla de Impuestos y cargos de la transacción. Por ende, estos detalles también son monitoreados en la Regla de Envío. 

<img alt="Shipping Account" class="screenshot"  src="{{docs_base_url}}/assets/img/articles/shipping-charges-3.png">

#### Aplicación de la Regla de Envío

A continuación hay un ejemplo de cómo se aplican automáticamente los gastos de envío en la Orden de Venta de acuerdo a una Regla de Envío. 

<img alt="Shipping Rule Application" class="screenshot"  src="{{docs_base_url}}/assets/img/articles/shipping-charges-4.gif">
