<!-- add-breadcrumbs -->
# Grupo de Proveedores
**Un Grupo de Proveedores es un conjunto de proveedores que son similares en algún aspecto.**

Un proveedor puede distinguirse de un contratista o subcontratista, quien por lo general realiza un aporte especializado a los productos. Un proveedor es también conocido como vendedor. Hay distintos tipos de proveedores de acuerdo a los bienes y productos que proveen.

ERPNext permite crear categorías personalizadas de proveedores. Estas categorías son conocidas como Grupos de Proveedores. Por ejemplo, si se cuenta principalmente con empresas farmacéuticas y distribuidores FMCG, se pueden crear nuevos Grupos de Proveedores y nomenclarlos de forma acorde.

Para acceder a Grupos de Proveedores ir a:
> Inicio > Compras > Proveedor > Grupo de Proveedores

## 1. Prerrequisitos
Antes de crear y utilizar un Grupo de Proveedores se recomienda crear lo siguiente: 

* [Proveedor](/docs/user/manual/es/buying/supplier)

## 2. Creación de un Grupo de Proveedores
1. Ir al listado de Grupo de Proveedores y hacer click en Nuevo.
1. Escribir un nombre para el nuevo Grupo de Proveedores.
1. Se puede configurar un Grupo de Proveedores Principal para este Grupo de Proveedores. 
1. Hacer click en la opción Es Grupo lo convertirá en un Grupo de Proveedores Principal.
1. Tambien se puede asignar una Plantilla de Términos de Pago Predeterminados. Esto resulta últil en caso de que, por ejemplo, todos los proveedores de hardware pidan la mitad del pago al generar la Orden de venta y la otra mitad luego del envío. 
1. Guardar.

<img class="screenshot" alt="Supplier Group" src="{{docs_base_url}}/assets/img/buying/supplier-group.png">

Se puede clasificar a los proveedores dentro de un rango de opciones disponibles en ERPNext.
Seleccionar dentro de una serie de opciones como Distribuidor, Electrónico, Hardware, Local, Farmacéutico, Materias Primas, Servicios, etc. Clasificar a los proveedores en diferentes tipologías facilita la contabilidad y los pagos. 

## 3. Árbol de Grupo de Proveedores

También se puede construir un Grupo de Proveedores en forma de jerárquica de Árbol, de forma similar al Plan de Cuentas.

Para ver la estructura de Árbol, hacer click en **Árbol** en la barra lateral. Para volver a la vista de lista seleccionar: **Menú > Vista de Lista**.

<img class="screenshot" alt="Supplier Group" src="{{docs_base_url}}/assets/img/buying/supplier-group-tree.png">

Con los nuevos [Permisos de Usuario](/docs/user/manual/es/setting-up/users-and-permissions) pueden aplicarse permisos basados en jerarquías. 
Esto quiere decir que, si un usuario tiene permitdo ver el nodo principal del Grupo de Proveedores, también puede ver los nodos secundarios de ese nodo principal. 

Por ejemplo, en la imagen mostrada anteriormente, el permiso aplicado para un usuario le permite ver el documento "Distribuidor". Por ende, el usuario también tiene permiso para ver sus nodos secundarios como "Distribuidor de Libros", "Distribuidor Electrónico", etc. 

### 4. Temas Relacionados
1. [Proveedor](/docs/user/manual/es/buying/supplier)
