<!-- add-breadcrumbs -->
# Configuración de Compras

La Configuración de Compras es donde se pueden definir las propiedades que luego serán aplicadas a las transacciones del módulo de Compra.
Se puede encontrar en:
> Inicio > Compras > Configuración > Configuración de Compras

![Buying Settings]({{docs_base_url}}/assets/img/buying/buying-settings.png)

Veamos las opciones disponibles que pueden ser configuradas:

## 1. Proveedores
### 1.1 Nombrar proveedores por

Cuando un proveedor es guardado, el sistema genera una identificación única o nombre para ese Proveedor la cual podrá ser utilizada para hacer referencia al mismo en distintas transacciones de Compra. 

Si no está configurado de otra forma, ERPNext utiliza el Nombre del Proveedor como el identificador único. Si se quiere identificar a los Proveedores utilizando nombres como SUPP-00001, SUPP-00002, u otras series pautadas, seleccionar "Secuencias e identificadores" en el campo "Nombrar proveedores por".

Se puede definir o seleccionar el patrón de Secuencias e identificadores desde: **Configuraciones > Información > Secuencias e identificadores**

Hacer click [aquí](/docs/user/manual/es/setting-up/settings/naming-series) para saber más respecto a definir Secuencias e identificadores. 

### 1.2 Grupo de Proveedores Predeterminado

Configurar lo que debería ser el valor predeterminado de Grupo de Proveedores al crear un nuevo Proveedor. Por ejemplo, si la mayoría de los proveedores son de hardware, se puede establecer el valor predeterminado como "Hardware". 

## 2. Compras
### 2.1 Lista de Precios predeterminada

Configurar la Lista de Precios Predeterminada, la cual se usará al crear una nueva Transacción de Compra, el valor predeterminado es "Compra Estándar". Los precios de los productos serán obtenidos de esta Lista de Precios. Se puede modificar la "Lista de Precios" ingresando a la misma para cambiar la moneda y el país. 

### 2.2 Se requiere Orden de compra para la creación de Facturas y Recibos de compra

Si esta opción está configurada como "Si", ERPNext no permitirá crear una Factura de Compra o Recibo de Compra sin crear primero una Orden de Compra. Si se generan transacciones al por menor, donde el pedido sucede fuera de línea, entonces la Orden de Compra puede saltearse. Si se están aceptando Productos de muestra, se puede crear directamente un Recibo de Compra para recibir los Productos en el Almacén.  

Esta configuración puede ser anulada para un proveedor en particular al habilitar la casilla "Permitir la creación de facturas de compra sin orden de compra", en la función proveedor. 

<img alt="Purchase Order Required" class="screenshot" src="{{docs_base_url}}/assets/img/buying/po-required.png">

### 2.3 Se requiere Recibo de compra para la creación de Facturas de compra

Si esta opción está configurada como "Si", ERPNext no permitirá crear Factura de Compra sin primero crear un Recibo de Compra. En caso de que el Producto en transacción sea un servicio, no requerirá un recibo, por lo que se puede crear una Factura directamente.  

Esta configuración puede ser anulada para un proveedor en particular al habilitar la casilla "Permitir la creación de facturas de compra sin recibo de compra", en la función proveedor. 

<img alt="Purchase Receipt Required" class="screenshot" src="{{docs_base_url}}/assets/img/buying/pr-required.png">

### 2.4 Mantener mismo precio durante todo el ciclo de compra 

Si esta opción está tildada, ERPNext no permitirá cambiar el precio de un Producto en una Factura de Compra o Recibo de Compra creado desde una Orden de Compra, es decir, mantendrá el mismo precio a lo largo del ciclo de compras. Si existe la posibilidad de que el precio del Producto pueda cambiar, se debe destildar esta opción.

Se puede configurar en el campo "Acción si no se mantiene el mismo precio" la acción que el sistema deberá realizar si el precio no es el mismo:

- **Detener**: ERPNext generará un mensaje de error que impedirá cambiar el precio.
- **Advertir**: el sistema permitirá guardar la transacción pero mostrará un mensaje de advertencia.

## 3. Permitir que el producto sea añadido varias veces en una transacción

Cuando esta casilla está destildada, un producto no puede ser añadido muchas veces en la misma Orden de Compra. Sin embargo, se puede cambiar la cantidad. Esta es una casilla de verificación para prevenir compras accidentales del mismo producto. Puede ser habilitada para usos específicos donde hay muchas fuentes para el mismo material, por ejemplo, en fabricación. 

### 4. Temas Relacionados
1. [Grupo de Proveedores](/docs/user/manual/es/buying/supplier-group)
