<!-- add-breadcrumbs -->
# Mantenimiento de Activos

**Mantenimiento de Activos se refiere a una actividad realizada sobre los Activos para mantener su desempeño o condición.**

ERPNext provee funciones para rastrear los detalles de: tareas individuales de mantenimiento/calibración para un activo por fecha, de la persona responsable del mantenimiento y de la fecha futura en la que realizar un nuevo mantenimiento. 

Para desempeñar un Mantenimiento de activos en ERPNext:

1. Habilitar la opción "Requiere Mantenimiento" en el Activo.
2. Crear un Equipo de Mantenimiento de Activos.
3. Crear el Mantenimiento de Activos.
4. Se crea un registro de Mantenimiento de activos.
5. Crear un registro de Reparación de Activos.

Para acceder al listado de Mantenimiento de Activos ir a:
> Inicio > Bienes > Mantenimiento > Mantenimiento de Activo

## 1. Prerrequisitos
Antes de crear y utilizar el Mantenimiento de Activos, se recomienda crear lo siguiente:

1. [Activos](/docs/user/manual/es/asset/asset)
1. Ir al Activo y tildar la opción "Requiere Mantenimiento", para habilitar el Mantenimiento de Activos.

<img class="screenshot" alt="Asset" src="{{docs_base_url}}/assets/img/asset/maintenance_required.png">

3. [Equipo de Mantenimiento de Activos](/docs/user/manual/es/asset/asset-maintenance-team)

## 2. Creación de un Mantenimiento de Activos
Para cada activo se debe crear un registro de Mantenimiento de Activos realizando una lista de todas las tareas de mantenimiento asociadas al mismo, el tipo de mantenimiento (Mantenimiento Preventivo o Calibración), la periodicidad, a quién está asignado y la fecha de inicio y fin del mantenimiento. De acuerdo con la fecha de inicio y la periodicidad se calculará automáticamente la próxima fecha y se creará una Tarea para el Asignado. 

1. Ir al listado de Mantenimiento de Activos y hacer click en Nuevo. 
1. Seleccionar el Activo.
1. Seleccionar el Equipo de Mantenimiento de Activos.
1. Añadir las Tareas de Mantenimiento en la tabla.
  1. Configurar el Estado de Mantenimiento ya sea "Planificado", "Atrasado", o "Cancelado".
  1. Seleccionar la periodicidad con la cual deben llevarse a cabo las tareas. Así se calculará la próxima fecha de realización. 
1. Guardar.
1. Luego de guardar, se puede asignar la tarea a un usuario.
  <img class="screenshot" alt="Asset" src="{{docs_base_url}}/assets/img/asset/asset_maintenance.png">

Si el producto es seriado, se puede ingresar el número de serie. 

## 3. Características
### 3.1 Tareas de Mantenimiento

* **Tipo de Mantenimiento**: Si es mantenimiento "Preventivo" o "Calibración" para restaurar el activo a un funcionamiento adecuado. 
* **Fecha de Inicio y Finalización**: Configurar la fecha de inicio y finalización en el momento en que el mantenimiento debe empezar y terminar. 
* **Última Fecha de Finalización**: Si el mantenimiento no fue realizado antes de o en la misma fecha programada, la fecha en que efectivamente se realizó el mantenimiento puede ser registrada aquí.

### 3.2 Mantenimiento de Activos en Tareas

Al asignar el mantenimiento a un usuario, éste aparecerá en su lista de Tareas. 

![Asset Maintenance](/docs/assets/img/asset/asset-maintenance-todo.png)


## 4. Temas Relacionados
1. [Ajuste del Valor del Activo](/docs/user/manual/es/asset/asset-value-adjustment)
1. [Depreciación de Activos](/docs/user/manual/es/asset/asset-depreciation)
1. [Deshechar un Activo](/docs/user/manual/es/asset/scrapping-an-asset)
