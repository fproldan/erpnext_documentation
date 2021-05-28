<!-- add-breadcrumbs -->
# Filtros de Dimensiones contables

En ERPNext se puede controlar la clasificación de varias dimensiones contables contra una cuenta específica utilizando filtros.

Para acceder a la lista de Filtros de Dimensiones contables ir a:
> Inicio > Contabilidad > Filtros de Dimensiones contables

## 1. Creación de Filtros de Dimensiones contables

1. Ir al listado de Filtros de Dimensiones contables y hacer click en Nuevo.
1. Seleccionar la Dimensión contable a la cual se aplicará la restricción.
1. Elegir "Permitir" o "Restringir" en el campo correspondiente.
1. Agregar las cuentas para las cuales se aplicará la restricción. Se puede tildar la opción "Es obligatorio" si la dimensión contable debe estar presente para una cuenta específica.
1. Añadir en la tabla de Dimensiones los valores que serán permitidos/restringidos para las cuentas mecionadas.

<img alt="Create accounting dimension filter" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/accounting-dimension-filter.png">

## 2. Características

### 2.1 Filtrado de dimensiones contables en transacciones

En base a las restricciones aplicadas a la cuenta, solo las dimensiones permitidas serán filtradas y mostradas en las transacciones.

<img alt="Filter Apply" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/accounting-dimension-filter-apply.png">

### 2.2 Validación de dimensiones inválidas u obligatorias

En el caso de que falte asignar una dimensión que es obligatoria o que una dimensión restringida haya sido aplicada a una cuenta, el sistema no permitirá validar la transacción hasta que se corrija la inconsistencia.

<img alt="Invalid Dimension" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/invalid-dimension.png">

<img alt="Mandatory Dimension" class="screenshot" src="{{docs_base_url}}/assets/img/accounts/mandatory-dimension.png">


### Temas relacionados
1. [Centro de costos](/docs/user/manual/es/accounts/cost-center)
1. [Presupuesto](/docs/user/manual/es/accounts/budgeting)
1. [Dimensiones contables](/docs/user/manual/es/accounts/accounting-dimensions)
