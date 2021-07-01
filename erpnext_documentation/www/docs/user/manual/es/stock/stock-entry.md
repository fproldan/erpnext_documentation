<!-- add-breadcrumbs -->
# Entradas de Inventario

**Una Entrada de Inventario permite registrar movimientos de Productos entre Almacenes.**

Para acceder al listado de Entradas de Inventario ir a:
> Inicio > Almacén > Transacciones de Inventario > Entrada de Inventario

Pueden realizarse Entradas de Inventario con los siguientes objetivos: 

* **Expedición de Material**: Si el material es enviado a alguien dentro o fuera de la empresa (Material Saliente). Los Productos serán quitados del Almacén configurado como Almacén de Origen.
* **Recepción de Material**: Si el material es recibido (Material Ingresante). Los Productos serán sumados al Almacén configurado como Almacén de Destino. 
* **Transferencia de Material**: Si el material es trasladado de un Almacén de la empresa a otro.
* **Transferencia de Material para Fabricación**: Si se transfieren materias primas para fabricación. La transferencia puede generarse desde una [Orden de Trabajo](/docs/user/manual/en/manufacturing/work-order) o una [Tarjeta de Empleo](/docs/user/manual/en/manufacturing/job-card). Para saber más, visitar la página [Lista de Materiales](/docs/user/manual/en/manufacturing/bill-of-materials).
* **Consumo de Material para Fabricación**: Puede haber muchos registros de consumo de existencias generadas desde una Orden de Trabajo para fabricación. Para más detalles, hacer click [aquí](/docs/user/manual/en/manufacturing/articles/material_consumption).
* **Manufactura**: Si el Material se recibe desde una Operación de Fabricación/Producción. 
* **Reempaque**: Si el producto/s original/es se vuelve/n a empacar generando producto/s nuevo/s. 
* **Enviar al subcontratista**: Si el Material es enviado para una actividad de subcontratación. Este registro se realiza desde una Orden de Compra. Para saber más visitar la página [subcontratación](/docs/user/manual/en/manufacturing/subcontracting).
* **Almacén de Envío**: Este documento se selecciona en la Entrada de Inventario con tipo "Almacén de Recepción", a fin de confirmar cuántos productos fueron recibidos, en caso de que el Material se envíe a un Almacén y necesite confirmación en la recepción. El estado será "Bienes en Tránsito" hasta que los mismos sean recibidos, luego de lo cual el estado cambiará a "Bienes Transferidos". 
* **Almacén de Recepción**: Si el Material se recibe en un Almacén, se seleccionará la Entrada de Inventario con tipo "Almacén de Envío" y allí se actualizará el número de bienes recibidos. 

Para conocer más en detalle los tipos de registros de inventario, [visitar esta página](/docs/user/manual/es/stock/articles/stock-entry-purpose).

## 1. Prerrequisitos
Antes de crear y utilizar una Entrada de Inventario se recomienda crear lo siguiente: 

* [Almacén](/docs/user/manual/es/stock/warehouse)
* [Producto](/docs/user/manual/es/stock/item)

## 2.Creación de una Entrada de Inventario
Las Entradas de Inventario con objetivos de Fabricación por lo general se crean desde una [Orden de Trabajo](/docs/user/manual/en/manufacturing/work-order). Para crear una Entrada de Inventario con otros objetivos de forma manual, seguir los siguientes pasos:

1. Ir al listado de Entrada de Inventario y hacer click en Nuevo.
1. Seleccionar el objetivo de la Entrada de Inventario de entre los citados anteriormente.
1. Si se configuran los Almacén de Origen o Destino Predeterminados, los mismos serán completados automáticamente en las filas de la tabla de Productos. 
1. Los Almacenes de Origen/Destino estarán disponibles de acuerdo al objetivo seleccionado para la Entrada de Inventario. 
1. Seleccionar los Productos e ingresar la Cantidad
1. Se tomará el precio básico y se calculará el Importe de forma automática.
1. Guardar y Validar.

    <img class="screenshot" alt="Stock Entry" src="{{docs_base_url}}/assets/img/stock/stock-entry.png">

Por lo general, "Almacén de Origen" y "Almacén de Destino", son configurados para registrar un movimiento.

### 2.1 Opciones Adicionales al crear una Entrada de Inventario

* **Orden de Trabajo**: Si se trata de un registro de Fabricación, se mostrará la Orden de Trabajo en este campo. 
* **Editar Fecha y Hora de Contabilización**: Permitirá editar la fecha y hora de contabilización de la Entrada de Inventario 
* **Inspección Requerida**: Si se requiere una [Inspección de Calidad](/docs/user/manual/es/stock/quality-inspection) para los Productos antes de validar la Entrada de Inventario. 
* **Desde Lista de Materiales**: Si se trata de un registro de Fabricación, se mostrará la Lista de Materiales asociada al Producto que está siendo fabricado. 

