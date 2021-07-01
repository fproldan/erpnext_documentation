<!-- add-breadcrumbs -->
# Añadir Usuarios

Los Usuarios pueden ser añadidos por el Administrador del Sistema. Para agregar usuarios ir a:
> Inicio > Usuarios > Usuarios > Usuario

Hay dos tipos principales de Usuarios:

**Usuarios del Sitio Web**: Clientes, Proveedores, Estudiantes, etc., que sólo tienen acceso al portal y no a los módulos.
**Usuarios del Sistema**: Personas que usan ERPNext en la Empresa con acceso a módulos, datos de la empresa, etc.

Para saber más respecto a estos dos tipos de usuarios, hacer click [aquí](/docs/user/manual/es/setting-up/articles/difference-between-system-user-and-website-user).

En cada Usuario puede ingresarse mucha información. Para fines de utilización, la información ingresada para usuarios de sitio web es mínima: Nombre y Correo Electrónico. 

Una Dirección de Correo Electrónico es la clave única (ID) para identificar a los Usuarios.

## 1. Creación de un Usuario

1. Ir al listado de Usuarios y hacer click en Nuevo.
1. Añadir la dirección de Correo Electrónico y el nombre del usuario.
1. Guardar.

    <img class="screenshot" src="{{docs_base_url}}/assets/img/users-and-permissions/add-user-details.png" alt="Add User Details">

Detalles como Nombre de Usuario e Idioma también pueden cambiarse.

## 2. Características

### 2.1 Roles

Luego de guardar, se verá un listado de roles y casillas de verificación a su lado. Hacer click en los roles que se desea asignar al usuario y guardar el documento. Los roles tienen permisos predefinidos, para saber más al respecto, hacer click [aquí](/docs/user/manual/es/setting-up/users-and-permissions/role-based-permissions). Se pueden configurar [Perfiles de Roles](/docs/user/manual/es/setting-up/users-and-permissions/role-and-role-profile) para utilizar como una plantilla que seleccione muchos roles juntos. 

<img class="screenshot" src="{{docs_base_url}}/assets/img/setup/users/user-2.png" alt="User Roles">

### 2.2 Más Información
En esta sección puede ingresarse más información del usuario: 

* Género
* Teléfono
* Teléfono Celular
* Fecha de Nacimiento
* Ubicación
* Intereses
* Biografía
* Imagen

Hacer click en "Silenciar sonidos" desactivará los sonidos que se reproducen al interactuar con los documentos. El usuario puede necesitar hacer click en Menú > Actualizar para que se realicen los cambios.

### 2.3 Cambiar Contraseña

* **Establecer nueva contraseña**: Como Administrador de Sistema, se puede configurar una nueva contraseña para el usuario, si la anterior debía ser cambiada. 
* **Cerrar sesión en todos los dispositivos después de cambiar la contraseña**: Al cambiar la contraseña del usuario, se cerrará su sesión en la computadora o cualquier otro dispositivo móvil en el que estuviera conectado.

### 2.4 Seguir Documento

Tildando la opción "Enviar notificaciones de documentos seguidos por mí" se puede recibir notificaciones a través de correo electrónico cuando los mismos son actualizados. Más información [aquí](/docs/user/manual/es/setting-up/email/document-follow). También se puede definir la Frecuencia con la cual se reciben estas notificaciones.

### 2.5 Correo Electrónico

* **Enviar notificaciones para hilos de correo electrónico**: El usuario recibirá notificaciones para conversaciones vía Correo Electrónico que sucedan en tipos de documento como Oportunidades. 
* **Enviarme una copia de los correos electrónicos salientes**: Envía al usuario una copia de los correos electrónicos que envía. Esto resulta útil para saber si el correo original fue enviado.
* **Permitir menciones**: Permitir que el nombre de este usuario aparezca en hilos de conversaciones para que pueda ser mencionado utilizando '@'.
* **Firma de correo electrónico**: la firma de correo electrónico ingresada aquí será la predeterminada para todos los correoes electrónicos salientes del usuario. Esto es diferente al pie de página, el cual es configurado desde la [Compañía](/docs/user/manual/es/setting-up/company-setup).
* **Correos electrónicos del Usuario**: en esta tabla se puede suscribir al usuario a diferentes listas de correo electrónico de la empresa. Añadir una nueva fila y seleccionar la lista de correo electrónico que se quiere asignar al usuario. Por ejemplo, las listas de mails pueden ser trabajos, asistencia, ventas, etc. Para saber más respecto a Cuentas de correo electrónico, hacer click [aquí](/docs/user/manual/es/setting-up/email/email-inbox).

### 2.6 Permitir Acceso a Módulos

Los usuarios tendrán acceso a todos los módulos para los cuáles tienen acceso de acuerdo con su rol. Si se desea restringir el acceso a ciertos módulos para este usuario, destildar los módulos desde este listado. 

<img class="screenshot" src="{{docs_base_url}}/assets/img/setup/users/user-3.png" alt="User Block Module">

### 2.6.1 Perfil de módulo

