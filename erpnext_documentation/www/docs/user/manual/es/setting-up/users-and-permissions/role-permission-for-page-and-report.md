<!-- add-breadcrumbs -->
# Permisos de Rol Para Página y Reporte

**El acceso a diferentes páginas y reportes puede ser controlado en Permisos de Rol Para Páginas y Reporte.**

Los tipos de Documento son Orden de Venta, Cliente, Proveedor, etc. Que sean **tipos de documento** significa que contienen muchos documentos de ese tipo. Una Página es una sola página como [Configuraciones de Venta](/docs/user/manual/es/selling/selling-settings). No se pueden crear muchas Configuraciones de Venta, pero sí se pueden crear muchas Ordenes de Venta. 

En ERPNext, los usuarios pueden crear una interfaz de usuario personalizada utilizando Página, y un informe personalizado a través del [Generador de Reportes](/docs/user/videos/learn/report-builder.html) o [Informe de Consulta](https://frappe.io/docs/user/en/guides/reports-and-printing/how-to-make-query-report). ERPNext tiene un sistema de [permisos basados en roles](/docs/user/manual/es/setting-up/users-and-permissions/role-based-permissions) donde se pueden asignar roles a usuarios. El mismo rol puede asignarse a la página y al reporte para acceder a ellos. 

Si se quieren restringir los roles que pueden acceder a ciertas páginas y reportes en ERPNext, esto puede hacerse a través de Permiso de rol para Página y Reporte.

Para acceder a Permiso de rol para Página y Reporte, ir a:
> Inicio > Usuarios > Permisos > Permiso de rol para Página y Reporte

## 1. Utilización de la herramienta Permiso de rol para Página y Reporte

Un usuario puede asignar los roles para la página y reportes utilizando "Permiso de rol para Página y Reporte".

<img alt="Tools to assign custom roles to the page" class="screenshot" src="{{docs_base_url}}/assets/img/users-and-permissions/role-permission-for-page-and-report.png">

### 1.1 Restablecer Predeterminados

Utilizando el botón "Restablecer Predeterminados", el usuario puede eliminar los permisos personalizados aplicados en una página o reporte. De esta forma, se aplicarán los permisos predeterminados a esa página o reporte.

<img alt="Reset the default roles" class="screenshot" src="{{docs_base_url}}/assets/img/users-and-permissions/reset-roles-permission-for-page-report.png">

## 2. Temas Relacionados
1. [Rol y Perfil de Rol](/docs/user/manual/es/setting-up/users-and-permissions/role-and-role-profile)
1. [Permisos Basados en Roles](/docs/user/manual/es/setting-up/users-and-permissions/role-based-permissions)
1. [Permisos de Usuario](/docs/user/manual/es/setting-up/users-and-permissions/user-permissions)
