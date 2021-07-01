<!-- add-breadcrumbs -->
# Valoración: FIFO y Promedio Móvil

### Valoración de productos

Una de las mejores funciones de cualquier sistema de inventario es poder hallar el valor de cualquier producto de acuerdo a su valor histórico o precio promedio. También se puede encontrar el valor de todos los productos para el Balance general.

La valoración es importante porque: 

  * El precio de compra puede fluctuar.
  * El valor puede cambiar de acuerdo a un proceso (valor agregado)
  * El valor puede cambiar debido a desgaste, pérdida

Pueden aparecer los siguientes términos:

  * Precio: Precio con el cual tiene lugar la transacción. 
  * Precio de valoración: Tarifa a la cual el producto es establecido para la valoración. 

Estas son las dos formas principales en que ERPNext valora los productos.

  * **FIFO (Primero que entra, primero que sale):** En este sistema, ERPNext asume que se van a consumir/vender primero esos productos que se compraron primero. Por ejemplo, si se compra un producto a un precio X y luego de unos días a precio Y, cuando sea que se venda el producto, ERPNext reducirá primero la cantidad del producto con precio X y luego con Y. 

<img alt="FIFO" class="screenshot" src="{{docs_base_url}}/assets/img/stock/fifo.png">

  * **Promedio Móvil:** En este método, ERPNext asume que el valor de un producto en cualquier punto es el precio promedio de todas las unidades de ese producto que se encuentran en existencia. Por ejemplo, si el valor de un producto es X en un depósito con cantidad Y, y otra cantidad Y1 es sumada al depósito, a costo X1, el nuevo valor será: 

> Nuevo Valor X2 = (X * Y + X1 * Y1) / (Y + Y1)