### 2.2 Tipo de Entrada de Inventario
También se puede crear un Tipo de Entrada de Inventario donde solo el nombre será diferente, por ejemplo, "Registro de Chatarra". El objetivo será Transferencia de Material pero el nombre será distinto. Esto resulta útil si se desea que ciertos usuarios solo tengan acceso a acciones específicas relacionadas con el inventario. 

![Stock Entry Type](/docs/assets/img/stock/stock-entry-type.png)

## 3. Características

### 3.1 Tabla de Productos
Aquí se mostrarán detalles sobre el Producto, Precio, Cantidad, etc. 

El seleccionar la casilla "Permitir tasa de valoración cero" permitirá validar la Entrada de inventario inclusive si el Valor del producto es 0. Esto puede deberse a que el producto sea una muestra o a un acuerdo mutuo con el Proveedor.

Se puden configurar Almacenes de Origen y Destino diferentes para Productos diferentes. 

### 3.2 Costos Adicionales

Si el registro de inventario es un registro de ingreso, es decir, se están recibiendo productos en almacén de destino, se pueden añadir costos adicionales (como Gastos de Envío, Derechos Aduaneros, Costos de Operación, etc) relacionados  con el proceso. Los costos adicionales serán considerados en el cálculo de la Tarifa de Valoración de los productos. 

Para añadir costos adicionales:

1. Seleccionar la Cuenta de Gastos en la cual se registrarán los gastos de esta Entrada de Inventario. 
1. Ingresar la descripción y el monto del costo en la tabla de Costos Adicionales. 

<img class="screenshot" alt="Stock Entry Additional Costs" src="{{docs_base_url}}/assets/img/stock/additional-costs-table.png">

Los Costos Adicionales introducidos se distribuirán entre los productos recibidos (en el Almacén de Destino mencionado) de forma proporcional con el Monto Básico de los productos. Y los costos adicionales distribuídos serán sumados al precio básico del producto para calcular la Tarifa de Valoración. 

Al expandir la tabla de Productos, la Cantidad y la Tarifa se muestran como se verá a continuación.
<img class="screenshot" alt="Stock Entry Item Valuation Rate" src="{{docs_base_url}}/assets/img/stock/stock-entry-item-valuation-rate.png">

### 3.3 Dimensiones Contables
Se pueden clasificar diferentes transacciones de acuerdo con diferentes dimensiones. De forma predeterminada [Proyectos](/docs/user/manual/es/projects/project) puede ser considerada como una dimensión, debido a que es práctica común rastrear los costos de diferentes proyectos. Para saber más respecto a Dimensiones Contables, [visitar esta página](/docs/user/manual/es/accounts/accounting-dimensions).

### 3.4 Ajustes de Impresión

#### Membrete
Se pueden imprimir las Entradas de inventario en papel con el membrete de la empresa. Saber más [aquí](/docs/user/manual/en/setting-up/print/letter-head).

#### Encabezado
Los encabezados de las Entradas de inventario pueden ser modificados al imprimir el documento. Se puede hacer esto seleccionando **Encabezado**. Para crear nuevos Encabezados ir a: Inicio > Configuraciones > Impresión > Encabezado. Leer más [aquí](/docs/user/manual/es/setting-up/print/print-headings).

### 3.5 Más Información

* **De apertura**: Si este registro es el primer registro de inventario para los Productos.
* **Observaciones**: Cualquier observación adicional respecto al Producto.
* **Porcentaje Transferido**: El porcentaje de Productos transferido de acuerdo con el objetivo de la Entrada de Inventario. 
* **Monto Total**: El monto total de Productos transferidos.

### 3.6 Inventario Perpetuo

Si el sistema de inventario perpetuo se encuentra habilitado, los costos adicionales se registrarán en la Cuenta de Gastos mencionada en la tabla de Costos Adicionales. 

<img class="screenshot" alt="Additional Costs General Ledger" src="{{docs_base_url}}/assets/img/stock/stock-entry-additional-cost.png">

<img class="screenshot" alt="Additional Costs General Ledger" src="{{docs_base_url}}/assets/img/stock/additional-costs-general-ledger.png">

### 3.7 Luego de Enviar
Luego de Enviar una Entrada de Inventario, se puede acceder al inventario de existencias o al libro contable desde el tablero. 

<img class="screenshot" alt="Additional Costs General Ledger" src="{{docs_base_url}}/assets/img/stock/stock-entry-submit.png">

## 4. Temas Relacionados
1. [Objetivo de la Entrada de Inventario](/docs/user/manual/es/stock/articles/stock-entry-purpose)
1. [Conciliación de Inventario](/docs/user/manual/es/stock/stock-reconciliation)
1. [Saldo de apertura de stock para Productos seriados y en lote](/docs/user/manual/es/stock/articles/opening-stock-balance-entry-for-serialized-and-batch-item)
1. [Orden de Trabajo](/docs/user/manual/en/manufacturing/work-order)
1. [Plan de Producción](/docs/user/manual/en/manufacturing/production-plan)
1. [Tarjeta de Empleo](/docs/user/manual/en/manufacturing/job-card)
