<!-- add-breadcrumbs -->
# Reportes contables

Algunos de los reportes más importantes son:

## 1. Compañía y cuentas
### Balance general
Ir a: **Contabilidad > Balance general > Balance general**.

En el Balance general se detallan las cuentas de Débito y Crédito de cada una de las transacciones realizadas.

Este reporte se basa en la tabla de Entradas de Balance general y se le pueden aplicar diversos filtros predefinidos como Cuenta, Centro de costos, Tercero, Proyecto y Período, entre otros. Esto ayuda a obtener información actualizada de todas las entradas realizadas en un determinado período contra una cuenta. El resultado puede agruparse por Cuenta, Comprobante/Transacción y Tercero con balances de apertura y cierre para cada grupo. En el caso de contabilidad con múltiples divisas, también hay una opción para chequear los montos en cualquier moneda distinta a la de la compañía.

<img alt="General Ledger" class="screenshot"
    src="{{docs_base_url}}/assets/img/accounts/reports/general-ledger.png">

## 2. Estados contables
### 2.1 Cuentas por cobrar y Cuentas por pagar
Ir a: **Contabilidad > Cuentas por cobrar/pagar > Cuentas por cobrar/pagar**.

Estos reportes ayudan a llevar el seguimiento de los saldos pendientes de Clientes y Proveedores. También provee un análisis en el tiempo, por ejemplo, un desglose del monto en base al período en el cual estuvo pendiente.

<img alt="Accounts Receivable" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/accounts-receivable.png">

#### 2.1.1 Cuentas por cobrar en base a Términos de Pago
También se pueden ver estas cuentas en base a los [Términos de pago](/docs/user/manual/es/accounts/payment-terms).

Este reporte se puede ver haciendo click en la opción "Basada en Términos de Pago".

<img alt="Accounts Receivable" class="screenshot"
    src="{{docs_base_url}}/assets/img/accounts/reports/accounts-receivable-1.png">

Así se pueden ver los montos pendientes contra cada Término de pago. El **Monto facturado** muestra el importe de cada término de pago y **Monto pagado** el importe pagado contra cada término. El pago de cada término es asignado utilizando un orden FIFO.

<img alt="Accounts Receivable" class="screenshot"
    src="{{docs_base_url}}/assets/img/accounts/reports/accounts-receivable-2.png">

### 2.2 Balance de comprobación
Ir a: **Contabilidad > Estados financieros > Balance de comprobación**.

Un Balance de comprobación es un reporte contable que lista los balances contables de todas las cuentas (cuenta y grupo de cuenta) para cualquier período. Una compañía prepara un Balance de comprobación de forma periódica, normalmente al final de cada período. El propósito general del Balance de comprobación es garantizar que las entradas en el sistema de contabilidad de la compañía son matemáticamente correctas. Los totales de la columnas de Debe y Haber deben ser iguales en cualquier período, para asegurar que las entradas son correctas. En ERPNext, el reporte posee las siguientes columnas:

  * Apertura (Deb): saldo de débito inicial en la fecha desde
  * Apertura (Cred): saldo de crédito inicial en la fecha desde
  * Debe: monto total debitado en la cuenta en el período seleccionado
  * Haber: monto total acreditado en la cuenta en el período seleccionado
  * Cierre (Deb): saldo de débito final en la fecha hasta
  * Cierre (Cred): saldo de crédito final en la fecha hasta

También hay opciones para incluir o excluir entradas de cierre de período, mostrar u ocultar cuentas con balance cero y para mostrar saldos de pérdidas y ganancias de años fiscales previos no cerrados. Todos los valores son mostrados en la moneda de la compañía.

<img alt="Trial Balance" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/trial-balance.png">

### 2.3 Hoja de balance
Ir a: **Contabilidad > Estados financieros > Hoja de balance**.

Una Hoja de balance es el Estado financiero de una Compañía que presenta activos, pasivos y capital de un momento determinado.

La Hoja de balance en ERPNext brinda más flexibilidad para analizar la posición fiscal. Se puede consultar el reporte incluyendo varios años para comparar los valores, los cuales se pueden chequear para un Libro de finanzas o Centro de costos específico. También se puede elegir cualquier otra moneda en función de la cual mostrar los balances.

<img alt="Balance Sheet" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/balance-sheet.png">

### 2.4 Estado de Flujos de Efectivo
Ir a: **Contabilidad > Estados financieros > Flujo de fondos**.

El Flujo de fondos es un estado financiero que muestra los ingresos y egresos de efectivo o equivalentes de la compañía. Es usado para analizar la posición de liquidez de la compañía.

<img alt="Cash Flow Statement" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/cash-flow.png">

### 2.5 Cuenta de pérdidas y ganancias
Ir a: **Contabilidad > Estados financieros > Estado de pérdidas y ganancias**.

