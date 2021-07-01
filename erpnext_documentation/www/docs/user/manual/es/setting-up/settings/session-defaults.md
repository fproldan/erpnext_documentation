<!-- add-breadcrumbs -->
# Predeterminados de Sesión

**Los Predeterminados de Sesión son valores predeterminados configurables que se encuentran preestablecidos durante sesiones de usuario.**

Consideremos una situación donde hay 8 compañías configuradas en una cuenta, y se tiene que completar el campo "Compañía" cada vez que se crea una nueva Orden de Venta. Este es un proceso que consume mucho tiempo cuando se debe lidiar con muchas Ordenes de Venta diariamente. 

## 1. Creación de Predeterminados de Sesión

### 1.1 Configuración predeterminada de sesión

1. Ir a Configuración predeterminada de sesión. Allí se podrá ver la tabla "Valores predeterminados de sesión".
2. Hacer click en "Añadir Fila".
3. Seleccionar el DocType para el cual se desea configurar los Predeterminados de Sesión.
4. Guardar.

    <img class="screenshot" alt="Session Defaults Settings" src="{{docs_base_url}}/assets/img/setup/settings/session-defaults-settings.png">

### 1.2 Configurar los Valores Predeterminados de Sesión

1. Hacer click en el menú "Configuraciones" en la barra de herramientas. Hacer click en "Predeterminados de Sesión".

    <img class="screenshot" alt="Session Defaults Menu" src="{{docs_base_url}}/assets/img/setup/settings/session-defaults-menu.png">

2. Aparecerá una ventana de "Predeterminados de Sesión". Configurar los valores predeterminados para los campos respectivos y Guardar.

    <img class="screenshot" alt="Session Defaults Prompt" src="{{docs_base_url}}/assets/img/setup/settings/session-defaults-prompt.png">

Luego de guardar, se configurarán los valores predeterminados en todos lados. 

Se puede abrir una nueva Orden de Venta para verificar lo anterior. El campo compañía se encuentra configurado según la Compañía predeterminada. 

<img class="screenshot" alt="Session Defaults Set" src="{{docs_base_url}}/assets/img/setup/settings/session-defaults-set-1.png">

Abrir una nueva Tarea. El campo "Proyecto" se encuentra configurado de acuerdo con el Proyecto predeterminado. 

<img class="screenshot" alt="Session Default Set" src="{{docs_base_url}}/assets/img/setup/settings/session-defaults-set-2.png">

Abrir un informe, por ejemplo, Libro Mayor. El filtro de Compañía está configurado según la Compañía predeterminada. 

<img class="screenshot" alt="Session Default " src="{{docs_base_url}}/assets/img/setup/settings/session-defaults-set-3.png">

## 2. Características

### 2.1 Predeterminados eliminados al cerrar sesión

Los valores predeterminados se configuran para ese usuario en particular y para la sesión en curso. Una vez cerrada la sesión, estos valores predeterminados son eliminados. 

### 2.2 Visibilidad del botón 'Configuraciones'

El botón Configuraciones solo es visible para el Administrador de Sistema o para una persona con permiso para acceder a "Configuraciones Predeterminadas de Sesión". Este botón deriva a las Configuraciones Predeterminadas de Sesión donde se pueden añadir o eliminar tipos de documentos para los cuales se desean configurar Predeterminados de Sesión. 

<img class="screenshot" alt="Session Defaults Prompt" src="{{docs_base_url}}/assets/img/setup/settings/settings-button.png">

### 3. Temas Relacionados
1. [Predeterminados globales](/docs/user/manual/es/setting-up/settings/global-defaults)
1. [Configuración del Sistema](/docs/user/manual/es/setting-up/settings/system-settings)
