<!-- add-breadcrumbs -->
# Factura de Ventas Desde Registro de horas

Se puede facturar a un Cliente en base al número total de horas que ha trabajado un empleado para ese cliente. El número real de horas de trabajo facturable puede rastrearse a través de un [Registro de horas](/docs/user/manual/es/projects/timesheets/). 

**Puede generarse una factura de ventas desde cada Registro de horas validado por un empleado, la cual puede utilizarse para facturar al cliente.**


<img class="screenshot" alt="Sales Invoice" src="{{docs_base_url}}/assets/img/project/projects-sales-invoice-from-timesheet.png">

## 1. Creación de una Factura de Venta desde un Registro de horas

  1. Una vez que el Registro de horas es validado, hacer click en "Crear Factura de Venta".
  2. Ingresar el Código de Producto y el nombre del Cliente que debe ser facturado desde este Registro de horas. El Producto puede ser un Producto o un Servicio. Hacer click en "Crear Factura de Venta".
  3. Todos los detalles del Registro de horas serán completados de forma automática en la Factura de Venta.
  4. La fecha y hora de contabilización se configurará como la fecha actual, se podrá editar luego de tildar la opción "Editar fecha y hora de contabilidad". 
  5. De forma opcional se pueden incluir pagos para POS o convertir la factura en una Nota de crédito.
  6. Guardar y validar.
  
Para obtener los detalles de forma automática en una Factura de Venta, hacer click en el botón **Obtener Productos Desde**. Los detalles pueden ser obtenidos desde Orden de Venta, Nota de Entrega o Cotización. Los detalles como la OC del Cliente, su Dirección y Número de Contacto, la Moneda y la Lista de Precios, y los Productos se completarán automáticamente.  

<img class="screenshot" alt="Sales Invoice" src="{{docs_base_url}}/assets/img/project/timesheet/timesheet-billing-to-sales-invoice.gif">

## 2. Características

Detalles Adicionales al crear Factura de Venta desde Registro de horas:

  * **Dimensiones Contables**: Las Dimensiones Contables permiten relacionar transacciones con Territorios, Sucursales y Proyectos específicos, entre otros. Esto ayuda a ver los estados contables de forma separada de acuerdo con los criterios seleccionados. Para saber más visitar la página [Dimensiones Contables](/docs/user/manual/es/accounts/accounting-dimensions).
  * **Lista de registros de horas**: Como la Factura se crea desde un Registro de horas, los detalles de la misma se obtendrán de forma automática. Se puede hacer click en "Añadir Fila" para añadir más Registros de horas a esta Factura. 

Todos los otros detalles pueden añadirse de la misma forma en que se añadirían en cualquier [Factura de Venta](/docs/user/manual/es/accounts/sales-invoice).

## 3. Luego de validar

Una vez que se haya validado la Factura de Venta, detalles como "Total de Horas Facturadas", "Monto Total Facturado" y "Procentaje Monto Facturado" serán actualizados en el Registro de horas. Además, también puede generarse un [Recibo de Sueldo](/docs/user/manual/es/projects/salary-slip-from-timesheet) desde el Registro de horas.

{siguiente}
