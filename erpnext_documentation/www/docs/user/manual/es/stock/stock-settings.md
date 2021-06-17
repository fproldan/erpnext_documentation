<!-- add-breadcrumbs -->
# Configuración de Inventarios

Se pueden establecer configuraciones predeterminadas para las transacciones de inventario desde la página Configuración de Inventarios.

## 1. Nombrar productos por

![Stock Settings](/docs/assets/img/stock/stock-settings-1.png)

De forma predeterminada, el nombre del Producto se establece de acuerdo al Código de Producto ingresado. Si se desea que los Productos se nombren de acuerdo con [Secuencias e identificadores](/docs/user/manual/es/setting-up/settings/naming-series) configurados previamente, seleccionar la opción "Secuencias e identificadores".

## 2. Configuraciones Predeterminadas

### 2.1 Grupo de productos predeterminado
Este será el grupo de productos predeterminado al cual se asignará un nuevo producto. Los Grupos de Productos son últiles para clasificar y configurar propiedades para todo el grupo. Para saber más, visitar la página [Grupo de Productos](/docs/user/manual/es/stock/item-group).

### 2.2 Unidad de Medida (UOM) predeterminada para Inventario
La unidad de medida predeterminada para las existencias es Números (Nos), puede ser modificada desde este campo. 

### 2.3 Almacén por defecto
Configurar el Almacén predeterminado desde donde se realizan las transacciones de inventario. Este campo será tomado para el Almacén Predeterminado en el Producto: 
    ![Stock Settings](/docs/assets/img/stock/stock-settings-def.png)

### 2.4 Almacén de retención de muestras
Este es el Almacén en el cual se almacenan las muestras de reserva. Para saber más visitar [esta página](/docs/user/manual/es/stock/retain-sample-stock).

