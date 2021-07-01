<!-- add-breadcrumbs -->

# Regla de Asignación

**Una Regla de Asignación permite configurar asignaciones automáticas de documentos a Usuarios.**

Una Regla de Asignación será útil en situaciones donde se cuenta con un equipo de asistencia e ingresan tickets de este tipo. Para asignar esos tickets de forma automática entre los empleados, se puede utilizar una Regla de Asignación.

Para acceder a Reglas de Asignacion ir a:
> Inicio > Configuraciones > Reglas de Asignación

## 1. Creación de una Regla de Asignación
Para configurar una asignación:

1. Ir al listado de Regla de Asignación y hacer click en Nuevo.
1. Seleccionar el Tipo de Documento que se quiere asignar automáticamente (por ejemplo **Incidencia**).
1. Ingresar la "Descripción" que será agregada a Tareas Pendientes.
1. Seleccionar la condición para la asignación.
    Se pueden escribir expresiones simples en Python para asignaciones automáticas en `Condición de asignación`, `Condición de desasignación` y `Condición de cierre`. Se tendrá acceso a todas las propiedades del documento y se podrán usar operadores como >, <, ==, etc, así como también distintas condiciones como `y` y `o`.

    Ejemplos:

    - `estado == "Abierto"`
    - `tipo_de_incidencia == "Técnico" y prioridad=="Alta" y estado == "Abierto"`

1. Seleccionar la regla de asignación:
    
    ![Assignment Rule](/docs/assets/img/automation/assignment-rule-select.png)

    * **Round Robin**: Asignar cada documento a un Usuario en secuencia. 
    * **Balanceo de carga**: Asignar nuevos documentos al Usuario con menor número de asignaciones.
    
    Para cualquiera de estas dos opciones, seleccionar la lista de Usuarios a los cuales se aplicará la Regla de Asignación:
    
    <img class="screenshot" alt="Assign" src="{{docs_base_url}}/assets/img/automation/auto-assign-2.png">

    * **Basado en el campo**: Asignar al usuario que corresponda según lo configurado en Campo
    
        Seleccionar el campo que contiene un enlace de Usuario al cual se le asignará la regla:
        
        <img class="screenshot" alt="Field Assign" src="{{docs_base_url}}/assets/img/automation/field-auto-assign.png">

1. Guardar.

Se pueden usar propiedades del documento en el campo Descripción que serán parte de la asignación. Las Reglas de Asignación de mayor "Prioridad" serán aplicadas primero.

Ejemplo:

Se ha asignado la Incidencia de Alta Prioridad *Archivo Cargado pero que no funciona*.

### 1.1 Reglas de Asignación Múltiples

También se pueden configurar múltiples asignaciones automáticas para cada Tipo de Documento, se aplicará primero el que tenga Prioridad más alta:

Aquí hay un ejemplo de una Regla de Asignación.

Configurar Tipo de Documento, Descripciones y Condiciones.

<img class="screenshot" alt="Assign" src="{{docs_base_url}}/assets/img/automation/auto-assign-1.png">

### 2. Temas Relacionados
1. [Flujos de Trabajo](/docs/user/manual/es/setting-up/workflows)
1. [Acciones de Flujo de Trabajo](/docs/user/manual/es/setting-up/workflow-actions)
