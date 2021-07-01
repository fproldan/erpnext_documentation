<!-- add-breadcrumbs -->
# Administrar Niveles de Permisos 

El Nivel de Permiso es una forma de reducir la cantidad de información visible o editable en un DocType específico para ciertos Grupos de Usuarios. Aunque se puede definir la visibilidad o editabilidad para cada DocType, personalizando la Pauta de Permisos del DocType. Con el Nivel de Permisos se puede cambiar esto para Secciones o Campos específicos. 

En cada documento se puede agrupar a los campos por "niveles". Cada grupo de campos es identificado con un número único (0, 1, 2, 3 etc.). Puede aplicarse un conjunto distinto de pautas de permisos a cada grupo de campos. De forma predeterminada, todos los campos son nivel 0.

El Nivel de Permisos para un campo puede definirse en [Personalizar Formulario](/docs/user/manual/en/customize-erpnext/customize-form).

<img alt="Perm Level Field" class="screenshot" src="{{docs_base_url}}/assets/img/articles/perm-level-1.gif">

Si se necesita asignar diferentes permisos de un campo en particular a diferentes usuarios, esto puede hacerse a través del Nivel de Permisos. Ejemplo:

Una Nota de Entrega es accesible tanto para el Gerente de almacén como para el Usuario de almacén. No se desea que el Usuario de almacén acceda al campo relacionado al Monto en la Nota de Entrega, pero otros campos deberían ser visibles como lo son para el Gerente de almacén. 

Para todos los campos relacionados que no deberían ser visibles, se puede configurar el Nivel de Permiso en 2. 

Los Gerentes de almacén tendrán permiso para campos de la Nota de Entrega con Nivel de Permiso 2, mientras que los Usuarios de almacén no tendrán ningún permiso en Nivel de Permiso 2 para la Nota de Entrega porque su rol no ha sido asignado con una pauta que les permita leer o escribir en Campos con Nivel de Permiso 2, como se muestra a continuación.

<img alt="Perm Level Rule" class="screenshot" src="{{docs_base_url}}/assets/img/articles/perm-level-2.png">

Considerando la misma situación, si se desea que un Usuario de almacén acceda a un campo con Nivel de Permiso 2, pero no se le quiere dar permiso para que edite, el Usuario de almacén recibirá un permiso de solo lectura en Nivel de Permiso 2, es decir que no podrá escribir/editar. 

<img alt="Perm Level Rule 2" class="screenshot" src="{{docs_base_url}}/assets/img/articles/perm-level-3.png">

Los Niveles de Permiso (1, 2, 3 o 2, 1, 3 o 3, 2, 1) no necesariamente tienen que estar en un orden en particular. No implican jerarquía, El Nivel de Permiso es usado principalmente para agrupar un determinado número de campos, y luego asignar permisos a Roles para ese grupo. De esa forma, se puede configurar cualquier nivel de permiso para un ítem, y luego realizar la configuración de permisos para el mismo.

Si se quieren cambiar los permisos para todos los campos en una sección, se puede cambiar el nivel de permiso para el campo sección y esto se aplicará para todos los campos en la sección. 

<!-- markdown -->
