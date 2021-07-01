<!-- add-breadcrumbs -->
# Inspección de Calidad

En ERPNext, se puede configurar que los productos entrantes o salientes pasen por Inspecciones de Calidad.

Para habilitar esta función ir a:
> Inicio > Almacén > Herramientas > Inspección de Calidad

## 1. Prerrequisitos
Antes de crear y utilizar una Inspección de Calidad se recomienda crear lo siguiente: 

* [Producto](/docs/user/manual/es/stock/item)
* Habilitar los Criterios de Inspección de Calidad en el Producto: 

    ![Enable Quality Inspection](/docs/assets/img/stock/enable-quality-inspection.png)

## 2. Creación de una Inspección de Calidad

1. Desde un Recibo de Compra/Nota de Entrega en Borrador, ir al campo Inspección de Calidad en la tabla de Productos y hacer click en Crear Nueva Inspección de Calidad.
1. Seleccionar el tipo de inspección, sea Entrante (Compra), Saliente (Ventas), o En Proceso (Fabricación). 
1. Seleccionar el tipo de documento de Referencia, es decir Recibo de Compra, Factura de Compra, Nota de Entrega, Factura de Venta o Entrada de Inventario. 
1. Seleccionar el Producto y configurar el tamaño de la muestra a ser inspeccionada. Tener en cuenta que solo se tomarán aquellos Productos que tengan habilitados Criterios de Inspección.  
1. Se utilizará la Plantilla de Inspección de Calidad configurada en el Producto. 
1. Se puede cambiar quién realizará la inspección y tambien añadir quién la verificará. 
1. Puede añadirse cualquier otra Observación respecto a la Inspección. 
1. Guardar y Validar.

<img class="screenshot" alt="Quality Inspection" src="{{docs_base_url}}/assets/img/stock/quality-inspection.png">

## 3. Temas Relacionados
1. [Recibo de Compra](/docs/user/manual/es/stock/purchase-receipt)
1. [Nota de Entrega](/docs/user/manual/es/stock/delivery-note)
1. [Entrada de Inventario](/docs/user/manual/es/stock/stock-entry)
1. [Factura de Venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Factura de Compra](/docs/user/manual/es/accounts/purchase-invoice)
