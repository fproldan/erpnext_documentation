<!-- add-breadcrumbs -->
# Número de Serie

Como se comentó en la página de [Producto](/docs/user/manual/es/stock/item), si un **Producto** es _seriado_, se mantiene un registro de **Número de Serie** (No. de Serie) para cada cantidad de ese Producto. Esta información ayuda a rastrear la ubicación del Número de Serie, y la información de su garantía y fecha de vencimiento.

Los **Números de Serie** también resultan útiles para mantener activos fijos. Pueden crearse [Calendarios de Mantenimiento](/docs/user/manual/en/support/maintenance-schedule) desde los Números de Serie a fin de planear y organizar las actividades de mantenimiento para esos activos (de ser necesario).

También se puede rastrear a qué **Proveedor** se compró el **Número de Serie** y a qué **Cliente** se lo vendió. El estado del **Número de Serie** informará
el estado actual de su inventario.

Si el Producto es _seriado_ se deberán ingresar los Números de Serie en la columna para tal fin, con cada Número de Serie en una nueva línea. 
Se pueden mantener unidades individuales de productos seriados utilizando Números de Serie.

Para acceder al listado de Números de Serie ir a:
> Inicio > Almacén > Número de Serie y de Lote > Número de Serie

## 1. Prerrequisitos
Antes de crear y utilizar Números de Serie se recomienda crear lo siguiente:

* [Producto](/docs/user/manual/es/stock/item)
* Tildar "Posee Número de Serie" en el Producto

    ![Serial No Enabled](/docs/assets/img/stock/serial-no-enabled.png)


## 2. Creación de un Número de Serie
Por lo general, los Números de Serie son creados automáticamente cuando se realizan transacciones de Productos seriados. Esto solo funciona si está habilitado el campo "Posee Número de Serie" y la serie está configurada en el Producto. 

Por ejemplo, se configuró una serie para el Producto como 'PB2L.#####'. Luego se generó una Entrada de Inventario para recibir el Producto. Los Números de Serie son creados en consecuencia. 

![Serial No Created](/docs/assets/img/stock/serial-no-created.png)

Sin embargo, si se desea crear Números de Serie de forma _manual_ seguir estos pasos:

1. Ir al listado de Número de Serie y hacer click en Nuevo.
1. Ingresar un Número de Serie.
1. Ingresar el Código de Producto y se obtendrán sus detalles.
1. Si se realiza cualquier transacción con un producto, el Número de Serie no puede ser habilitado o deshabilitado. 
1. Guardar.

El stock de un producto solo puede ser afectado si se realiza la transacción (Entrada de inventario, Recibo de compra, Nota de entrega, Factura de venta) utilizando el Número de serie. Al crearse directamente un nuevo Número de serie, no se puede definir el Almacén.

<img class="screenshot" alt="Serial Number" src="{{docs_base_url}}/assets/img/stock/serial-no.png">

### 2.1 Notas Respecto a Números de Serie

* El Estado se configura en base a la Entrada de Inventario.
* Solo los Números de Serie con el estado "Disponible" pueden ser enviados.
* Los Números de Serie pueden ser creados automáticamente desde una Entrada de Inventario o Recibo de Compra. Si se mencionan Números de Serie en la Columna de Números de Serie, se crearán automáticamente.  
* Si en el Producto se mencionan Series de Números de Serie, se puede dejar la columna en blanco en una Entrada de Inventario/Recibo de Compra. Los Números de Serie serán configurados automáticamente desde esa serie. 

## 3. Características
### 3.1 Detalles de Compra/Producción
Se muestra el documento desde el cual se creó el Número de Serie. Si se compró a un Proveedor, estará vinculado aquí. 

### 3.2 Detalles de la entrega
Si el Número de Serie fue generado desde una Orden de Venta, el Cliente estará vinculado aquí.

### 3.3 Detalles de Garantía/CMA
Si el Producto está bajo garantía o CMA (Contrato Anual de Mantenimiento), pueden configurarse las fechas de vencimiento de los mismos.

### 3.4 Más Información
Toda información adicional respecto a esta unidad específica de Producto puede configurarse en "Detalles del número de serie".

## 4. Temas Relacionados
1. [Codificación de Producto](/docs/user/manual/es/stock/articles/item-codification)
1. [Variantes de Producto](/docs/user/manual/es/stock/item-variants)
1. [Nombrar usando Número de Serie](/docs/user/manual/es/stock/articles/serial-no-naming)

