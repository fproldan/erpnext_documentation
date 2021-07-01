<!-- add-breadcrumbs -->
# Conciliación de Inventario

**La Conciliación de Inventario es el proceso de contar y evaluar materiales/productos de forma periódica a fin de año.**

Esto se hace para:

* Sincronizar la cuenta de inventario físico y la cuenta contable. 
* Valuar el inventario para preparar los estados contables.

La Conciliación de Inventario es usada en ERPNext para:

* Contabilizar las Existencias Iniciales
* Conciliar el inventario físico y en libros. 

Para acceder al listado de Conciliación de Inventario ir a:
> Inicio > Almacén > Herramientas > Conciliación de Inventario

## 1. Creación de una Conciliación de Inventario para Contabilizar las Existencias Iniciales

Utilizando la conciliación de inventario se puede actualizar el número de productos específicos en un Almacén en un momento específico. 
También se pueden añadir Productos en el inventario que tengan Números de Serie y de Lote. 

1. Ir al listado de Conciliación de Inventario y hacer click en Nuevo.
1. Seleccionar el Objetivo como "Apertura de stock". Se puede editar la Fecha y Hora de contabilización.
1. Seleccionar Código de Producto, Almacén, Cantidad y Tarifa de Valoración. Si hay Número de Serie y Lote añadirlo.
1. Si se desea generar automáticamente Números de Serie y Lote entonces mantener esos campos en blanco. 
    * Para generar automáticamente Números de Serie se debe configurar "Serie de Números de Serie" en el Producto. 
    * Para generación automática de Número de Lote, se debe habilitar la casilla "Crear nuevo lote automáticamente" en el producto.
1. La Cuenta de Diferencia se configurará como "Apertura Temporal". 
1. Guardar y Validar.

    ![Opening Stock](/docs/assets/img/stock/opening_stock.png)

> Observación: La opción Mantener Stock debe estar habilitada en el Producto para que esto funcione.

## 2. Creación de una Conciliación de Inventario para Conciliar el Conteo Físico y Contable

La Conciliación de Inventario es el proceso de contar y evaluar las existencias de forma periódica y a fin de año para valuar el inventario total y preparar los estados contables. En este proceso, los inventarios físicos son revisados y registrados en el sistema. Las existencias físicas de productos y los valores en el sistema deberían ser precisos y concordantes. Si no lo son, se puede utilizar la herramienta de Conciliación de Iventario para conciliar el balance de inventario y los valores con los reales. 

Para conciliar el inventario:

1. Ir al listado de Conciliación de Inventario y hacer click en Nuevo.
1. Seleccionar el Objetivo como "Conciliación de Inventario". Se puede editar la Fecha y Hora de contabilización.
1. Configurar Código de Producto y Almacén.
1. La Cantidad actual y la Tarifa de Valoración serán obtenidas, cambiar la cantidad de acuerdo a lo que se requiera. 
1. La cuenta de gastos en la Cuenta de Diferencia se configurará de forma predeterminada como "Ajuste de Existencias". 
1. El Centro de Costos predeterminado será "Principal", cambiar de ser necesario.
1. Guardar y Validar.
  
    ![Stock Reconciliation](/docs/assets/img/stock/stock_recon.png)


## 3. Características

### 3.1 Subir Información Usando Planilla 

Si se cuenta con muchos productos, se pueden subir los detalles a través de una planilla. 

1. Bajar Plantilla

  Abrir nueva Conciliación de Inventario y hacer click en el botón Descargar para bajar la plantilla en formato CSV.

  <img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-recon-1.png">

2. Ingresar los datos en la Plantilla CSV.

  El formato CSV es sensible a mayúsculas. No editar los encabezados que están pre configurados en la plantilla. En la columna de Código de Producto y Almacén, ingresar el Código de Producto exacto y el Almacén como fue creado en la cuenta ERPNext. Para cantidad, ingresar el nivel de existencias que se desea configurar para ese producto en un Almacén específico. 

  <img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-reco-data.png">


3. Subir el archivo CSV con los datos haciendo click en el botón "Subir". 

  <img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-recon-2.png">


4. Revisar, guardar y validar.

  <img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-reco-upload.gif">

5. Revisar el Mayor de Inventario para ver el balance de existencias actualizado.

  <img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-reco-ledger.png">

### 3.2 Obtener el Balance de Inventarios y la Valoración para una Fecha y Hora específicas 

Se puede importar el balance de inventarios y la valoración en una fecha y hora específicas, para un Almacén seleccionado, haciendo click en el botón **Producto**. Se pueden actualizar la Cantidad y la Tarifa de Valoración como se necesite. 

<img class="screenshot" alt="Stock Reconciliation Items Button" src="{{docs_base_url}}/assets/img/stock/stock_reconciliation_items_button.gif">

## 4. Funcionamiento de la Conciliación de Inventario

Una vez que se crea la conciliación de inventario para actualizar la cantidad en una fecha y hora específica para un producto en un Almacén, la misma no será modificada por transacciones de existencias subsecuentes, incluso si las mismas tienen una fecha y hora de contabilización anterior a la fecha de conciliación de inventario. En otras palabras, registros de fechas anteriores no cambiarán los números del inventario una vez realizada la Conciliación de Inventario. 

