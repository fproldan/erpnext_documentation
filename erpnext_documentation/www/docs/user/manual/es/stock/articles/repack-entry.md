<!-- add-breadcrumbs -->
# Entrada de inventario reempacar

La entrada para reempacar se crea para aquellos productos comprados al por mayor que deben ser embalados en paquetes más chicos. Por ejemplo, un producto comprado en toneladas puede volver a embalarse en kilos.

Observaciones:
1. El producto comprado y el que es reempacado tendrán Códigos de Producto diferentes. 
2. La entrada para reempacar puede ser realizada con o sin Lista de Materiales.

En una entrada para reempacar, puede haber uno o más productos a ser reembalados. Por ejemplo:
Asumiendo que se está comprando cajas de pintura en aerosol de un color específico (Verde, Azul, etc), y luego se vuelve a empacar para crear paquetes que contengan múltiples colores de pintura en aerosol (Azul-Verde, Verde-Amarillo, etc.).

### 1. Nueva Entrada de inventario

> Almacén > Transacciones de Inventario > Entrada de inventario > Nueva

### 2. Ingresar Productos

Seleccionar el Tipo de entrada de stock como "Reempaque"

Para materias primas o insumos, solo se proveerá el Almacén de Origen. 

Para productos reembalados, solo estará disponible el Almacén de destino. Se deberá proveer valoración para los productos reembalados.  

<img alt="Repack Entry" class="screenshot" src="{{docs_base_url}}/assets/img/articles/repack-1.png">

Actualizar Cantidad para todos los Productos seleccionados

### 3. Validar Entrada de inventario

Al validar la Entrada de inventario, se reducirán las existencias del insumo desde el Almacén de Origen y se añadirán las existencias del producto reembalado al Almacén de destino. 

<img alt="Repack Stock Entry" class="screenshot" src="{{docs_base_url}}/assets/img/articles/repack-2.png">

<!-- markdown --> 
