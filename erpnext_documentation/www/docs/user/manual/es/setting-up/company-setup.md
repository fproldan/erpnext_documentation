<!-- add-breadcrumbs -->
# Compañía

**Una compañía es una entidad legal conformada por un grupo de personas con el objetivo de llevar adelante una iniciativa comercial o industrial.**

En ERPNext, la primera compañia es creada junto con la cuenta de ERPNext. Por cada compañía, se puede determinar una actividad principal como manufactura, ventas minoristas o servicios, entre otros.

Si se tiene más de una compañía, es posible crearlas desde:

> Inicio > Contabilidad > Compañía

## 1. Creación de una nueva compañía
1. Ir al listado de Compañías, hacer click en Nuevo.
1. Ingresar el nombre, abreviación y divisa/moneda predeterminada de la compañía.
1. Guardar.

La abreviación de la compañía es generada automáticamente, por ejemplo, FT para Frappe Technologies. Esta abreviación ayuda a diferenciar cuentas, centros de costo, plantillas de impuestos, almacenes, etc. de una compañía de los de otra. 

También es posible asignar un logo y una descripción a cada compañía.

![Company Master](/docs/assets/img/setup/company-master.png)

### 1.1 Estructura multi-compañía

Es posible que se tenga un grupo de compañías, algunas más grandes que otras, que son parte de una compañía mayor.

En ERPNext, la estructura de compañías puede ser paralela (compañías hermanas), compañías padre-hija o una combinación de ambas.

Una compañía padre es una organización mayor que cuenta con una o más compañías hijas. Una compañía hija es subsidiaria de la compañía padre.

La vista de árbol de compañías muestra la estructura general de las compañías creadas.

<img class="screenshot" alt="Company Tree" src="{{docs_base_url}}/assets/img/accounts/company-tree.png">

Una vez conformado el árbol de compañías, ERPNext validará si las cuentas de las compañías hijas coinciden con las de la compañía padre. Todas las cuentas pueden combinarse en un Plan de cuentas consolidado.

### 1.2 Otras opciones en la creación de compañías

* **Dominio**: es la actividad principal de la compañia. Ej: manufactura, servicios, etc.
* **Es un grupo**: si está tildado, se creará como compañía padre.
* **Empresa matriz**: si es una compañía hija, se deberá seleccionar en este campo la compañía a la cual pertenece. Una vez seleccionada, el Plan de cuentas de la nueva compañía se creará tomando como modelo la compañía padre.

### 1.3 Plan de cuentas
Por cada compañía, se mantiene un Plan de cuentas independiente. Esto permite separar la contabilidad de cada compañía cumpliendo con los requisitos legales. También es posible importar Planes de cuentas mediante el [Importador de Planes de cuentas](/docs/user/manual/en/setting-up/chart-of-accounts-importer).

<img class="screenshot" alt="Company Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/company-coa.png">

ERPNext posee Planes de cuentas disponibles para ciertos países. Cuando se crea una nueva compañía, se puede seleccionar generar el Plan de cuentas de una de las siguientes formas:

* Plan de cuentas estándar
* Basado en el Plan de cuentas de una compañía existente

<img class="screenshot" alt="Company Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/company-coa-2.png">

Nótese que, si se seleccionó una compañía padre, el Plan de cuentas será creado en base al de esa compañía.

### 1.4 Predeterminados
En la compañía se puede especificar una gran cantidad de valores predeterminados para otros documentos y cuentas. Estas configuraciones por defecto son de ayuda en las entradas rápidas de transacciones contables, donde el valor para la cuenta será tomado de la compañía (si ese campo está definido). Tan pronto como la compañía es creada, se crea un Plan de cuentas y Centro de costos de forma automática.

Es posible especificar por defecto los siguientes datos:

* Libro de Finanzas Predeterminado
* Encabezado predeterminado
* Lista de vacaciones / festividades predeterminadas
* Horas de trabajo estándar
* Términos / Condiciones predeterminados
* País
* ID de impuesto
* Fecha de Fundación

## 2. Características
### 2.1 Objetivo Mensual de Ventas
Es posible establecer un objetivo de ventas mensuales para la empresa, por ejemplo, $10,000. El total de ventas mensuales estará visible una vez se realicen las transacciones. Para más información consulte el siguiente [artículo](/docs/user/manual/en/setting-up/setting-company-sales-goal).

### 2.2 Configuración de Cuentas
Algunas de las siguientes cuentas serán creadas junto con la compañía, otras pueden ser agregadas luego. Las cuentas existentes se pueden ver en el [Plan de cuentas](/docs/user/manual/es/accounts/chart-of-accounts). Estos valores pueden ser modificados luego de ser necesario.

* Cuenta bancaria predeterminada
* Cuenta de efectivo predeterminada
* Cuenta por cobrar predeterminada
* Cuenta de redondeo predeterminada
* Centro de costos predeterminado (redondeo)
* Cuenta de Desajuste
* Cuenta de Descuento Permitido
* Cuenta de Descuento Recibido
* Cuenta de Ganancias/Pérdidas para cambio
* Cuenta de Ganancias/Pérdidas para cambio no realizado
* Cuenta por pagar predeterminada
* Cuenta Predeterminada de Anticipo de Empleado
* Cuenta de costos (venta) predeterminada
* Cuenta de ingresos predeterminada
* Cuenta de ingresos diferidos predeterminada
* Cuenta de gastos diferidos predeterminada
* Cuenta de pago de nómina predeterminada
* Cuenta de pago por reclamación de gastos predeterminada
* Centro de costos predeterminado
* Límite de Crédito
* Plantilla de Términos de Pago Predeterminados

