<!-- add-breadcrumbs -->
# Entrada de apertura de stock para Productos seriados y en lote 

Para aquellos Productos que cuentan con Número de Serie y Número de Lote, la entrada de inventario de apertura debe ser realizada a través de una Entrada de inventario. Hacer click [aquí](/docs/user/manual/es/stock/serial-no) para aprender cómo se administra el inventario seriado en ERPNext.

La entrada de apertura no puede ser actualizada a través de una Conciliación de Inventario en el caso de productos seriados y en lote, ya que en ERPNext el nivel de existencias para un producto seriado se calcula en base a la cuenta de los Números de Serie existentes para ese producto. Por ende, a menos que se creen Números de Serie para el producto seriado, su nivel de existencias no será actualizado. En la Herramienta de Conciliación de Inventario, solo se pueden actualizar las existencias iniciales para un producto, pero no los Números de Serie y de Lote. 

### Saldo de apertura para el producto seriado

A continuación se detallan los pasos para crear una entrada de saldo de apertura de existencias para el producto Seriado y en Lote. 

#### Paso 1: Nuevo Ingreso de Existencias

> Almacén > Transacciones de Inventario > Entrada de inventario > Nuevo

#### Paso 2: Seleccionar el objetivo

El Tipo de entrada de stock debería ser `Recepción de Material`.

#### Paso 3: Actualizar fecha de contabilización

La Fecha de contabilización debería ser la fecha en que se desea actualizar el saldo de apertura para un producto. 

#### Paso 4: Actualizar Almacén de destino

El Almacén de destino sera aquel en que se actualizará el saldo de apertura del producto. 

#### Paso 5: Seleccionar productos

Seleccionar productos para los cuales es actualizado el saldo de apertura. 

#### Paso 6: Actualizar Cantidad Inicial

Para el producto seriado, actualizar cantidad a la cantidad de Números de Serie que haya. 

Para el producto seriado, mencionar Números de Serie equivalentes a su Cantidad. O, si los Números de Serie están configurados para ser creados en base a un Prefijo, no es necesario mencionarlos manualmente. Hacer click [aquí](/docs/user/manual/es/stock/articles/serial-no-naming) para aprender más respecto a nombrar con Números de Serie. 

Para un producto en lote, proveer el ID del Lote en el cual se actualizará el saldo de apertura. Preparar el lote y actualizarlo para el producto en Lote. Para crear nuevo Lote ir a: 

> Almacén > Número de serie y de lote > Lote > Nuevo

Hacer click [aquí](/docs/user/manual/es/stock/articles/managing-batch-wise-inventory) para aprender más respecto a cómo se administra el inventario en base a Lotes en ERPNext.

#### Paso 7: Actualizar la Valoración del Producto

Actualizar la valoración del producto, la cuál será por unidad de producto. Si diferentes unidades del mismo producto tienen distintas valuaciones, las mismas deben ser actualizadas en una fila diferente, con Valuaciones diferentes.

#### Paso 8: Cuenta de Diferencia

Al tratarse de un sistema de inventario perpetuo, se crea una entrada contable por cada transacción de existencias. El sistema contable de doble entrada requiere que el Total de Débitos coincida con el Total de Créditos en una entrada. Al validar la Entrada de inventario, el sistema debita la cuenta Almacén por el valor total de productos. Para balancear esto, se utiliza una cuenta temporal como Cuenta de Diferencia. 

<img alt="Difference Account" class="screenshot" src="{{docs_base_url}}/assets/img/articles/difference-account-1.png">

#### Paso 9: Guardar y Validar la Entrada de inventario

Al Validar una Entrada de inventario, se realizará un registro del inventario de existencias, y el saldo de apertura será actualizado para los productos en la Fecha de contabilización dada.

<!-- markdown -->
