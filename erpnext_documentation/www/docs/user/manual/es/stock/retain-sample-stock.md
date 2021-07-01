<!-- add-breadcrumbs -->
# Retener Stock de Muestras

**Una Muestra de Producto es un lote de cualquier Producto guardado en caso de que debiera realizarse algún análisis posteriormente.**

El Producto para el cual se crea una muestra de producto puede ser materia prima, material de empaque, o productos finales. 

## 1. Prerrequisitos
Antes de utilizar muestras de productos se recomienda crear lo siguiente: 

* [Producto](/docs/user/manual/es/stock/item)
* [Lote](/docs/user/manual/es/stock/batch)
* [Almacén](/docs/user/manual/es/stock/warehouse)

## 2. Configuración del Almacén de Retención de Muestras en Configuración de Inventarios

Se recomienda crear un nuevo Almacén, de forma separada, para retener muestras y no utilizarlo en producción.

<img class="screenshot" alt="Sample Retention Warehouse" src="{{docs_base_url}}/assets/img/stock/sample-warehouse.png">

### 2.2 Permitir Retención de Muestras en el Producto

La Retención de Muestra se basa en los Lotes, por lo cual, primero debe tildarse la opción "Posee número de lote". Luego tildar la opción Retener muestra y configurar la Cantidad máxima de muestras para un lote.  

<img class="screenshot" alt="Retain Sample" src="{{docs_base_url}}/assets/img/stock/retain-sample.png">

### 2.3 Realizar Entrada de Inventario

* Cuando se crea una [Entrada de Inventario](/docs/user/manual/es/stock/stock-entry) con el objetivo de Recepción de Material, puede configurarse la Cantidad de Muestras para aquellos productos que tengan la opción de Retención de Muestra habilitada. Se debe seleccionar el Número de lote para el/los Producto/s. La cantidad de Muestra no puede ser mayor al Máximo configurado en el Producto.  

    <img class="screenshot" alt="Retain Sample" src="{{docs_base_url}}/assets/img/stock/material-receipt-sample.png">

* Al validar esta Entrada de Inventario, estará disponible el botón "Crear Entrada de Inventario de retención de muestra" para realizar otra Entrada de Inventario  para la transferencia de los productos de muestra del lote mencionado al almacén de retención de muestras configurado en Configuración de Inventarios.

    ![Sample Retention Button](/docs/assets/img/stock/sample-retention-button.png)

* Hacer click en este botón llevará a la generación de una nueva Entrada de Inventario de tipo "Transferencia de Material". Este registro transfiere la muestra retenida desde el Almacén de Destino al Almacén de Retención de Muestras. Este registro tendrá toda la información, verificar y hacer click en validar. 

    <img class="screenshot" alt="Retain Sample" src="{{docs_base_url}}/assets/img/stock/material-transfer-sample.png">

### 3. Temas Relacionados
1. [Almacén](/docs/user/manual/es/stock/warehouse)
