<!-- add-breadcrumbs -->
# Dimensiones contables


Utilizar dimensiones contables consiste en clasificar cada transacción con su dimensión correspondiente como Sucursal, Unidad de negocios, etc. Esto permite mantener cada sección por separado, limitando el mantenimiento general en las cuentas del Balance general y sin alterar el Plan de cuentas.

Los Centros de costos y los Proyectos son tratados como dimensiones por defecto en ERPNext. Al configurar un campo en Dimensiones contables, el mismo será añadido en los reportes de transacciones cuando corresponda. 

En ERPNext se pueden crear dimensiones contables configurables y utilizarlas en transacciones y reportes.

Para acceder a la lista de dimensiones contables ir a:
> Inicio > Contabilidad > Configuración > Dimensiones contables

## 1. Creación de dimensiones contables

1. Ir a la lista de Dimensiones contables y hacer click en Nuevo.
1. Seleccionar el tipo de Documento de referencia que se desea utilizar como dimensión personalizada. Por ejemplo, si se selecciona Departamento como Documento de referencia, entonces la dimensión se basará en el Depertamento.
1. Ingresar el nombre de la dimensión (este nombre aparecerá en las transacciones para las cuales las dimensiones son creadas).
1. Dentro de la tabla de valores por defecto se pueden mencionar dimensiones predefinidas específicas para cada Compañía. Estas dimensiones serán traídas automáticamente en las transacciones realizadas dentro de cada Compañía.
1. Tildar la opción "Obligatorio" si se desea que la dimensión sea requerida siempre en las transacciones.

<img alt="Create custom dimension" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/accounting-dimension.png">


## 2. Características

Al crear la dimensión, se crearán automáticamente campos personalizados para cada dimensión. Estos campos estarán visibles en la sección de Dimensiones contables dentro de las transacciones que impactan en las Entradas contables (Balance general).

### 2.1 Uso de dimensiones en las transacciones

Para clasificar una transacción con una dimensión se puede seleccionar la dimensión deseada en la sección correspondiente.

<img alt="Create custom dimension" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/dimension-section.png">

<img alt="Create custom dimension" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/dimension-transaction.png">

### 2.2 Filtrado de reportes basados en dimensiones

También se puede filtrar los diversos reportes fiscales como el de Estado de pérdidas y ganancias, Hoja de balance, Balance general haciendo uso de estas dimensiones.

<img alt="Create custom dimension" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/report-dimensions.png">

### 2.3 Dimensión contable obligatoria para cuentas de Pérdida y ganancia y de Hoja de balance

Pérdida y ganancia es el grupo de cuentas de Ingreso y Egreso que representan las transacciones realizadas en un determinado período de tiempo.

Las cuentas de la Hoja de balance son Aplicación de fondos (Activos) y Fuentes de fondos (Pasivos), las cuales representan el valor neto de la compañia en un momento determinado.

Al seleccionar las opciones "Obligatorio para cuentas de Pérdida y ganancia" u "Obligatorio para cuentas de Hoja de balance" se puede configurar que dichas dimensiones sean requeridas para estos tipos de cuentas.

<img alt="Create custom dimension" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/dimension-mandatory.png">

### 2.4 Deshabilitación de dimensiones que ya no son necesarias

Es posible deshabilitar las dimensiones que ya no son utilizadas. Las transacciones que poseían dicha dimensión se mantendrán intactas.

<img alt="Create custom dimension" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/dimension-disable.png">


### Temas relacionados
1. [Centro de costos](/docs/user/manual/es/accounts/cost-center)
1. [Presupuesto](/docs/user/manual/es/accounts/budgeting)
1. [Reportes contables](/docs/user/manual/es/accounts/accounting-reports)
