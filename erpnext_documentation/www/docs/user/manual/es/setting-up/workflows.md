<!-- add-breadcrumbs -->
# Flujos de Trabajo

**Con flujos de trabajo se puede reescribir cómo un proceso de trabajo en particular es aprobado en ERPNext.**

Se pueden configurar muchos niveles de aprobación para un Flujo de Trabajo en ERPNext. Para permitir a varias personas enviar pedidos, para aprobaciones por múltiples usuarios, ERPNext requiere completar las condiciones de Flujos de Trabajo. 
ERPNext verifica todos los permisos antes de validar. 

Abajo se muestra un ejemplo de un Flujo de Trabajo para un pedido de licencia:

<img class="screenshot" alt="Workflow" src="{{docs_base_url}}/assets/img/setup/workflow-leave-fl.png">

Este es un ejemplo de una aprobación de dos niveles con cancelación. Si el usuario pide licencia, este pedido será enviado a la oficina de Recursos Humanos.
La oficina de Recursos Humanos (Usuario de Recursos Humanos) rechaza o aprueba este pedido. Una vez que este proceso está completo, el Gerente del usuario (quien aprueba la licencia) recibirá la indicación de que la oficina de Recursos Humanos ha Aprobado o Rechazado. El Gerente, que es la autoridad de aprobación, Aprobará o Rechazará el pedido.
De acuerdo con todo lo anterior, el usuario obtendrá su estado de Aprobado o Rechazado. 

Para crear reglas de Flujos de Trabajo ir a:

> Inicio > Configuración > Flujos de Trabajo > Flujos de Trabajo

Una vez creado un Flujo de Trabajo, se pueden tomar acciones respecto al mismo a través de [Acciones de flujo de trabajo](/docs/user/manual/es/setting-up/workflow-actions).

## 1. Prerrequisitos
Antes de crear un Flujo de Trabajo, se recomienda crear lo siguiente:

* [Estados de flujo de trabajo](/docs/user/manual/es/setting-up/workflow-state) como Aprobado, Cancelado, etc. 

## 2. Creación de un Flujo de Trabajo
1. Ir al listado de Flujo de Trabajo y hacer click en Nuevo.
1. Ingresar un nombre para el **Flujo de Trabajo** y seleccionar el Tipo de Documento sobre el cual será aplicado.
1. Ingresar los diferentes estados del Flujo de Trabajo. Para cada uno de ellos se asignará el Estado del Documento, seleccionar qué campo actualizar en la columna Actualizar Campo e ingresar qué valor será actualizado en el campo Actualizar Valor.

    Los Estados de Flujo de Trabajo pueden tener distintos colores. Por ejemplo: Verde para éxito. Estados de Documento:  Guardado = 0, Enviado = 1, Cancelado = 2.

    <img class="screenshot" alt="Workflow" src="{{docs_base_url}}/assets/img/setup/workflow-1.png">

    El campo seleccionado en Actualizar Campo será actualizado en el tipo de documento cuando cambie el Estado. El Valor de Actualización es el texto que aparece en el campo seleccionado en Actualizar Campo. De esta forma, aquí el campo estado es actualizado a Pedido, Aprobado, etc.

1. Reglas de Transición

    <img class="screenshot" alt="Workflow" src="{{docs_base_url}}/assets/img/setup/workflow-2.png">

    En el campo "Acción" se define la forma en que el aprobador puede proceder respecto al pedido de licencia. Estado Siguiente es el Estado en el que se encontrará el documento cuando se aplique la Accción. Aquí cambia de Pedido a Aprobado por Recursos Humanos cuando se realiza la acción Aprobar sobre el mismo.

1. Dentro del "Campo Estado de Flujo de Trabajo", ingresar un nombre para el Campo Personalizado que será añadido al Doctype Pedido de Licencia en este caso.
1. Al guardar, se creará el Campo Personalizado en el DocType.

### 2.2 Aspectos a tener en cuenta al crear un Flujo de Trabajo

