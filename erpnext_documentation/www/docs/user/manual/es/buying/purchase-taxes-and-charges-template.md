<!-- add-breadcrumbs -->
# Plantilla de Impuestos (Compra)

**Los Impuestos y cargos de Compra pueden ser aplicados a cualquier producto que se compre.**

La Plantilla de Impuestos (Compra) es similar a la Plantilla de Impuestos (Venta). Las plantillas creadas desde este formulario pueden ser utilizadas en Ordenes de Compra y Facturas de Compra para registros internos.

Si se quiere usar Cuentas Fiscales en la plantilla de impuestos debe configurarse el Tipo de Cuenta como "Fiscal" para esa cuenta particular.

Para acceder a la Plantilla de Impuestos (Compra) ir a: 
> Inicio > Compras > Configuración > Plantilla de Impuestos (Compra)

## 1. Añadir Impuestos de Compra a través de una plantilla
Antes de crear una nueva plantilla, es importante saber que ya hay plantillas creadas para muchos de los impuestos comúnmente usados.

1. Hacer click en Nuevo.
2. Ingresar el nombre del Impuesto.
3. En "tipo", configurar sobre qué va a ser calculado el impuesto y su tasa. Hay cuatro opciones en esta sección según las cuales el impuesto puede ser calculado.
    1. Real: Ingresar un monto fijo del impuesto.
    2. Sobre el total neto: Sobre el total neto de todos los productos.
    3. Sobre la fila anterior: Esto es para generar gastos compuestos. Por ejemplo, aplicar un impuesto sobre el monto al cual ya se le aplicó otro impuesto en la fila anterior.
    4. Sobre el total de la fila anterior: Igual que lo explicado anteriormente pero aplicado al total de la factura y no solo al monto de un producto.
    5. Sobre cantidad de producto: El impuesto será calculado como Tasa del Impuesto * Cantidad de Producto. Por ejemplo, si la tasa del impuesto es 2% y el número de productos es 2, entonces la Tarifa del Impuesto será 4, si el número de productos es 5, la Tarifa será 10, y así sucesivamente.
4. Seleccionar una cuenta principal que ya tenga las tasas impositivas predeterminadas, o crearla.
5. Si se selecciona aplicar predeterminadamente, se aplicará esta plantilla de forma predeterminada para las nuevas transacciones de Compra.
6. Guardar.
<img class="screenshot" alt="Purchase taxes" src="{{docs_base_url}}/assets/img/buying/purchase-taxes.png">


## 2. Características
### 2.1 Tabla de Impuestos (Compra)

* **Considerar impuestos o cargos por**: Total - por el total de todos los productos. Valuación - por cada producto. Valuación y total - se aplica el impuesto/gasto a los dos. Leer este [artículo](/docs/user/manual/es/accounts/articles/what-is-the-differences-of-total-and-valuation-in-tax-and-charges) para entender la diferencia.
* **Agregar o deducir:** ya sea que se desee agregar o deducir el impuesto del producto.

* **Fila de referencia #**: Si el impuesto esta basado "Sobre la fila anterior" o "Sobre el total de la fila anterior" se puede seleccionar el número de fila que será usado de base para este cálculo (la configuración predeterminada es la fila anterior).
   <img class="screenshot" alt="Purchase taxes table" src="{{docs_base_url}}/assets/img/buying/purchase-taxes-table.png">

* **¿Está incluido este impuesto en el precio base?**: Si esta casilla está seleccionada, se considerará que el importe del impuesto ya está incluido en el Precio Impreso/Monto Impreso.
* **Encabezado de cuenta:** La cuenta bajo la cual se registrará este impuesto. Si se selecciona IVA u otras de las cuentas ya existentes, la tarifa será completada automáticamente. 
* **Centro de Costos:** Si el impuesto/gasto es un ingreso (como envío) o gasto, debe ser contabilizado en relación a un Centro de Costos.
* **Descripción:** Description of the tax (that will be printed in invoices/quotes).
* **Precio:** La tasa del impuesto, por ejemplo: 14 = 14%.
* **Importe:** El monto de impuesto a ser aplicado, por ejemplo: 100.00 = â‚¹100.


### 3. Temas relacionados
1. [Orden de Compra](/docs/user/manual/es/buying/purchase-order)
1. [Configuración de Compras](/docs/user/manual/es/buying/buying-settings)
