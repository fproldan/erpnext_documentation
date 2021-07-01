<!-- add-breadcrumbs -->
# Presupuesto

**El Presupuesto es un plan financiero que ayuda a controlar los gastos de la Compañía.**

En ERPNext, se pueden definir y administrar presupuestos contra Centros de costo o Proyectos. Desde la versión 12, también se pueden crear diferentes [Dimensiones contables](/docs/user/manual/es/accounts/accounting-dimensions) para clasificar transacciones según diferentes criterios.

Por ejemplo, si se realizan ventas online, se puede definir un presupuesto para publicidad y configurar ERPNext para detenerlas o notificar cuando se está gastando más de lo previsto.

Los Presupuestos también son importantes para la planificación. Al hacer planes para el próximo año fiscal, normalmente se elige un objetivo sobre el cual dirigir los ingresos, para lo cual se deben definir los gastos. Establecer un presupuesto asegurará que estos gastos no sobrepasen ciertos límites en ningún momento.

Para acceder a la lista de Presupuesto, ir a:
> Inicio > Contabilidad > Centro de costos y presupuesto > Presupuesto

## 1. Creación de un presupuesto
1. Ir al listado de Presupuesto y hacer click en Nuevo.
1. Seleccionar contra qué presupuestar, ya sea Centro de costo, Proyecto o una [Dimensión contable](/docs/user/manual/es/accounts/accounting-dimensions).
1. En la tabla de cuentas, seleccionar una cuenta de ingresos/gastos para la cual se creará el presupuesto. Ej: presupuesto para los gastos telefónicos del año.
 
 <img class="screenshot" alt="Budget" src="{{docs_base_url}}/assets/img/accounts/budget-account.png">
 
4. Ingresar el monto para esa cuenta.
1. Guardar y validar.


## 2. Características
### 2.1 Distribución mensual

También se puede definir una Distribución mensual para repartir el presupuesto entre los meses del año fiscal. Si no se define una distribución mensual, ERPNext calculará el presupuesto anual, o mensual pero en proporciones iguales.

<img class="screenshot" alt="Monthly Distribution" src="{{docs_base_url}}/assets/img/accounts/monthly-budget-distribution.png">

### 2.2 Acciones de control (Alertas)

Las acciones de control pueden ser activadas cuando:

* Se valida una [Solicitud de Materiales](/docs/user/manual/en/stock/material-request).
* Se valida una [Orden de venta](/docs/user/manual/en/buying/purchase-order). 
* Se registra un gasto real (mediante un Asiento contable o una Factura de compra).

También se puede puede configurar para presupuestos anuales o mensuales.

![Control Actions](/docs/assets/img/accounts/control-actions.png)

Hay tres tipos de acciones de control.

* **Detener**: no se permitirá a los usuarios validar las transacciones.
* **Advertir**: se mostrará un mensaje de advertencia pero se permitirá a los usuarios validar las transacciones.
* **Ignorar**: no se evitará que los usuarios validen transacciones ni se mostrarán mensajes de advertencia.

Se pueden definir diferentes acciones para presupuestos mensuales y anuales. Si se excede al presupuesto, se mostrará una advertencia:

<img class="screenshot" alt="Monthly Distribution" src="{{docs_base_url}}/assets/img/accounts/budget-warning.png">

Nótese que una advertencia similar se accionará para cualquier tipo de transacción seleccionada en el presupuesto para la cuenta definida.

## 3. Variación de Presupuesto

En cualquier momento se puede chequear el reporte de Variación de Presupuesto para analizar los gastos registrados contra el presupuesto designado a un determinado Centro de costos o Proyecto.

Para acceder al reporte de Variación de Presupuesto, ir a:

> Inicio > Contabilidad > Centro de costos y presupuesto > Variación de Presupuesto

<img class="screenshot" alt="Budget Variance Report" src="{{docs_base_url}}/assets/img/accounts/budget-variance-report.png">


## 4. Temas relacionados
1. [Centro de costos](/docs/user/manual/es/accounts/cost-center)
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Factura de compra](/docs/user/manual/es/accounts/purchase-invoice)
