<!-- add-breadcrumbs -->
# Precio de Producto

**Precio de Producto es el registro donde se pueden cargar los precios de compra y venta de un producto.**

## 1. Como Crear un Precio de Producto
1. Hay dos formas de crear un nuevo formulario de Precio de Producto:

    **Ventas/Compras/Existencias > Productos y Precios > Precio de Producto > Nuevo**.
 
    O

    **Existencias > Producto > Hacer click en el signo "+" al lado de Precio de Producto**.
2. Seleccionar el Producto. El nombre, Unidad de Medida y la descripción seran obtenidas automáticamente.
3. Seleccionar el Listado de Precios de Venta/Compra o cualquier otro listado de precios que se haya creado. 
4. Ingresar el precio en el campo Precio.
5. Guardar.
    <img class="screenshot" alt="Item Price list" src="{{docs_base_url}}/assets/img/stock/item-price-1.png">


### 1.1 Seleccionar el Listado de Precios

En ERPNext se pueden crear múltiples Listados de Precios a fin de registrar de forma separada el precio de Compra y Venta de un producto. A su vez, si el precio de venta del producto cambia de acuerdo al Territorio u otro criterio se pueden crear múltiples Listados de Precios para el mismo.

En Seleccionar el Listado de Precios, también se tomarán la moneda y la aplicabilidad del precio para compra/venta o las dos. Si se desea que el Precio de Producto sea tomado en las transacciones de compra o venta se debe seleccionar el campo "Listado de Precios" al hacer la transacción, en la sección Moneda y Listado de Precios.  

Para ver todos los Precios de Producto juntos, ir a:

**Existencias > Informes de Existencias > Precio de Productos**

Visitar la página [Listado de Precios](/docs/user/manual/en/stock/price-lists) para saber más.

## 2. Características

###2.1 Unidad de embalaje
Esta es la cantidad que debe ser comprada o vendida por unidad de medida. Por ejemplo si la Unidad de Embalaje es dos, y la unidad de medida es uno, la cantidad de productos transferidos serán dos. La unidad preestablecida es 0, se puede usar una unidad de medida no entera como por ejemplo 1,5 Kg de Avena para 1 Unidad de Embalaje. Si se deja en 0 no afectará a ninguna transacción.

###2.2 Cantidad mínima
Esta es la cantidad mínima de productos a ser transferidos para que este precio sea aplicable y actualizado en el Listado de Precios de Productos. 

### 2.3 Aplicar Listado de Precios a un Cliente/Proveedor específico 
Si se selecciona un listado de Precio de Venta, aparecerá un campo de cliente donde se puede asignar ese precio de producto a un cliente específico. De la misma forma, si se selecciona un listado de Precio de Compra, aparecerá un campo de Proveedor para que se puede seleccionar un Proveedor específico. 

###2.4 Validez
Hay dos campos "Válido desde" y "Válido hasta". Válido desde, se configura en la fecha en que se creó el Precio del Producto, también se puede seleccionar la fecha "Válido hasta" después de la cuál el Precio de Producto dejará de tener validez. 

###2.5 Tiempo de entrega en días
El número aproximado de días que el producto tardará en llegar al depósito. Se pueden establecer diferentes Precios de Producto de acuerdo a la cantidad de tiempo que un mismo producto tardará en llegar desde diferentes vendedores. 

###2.6 Observaciones
En este campo se puede añadir cualquier obsevación respecto al Precio de Producto. 

## 3. Video 

<div>
    <style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style>
    <div class='embed-container'>
        <iframe src='https://www.youtube.com/embed/FcOsV-e8ymE?start=193' frameborder='0' allowfullscreen>
        </iframe>
    </div>
</div>

### 4. Temas relacionados
1. [Producto](/docs/user/manual/en/stock/item)
1. [Aplicar descuento](/docs/user/manual/en/selling/articles/applying-discount)