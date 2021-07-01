<!-- add-breadcrumbs -->
# Configuración del Sistema

**Desde Configuración del Sistema se definen aspectos generales de la cuenta de ERPNext.**

Se puede configurar para que el sistema utilice una zona horaria en particular, fecha, número o formato de moneda, así como también la expiración de sesión.

Para abrir la Configuración del Sistema ir a:

> Inicio > Configuraciones > Configuración del Sistema

<img class="screenshot" alt="System Settings" src="{{docs_base_url}}/assets/img/setup/settings/system-settings.png">


## 1. Secciones en Configuración del Sistema

### 1.1 General

* **País**: Se puede configurar el país predeterminado aquí, este dato será usado al crear nuevas direcciones. Si la compañía tiene muchas sucursales en distintos países, se puede elegir la ubicación de la casa central.
* **Zona Horaria**: Configura la hora de forma automática de acuerdo con la zona horaria.
* **Idioma**: Configura el idioma general para la cuenta ERPNext. De esta forma, el idioma se cambiará en todos los menús, transacciones, documentos, etc.

### 1.2 Formato de Fecha y Número

* **Formato de Fecha**: Formato en el cual se mostrarán las fechas. Por ejemplo, dd.mm.aaaa o mm/dd/aaaa. Esto depende de cómo se formateen las fechas en la región. 
* **Formato de Hora**: Formato en el cual se mostrará la hora. Se puede elegir mostrar (`HH:mm:ss`) u ocultar segundos configurando la opción como (`HH:mm`).
* **Formato Numérico**: Formato en el cual se mostrarán los números. Por ejemplo: 1.000 o 1000.00
* **Precisión de Decimales**: El número de ceros mostrados luego del punto decimal para las cantidades y demás. El rango está entre 2-9. El predeterminado es 3.
* **Precisión de Moneda**: Numero de ceros mostrados luego del punto decimal para valores de moneda. Si se deja en blanco, se basará en el **Formato Numérico**.

### 1.3 Copias de seguridad

En ERPNext se pueden realizar copias de seguridad tanto de las bases de datos como de los archivos. Las copias de seguridad de las bases de datos se crean de forma automática, mientras que las de archivos deben ser explícitamente descargadas.

En este campo se define el número de copias luego de las cuales se eliminarán las más viejas. De forma predeterminada, se guardan 3 copias cada 24 horas. Las nuevas copias se crean de forma automática cada pocas horas y la nueva eliminará la vieja. Para realizar copias de seguridad de archivos, hacer click en el botón "Descargar copia de seguridad de archivos" de Descargar Copia de Seguridad.

Realizar copias de seguridad en el sistema de forma regular es una buena práctica en caso de que ocurra algún problema y se quiera volver al estado anterior, o simplemente para mantener registros. 

### 1.4 Permisos

Al utilizar permisos se puede limitar el acceso de los usuarios a tipos de documentos. La limitación puede basarse en campos como Compañía, Territorio, Sucursal, etc. Para saber más respecto a Permisos de Usuarios hacer click [aquí](/docs/user/manual/es/setting-up/users-and-permissions/user-permissions).

Si está tildada la opción "Aplicar Permisos Estrictos de Usuario" y los Permisos de Usuarios se definen para un DocType respecto a un Usuario, entonces todos los documentos en los que el valor del enlace esté en **blanco**, no serán mostrados a ese Usuario. 

Esto se puede hacer desde
> Inicio > Usuarios > Permisos > Permisos de Usuario

Por ejemplo: Si se configuran los Permisos de Usuario por Territorio y se configura el valor como Argentina. Si la opción no está tildada, todas las transacciones (Ordenes de venta, Cotizaciones, etc) con Argentina y **blanco** serán mostradas a los usuarios.

Si la opción "Aplicar Permisos Estrictos de Usuario" está tildada, los documentos donde el Territorio esté en blanco no serán mostrados a los usuarios. 

### 1.5 Seguridad

* **Expiración de sesión**: Número de horas de inactividad luego de las cuales se cerrará la sesión. Esto brinda una mayor seguridad. Por ejemplo, si no hay actividad por 6 horas, la sesión se cerrará. 
* **Expiración de sesión en dispositivo móvil**: Expiración de sesión cuando se ha ingresado desde un teléfono móvil. 
* **Permitir sólo una sesión por usuario**: Si se desea usar un solo conjunto de credenciales para muchos usuarios, se debe tildar esta opción. El número de sesiones en simultáneo puede cambiarse por cada Usuario. Las sesiones en dispositivos móviles no se cuentan aquí. 
* **Permitir inicio de sesión con número de teléfono móvil**: Al tildar esta opción se puede iniciar sesión en ERPNext utilizando un número de teléfono celular válido, configurado en la cuenta de Usuario.
* **Permitir inicio de sesión con Nombre de Usuario**: Permitir el inicio de sesión a través del nombre de usuario configurado en el [Usuario](/docs/user/manual/es/setting-up/users-and-permissions/adding-users).
* **Mostrar el error completo y permitir reportarlos al desarrollador**: Esto mostrará todo el error en la pantalla y permitirá informar al respecto. Si se posee conocimiento técnico en este área, se podrá entender mejor el error leyendo el mensaje completo.
* **Quitar etiquetas EXIF de las imágenes**: Metadata de archivos de imagen almacenada en formato EXIF puede ser aprovechada para obtener información privada del usuario. Esta opción permite a los usuarios eliminar este tipo de datos de las imágenes antes de almacenarlas en el sistema.

