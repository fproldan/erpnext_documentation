# Cierre de libros contables en ERPNext

Este es un paso importante en el ciclo contable, por lo que a continuación se detalla una guía para realizarlo correctamente en ERPNext.

<!-- imagen -->

Al finalizar el año fiscal se necesita iniciar los libros contables desde cero. Por esto, realizar el cierre de los mismos es una parte esencial del negocio ya que permite medir el rendimiento general, resaltar saldos que serán pasados al año siguiente, ayuda a remover inconsitencias en los registros y crea un marco para los reportes financieros futuros.

La siguiente es una guía para el cierre de libros contables.

1. Revisión de cuentas por cobrar/pagar
1. Conciliación de cuentas
1. Comprobante de cierre de período
1. Establecer el nuevo año fiscal como predeterminado

### Revisión de cuentas por cobrar/pagar

Verificar la lista de Ordenes para las cuales todavía no se generó la Factura correspondiente, chequear la lista de Facturas pendientes y registrar sus pagos proveerá una mejor visión de lo que se tiene y lo que se debe. Las facturas impagas más antiguas pueden causar incosnistencias en la contabilidad. Una vez corregido, se debe enviar los reportes pendientes para asegurar que los balances son correctos.

### Conciliación de cuentas
1. **Conciliación bancaria:**

El proceso para vincular transacciones ingresadas en ERPNext desde el Extracto bancario también ayuda a registrar otros cargos que no aparecen en los libros contables.

Usar la herramienta de [Actualización de Fechas de Transacciones Bancarias](docs/user/manual/es/accounts/bank-reconciliation#2-how-to-update-bank-transaction-dates) para vincular los saldos del Extracto bancario.

> Inicio > Contabilidad > Banco y Pagos > Actualización de Fechas de Transacciones Bancarias

2. **Conciliación de facturas:**

Es el proceso de asignar las **Entradas de pago** contra los Clientes y Proveedores para obtener cuentas por cobrar/pagar precisas.

Usar la herramienta de [Conciliación de pagos](docs/user/manual/es/accounts/payment-reconciliation) para vincular los pagos no asignados o anticipados con las facturas pendientes.

> Inicio > Contabilidad > Banco y Pagos > Conciliacion de pagos con facturas

3. **Conciliación de inventarios:** esto ayuda a mantener sincronizado el stock físico con el registrado en el sistema.

Usar [Conciliación de inventarios](docs/user/manual/es/setting-up/stock-reconciliation) para mantener el stock al día.

> Inicio > Almacén > Herramientas > Conciliación de inventarios

Para realizar una auditoría, el contador necesitará los siguientes reportes:

- Estados financieros: Hoja de balance, Estado de pérdidas y ganancias y Flujo de fondos.
- Extracto bancario y Préstamos.
- Depreciación de activos y Balances.


## [Comprobante de cierre de período](docs/user/manual/es/accounts/period-closing-voucher)

Este paso asegurará que todos los ingresos y gastos estén balanceados y que se inician los registros desde cero.

Esto restablece las cuentas de ingresos y egresos, y registra los montos correspondientes en la cuenta selecionada como se ve en el siguiente Balance general.

<!-- imagen -->

Una vez que el contador realizó todas las entradas de ajuste para balancear las cuentas, estas pueden ser **congeladas**.

Para esto se puede::

- Ir a Configuración de cuentas e ingresar la fecha hasta la cual se desea congelar las cuentas.

<!-- imagen -->

- Crear un [Período contable](docs/user/manual/es/accounts/accounting-period) para evitar la creación de transacciones fuera del período.

<!-- imagen -->

Esta configuración detendrá la generación de Facturas de compra para el período mencionado.

## Cambio de año fiscal

ERPNext crea un [Año fiscal](docs/user/manual/es/accounts/fiscal-year) al final de cada uno de ellos. Para que esto suceda de forma predeterminada hacer click en "Establecer como Predeterminado" en el año deseado; esto hará que las transacciones se creen solo en ese año.

> Inicio > Contabilidad > Maestros Contables > Año Fiscal

<!-- imagen -->