* Crear un Flujo de Trabajo en ERPNext esencialmente anula los flujos de trabajo de Guardado y Validación regulares. Por ende, el documento funcionará en base al Flujo de Trabajo configurado y no según el código de proceso de trabajo preestablecido. Por ende, puede que no exista botón u opción Validar si no ha sido especificada en el Flujo de Trabajo creado. 

    Si no se aplica un Flujo de Trabajo a un documento, y ese documento es validable, entonces cuenta con el proceso de trabajo predeterminado con los estados: Borrador - Validado - Cancelado. Si se está aplicando un Flujo de Trabajo a un documento validable, esos estados predterminados deberán ser manejados por el usuario.

* Un documento no puede ser cancelado a menos que esté validado. 

* Si se desea dar la opción de cancelar, se deberá escribir un paso de transición de flujo de trabajo que especifique que luego de validado se puede cancelar. 

* Si los campos en la columna Actualizar Campo no están actualizados, se creará un nuevo campo personalizado con el nombre configurado en el campo "Campo Estado del Flujo de Trabajo".

### 2.3 Otras opciones para un Flujo de Trabajo

1. Está activo: Al hacer click en esta opción, todos los otros Flujos de Trabajo para el DocType seleccionado se vuelven inactivos.
1. No sobreescribir el estado: El estado de este Flujo de Trabajo no anulará el estado del documento (Pedido de Licencia) en la vista de lista. 
1. Enviar alerta de Correo Electrónico: Se enviarán correos electrónico al usuario con las siguientes acciones posibles del proceso de trabajo.

## 3. Características

### 3.1 Habilitar/Inhabilitar Estado Opcional del Flujo de Trabajo

En Estados, el estado opcional del Flujo de Trabajo significa que el estado puede no ser parte de la aprobación final. 

Por ejemplo, estados como Cancelado o Rechazado pueden ser opcionales.
![Optional State](/docs/assets/img/setup/workflow-optional-state.png)

**Observación:** Las Acciones del Flujo de Trabajo no son creadas para estados opcionales.

### 3.2 Condiciones

También se pueden añadir condiciones para que la Transición sea válida. Por ejemplo, en este caso, si alguien pide una licencia de más de 5 días, debe aprobar la solicitud un rol en particular. Para que esto suceda, se puede ingresar una propiedad para **Condición** dentro de Aprobado por Recursos Humanos como:

```
doc.total_leave_days <= 5
```

Por ende, si alguien pidiera una licencia de menos de 5 días, solo esa transición en particular será aplicada. Aquí, `total_días_licencia` es el nombre de campo del campo "Total de Días de Licencia" del Pedido de Licencia. Para ver el nombre de un campo ir a Menú > Personalizar.

Esto puede extenderse a cualquier propiedad del documento.

## 4. Ejemplo del Flujo de un Pedido de Licencia

Cuando un Empleado guarda un Pedido de Licencia, el estado del documento cambia a "Pedido":

<img class="screenshot" alt="Workflow" src="{{docs_base_url}}/assets/img/setup/workflow-3.png">

Cuando el usuario de Recursos Humanos inicia sesión, puede Aprobar o Rechazar. Si se aprueba, el estado del documento cambia a "Aprobado por RH". Sin embargo, todavía debe ser aprobado por el Aprobador de Licencias.

<img class="screenshot" alt="Workflow" src="{{docs_base_url}}/assets/img/setup/workflow-4.png">

Cuando el Aprobador de Licencias abre la página de Pedido de Licencia, finalmente puede "Aprobar" o "Rechazar" el Pedido de Licencia.

<img class="screenshot" alt="Workflow" src="{{docs_base_url}}/assets/img/setup/workflow-5.png">

## 5. Temas Relacionados
1. [Acciones de Flujo de Trabajo](/docs/user/manual/es/setting-up/workflow-actions)
1. [Regla de Asignación](/docs/user/manual/es/automation/assignment-rule)