Un Estado de pérdidas y ganancias es un estado financiero que sumariza todos los ingresos y gastos en un período.

En ERPNext, se puede consultar el reporte incluyendo múltiples años/períodos para comparar los valores. También se pueden chequear valores de un Libro de finanzas, Proyecto o Centro de costos específico. También se puede elegir cualquier otra moneda en función de la cual mostrar los balances. Si se desea consultar la información de forma trimestral/mensual, se puede elegir mostrar saldos acumulados o solo por cada período.

<img alt="Profit and Loss Statement" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/profit-and-loss.png">

### 2.6 Estado Financiero Consolidado
Ir a: **Contabilidad > Estados financieros > Estado Financiero Consolidado**.

El reporte muestra una vista unificada de la Hoja de balance, el Estado de pérdidas y ganancias y Flujo de fondos de la compañía que representa el grupo, fusionando los estados financieros de todas las compañías subsidiarias. Muestra los balances de cada compañía así como los acumulados de la compañía grupo.

<img alt="Consolidated Financial Statement" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/consolidated-financial-statement.png">

## 3. Impuestos
### 3.1 Registros de ventas y compras
Ir a: **Contabilidad > Impuestos > Registro de ventas *o* Registro de compras**.

Los registros de ventas y compras muestran todas las transacciones en un determinado período con sus montos facturados y detalles de impuestos. En este reporte cada impuesto tiene una columna propia, por lo que se puede obtener facilmente el total de cada tipo de impuesto acumulado/pagado en un período, lo cual ayuda al realizar el pago de los mismos al gobierno.

<img alt="Sales Register" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/sales-register.png">

## 4. Presupuesto y Centro de costos
### 4.1 Variación presupuestaria
Ir a: **Contabilidad > Presupuesto y Centro de costos > Variación de Presupuesto**.

En ERPNext, se puede asignar un presupuesto de gasto para una cuenta de este tipo contra un centro de costo específico. Este reporte ofrece una comparación entre los gastos presupuestados y los gastos reales, y la desviación (diferencia entre los dos) en vistas mensuales/trimestrales/anuales.

<img alt="Budget Variance" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/budget-variance.png">

## 5. Analítica
### 5.1 Detalle de Ventas y Compras
Ir a: **Contabilidad > Analítica > Detalle de Ventas *o* Detalle de Compras**.

El Detalle de Ventas y Compras muestra todas las transacciones de compra y venta de un determinado período con el precio del producto, cantidad, importe y detalles de los impuestos. En este reporte, cada impuesto tiene una columna propia por lo que es sencillo obtener los impuestos individuales aplicados a cada producto. Observando este reporte se puede determinar rápidamente qué productos se venden/compran más.

<img alt="Item Wise Sales Register" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/item-wise-sales-report.png">

Se puede realizar un análisis más detallado usando los filtros de "Agrupar por", para obtener información de un determinado Cliente, Proveedor, Territorio, etc. De esta forma se puede saber qué Producto es más popular en cierta región o qué Cliente es el principal comprador de tal Producto.

<img alt="Group By Sales Register" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/group-by-sales-register.png">

### 5.2 Tendencias de ventas o de compras
Ir a: **Contabilidad > Analítica > Tendencias de ventas *o* Tendencias de compras**.

Otro informe útil es el de tendencias de facturación. Mediante este reporte se puede saber fácilmente la tendencia mensual, trimestral, semestral o anual de las compras/ventas, en función a la cantidad y el monto acumulado.

<img alt="Sales Invoice Trends" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/sales-invoice-trends.png">

## 6. Por facturar
- **Ordenes por facturar:** el reporte muestra los productos que han sido ordenados por los clientes contra las facturas que no han sido creadas todavía o fueron creadas de forma parcial.
- **Envios por facturar:** productos entregados a los clientes cuya factura de venta no fue creada todavía o fue creada de forma parcial.
- **Ordenes de compra por facturar:** el reporte muestra los productos que fueron pedidos a los proveedores, pero no poseen factura de compra o tienen factura de compra parcial.
- **Recepciones por facturar:** productos que fueron recibidos pero no tienen factura de compra o tienen factura de compra parcial.

## 7. Otros reportes
### 7.1 Balance de Terceros
Ir a: **Contabilidad > Otros Reportes > Balance de Terceros**.

Por lo general se necesita ver el Balance de comprobación de los Clientes o Proveedores. Con este reporte se puede obtener para todos los clientes/proveedores o para cada uno de ellos de forma individual.

<img alt="Sales Invoice Trends" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/reports/party-wise-trail-balance.png">

### 7.2 Saldo de Clientes
Este reporte muestra el límite de crédito, saldo pendiente y crédito de cada Cliente.