### 2.5 Método predeterminado de valoración
El método predeterminado es FIFO (Primero que Entra Primero que Sale), aunque también puede ser valoración por Promedio Móvil. Si se selecciona Promedio Móvil, los Productos nuevos serán valuados de acuerdo al método Promedio Móvil. Se puede cambiar esto al crear nuevos Productos en el formulario de Productos. Una vez que se guarda el producto, el Método de Valoración no puede ser modificado. Leer más [aquí](https://frappe.io/blog/erpnext-features/inventory-valuation-method-fifo-vs-moving-average).

## 3. Porcentaje permitido de sobreentrega/recibo
Este es el porcentaje en el cual se permite recibir o enviar más que la cantidad pedida. Por ejemplo: si se pidieron 100 unidades, el Proveedor manda 120 y el porcentaje es 10%, entonces solo se pueden recibir 110 unidades. De forma predeterminada este campo está configurado en 0. 

## 4. Rol autorizado para sobreentregar/recibir
Los usuarios con este rol pueden entregar/recibir por encima del porcentaje permitido.

## 5. Mostrar Campo de Código de Barras
Un campo para ingresar detalles de Código de Barras para un producto. Si este campo no está seleccionado, no será visible en el formulario de Producto. 

## 6. Convertir la descripción del producto a HTML limpio 
Generalmente, las descripciones de producto son copiadas de un sitio web o un Word/PDF y contienen muchos estilos integrados. Esto estropea la vista de Impresión de las facturas o cotizaciones. 

Para mejorar esto, se puede tildar la opción "Convertir la descripción del producto a HTML limpio". Esto permitirá que, cuando se guarden los Productos, sus descripciones sean depuradas. 

Se puede deshabilitar esta propiedad si se desea controlar las descripciones, vistas y permitir que se integren al HTML.

## 7. Inserción Automática

![Stock Settings](/docs/assets/img/stock/stock-settings-2.png)

### 7.1 Inserción automática de precio de lista 
Al habilitar esto, se introducirá automáticamente un Precio de Producto a la Lista de Precios de un Producto al utilizar dicho Producto en su primera transacción. Este precio será tomado del campo "Precio" configurado en la primera transacción con el Producto. La Lista de Precios depende de si se está realizando una transacción de Compra o Venta. 

Observar que, el Precio de Producto será introducido automáticamente solo en la primera transacción en caso de que no hubiese sido ingresado con anterioridad.

Si esta opción no está tildada, el "Precio de Venta Estándar" configurado para el Producto al crearlo será tomado como Precio de Producto.

### 7.2 Establecer números de serie automáticamente basados en FIFO
Los Números de Serie para las existencias se configurarán automáticamente de acuerdo con los Productos ingresados en base al sistema: primero que entra, primero que sale. Los Números de Serie serán configurados automáticamente en transacciones como Facturas de Compra/Venta, Notas de Entrega, etc. 

## 8. Permitir Inventario Negativo
Esto permitirá que las existencias de productos se muestren en valores negativos. El uso de esta opción depende del caso de uso. Por ejemplo, los asientos de transacciones de inventario son ingresados a fin de semana o fin de mes. En este caso, las existencias negativas deben ser habilitadas para que se pueda continuar con los asientos de transacciones de compra/venta.

## 9. Establecer la cantidad en transacciones según la entrada de Número de serie
La cantidad de productos será configurada de acuerdo con los números de serie. Por ejemplo, si el usuario ingresó números de serie como A001, A002 y A003, entonces el sistema establecerá que la cantidad de productos en la transacción es 3.

## 10. Orden automática de Materiales

![Stock Settings](/docs/assets/img/stock/stock-settings-3.png)

### 10.1 Generar Solicitud de Materiales cuando las existencias alcancen el Nivel de Pedido

Esta opción es útil si se desea asegurar un abastecimiento constante de materias primas/productos para evitar faltantes. 
Una [Solicitud de Materiales](/docs/user/manual/es/stock/material-request) se generará automáticamente cuando las existencias alcancen el nivel de pedido establecido en el [Producto](/docs/user/manual/es/stock/item#34-automatic-reordering).

### 10.2 Notificar por correo electrónico sobre la creación de una Solicitud de Material automática
Se enviará un correo al usuario con el rol de "Gerente de Compras" cuando se genere una Solicitud de Materiales automática. 

## 11. Configuración de transferencia entre almacenes

<img class="screenshot" alt="Delivery Note Material Transfer" src="{{docs_base_url}}/assets/img/stock/inter-warehouse.png">

### 11.1 Permitir Transferencia de material de la Nota de entrega a la Factura de venta 

Esta opción resulta útil cuando se debe presentar una transferencia de materiales como Nota de Entrega. Por ejemplo, si hay requerimientos estatutarios donde deben aplicarse impuestos a cada transferencia de Materiales. Es más facil administrar una situación como esta en una transacción como Nota de Entrega, que en Entrada de Inventario. 

### 11.2 Permitir la Transferencia de material desde el Recibo de compra a la Factura de compra

Similar a la opción anterior, esta opción es útil cuando se debe presentar una transferencia de materiales como Recibo de Compra. 

Para saber más respecto a transferencias de materiales entre almacenes a través de Nota de Entrega y Factura de Compra ver el artículo [Transferencia de Material desde Nota de Entrega y Factura de Compra](/docs/user/manual/es/stock/articles/material-transfer-from-delivery-note)

## 12. Congelar Entradas de Inventario

Pasada esta fecha, el usuario no tendrá permitido realizar Entradas de Inventario.

![Stock Settings](/docs/assets/img/stock/stock-settings-4.png)

* **Inventario Congelado Hasta**: Una fecha límite hasta la cual las existencias estarán congeladas. 
* **Congelar existencias anteriores a (días)**: Transcurrida una x cantidad de días, las existencias serán congeladas. Esto se calcula en base a la fecha de creación del producto. 
* **Rol autorizado para crear/editar transacciones congeladas**: El rol seleccionado en este campo, tendrá permiso para editar las transacciones congeladas.

## 13. Identificación de Lote
Configuraciones generales para lotes de productos a ser identificados por [Secuencias e identificadores](/docs/user/manual/es/setting-up/settings/naming-series). Se puede anular esto en el Producto.
