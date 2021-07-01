<!-- add-breadcrumbs -->
# Calificación del Proveedor

**La Calificación de Proveedores es una herramienta de evaluación que se utiliza para analizar el desempeño de los proveedores.**

La Calificación de Proveedores puede ser utilizada para tener registro de la calidad de los productos, los envíos y la capacidad de respuesta de los proveedores a través de largos períodos de tiempo. Esta información generalmente se utiliza para ayudar en decisiones de compra. 
La Calificación de Proveedores es creada de forma manual para cada proveedor.

Para acceder a la Calificación de Proveedores ir a:
> Inicio > Compras > Calificación de Proveedores > Calificación de Proveedores


## 1. Prerrequisitos

Antes de crear y utilizar una Calificación de Proveedores, se recomienda crear lo siguiente:

* [Proveedor](/docs/user/manual/es/buying/supplier)

## 1. Creación de una Calificación de Proveedores

1. Ir al listado de Calificación de Proveedores y hacer click en Nuevo.
2. Seleccionar el Proveedor a evaluar.
3. Seleccionar el período de evaluación ya sea semanal, mensual o anual.
4. Configurar la Función de ponderación (detalles en la próxima sección).
5. Una Calificación de Proveedores se crea de forma individual para cada proveedor. Solo puede crearse una Calificación para cada proveedor.

<img class="screenshot" alt="Purchase Order" src="{{docs_base_url}}/assets/img/buying/supplier-scorecard.png">

## 2. Características

### 2.1 Configuración de Calificación

La Calificación de Proveedores consiste en una serie de períodos de evaluación, durante los cuales se analiza el desempeño de un proveedor. Este período puede ser semanal, mensual o anual. La puntuación actual es calculada desde la puntuación de cada período de evaluación utilizando la función de ponderación. La fórmula predeterminada es ponderada linealmente durante los 12 períodos de puntuación previos.  
<img class="screenshot" alt="Purchase Order" src="{{docs_base_url}}/assets/img/buying/supplier-scorecard-weighing.png">
Esta fórmula es adaptable.

#### Reputación del Proveedor

La reputación del proveedor se utiliza para clasificar de forma rápida a los proveedores de acuerdo con su desempeño. Son personalizables para cada proveedor. 

La reputación de un proveedor también puede utilizarse para evitar que los proveedores sean incluídos en Solicitudes de Cotización o sean receptores de Ordenes de compra. Al hacer click en Edit y expandir una fila en la tabla de "Clasificación por puntajes" se puede ver la siguiente pantalla.
<img class="screenshot" alt="Purchase Order" src="{{docs_base_url}}/assets/img/buying/supplier-scorecard-standing.png">

### 2.2 Configuración de Criterios

Un proveedor puede ser puntuado en base a distintos criterios individuales de evaluación, incluyendo (aunque no limitado a) tiempo de respuesta de cotización, calidad del producto enviado, y puntualidad de los envíos. Estos criterios son ponderados para determinar el puntaje final del período. 

Para crear nuevos Criterios ir a Compras > Calificación de Proveedores > Criterios de Calificación del Proveedor
<img class="screenshot" alt="Purchase Order" src="{{docs_base_url}}/assets/img/buying/supplier-scorecard-criteria.png">

Observación: Los criterios ponderados para el sistema de puntuación deben sumar 100.

### 2.3 Variables de la Criterios de Calificación de Proveedores

El método para calcular cada criterio es determinado a través del campo Fórmula de Criterios, que puede utilizar una serie de variables preestablecidas. Esto puede verse en la captura de pantalla mostrada anteriormente.

El valor de cada una de estas variables es calculado para cada proveedor a lo largo del período de puntuación. Ejemplos de dichas variables son: 

 - El número total de productos recibidos del proveedor 
 - El número total de productos aceptados del proveedor 
 - El número total de productos rechazados del proveedor
 - El número total de envíos del proveedor
 - El monto total (en dólares) recibido del proveedor

![Supplier Scorecard variable](/docs/assets/img/buying/supplier-scorecard-variables.png)

La fórmula de criterios debe ser adaptada para evaluar a los proveedores en cada criterio de una forma que resulte útil a los requerimientos de la empresa. 

### 2.4 Fórmulas de Evaluación
La fórmula de evaluación utiliza las variables establecidas o adaptadas para evaluar un aspecto del desempeño del proveedor durante el período de puntuación. Las fórmulas pueden usar las siguientes funciones matemáticas: 

* suma: + 
* resta: -
* multiplicación: *
* división: /
* min: min(x,y)
* max: max(x,y)
* si/sino (if/else): (x) if (formula) else (y)
* menor que: <
* mayor que: >
* variables: {nombre_de_variable}

Es crucial que la fórmula sea posible de resolución para todos los valores de variable. Esto suele ser un problema si el valor del resultado es 0. Por ejemplo: 
```
{total_productos_aceptados} / {total_productos_recibidos}
```

Este ejemplo podría resolverse en 0 / 0 para períodos en que no hay productos recibidos, y por ende, en este caso debería corregirse:
```
({total_productos_aceptados} / {total_productos_recibidos}) 
if {total_productos_recibidos} > 0
else 1.
```

### 2.5 Evaluando al Proveedor
Se genera una evaluación por cada Período de la Calificación de Proveedores al hacer click en el botón "Generar Períodos Faltantes del Sistema de Puntuación de Proveedores". Aquí puede verse la puntuación actual del proveedor así como también un gráfico visual que muestra el desempeño del proveedor a lo largo del tiempo. Cualquier accion contra el proveedor también será anotada aquí, como por ejemplo advertencias al crear Solicitudes de Cotización y Ordenes de Compra o directamente restricción de esas acciones para ese proveedor. 

### 3. Temas Relacionados
1. [Proveedor](/docs/user/manual/es/buying/supplier)
1. [Cotización del Proveedor](/docs/user/manual/es/buying/supplier-quotation)
