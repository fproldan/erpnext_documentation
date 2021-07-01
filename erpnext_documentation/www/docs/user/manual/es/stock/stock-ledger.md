<!-- add-breadcrumbs -->

# Mayor de Inventarios

**El Mayor de Inventarios es un informe detallado que registra todos los movimientos de inventario de una empresa.**

Las transacciones hacia adentro o hacia afuera relacionadas a Fabricación, Compras, Ventas y Transferencias de stock son registradas en el Mayor de Inventarios que luego se refleja en el Reporte de Mayor de Inventarios. 

Refleja la cantidad y el valor de las existencias **enviadas, recibidas, o transferidas** junto con los productos en inventario y sus detalles de almacén.

Puede ser referido cuando está habilitado el sistema de **Inventario Perpetuo**, ya que este informe refleja la historia de todas las transacciones de inventario. Presenta una visión más detallada de las transacciones de inventario.

## Atributos del Reporte de Mayor de Inventarios

* **Tasa entrante**: Refleja el valor real de las existencias, al cual fueron traídas a inventario. 
Refleja el mismo valor ingresado en el campo *Precio* del documento.

* **Valor de Balance**: Representa el valor total de las existencias remanentes en inventario. Es el producto de la Tarifa de Valoración y el Cantidad en Balance de un producto. 

* **Tasa de Valoración**: Se calcula de acuerdo con el método de valoración seleccionado.

Así es como el Reporte de Mayor de Inventarios representa una **Entrada de Inventario** de tipo *Recepción de Material*.

![Stock Ledger Report](/docs/assets/img/stock/stock-ledger.png)

Refleja un producto **Silla** de cantidad *1000 unidades* con una Tasa entrante (Precio Básico) de *3000* recibido en el almacén *Tiendas - L* además de calcular la Tasa de Valoración y el Valor de Balance. 

Se puede hacer click en **Comprobante #** para abrir el documento desde donde fue creada esta transacción. 

Los Mayores de Inventarios son generados desde las siguientes transacciones:

-   Factura de Venta, Factura de Compra (con *Actualizar Stock* habilitado)
-   Nota de Entregs
-   Recibo de Compra
-   Entrada de Inventario
-   Conciliación de Inventario

Se pueden añadir campos de los Tipos de Documento previamente mencionados, haciendo click en Menú > Añadir Columna.
