<!-- add-breadcrumbs -->
# Lote

**El Lote en ERPNext permite agrupar muchas unidades de un Producto y asignarles un único valor/número/etiqueta llamado Número de Lote.**

Esto se hace de acuerdo al Producto. Si el Producto es en lote, entonces debe mencionarse el Número de Lote en cada transacción de inventario. Los números de Lote pueden configurarse de forma manual o automática. Esta funcionalidad es útil para configurar fechas de vencimiento de muchos Productos o moverlos conjuntamente a diferentes Almacenes.

Para acceder al listado de Número de Lote ir a:
> Inicio > Almacén > Número de Serie y de Lote > Lote


## 1. Prerrequisitos
Antes de crear y utilizar un Lote se recomienda crear lo siguiente:

* [Producto](/docs/user/manual/es/stock/item)
* Habilitar "Posee Número de Lote" en el Producto

    ![Batch No Enabled](/docs/assets/img/stock/batch-no-enabled.png)


## 2. Creación de un nuevo Lote

Para configurar un producto como en lote, debe habilitarse el campo "Posee Número de Lote" en el Producto. Si no se seleccionó "Crear Nuevo Lote Automáticamente" al crear un producto, se deberán crear los Lotes de forma Manual. 

Para crear un nuevo lote ir a:

1. Ir al listado de Lote y hacer click en Nuevo.
1. Configurar la ID del Lote.
1. Seleccionar el Producto.
1. Si se realiza cualquier transacción con el producto, no puede configurarse ni desconfigurarse el número de lote.
1. Guardar.

Cuando se habilitan los Lotes para un Producto, también estará disponible la opción de [Retener muestra](/docs/user/manual/es/stock/retain-sample-stock). 

### 2.1 Creación Automática de Lote
Si se quiere crear un lote automáticamente al crear un Recibo de Compra, se debe habilitar la casilla "Crear nuevo lote automáticamente" en el Producto:

<img class="screenshot" alt="Item Setup for Batches" src="{{docs_base_url}}/assets/img/stock/item_setup_for_batch.png">

## 3. Características
### 3.1 Dividir y Mover Lotes

Al abrir un lote, se verán en la página todas las cantidades que pertenecen a ese lote.

<img class="screenshot" alt="Batch View" src="{{docs_base_url}}/assets/img/stock/batch_view.png">

* Para mover el lote de un Almacén a otro, se puede hacer click en el botón **Mover**.

* También se puede dividir un lote en lotes mas chicos haciendo click en el botón **Dividir**. Esto creará un nuevo Lote en base a este y las cantidades se dividirán entre ambos.

    ![Split Batch](/docs/assets/img/stock/batch_split.png)

* Si se configura la fecha de vencimiento, el Lote se mostrará como "No Vencido" hasta la fecha de vencimiento, luego de la cual se mostrará un cartel de "Vencido". Si no se configura fecha, el Lote mostrará "No Configurada".

### 3.2 Transacciones de Productos en Lote

Se deberá crear un Lote antes de crear un Recibo de Compra.
De esta forma, cada vez que se cree un Recibo de Compra u Orden de Trabajo para un producto en lote, primero se deberá crear su Número de Lote, y luego seleccionarlo en la Orden de Compra o Entrada de Inventario.

En cada transacción de existencias (Recibo de Compra, Nota de Entrega, Factura) con un producto en lote, se deberá ingresar el Número de Lote del Producto. 

> Observación: En transacciones de existencias, los ID de los Lotes serán filtrados en base al Código de Producto, Almacén, Fecha de Vencimiento del Lote (comparada con la fecha de contabilización de la transacción) y Cantidad Actual en Almacén.
Al buscar el ID del Lote sin haber ingresado un valor en el campo Almacén, el filtro de Cantidad Actual no será aplicado. 

### 4. Temas Relacionados
1. [Número de Serie](/docs/user/manual/es/stock/serial-no)
1. [Saldo de apertura de stock para Productos seriados y en lote](/docs/user/manual/es/stock/articles/opening-stock-balance-entry-for-serialized-and-batch-item)
1. [Administrar Inventario en base a Lotes ](/docs/user/manual/es/stock/articles/managing-batch-wise-inventory)
