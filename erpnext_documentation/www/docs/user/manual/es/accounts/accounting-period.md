<!-- add-breadcrumbs -->
# Período contable

**Un Período contable define un lapso de tiempo en el cual se registran los estados financieros.**

En ERPNext, una vez finalizado un período contable, ciertas transacciones (facturas de venta/compra, entradas de inventario, entradas de nómina, asientos contables, etc) ya no pueden ser creadas. En otras palabras, estas transacciones solo pueden ser creadas dentro de un determinado Período contable.

**¿Por qué es necesario un Período contable?**

Cuando las transacciones son validadas, afectan las cuentas y los reportes en los cuales se procesa la información contable. Esto puede causar complicaciones cuando se necesita generar reportes financieros para auditorías realizadas por autoridades o en el cierre de los libros contables al finalizar el año fiscal.

En estos casos se puede usar el Período contable para limitar el lapso de tiempo dentro del cual las transacciones pueden ser validadas con el objetivo de preservar la integridad de los reportes correspondientes.

## 1. Creación de un período contable

### 1.1 ¿Para qué sirve el tilde "Cerrado" junto a las transacciones seleccionadas?

![Accounting Period Child Table](/docs/assets/img/accounts/accounting-period-closed.png)

La opción "Cerrado" en la tabla hija para los distintos tipos de transacciones es usada para determinar cuales no podrán ser validadas fuera del Período contable.

Tener en cuenta que cuando el Período contable finalice, no se aplicarán restricicones a las transacciones que no tengan tildada esta opción.

1. Ingresar un nombre para el Período contable.
1. Definir las fechas de inicio y fin del período.
1. Agregar o quitar transacciones de la tabla.
1. Guardar y validar.

 ![Accounting Period](/docs/assets/img/accounts/accounting-period.png)


Si se intenta validar una transacción restringida luego de la finalización del período se mostrará un mensaje advirtiendo sobre la situación.

![Accounting Period](/docs/assets/img/accounts/accounting-period-1.png)

> Nota: Ningún rol tiene permitido validar transacciones restringidas por un período contable, ni siquiera el definido como "Rol que permite definir cuentas congeladas y editar asientos congelados" en la [Configuración de cuentas](/docs/user/manual/es/accounts/accounts-settings).

## 2. Temas relacionados
* [Cierre de período](/docs/user/manual/es/accounts/period-closing-voucher)
