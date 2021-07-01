<!-- add-breadcrumbs -->
# Administrar Documentos con Estructura de Árbol 

Algunos de los documentos en ERPNext utilizan una estructura de árbol. Las funciones con estructura de árbol permiten configurar una función Principal y funciones Secundarias dentro de esas principales. Configurar esta estructura permite crear informes inteligentes y seguir el rastro del crecimiento a cada nivel en la jerarquía.  

A continuación está la lista parcial de documentos que poseen estructuras de árbol. 

* Plan de Cuentas
* Lista de Centros de Costo
* Grupo de Clientes
* Territorio
* Vendedor
* Grupo de Productos

A continuación están los pasos para administrar y crear registros en estructuras de árbol. Considérese el Territorio para entender la administración de documentos con estructura de árbol. 

#### Paso 1 : Ir al documento

`Comercialización > Configuraciones > Territorio`

#### Paso 2 : Territorio Principal

<img alt="Default Territories" class="screenshot" src="{{docs_base_url}}/assets/img/articles/territory-2.png">

Al hacer click en Territorio Principal, se verá la opción de añadir un territorio secundario dentro del mismo. Todos los grupos de Territorio predeterminados se encontrarán enlistados dentro del grupo Principal "Todos los Territorios". Se pueden añadir más Grupos Principales o Secundarios dentro del mismo. 

#### Paso 3: Añadir nuevo Territorio

Al hacer click en Añadir Secundario, una ventana de diálogo proveerá dos campos.

**Nombre del Grupo de Territorio**

El Territorio se guardará con el Nombre de Territorio ingresado aquí.

**Nodo de Grupo**

Si el campo Nodo de Grupo está configurado como Si, entonces este territorio será creado como Principal, lo cual significa que se podrán crear sub territorios dentro del mismo. Si se selecciona No, entonces será un Territorio secundario que podrá ser seleccionado en otros documentos. 

<div class="well">Solo los Grupos de Territorios secundarios pueden seleccionarse en otras funciones y transacciones.</div>

<img alt="Default Territories" class="screenshot" src="{{docs_base_url}}/assets/img/articles/territory-1.gif">

A continuación se puede ver cómo se verán enlistados los Territorios Secundarios dentro de un Territorio Principal. 

<img alt="Adding new Territories" class="screenshot" src="{{docs_base_url}}/assets/img/articles/territory-3.png">

Siguiendo estos pasos, también se podrán administrar otros documentos con estructura de árbol en ERPNext.

<!-- markdown -->