Los ejemplos se muestran a continuación:

### 4.1 Para Productos No Seriados

Consedérese un producto con código 'ABC001' en un Almacén 'Mumbai'.
Asumiendo que las existencias al 10 de enero son de 100 unidades.
Se realiza la Conciliación de Inventario el 12 de enero para configurar el balance de exitencias en 150 unidades. 

El Mayor de Inventario se verá como se muestra a continuación:
<html>
   <table border="1" cellspacing="0px">
      <tbody>
         <tr align="center" bgcolor="#EEE">
            <td><b>Fecha de contabilización</b></td>
            <td><b>Cantidad</b></td>
            <td><b>Balance de Cantidad</b></td>
            <td><b>Tipo de Comprobante</b></td>
         </tr>
         <tr>
            <td>10/01/2014</td>
            <td align="center">100</td>
            <td>100&nbsp;</td>
            <td>Recibo de Compra</td>
         </tr>
         <tr>
            <td>12/01/2014</td>
            <td align="center">150</td>
            <td>150</td>
            <td>Conciliación de Inventario</td>
         </tr>
      </tbody>
   </table>
</html>

Si se realiza un nuevo registro de un Recibo de Compra el 5 de enero de 2014, lo cual es anterior a la fecha del registro de Conciliación de Inventario, el Mayor de Inventario se verá como se muestra a continuación. 
<html>
    <table border="1" cellspacing="0px">
        <tbody>
            <tr align="center" bgcolor="#EEE">
                <td><b>Fecha de contabilización</b></td>
                <td><b>Cantidad</b></td>
                <td><b>Cantidad de Balance</b></td>
                <td><b>Tipo de Comprobante</b></td>
            </tr>
            <tr>
                <td>05/01/2014</td>
                <td align="center">20</td>
                <td style="text-align: center;">20</td>
                <td>Recibo de Compra</td>
            </tr>
            <tr>
                <td>10/01/2014</td>
                <td align="center">100</td>
                <td style="text-align: center;">120</td>
                <td>Recibo de Compra</td>
            </tr>
            <tr>
                <td>12/01/2014</td>
                <td align="center"><br></td>
                <td style="text-align: center;"><b>150</b></td>
                <td>Conciliación de Inventario<br></td>
            </tr>
        </tbody>
    </table>
</html>

Como se puede ver, la Cantidad de Balance al 10 de enero se actualizó de 100 a 120. Pero la Cantidad de Balance al 12 de enero no se actualizó de 150 a 170.


### 4.2 Para Productos Seriados

Para un Producto ITEM-00225 que tiene los 6 números de serie HJF00020, HJF00021, HJF00022, HJF00023, HJF00024, HJF00025 con una tarifa de valoración de 530 por número de serie. A fin de año, el usuario se entera que sólo tiene 3 Números de Serie de ese producto con una Tarifa de Valoración de 620. Por ende, para eliminar los números de serie viejos HJF00020, HJF00021, HJF00022, HJF00023, HJF00024, HJF00025 y añadir los nuevos números de serie con la nueva Tarifa de Valoración puede utilizarse la Conciliación de Inventario como se muestra a continuación:

Seleccionar el producto ITEM-00225 en la conciliación de inventario, al hacer esto, el sistema obtendrá automáticamente los números de serie existentes. Luego, configurar la cantidad en 3, la Tarifa de Valoración en 620 y los números de serie como HJF00026, HJF00027, HJF00028.


<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-recon-for-serialized.png">

Antes de la conciliación, la tarifa de valoración era 530 y la cantidad disponible 6, por ende, el valor total de inventario era 3180. Luego de la conciliación, la tarifa de valoración ha cambiado a 620 y la cantidad disponible a 3, por lo cual el nuevo valor de inventario es 1860. Para ajustar el valor de inventario en la contabilidad, el sistema acreditó un monto extra 3180 - 1860 = 1320 a la cuenta Almacén y debitó a la cuenta de ajuste de inventario. Los registros de contabilidad general son como se muestra a continuación: 

Para ver los registros de contabilidad general hacer click en el botón Ver > Libro de Contabilidad

<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/gl_entry_for_serialized_items.png">

El balance de inventario luego del envío de la conciliación de inventario:
<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock_balance_after_stock_reco_submission.png">

La contabilidad general para la cuenta de Almacén Nagpur luego del envío de la conciliación de inventario:
<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/general_ledger_after_stock_reco_submission.png">

### 4.3 Para Productos en Lote

La conciliación de inventario para productos en lote será utilizada para añadir un nuevo lote o actualizar la cantidad de un lote existente. Por ejemplo, el lote JHGJH00003 tiene una cantidad actual de 60, pero si el usuario desea que ésta sea 100, entonces, utilizando la conciliación de inventario, el usuario puede actualizar la cantidad del lote. 

<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/for_batch_item_after_stock_reco_submission.png">

Informe Historial de Saldo por Lotes, luego de la validación de la conciliación de inventario:
<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/batchwise_balance_history_after_stock_reco_submission.png">

## 5. Temas Relacionados
1. [Entrada de Inventario](/docs/user/manual/es/stock/stock-entry)
1. [Contabilidad de Existencias en Inventario](/docs/user/manual/es/stock/accounting-of-inventory-stock)