### 1.6 Contraseña

* **Forzar al usuario a restablecer la contraseña**: Número de días luego de los cuales será obligatorio cambiar la contraseña. 0 significa sin límite. 
* **Activar política de contraseñas**: Habilita un verificador de fortaleza, de forma que los usuarios deban utilizar contraseñas fuertes para su inicio de sesión. 
* **Puntuación mínima de contraseña**: Puntaje para el verificador de fortaleza de las contraseñas.
    * 2 es media
    * 3 es fuerte
    * 4 es muy fuerte

    La complejidad se basa en el número de caracteres, letras mayúsculas, caracteres  especiales, etc. 
* **Límite de Generación de Vínculos para Cambiar la Contraseña**: Este campo permite limitar el número de pedidos de cambio de contraseña por hora, la configuración predeterminada es 3. Si se lo configura en 0 se permitirá un número ilimitado de pedidos de generación de vínculos para cambio de contraseña. 

### 1.7 Seguridad por Fuerza Bruta

* **Permitir intentos de inicio de sesión consecutivos**: cantidad de intentos luego de los cuales se bloqueará la cuenta por un período de tiempo específico. Esto ayuda si algún intruso intenta ingresar en la cuenta.
* **Permitir inicio de sesión después de error**: cantidad de segundos luego de los cuales se permitirá un inicio de sesión luego de intentos consecutivos fallidos.

### 1.8 Autenticación de Dos Factores

Las configuraciones para la Autenticación de Dos Factores pueden realizarse aquí.

Al hacer click en "Habilitar autenticación de dos factores", se verán las siguientes dos opciones.

* **Saltear autenticación de dos factores para usuarios que inician sesión desde una dirección IP restringida**: A los usuarios que inicien sesión desde direcciones IP restringidas, no se les solicitará la Autenticación de Dos Factores. Se pueden restringir las direcciones IP desde la función Usuario en el campo Restringir IP. 
* **Saltear la verificación de la dirección IP restringida si la autenticación de dos factores está habilitada**: Si esta opción está tildada, todos los usuarios pueden iniciar sesión utilizando la Autenticación de Dos Factores sin importar si su IP está retringida o no. 

* **Método de autenticación de dos factores**: Seleccionar el método de autenticación a ser utilizado - Aplicación OTP, SMS, o correo electrónico.
* **Tiempo de Expiración de la Página que Muestra el Código QR**: Tiempo de expiración para la imagen del Código QR si el método seleccionado es la "Aplicación OTP"
* **Nombre del Emisor de OTP**: Nombre del emisor de la Contraseña de un Solo Uso (OTP).

    <img class="screenshot" alt="Two Factor Auth" src="{{docs_base_url}}/assets/img/setup/settings/twofactor-settings.png">


### 1.9 Correo Electrónico

* **Pie de página del correo**: El nombre de la empresa, su dirección y otros detalles pueden añadirse aquí. Éste se configurará como predeterminado en todos los correos electrónicos salientes. 
* **Desactivar pie de página estándar en los correos electrónicos**: Si esta opción está tildada, el pie de página estándar se desactivará para correos electrónicos salientes. 
* **Ocultar pie de página en informes de correo electrónico automáticos**: Si se tilda esta opción, se ocultarán los pie de página en [Informes Automáticos de Correo Electrónico](/docs/user/manual/es/setting-up/email/auto-email-reports).
* **Enviar el enlace de la vista web del documento por correo electrónico**: ERPNext posee una vista de portal desde donde entidades como Clientes y Proveedores pueden registrarse y ver su historial de órdenes. Cuando se envía una transacción a través de correo electrónico a esa entidad, se puede incluir un vínculo del sitio web para ver ese mismo documento en el portal de la cuenta ERPNext. Esta opción habilita dicha funcionalidad. 

    ![Email Footer](/docs/assets/img/setup/settings/email-footer.png)

### 1.10 Chat

* **Habilitar Chat**: Esta opción habilitará el chat que puede ser utilizado para comunicaciones entre empleados.


### 2. Temas Relacionados
1. [Configuración de la Compañía](/docs/user/manual/es/setting-up/company-setup)
1. [Predeterminados Globales](/docs/user/manual/es/setting-up/settings/global-defaults)