Los perfiles de módulo actúan como una plantilla para determinar los módulos a los que se puede acceder. Se puede asignar uno de estos perfiles a cada usuario. Por ejemplo, un usuario de Recursos Humanos tendrá acceso al menos a los módulos de Recursos Humanos y Nóminas.

<img class="screenshot" src="{{docs_base_url}}/assets/img/setup/users/module-profile.png" alt="Module Profile">


### 2.7 Configuración de Seguridad

* **Sesiones simultáneas**: cantidad de inicios de sesión simultáneos a los que el usuario está habilitado. Se puede utilizar el mismo conjunto de credenciales para muchos usuarios permitiendo más sesiones. Esto puede restringirse globalmente desde [Configuración del Sistema](/docs/user/manual/es/setting-up/settings/system-settings#15-security). Para cuentas en la nube, el número total de sesiones en simultáneo no puede exceder el número total de usuarios suscriptos.
* **Tipo de Usuario**: Si el usuario tiene algún rol seleccionado que no sea Cliente, Proveedor, Paciente o Estudiante, automáticamente se convierte en Usuario de Sistema. Este campo es de solo lectura.
* **Iniciar sesión después de, Iniciar sesión antes de**: Especificar aquí si se desea dar acceso al sistema al usuario solo en horario de oficina, o durante los fines de semana. Por ejemplo, si los horarios de oficina son de 10 am a 6 pm, configurar "Iniciar sesión después de" para las 10:00 y el "Iniciar sesión antes de" para las 18:00. 
* **Restringir IP**: Restringir el inicio de sesión del usuario desde las IPs especificadas aquí. Esto puede utilizarse para que el usuario solo inicie sesión en las computadoras de la oficina. Pueden añadirse muchas IPs separadas por comas.

Esta sección también muestra otros detalles del usuario como Último Inicio de Sesión, Última IP y Última vez activo.

### 2.8 Autenticación de Tercero

Esto permitirá a los usuarios utilizar Facebook, Google, o GitHub para iniciar sesión. Para utilizar esta función, registrarse con una cuenta de programador en cualquiera de estas plataformas. Crear una aplicación en su consola, especificar el nombre de la aplicación, la URL de origen y la URL de finalización, copiar aquí el ID del cliente y la información secreta del cliente para comenzar a usarla. 

Para más detalles ir a [esta página](https://frappe.io/docs/user/en/guides/deployment/how-to-enable-social-logins).

### 2.9 Acceso API

Se pueden generar Claves secretas de API desde esta sección, utilizando el botón Generar Claves. Estas pueden utilizarse para acceder a los datos de la cuenta desde otra aplicación, por ejemplo un sistema POS fuera de línea.

### 2.10 Luego de Guardar

Luego de guardar un usuario, se verán estos botones en el tablero del mismo. 

![User dashboard buttons](/docs/assets/img/setup/users/user-after-save.png)

#### Permisos

* **Establecer permisos de usuario**: Esto llevará a la página de [Permisos de Usuario](/docs/user/manual/en/setting-up/users-and-permissions/user-permissions) de Bruce, desde donde se puede restringir el acceso de Bruce a documentos.
* **Ver Documentos Permitidos**: Esto llevará al informe 'Documentos Permitidos para el Usuario' para este usuario. Aquí se podrá ver a qué documentos accede Bruce. Por ejemplo, al seleccionar Orden de Venta, se verá la lista de Órdenes de Venta a las cuáles Bruce tiene acceso. 

#### Contraseña

* **Restablecer contraseña**: Se enviará al usuario un correo electrónico con instrucciones para cambiar la contraseña a su [Cuenta de Correo electrónico](/docs/user/manual/es/setting-up/email/email-account).
* **Restablecer clave secreta de OTP**: Restablecer clave para iniciar sesión a través de la Autenticación de Dos Factores.

### Crear correo electrónico de usuario

Hacer click en este botón permitirá crear una [Cuenta de Correo electrónico](/docs/user/manual/es/setting-up/email/email-account) para el usuario en base al correo ingresado.

### 3. Métodos de Inicio de Sesión

En Configuración del Sistema, dentro de la sección Seguridad, al hacer click en la opción "Permitir inicio de sesión con número de teléfono móvil" se podrá utilizar ese dato para iniciar sesión. Si bien, el Número de Teléfono Celular deberá ser único, el mismo no será tratado como un ID para el usuario. 

Iniciar sesión con correo electrónico:

<img class="screenshot" src="{{docs_base_url}}/assets/img/setup/users/user-login-email.png" alt="Email Login">

Iniciar sesión con correo electrónico o teléfono celular:

<img class="screenshot" src="{{docs_base_url}}/assets/img/setup/users/user-login-mobile.png" alt="Mobile No Login">

Luego de añadir estos detalles, guardar el Usuario.

### 4. Temas Relacionados
1. [Permisos Basados en el Rol](/docs/user/manual/es/setting-up/users-and-permissions/role-based-permissions)
1. [Permisos de Usuario](/docs/user/manual/es/setting-up/users-and-permissions/user-permissions)
1. [Seguimiento de Documentos](/docs/user/manual/es/setting-up/email/document-follow)