### 2.3 Configuración de inventarios
La funcionalidad de Inventario Perpetuo hará que las transacciones de stock impacten en los libros contables de la empresa. Más información en este [artículo](/docs/user/manual/en/stock/perpetual-inventory). Esta opción se encuentra habilitada por defecto.

* Cuenta de Inventario Predeterminada
* Cuenta de ajuste de existencias
* Inventario entrante no facturado
* Gastos de valoración

    ![Stock Settings in Company](/docs/assets/img/setup/company-stock-settings.png)

### 2.4 Configuración de depreciación de los activos fijos
Para gestionar activos fijos en una compañía, son necesarias las siguientes cuentas. La mayoría es creada por defecto. Estas cuentas se encuentran también en el [Plan de cuentas](/docs/user/manual/es/accounts/chart-of-accounts).

* Cuenta de depreciación acumulada
* Cuenta de gastos de depreciación
* Series para la Entrada de Depreciación de Activos (Entrada de Diario)
* Gastos incluidos en la valoración de activos
* Cuenta de ganancias/pérdidas por enajenación de activos fijos
* Centro de costos de depreciación de activos
* Cuenta de capital de trabajo en progreso
* Activo recibido pero no facturado

    ![Fixed Asset Depreciation](/docs/assets/img/setup/company-asset-depreciation.png)


### 2.5 Configuración de Cheques
Aquí se pueden definir las cuentas que serán usadas por defecto en transacciones con cheques
* Cuenta de Cheques Rechazados
* Cuenta de Valores en Cartera
* Cuenta de Depósitos
* Cuenta de Cobros


### 2.6 Detalle del presupuesto
Rol de aprobación de presupuesto de excepción: los usuarios con este rol tienen permitido sobrepasar el presupuesto establecido.

### 2.7 Información de la compañía
Sólo de forma informativa, los siguientes datos pueden ser definidos en ERPNext:

* Fecha de Incorporación
* Teléfono No.
* Fax
* Correo electrónico (Email)
* Sitio Web
* Dirección
* Detalles de registro: aquí se pueden guardar distintos números fiscales como referencia.

> Nota: al agregar aquí la dirección, es importante tildar el campo " Es la Dirección de su Compañia".

![Company Address](/docs/assets/img/setup/company-address.png)

Al guardar la compañía, se verán los siguientes detalles/acciones en el tablero:
![Company after Save](/docs/assets/img/setup/company-after-save.png)

### 2.8 Datos Fiscales
Para emitir comprobantes electrónicos se deben completar los siguientes datos:

* Razon Social
* CUIT
* Condicion de IVA
* Tipo de Conexion AFIP
* Inicio de Actividades
* Número de IIBB
* Certificado Privado
* Certificado Público
> Para saber cómo obtener estos certificados visitar la siguiente [página](docs/user/manual/es/accounts/certificado)

En caso de encuadrar en el régimen MiPyMEs:
* CBU
* Alias CBU

En caso de estar dentro de un régimen de percepciones/retenciones:
* Agente de Percepción
* Agente de Retención Ganancias
* Agente de Retención IIBB
* Jurisdicciones Convenio Multilateral
* CIT ARBA
* Ambiente ARBA


### 2.9 Eliminar las transacciones de la compañía
Con este botón se eliminarán todas las transacciones de la compañía. *Usar con precaución* ya que las transacciones eliminadas no podrán ser recuperadas.

#### Requerimientos

* el usuario debe tener el rol de administrador de sistema
* el usuario debe ser el creador de la compañía

#### Pasos
1. Clickear el botón **Eliminar las transacciones de la compañía**
1. Verificar la contraseña
1. Ingresar nombre de la compañía para confirmar
    ![Company after Save](/docs/assets/img/setup/company-delete-transactions.png)

Información como productos, cuentas, empleados, etc no es borrada.

#### Efecto de la eliminación de transacciones

* Ordenes de compra/venta, facturas, notas serán eliminadas
* El historial de ventas y las ventas mensuales serán limpiados
* Todas las notificaciones serán borradas
* Direcciones con las cuales se relaciona la compañía serán eliminadas
* Toda comunicación relacionada con la compañía será borrada
* Todas las secuencias serán reiniciadas
* Entradas de inventario relacionadas a un almacén de la compañía serán eliminadas

## 3. Temas relacionados
1. [Configuración de impuestos](/docs/user/manual/en/setting-up/setting-up-taxes)
1. [Configuración del sistema](/docs/user/manual/en/setting-up/settings/system-settings)
1. [Importador de Plan de cuentas](/docs/user/manual/en/setting-up/chart-of-accounts-importer)
1. [Usuarios y permisos](/docs/user/manual/en/setting-up/users-and-permissions)
1. [Agregar usuarios](/docs/user/manual/en/setting-up/users-and-permissions/adding-users)
1. [Encabezado](/docs/user/manual/en/setting-up/print/letter-head)
1. [Cuenta de correo](/docs/user/manual/en/setting-up/email/email-account)
1. [Administrador](/docs/user/manual/en/setting-up/users-and-permissions/administrator)
