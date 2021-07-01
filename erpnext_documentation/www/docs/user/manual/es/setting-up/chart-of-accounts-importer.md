<!--add breadcrumbs-->

# Importador de Plan de Cuentas

Cuando se crea una nueva compañía en ERPNext, el Plan de Cuentas se crea de forma predeterminada con una estructura preestablecida. Sin embargo, si la empresa ya cuenta con su propio Plan de Cuentas, es posible importarlo utilizando el Importador de Plan de Cuentas.

Cualquier Plan de Cuentas existente para esa compañía será eliminado. Es necesario asegurarse que la empresa que se está seleccionando no tiene transacciones existentes; si las tiene, se mostrará un error de validación. 

Para acceder al Importador de Plan de Cuentas ir a:
> Inicio > Importación de datos y configuraciones > Importador de Plan de Cuentas

## 1. Importación del Plan de Cuentas

1. Seleccionar la Compañía para la cual se desea importar el Plan de Cuentas.

1. Hacer click en el botón "Descargar Plantilla" para descargar la plantilla. Seleccionar el Tipo de Archivo en el cual se desea descargar la plantilla. Seleccionar el tipo de plantilla y hacer click en "Descargar". "Plantilla de Muestra" contiene ya datos de muestra, para dar una idea de cómo llenar la plantilla. Se pueden editar los campos en el mismo archivo o descargar una "Plantilla en Blanco" para tener una plantilla nueva.

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-template-download.png">


    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-blank-template.png">

1. Una vez descargada la plantilla, ingresar los detalles de la misma como se muestra a continuación. Tener en cuenta que es necesario crear cuentas para los siguientes tipos: "Costo sobre Ventas", "Depreciación", "Activo Fijo", "Cuentas de gastos", "Cuentas de ingresos", "Ajuste de existencias". Los grupos principales para estas cuentas deben ser: Activos, Pasivos, Ingresos, Gastos y Capital. 

    Para saber más respecto a "Tipos de Cuentas" y "Grupos Principales" hacer click [aquí](/docs/user/manual/es/accounts/chart-of-accounts)

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-sample-template.png">

1. Hacer click en "Adjuntar" para subir la plantilla. 

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-attach.png">

1. Una vez cargada la plantilla se podrá ver la vista previa del Plan de Cuentas en la sección de Vista previa del plan.

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-preview.png">

1. Si todo está correcto en la vista previa, hacer click en "Importar" en la esquina superior derecha y las cuentas serán creadas.

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-start-import.png">

1. Para verificar las cuentas creadas se puede ir al Plan de Cuentas de la Compañía.

    <img class="screenshot" alt="COA Import" src="{{docs_base_url}}/assets/img/setup/coa-import.png">

## 2. Temas Relacionados
1. [Plan de Cuentas](/docs/user/manual/es/accounts/chart-of-accounts)

