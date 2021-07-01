<!-- add-breadcrumbs -->
# Conservar el Código de Producto del Proveedor en el Producto 

Para cada producto, el código asignado puede ser diferente de aquel que el proveedor le dió a ese mismo producto. ERPNext permite rastrear el Código de Producto del Proveedor en el producto. A su vez, se puede obtener el Código de Producto del Proveedor en las transacciones de compra, de forma que el mismo reconozca fácilmente los productos de acuerdo con su Código de Producto. 

#### 1. Actualizar el Código de Producto de Proveedor en un Producto

En el Producto, dentro de la sección de Detalles de Proveedor, ingresar el Código de Producto que el Proveedor le asignó al mismo en la columna "Número de pieza del proveedor". 

<img alt="Supplier Item Code" class="screenshot" src="{{docs_base_url}}/assets/img/articles/supplier-item-code.png">

#### 2. Código de Producto de Proveedor en Transacciones

Cada transacción de compra tiene un campo en la tabla de Producto donde se ingresa el Código de Producto del Proveedor. Este campo está escondido en el formulario, así como también en el formato Estándar de impresión. Es posible hacerlo visible cambiando las propiedades para este campo desde [Editar Formulario](/docs/user/manual/en/customize-erpnext/customize-form.html)

El Código de Producto del Proveedor solo será obtenido en la transacción de compra, si tanto el Proveedor como el Código de Producto seleccionados en la transacción de compra coinciden con el valor mencionado en el Producto. 

<img alt="Supplier Item Code in transaction" class="screenshot" src="{{docs_base_url}}/assets/img/articles/supplier-item-code-in-purchase-order.png">


<!-- markdown -->
