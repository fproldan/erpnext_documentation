<!-- add-breadcrumbs -->
# Lista de Embalaje

**Una Lista de embalaje es un documento que enumera los productos que se encuentran en un envío.**

Por lo general se la adjunta a los bienes enviados.

Desde una Nota de Entrega pueden crearse muchas Listas de Embalaje. Esto es útil cuando el envío está empaquetado en cajas diferentes. Cada caja puede tener el peso y número de Productos que contiene. Por ejemplo, si se envían 20 sillas en 4 cajas, cada caja contiene 5 sillas con diferentes Listas de Embalaje para cada caja. 

Para acceder al listado de Lista de Embalaje ir a::
> Inicio > Almacén > Herramientas > Lista de Embalaje

> Observación: Para crear Listas de Embalaje desde una Nota de Entrega, esta debe estar en borrador.  

## 1. Prerrequisitos
Antes de crear y utilizar una Lista de Embalaje se recomienda crear lo siguiente:

* [Nota de Entrega](/docs/user/manual/es/stock/delivery-note)

## 2. Creación de una Lista de Embalaje
Por lo general, las Listas de Embalaje se crean desde una Nota de Entrega cuando la misma se encuentra en estado de Borrador. Sin embargo, si se desea crear una Lista de Embalaje de forma manual, se debe seguir los siguientes pasos: 

1. Ir al listado de Lista de Embalaje y hacer click en Nueva.
1. Seleccionar la Nota de Entrega.
1. Ingresar el Número de Paquete de esta Lista de Embalaje en el campo "Desde paquete nro.".
1. Hacer click en el botón Obtener Productos para ingresar los Productos y Cantidades en la tabla de Productos.
1. Guardar.

La mayoría de estos detalles se obtendrán automáticamente si se genera la Lista de Embalaje desde una Nota de Entrega.

<img class="screenshot" alt="Packing Slip" src="{{docs_base_url}}/assets/img/stock/packing-slip.png">

### 2.1 Opciones Adicionales al crear una Lista de Embalaje
**Número de Paquete**: Si hay muchos paquetes del mismo tipo en el envío entonces conviene configurar los Números de Paquete Desde y Hasta. Por ejemplo, los números de paquete del 1 al 5 en una Lista de Embalaje, luego los números de paquete del 6 al 10 y así sucesivamente.  Esto se verá al imprimir la Lista de Embalaje. Tener en cuenta que esto sólo funcionará si el Envío contiene toda esa cantidad de Productos.

## 3. Características

### 3.1 Tabla de Productos

* Si es un Producto en Lote, es necesario seleccionar el Número de Lote.
* La Cantidad, Unidad de Medida, Peso Neto y Peso en UOM se obtendrán de la Nota de Entrega.
* Salto de Página creará un salto de página justo antes de este producto al imprimir.

### 3.2 Detalles de peso del paquete

Estos detalles se verán al imprimir la Lista de Embalaje.

**Peso neto**: Se calcula como la suma del peso de todos los Productos en la tabla.

**Peso bruto**: Este es el peso final total, incluye el peso de los materiales de embalaje utilizados. 

**Peso bruto de la unidad de medida (UOM)**: Aquí puede configurarse una UOM para el peso final del producto.

### 3.3 Membrete
Se puede imprimir la Lista de Embalaje en papel con el membrete de la empresa. Saber más [aquí](/docs/user/manual/es/setting-up/print/letter-head).


### 4. Temas Relacionados
1. [Inspección de Calidad](/docs/user/manual/es/stock/quality-inspection)
1. [Nota de Entrega](/docs/user/manual/es/stock/delivery-note)
