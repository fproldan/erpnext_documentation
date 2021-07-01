<!-- add-breadcrumbs -->
# Administrar Productos Finales Rechazados

Puede suceder que algunos productos manufacturados no pasen las pruebas de calidad y sean rechazados.

El proceso de fabricación estándar en ERPNext no cubre la administración de productos rechazados. Por ende se deberían crear entradas de productos finales tanto para los productos aceptados como para los rechazados. Con esto, los productos rechazados serán recibidos también en el almacén de productos finales. 

Para mover los productos rechazados desde ese almacén, se debería crear una entrada de Transferencia de Material. Debajo se encuentran los pasos para crear dicha entrada.

#### Paso 1: Nuevo Entrada de Inventario

> Almacén > Transacciones de Inventario > Entrada de Inventario > Nuevo

#### Paso 2: Objetivo

Tipo de entrada de stock = Transferencia de Material

#### Paso 3: Almacén

Almacén de Origen = Almacén de Productos Finales

Almacén Objetivo = Almacén de Productos Rechazados

#### Paso 4: Productos

Seleccionar los productos que no hayan pasado la prueba de calidad e ingresar el total de productos rechazados en el campo Cantidad. 

#### Paso 5: Validar el Entrada de Inventario

Al Guardar y Validar la Entrada de Inventario, las existencias de productos rechazados serán movidas desde el Almacén de Productos Finales hacia el Almacén de Productos Rechazados. 


<!-- markdown -->
