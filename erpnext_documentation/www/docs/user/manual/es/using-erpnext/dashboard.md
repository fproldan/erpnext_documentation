<!-- add-breadcrumbs -->
# Tablero

**El Tablero provee un vistazo rápido de los indicadores de desempeño relevantes para el proceso de negocios.**

Cada Tablero consiste en un o varios Gráficos, cada uno de los cuales está configurado con información proveniente de algo llamado Fuente de Gráficos de Tablero. 

Para acceder al Tablero ir a: 

> Inicio > Personalización > Tableros > Tablero

## 1. Creación de un Tablero

1. Ir al Listado de Tableros y hacer click en Nuevo.
2. Ingresar el Nombre del Módulo para el cuál se desea ver el Tablero.
3. Ingresar los Gráficos de Tablero que se desea parametrizar para este Tablero.
4. Guardar.

Al hacer click en "Mostrar Tablero", se podrá ver el Tablero representando de forma gráfica las transacciones.

<img class="screenshot" alt="Accounting Dashboard" src="{{docs_base_url}}/assets/img/customize/dashboard-0.png">

## 2. Añadir Gráficos al Tablero

Añadir gráficos a este tablero seleccionando "Gráficos de Tablero" existentes o creando nuevos.

<img class="screenshot" alt="Add Chart To Dashboard" src="{{docs_base_url}}/assets/img/customize/dashboard-1.png">

Guardar cambios y hacer click en el botón "Mostrar Tablero" para ver el tablero.

<img class="screenshot" alt="Show Dashboard Button" src="{{docs_base_url}}/assets/img/customize/dashboard-6.png">

## 3. Creación de un Gráfico de Tablero

Para crear un nuevo Gráfico de Tablero ir a: 

> Inicio > Personalizaciones > Tableros > Gráfico de Tablero > Nuevo

Proveer un nombre para el gráfico, esto se mostrará en el tablero como la etiqueta del gráfico, y seleccionar una "Fuente de Gráficos de Tablero" como la fuente de datos para este gráfico. 

**Observación:** Sólo puede crear "Fuentes de Gráficos de Tablero" el Usuario Administrador en Modo Desarrollador. 

<img class="screenshot" alt="Select Dashboard Chart Source" src="{{docs_base_url}}/assets/img/customize/dashboard-2.png">

Luego de configurar el campo Fuente de Gráfico, se mostrará la tabla de filtros.

Hacer click en la tabla para editar los filtros. 

<img class="screenshot" alt="Filters Table" src="{{docs_base_url}}/assets/img/customize/dashboard-3.png">

Se mostrará un modal para configurar los filtros. Hacer click en "Configurar" para configurar los filtros.
<img class="screenshot" alt="Filters Modal" src="{{docs_base_url}}/assets/img/customize/dashboard-4.png">

Luego de configurar el campo Fuente de Gráfico, se actualizará la tabla de Filtros con los valores seleccionados. 
<img class="screenshot" alt="Filters Table With Selected Filter Values" src="{{docs_base_url}}/assets/img/customize/dashboard-5.png">

## 4. Utilización de los Tableros

Cada gráfico se mostrará de acuerdo a los campos configurados en el Gráfico de Tablero correspondiente. El resultado fuente de los gráficos es guardado en la memoria caché para evitar búsquedas redundantes. Como los datos del gráfico pueden ser antiguos, cada gráfico también mostrará la última fecha de sincronización. 

<img class="screenshot" alt="Chart Options" src="{{docs_base_url}}/assets/img/customize/dashboard-7.png">

Los filtros utilizados para generar los datos del gráfico también pueden cambiarse haciendo click en "Configurar Filtros". El gráfico se actualizará automáticamente de acuerdo con los filtros configurados.

<img class="screenshot" alt="Modal For Chart Filters" src="{{docs_base_url}}/assets/img/customize/dashboard-8.png">

Para obtener los datos más recientes, cada gráfico debe ser actualizado haciendo click en el botón **Forzar Actualización** desde el menú desplegable. 

{siguiente}
