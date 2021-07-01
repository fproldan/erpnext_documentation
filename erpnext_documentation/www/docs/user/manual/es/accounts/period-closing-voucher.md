<!-- add-breadcrumbs -->
# Cierre de período

**El Cierre de un período indica que la ganancia/pérdida de un período contable está balanceada y se puede comenzar la contabilidad del nuevo período.**

Al final de cada Año fiscal, luego de realizarse las auditorías, se puede realizar el cierre de los libros contables. Esto significa que se deben hacer entradas especiales como:

  * Depreciación
  * Cambio del valor de los activos
  * Impuestos y pasivos diferidos
  * Actualización de deudas incobrables

Una vez hecho esto se registran las Ganancias y Pérdidas.

Al hacer esto, el balance entre las cuentas de ingresos y egresos se vuelve cero. De esta forma se inicia un nuevo Año fiscal (o período) con una Hoja de balance equilibrada y cuentas de Ganancia y Pérdida limpias. En ERPNext, luego de realizar estas entradas especiales por medio de Asientos contables para el año fiscal actual, se deberá ajustar mediante el Cierre de período todas las cuentas de ingreso y egreso para que queden en cero.

Para acceder a la lista de Cierres de período, ir a:
> Inicio > Contabilidad > Apertura y cierre > Cierre de período

## 1. Creación de un Cierre de período

1. Ir al listado de Cierre de período y hacer click en Nuevo.
1. Establecer la Fecha de Contabilización.
1. Seleccionar la cuenta, generalmente se usa "Reservas y excedentes".
1. Ingresar una Observación.
1. Guardar y validar.
  ![Period Closing Voucher](/docs/assets/img/accounts/period-closing-voucher.png)

### 1.2 Campos

* **Fecha de transacción** será la fecha de creación del Cierre de período.
* **Fecha de Contabilización** será la fecha en la cual este cierre deberá ser ejecutado. Si el año fiscal termina el 31 de Diciembre, entonces esa fecha debería ser ingresada en este campo.
* **Cierre del año fiscal** será el año para el cual se está realizando el cierre.

### 1.3 Impacto del Cierre de período
El Cierre de período generará entradas contables (Balance general). Esto hará que el valor de las cuentas de ingresos y egresos sea cero y transferirá el balance de Ganancia/Pérdida a la cuenta de cierre.

Se deberá seleccionar como cuenta de cierre una cuenta de pasivo como "Reservas y excedentes" o cualquier cuenta de reserva de ingresos o de Capital de los propietarios.

![Period Closing Voucher ledger](/docs/assets/img/accounts/period-closing-voucher-ledger.png)

> **Nota:** si las entradas contables se realizan en el cierre de un año fiscal, incluso luego de haber creado el cierre para ese año, se deberá crear otro Cierre de período. Cierres posteriores solo transferirán el balance de Ganancia y pérdida a la cuenta de cierre.

### 2. Temas relacionados
1. [Año fiscal](/docs/user/manual/es/accounts/fiscal-year)
1. [Período Contable](/docs/user/manual/es/accounts/accounting-period)
