<!-- add-breadcrumbs -->
# Permisos Basados en Roles

**Los Permisos a diferentes documentos pueden ser controlados utilizando los Permisos Basados en Roles.**

ERPNext tiene un sistema de permisos basados en roles. Esto significa que se pueden asignar Roles a los Usuarios, y que los Permisos pueden configurarse en los Roles. En Administrar permisos se puede configurar qué roles acceden a qué documentos y con qué permisos (lectura, escritura, envío, etc).

Una vez que los roles son asignados a un usuario, su acceso puede limitarse a documentos específicos. La estructura de permisos permite definir diferentes reglas de permisos para diferentes campos utilizando un concepto llamado **Nivel de Permiso** de un campo. 

## 1. Administrar Permisos
Para empezar a Administrar Permisos ir a:
> Inicio > Usuarios > Permisos > Administrar Permisos

<img alt="Manage Read, Write, Create, Submit, Amend access using the Role Permissions Manager" class="screenshot" src="{{docs_base_url}}/assets/img/users-and-permissions/setting-up-permissions-leave-application.png">

Los permisos son aplicados en una combinación de: 

  * **Roles:** Como se vio anteriormente, a los Usuarios se les asignan Roles y es en base a esos Roles que se aplican las reglas de permisos. Por ejemplo, un usuario de ventas puede tener los roles de Empleado y Usuario de Venta.

  Ejemplos de Roles incluyen Administrador de Cuentas, Empleado, Usuario de RH, etc.

  * **Tipos de Documentos:** Cada tipo de documento o transacción tiene una lista separada de permisos basados en roles, como se puede ver en la captura de pantalla mostrada más arriba. 

  Ejemplos de Tipos de Documentos son Factura de Venta, Pedido de Licencia, Registro de Inventario, etc.

  * **Niveles de Permiso:** En cada documento se puede agrupar a los campos por "niveles". Cada grupo de campos se denota con un número único (del 0 al 9). A cada grupo de campos puede asignarse un conjunto de reglas de permisos por separado. De forma predeterminada, todos los campos son nivel 0. 

    El "Nivel" de permisos conecta los campos con nivel X a una regla de permiso con nivel X. Para saber más, hacer click [aquí](/docs/user/manual/en/setting-up/articles/managing-perm-level).

  * **Etapas de Documento:** Los permisos se aplican en cada etapa del documento como Creación, Guardado, Validación, Cancelación y Edición. Un rol puede tener permitido Imprimir, Enviar por Correo Electrónico, Importar o Exportar datos, acceder a Informes, o definir Permisos de Usuario. 

  * **Permisos de Usuario:** Utilizando los Permisos de Usuario en ERPNext un usuario puede estar restringido para acceder solamente a Documentos específicos para ese Tipo de Documento. Por ejemplo: Para un Territorio, de todos los Territorios. Los Permisos de Usuario definidos para otros Tipos de Documentos también se aplican si están relacionados al Tipo de Documento actual, a través de Campos Vinculados.
  
    Por ejemplo, un Cliente es un campo vinculado en una Orden de Venta o Cotización. En Administrar Permisos, los Permisos de Usuarios pueden configurarse utilizando el botón "Establecer permisos de usuario".

    Para configurar Permisos de Usuario en base a documentos/campos ir a:
    > Inicio > Usuarios > Permisos > [Permisos de Usuario](/docs/user/manual/es/setting-up/users-and-permissions/user-permissions)

  * **Añadir una Nueva Regla**: En Administrar Permisos, para añadir una nueva regla, hacer click en el botón **Añadir una nueva regla** y aparecerá una ventana emergente que pedirá seleccionar un Rol y un Nivel de Permiso. Una vez seleccionado esto, y haciendo click en "Agregar", se añadirá una nueva fila a la tabla de reglas. 

## 2. Permisos Basados en Roles

Un Pedido de Licencia es un buen ejemplo que incluye todas las áreas del Sistema de Permisos. 

