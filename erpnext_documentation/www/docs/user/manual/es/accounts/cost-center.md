<!-- add-breadcrumbs -->
# Centro de costos

**Un Centro de costos es una parte de una organización donde se registran los gastos o ingresos.**

En ERPNext los Centros de costos pueden ser usados como Centros de ganancias.

El Plan de cuentas está diseñado principalmente para proveer reportes a las autoridades de gobierno y de recaudación.

La mayoría de las empresas tienen múltiples actividades, como diferentes líneas de productos, sectores de mercado, áreas de negocio, etc. que comparten gastos generales. Idealmente cada una de estas ramas debería tener su propia estructura para reportar si son rentables o no. Por esta razón, existe una estructura alternativa llamada Árbol Centro de costos.

Un Centro de costos actúa como una [Dimensión contable](/docs/user/manual/es/accounts/accounting-dimensions) la cual ayuda a llevar un registro de los costos de ciertas áreas.

Se pueden definir Centros de costos en los siguientes niveles:

* Compañía
* Producto
* Orden/Factura

El Centro de costos puede ser vinculado a las siguientes transacciones:

1. [Facturas de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Facturas de compra](/docs/user/manual/es/accounts/purchase-invoice)
1. [Asientos contables](/docs/user/manual/es/accounts/journal-entry)
1. [Entradas de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Nota de entrega](/docs/user/manual/en/stock/delivery-note)

También se puede usar para [Presupuestos](/docs/user/manual/es/accounts/budgeting).

## 1. Árbol Centro de costos

Se puede modificar el Árbol Centro de costos de forma que se adapte de la mejor forma posible a la compañía. Cada entrada de ingreso/gasto también es registrada contra un Centro de costo. Si está configurado para "Permitir centro de costo en entrada de cuenta de balance", el sistema permitirá crear entradas de cuentas de la Hoja de balance contra Centros de costo.

Por ejemplo, si se tienen dos tipos de ventas:

 * Ventas en el local
 * Ventas online

En ese caso no se tendrá el gasto del envío para las ventas hechas en el local y no habrá gasto de alquiler a considerar en el precio para venta online. Si se desea obtener la rentabilidad de cada una de estas modalidades por separado, se deberá tener dos Centros de costos para diferenciar cada tipo de venta. Lo mismo para las compras.

Así, cuando se analizan las ventas se llega a un mejor entendimiento sobre qué rama del negocio es más rentable. Ya que en ERPNext es posible tener múltiples compañías, se pueden crear Centros de costos para cada una de ellas y gestionarlos por separado.

Para acceder al Árbol Centro de costos, ir a:
> Inicio > Contabilidad > Presupuesto y Centro de Costo > Centros de Costos

## 2. Creación de Centros de Costos
1. Ir a Árbol Centro de costos.
1. "Agregar hijo" en el nodo deseado.
1. También es posible agregar nuevos nodos, tildando la opción "Es un grupo".

Seleccionar otra compañía en el filtro hará que se muestre el árbol de Centros de costos de esa compañía.

<img class="screenshot" alt="Cost Center" src="{{docs_base_url}}/assets/img/accounts/chart-of-cost-center.png"> 

### 3. Temas relacionados
1. [Presupuesto](/docs/user/manual/es/accounts/budgeting)
1. [Facturas de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Facturas de compra](/docs/user/manual/es/accounts/purchase-invoice)
