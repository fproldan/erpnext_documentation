<!-- add-breadcrumbs -->
# Permisos de Usuario

**Los permisos de Usuario son una forma de restringir el acceso de los usuarios a documentos en particular.**

Los permisos basados en Roles permiten configurar acceso completo (de forma predeterminada) a un tipo de documento (doctype) como Factura de Venta, Ordenes, Cotizaciones, etc. Esto significa que cuando se asigna a un usuario el rol de Usuario de Venta, el mismo podrá acceder a todas las Ordenes de Venta y Cotizaciones. 

Los Permisos de Usuario pueden utilizarse para restringir el acceso a documentos seleccionados de acuerdo con los campos vinculados en el documento. Por ejemplo, considerando que se hacen negocios con muchos territorios y se quiere restringir el acceso de ciertos Usuarios de Venta a Cotizaciones/Ordenes de Venta pertenecientes a un territorio en particular. Esto puede hacerse a través de Permisos de Usuario. Estas restricciones pueden configurarse sobre Cliente, Proveedor, Grupo de Clientes, Grupo de Proveedores, etc. 

Configurar Permisos de Usuario resulta particularmente útil cuando se quiere restringir en base a: 

1. Permitir a un usuario el acceso a datos pertenecientes a una Compañía 
2. Permitir a un usuario acceder a datos relacionados a un Cliente o Territorio específico

Para acceder a los Permisos de Usuario ir a:
> Inicio > Usuarios > Permisos > Permisos de Usuario


## 1. Creación de Permisos de Usuario

1. Ir al listado de Permisos de Usuario y hacer click en Nuevo.
1. Seleccionar el Usuario para el cual se aplicará la regla.
2. Seleccionar el tipo de documento que será permitido (por ejemplo "Compañía").
3. En el campo Para valor, seleccionar el item específico que se quiere permitir (el nombre de la Compañía). 
4. Si se hace click en la casilla "Es predeterminado", el valor seleccionado en el campo "Para valor" será utilizado como predeterminado para todas las transacciones futuras por este usuario. Es decir, si la empresa "Unico Plastics In." se selecciona como "Para valor", esta Compañía se configurará como predeterminada para todas las transacciones futuras por este usuario.  

    <img src="{{docs_base_url}}/assets/img/users-and-permissions/user-perms/new-user-permission.png" class="screenshot" alt="Creating a new user permission">

    > Observación: Sólo puede configurarse un solo permiso de usuario como predeterminado, para un tipo de documento en particular, para un usuario específico.

## 2. Más acciones de Permisos de Usuario
### 2.1 Control Avanzado

### 2.1.1. Aplicable para

De forma opcional, se pueden aplicar permisos de usuario sólo para tipos de documento específicos seleccionando el deseado en el campo "Aplicable para" luego de deshabilitar la opción "Aplicar a todos los tipos de documentos".

<img src="{{docs_base_url}}/assets/img/users-and-permissions/user-perms/advanced-control.png" class="screenshot" alt="Applicable For">

En el Permiso de Usuario mostrado más arriba, el usuario podrá acceder sólo a Ordenes de Venta de la Compañía seleccionada. 

**Observación:** Si **Aplicable Para** no está configurado, el Permiso de Usuario se aplicará en todos los tipos de documento relacionados. 

### 2.1.2. Ocultar descendientes

El valor de **Permitir** podría ser un documento con una vista de árbol, por lo que tendrá registros hijos/descendientes.

Asumiendo que la Compañía definir en **Para valor** tiene una Compañía hija "Unico Toys", cuando se crea un Permiso de usuario para la Compañía padre, también se conceden dichos permisos para la Compañía hija.

Esta opción solo aparece si se selecciona un documento con vista de árbol. Al tildar esta opción no se concederán los permisos a los descendientes.

<img src="{{docs_base_url}}/assets/img/users-and-permissions/user-perms/hide-descendant-permissions.png" class="screenshot" alt="Hide Descendant Permissions">

### 2.2 Ignorar Permisos de Usuario en Ciertos Campos 

Otra forma de permitir que los documentos que han sido restringidos por Permisos de Usuario sean vistos por todos, es hacer click en la casilla "Ignorar Permisos de Usuario" en un campo en particular yendo a **Personalizar Formulario**.

Por ejemplo, si se desea que Activos no esté restringido para ningún usuario, entonces seleccionar **Activo** en tipo de formulario. En la tabla de campos, expandir el de Compañía y hacer click en "Ignorar Permisos de Usuario". 

<img src="{{docs_base_url}}/assets/img/users-and-permissions/user-perms/ignore-user-permissions.png" class="screenshot" alt="Ignore User Permissions on specific properties">


### 2.3 Permisos Estrictos

Esto restringe el acceso de los usuarios a un documento en una forma más estricta.

Para saber más ir a la página de [Configuración del Sistema](/docs/user/manual/es/setting-up/settings/system-settings#14-permissions).

### 2.4 Aplicación de Permisos de Usuario

Finalmente, una vez que se ha creado el permiso y se quiere ver como se aplica a distintos usuarios, se puede ingresar a **Documentos permitidos a los usuarios**. Mediante este informe se puede seleccionar el **Usuario** y tipo de documento, y ver a qué documentos puede acceder. 

Haciendo click en la opción de Mostrar Permisos, se verán los permisos de lectura/escritura/envío y otros niveles de acceso.

<img src="{{docs_base_url}}/assets/img/users-and-permissions/user-perms/permitted-documents.png" class="screenshot" alt="Permitted Documents for User report">

Observación: Si no se puede acceder a Orden de Venta o cualquier otro tipo de documento en esta lista, asegurarse que se han establecido correctamente los [roles](/docs/user/manual/es/setting-up/users-and-permissions/role-based-permissions).

Por ejemplo, el Usuario Bruce está restringido para la Compañía Unico Plastics Inc.
![User restricted to Company](/docs/assets/img/users-and-permissions/user-perms/user-restricted-to-company.png)

## 3. Temas Relacionados
1. [Añadir Usuarios](/docs/user/manual/es/setting-up/users-and-permissions/adding-users)
1. [Rol y Perfil de Rol](/docs/user/manual/es/setting-up/users-and-permissions/role-and-role-profile)
1. [Permisos Basados en Roles](/docs/user/manual/es/setting-up/users-and-permissions/role-based-permissions)
1. [Permisos de Roles para Página y Reportes](/docs/user/manual/es/setting-up/users-and-permissions/role-permission-for-page-and-report)
