<!-- add-breadcrumbs -->
# Rol y Perfil de Rol

**Un Rol define los permisos para acceder a varios documentos en ERPNext.**

Los roles definen un conjunto de permisos que pueden configurarse desde [Administrar permisos](/docs/user/manual/en/setting-up/users-and-permissions/role-based-permissions). Los roles más usados ya están definidos en ERPNext y se puede utilizar el sistema con ellos. De ser necesario se pueden añadir más roles. Por ejemplo, si se asigna el rol de Usuario de Ventas a un usuario, tendrán acceso a documentos como Cotizaciones y Órdenes de Venta, ya que los permisos ya están configurados para el rol de Usuario de Venta.

**Los Perfiles de rol almacenan muchos roles, a fin de que puedan asignarse varios roles de una sola vez.**

Los Perfiles de Rol actúan como una plantilla para almacenar y seleccionar muchos roles. Este Perfile de Rol puede luego asignarse a un [Usuario](/docs/user/manual/es/setting-up/users-and-permissions/adding-users). Por ejemplo, un Supervisor de Ventas tendrá los roles de Empleado, Gerente de Ventas, Usuario de Ventas y Gerente principal de Ventas.

Para acceder a Rol ir a:
> Inicio > Usuarios > Usuarios > Rol

## 1. Creación de un Rol
1. Ir al listado de Rol y hacer click en Nuevo.
1. Ingresar un Nombre del rol.
1. Elegir si el Rol tiene acceso de escritorio. Un rol que tiene acceso de escritorio puede acceder a los módulos y documentos de la empresa en ERPNext. El nivel de acceso depende de los roles asignados al Usuario.
1. Guardar.

Se puede añadir una autenticación de dos factores para el rol y también restringirlo a un dominio específico. Desde aquí se puede ir [Administrar Permisos](/docs/user/manual/es/setting-up/users-and-permissions/role-based-permissions) y configurar los permisos para el rol dentro de los distintos DocTypes.

![Permissions for new Role](/docs/assets/img/users-and-permissions/role-permissions.png)

## 2. Creación de un Perfil de Rol

Para acceder a Perfil de Rol ir a:
> Inicio > Usuarios > Usuarios > Perfil de Rol

1. Ir al listado de Perfil de Rol y hacer click en Nuevo.
1. Ingresar un Nombre.
1. Seleccionar los roles que se desea asignar a ese Perfil.
1. Guardar.

    ![Role Profile](/docs/assets/img/users-and-permissions/role-profile.png)

## 3. Temas Relacionados
1. [Permisos Basados en Rol](/docs/user/manual/es/setting-up/users-and-permissions/role-based-permissions)
1. [Permisos de Usuario](/docs/user/manual/es/setting-up/users-and-permissions/user-permissions)
1. [Permisos de Rol Para Página y Reportes](/docs/user/manual/es/setting-up/users-and-permissions/role-permission-for-page-and-report)

