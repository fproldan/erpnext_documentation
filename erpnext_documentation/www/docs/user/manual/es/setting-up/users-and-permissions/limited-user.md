<!-- add-breadcrumbs -->
# Usuario con acceso limitado

Los usuarios con acceso limitado verán solo documentos específicos de ciertos módulos.
Algunos usuarios no usan todos los módulos y requieren sólo algunos específicos. Por ejemplo, para registrar las asistencias diarias o solicitud de licencias, cada empleado debe ingresar al sistema. Pero, puede que haya 500 personas trabajando en la Compañía, de los cuales solo 100 usan todos los documentos y los 400 restantes solo necesitan acceder al registro de asistencia y solicitud de licencia.
El Tipo de usuario tiene un rol importante en el manejo de estos casos. Existen varios tipos de usuario como "Usuario de sistema" y "Usuario del sitio web". El usuario de sistema puede acceder tanto al escritorio como al portal web, mientras que el usuario de sitio web accede solo al portal. Para gestionar el caso de acceso limitado a documentos para empleados existe el tipo de usuario "Autogestión de empleado".

## Tipo de usuario

Para acceder a Tipo de usuario ir a:

> Usuarios > Tipo de usuario

<img class="screenshot" alt="User Type" src="{{docs_base_url}}/assets/img/users-and-permissions/user-type.png">

Usuario de sitio web y usuario de sistema son Tipos de usuario estándar y no pueden ser modificados o eliminados. Sin embargo, tipos de usuario personalizados pueden ser creados, editados y eliminados. Por defecto ningún usuario posee permiso de eliminarlos.

## Tipos de usuario personalizados

1) Para este tipo de usuario se debe seleccionar el Rol personalizado, documento sobre el cual se aplicarán los permisos, y el identificador del usuario.

<img class="screenshot" alt="User Type" src="{{docs_base_url}}/assets/img/users-and-permissions/user-type-role.png">

En la imagen se ve que el Empleado está vinculado al Usuario. Como en el campo "Aplicar permiso de usuario sobre" se seleccionó Empleado, el usuario del empleado solo puede ver los documentos en los que se vinculó el empleado. Por ejemplo, el usuario solo puede ver la nómina salarial creada para su empleado.

2) Tipos de documento:

El tipo de usuario personalizado solo puede acceder a los documentos mencionados en el tipo de usuario.

<img class="screenshot" alt="User Type" src="{{docs_base_url}}/assets/img/users-and-permissions/user-type-document-type.png">

Esta tabla también permite definir los permisos que el tipo de usuario tendrá sobre cada documento, similar a la función Administrar permisos. El tipo de usuario no será accesible como un rol en Administrar permisos.

3) Tipos de documento (selección de permisos):

En esta tabla se necesita listar todos los documentos que se desea que el tipo de usuario personalizado pueda seleccionar. No hay límite en el número de documentos que se pueden elegir. Los usuarios no podrán crear registros de documentos para los cuales tienen permiso de seleccionar.

<img class="screenshot" alt="User Type" src="{{docs_base_url}}/assets/img/users-and-permissions/user-type-select-perm.png">

## Agregar usuario personalizado

Al agregar un nuevo usuario se debe elegir el tipo de usuario. Para usuarios con tipo personalizado, el respectivo usuario debe estar vinculado al documento definido en el campo "Aplicar permiso de usuario sobre".


<img class="screenshot" alt="User Type" src="{{docs_base_url}}/assets/img/users-and-permissions/limited-access-user.png">
