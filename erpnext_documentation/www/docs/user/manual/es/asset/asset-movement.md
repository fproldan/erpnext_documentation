<!-- add breadcrumbs -->
# Movimiento de Activos

**El Movimiento de Activos se refiere al traslado de un Activo de una Ubicación a otra.**

En ERPNext, se puede rastrear la ubicación de un activo, o a quién es asignado. Para esto se necesita crear una transacción de Movimiento de Activos cada vez que un activo es trasladado de una ubicación a otra. También se puede mantener un registro de las asignaciones de activos a empleados.

Para acceder al listado de Movimiento de Activo ir a:
> Inicio > Bienes > Bienes > Movimiento de Activo

<img class="screenshot" alt="Asset" src="{{docs_base_url}}/assets/img/asset/asset-movement.png">

## 1. Prerrequisitos
Antes de crear y utilizar el Movimiento de Activos, es recomendable crear lo siguiente: 

* [Activo](/docs/user/manual/es/asset/asset)
* [Ubicación de Activo](/docs/user/manual/es/asset/asset-location)


## 2. Creación de un Movimiento de Activo
1. Ir al listado de Movimiento de Activos y hacer click en Nuevo.
1. Seleccionar el Objetivo del traslado entre "Incidencia", "Recepción", o "Transferencia". Los campos obligatorios cambiarán de acuerdo al objetivo definido. 
1. Seleccionar una fecha.
1. Seleccionar los Activos que se desean mover. Ubicación de Origen/Desde Empleado serán campos obtenidos automáticamente.
1. Seleccionar el Tipo de Documento de Referencia (Opcional) 
1. Seleccionar Nombre del Documento de Referencia (Opcional).
1. Guardar.
1. Validar.

Para realizar un Movimiento de Activos de múltiples activos, es recomendable ir a la Lista de Activos, seleccionar los activos a mover y hacer click en **Crear Movimiento de Activos** desde el menú de Acciones que se encuentra en la parte superior izquierda. 

<img class="screenshot" alt="Asset" src="{{docs_base_url}}/assets/img/asset/asset-movement-using-button.png">

También hay un botón para **Transferir Activos** en la parte superior derecha del formulario de Activos, para generar un Movimiento de Activos. Con esta funcionalidad se completan automáticamente los campos del activo.

<img class="screenshot" alt="Asset" src="{{docs_base_url}}/assets/img/asset/asset-movement-using-transfer-asset-button.png">