* Debería ser creado por un Empleado.
  Para esto, el Rol de Empleado debería tener permisos de Lectura, Escritura y Creación. 

  <img class="screenshot" alt="Giving Read, Write and Create Permissions to Employee for Leave Application"  src="{{docs_base_url}}/assets/img/users-and-permissions/setting-up-permissions-employee-role.png">

* Un **Empleado** solo debería poder acceder a su solicitud de Pedido de Licencia.
  Por ende, deberían crearse registros de Permisos de Usuario para cada combinación de Usuario-Empleado. 

  <img class="screenshot" alt="Limiting access to Leave Applications for a user with Employee Role via User Permissions Manager" src="/docs/assets/img/users-and-permissions/setting-up-permissions-employee-user-permissions.png">
  
* El **Administrador de RH** debería poder ver todos los Pedidos de Licencia. 
  Crear una Regla de Permiso para el Administrador de RH a un Nivel 0, con permisos de Lectura. Aplicar Permisos de Usuarios debería estar deshabilitada.

  <img class="screenshot" alt="Giving Submit and Cancel permissions to HR Manager for Leave Applications. 'Apply User Permissions' is unchecked to give full access." src="{{docs_base_url}}/assets/img/users-and-permissions/setting-up-permissions-hr-manager-role.png">

* El **Aprobador de Licencias** debería poder ver y actualizar los Pedidos de Licencia de empleados bajo su supervisión.
  El Aprobador de Licencias recibirá acceso de Lectura y Escritura a un Nivel 0. Los Documentos Relevantes de Empleados deberían estar enlistados en los Permisos de Usuario de los Aprobadores de Licencias. Este esfuerzo se reduce para Aprobadores de Licencias que estén mencionados en los Documentos de Empleados, al crear mediante programación los registros de Permisos de Usuario. 

  <img class="screenshot" alt="Giving Read, Write and Submit permissions to Leave Approver for Leave Applications.'Apply User Permissions' is checked to limit access based on Employee." src="{{docs_base_url}}/assets/img/users-and-permissions/setting-up-permissions-leave-approver-role.png">

* Debería ser Aprobada/Rechazada sólo por el Usuario de RH o Aprobador de Licencias. 
  El campo Estado de un Pedido de Licencia se configura a un Nivel 1. El usuario de RH y el Aprobador de Licencias tienen permisos de Lectura y Escritura de Nivel 0, mientras todos los demás reciben permisos de Lectura Nivel 1. 

  <img class="screenshot" alt="Limiting read access for a set of fields to certain Roles" src="/docs/assets/img/users-and-permissions/setting-up-permissions-level-1.png">

* El **Usuario de RH** debería poder delegar los Pedidos de Licencia a sus subordinados/as. 
  El Usuario de RH por lo general tiene derecho a Configurar Permisos de Usuarios. Un Usuario con el rol RH debería poder definir Permisos de Usuarios respecto a Pedidos de Licencia para otros usuarios.

  <img class="screenshot" alt="Let HR User delegate access to Leave Applications by checking 'Set User Permissions'. This will allow HR User to access User Permissions Manager for 'Leave Application'" src="{{docs_base_url}}/assets/img/users-and-permissions/setting-up-permissions-hr-user-role.png">

En caso de que se hayan asignado los roles correctamente pero se sigan recibiendo errores al acceder a los documentos, ir a [esta página](/docs/user/manual/es/setting-up/articles/report-permission-error).

## 3. Temas Relacionados
1. [Permisos Basados en Roles](/docs/user/manual/es/setting-up/users-and-permissions/role-based-permissions)
1. [Permisos de Usuario](/docs/user/manual/es/setting-up/users-and-permissions/user-permissions)
1. [Permisos de Rol Para Página y Reportes](/docs/user/manual/es/setting-up/users-and-permissions/role-permission-for-page-and-report)

