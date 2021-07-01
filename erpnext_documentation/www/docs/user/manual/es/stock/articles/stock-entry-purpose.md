<!-- add-breadcrumbs -->
# Objetivo de la Entrada de Inventario

Una Entrada de Inventario es una transacción de existencias, la cual puede ser utilizada con muchos objetivos. A continuación se detallarán los Objetivos de una Entrada de Inventario.

#### 1. Objetivo: Expedición de Material

La entrada de Expedición de Material se utiliza para enviar producto/os desde un almacén. Al validar la Expedición de Material, las exsitencias de ese producto serán deducidas del Almacén de Origen.

La Expedición de Material generalmente se realiza para productos consumibles de bajo valor como por ejemplo material de oficina, etc. También puede crearse una Expedición de Material para conciliar el inventario de productos seriados y en lote. 

<img alt="Material Issue" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-issue.png">

#### 2. Objetivo: Recepción de Material

La entrada de Recepción de Material se crea para ingresar existencias de producto/s a un almacén. Este tipo de entrada de inventario puede ser creado para actualizar el balance inicial de productos seriados o en lote. También sirve para ingresar productos comprados sin Orden de Compra. 

Con fines de valoración de inventario, la Valoración del Producto se convierte en un campo obligatorio en el registro de Recepción de Material. 

<img alt="Material Receipt" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-receipt.png">

#### 3. Objetivo: Transferencia de Material

El registro de Transferencia de Material se crea para Transferencias de Materiales entre almacenes.

<img alt="Material Transfer" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-transfer.png">

#### 4. Objetivo: Transferencia de Material para Fabricación

En el proceso de fabricación, las materias primas son enviadas desde los almacenes hacia el departamento de producción (generalmente Almacenes de Trabajo en Curso). Esta Transferencia de Material se crea desde una Orden de Trabajo. Los Productos en esta entrada con tomados desde la Lista de Materiales para el Producto, de acuerdo con lo seleccionado en la Orden de Trabajo. 

<img alt="Transfer for Manufacture" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-manufacture-transfer.gif">

#### 5. Objetivo: Manufactura

La Manufactura es creada desde una Orden de Trabajo. En este registro, tanto las materias primas como el producto a producir son tomados desde la Lista de Materiales seleccionada en la Orden de Trabajo. Para las materias primas solo se menciona el Almacén de Origen (por lo general Trabajo en Curso). Para el producto a ser fabricado solo se actualiza el almacén de destino, de acuerdo a lo configurado en la Orden de Trabajo. Al validar, las existencias de materias primas son quitadas del Almacén de Origen, lo cual indica que las mismas fueron consumidas en el proceso de fabricación. El Producto fabricado es añadido al Almacén de Destino, señalando la finalización del ciclo de producción.  

<img alt="Manufacture" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-manufacture.gif">

#### 6. Objetivo: Reempaque

La entrada de Reempaque se crea cuando se compran productos al por mayor y luego se vuelven a embalar en paquetes más pequeños. Ver esta [página](/docs/user/manual/es/stock/articles/repack-entry) para saber más al respecto.

#### 7. Objetivo: Enviar al subcontratista

Una transacción de subcontratación implica una transferencia de materias primas hacia el almacén del subcontratado. Esto requiere crear un almacén para el mismo. Ver esta [página](/docs/user/manual/en/manufacturing/subcontracting) para saber más respecto a Subcontratación.

<img alt="Subcontract" class="screenshot" src="{{docs_base_url}}/assets/img/articles/stock-entry-subcontract.gif">

<!-- markdown -->
