<!-- add-breadcrumbs -->
# Socios de Ventas 

**Los Socios de Ventas son aquellas personas y empresas que asisten a otras para hacer negocios.**

Los Socios de Ventas pueden tener distintos nombres en ERPNext. Se les puede decir Socio Estratégico, Distribuidor, Agente, Minorista, Socio de Implementación, Revendedor, etc. 

Para cada Socio de Ventas, se puede definir una tasa de comisión. Cuando un socio de Ventas es seleccionado en una transacción, su comisión se calcula sobre el Total Neto de la Orden de Venta/Factura de Venta o Nota de Entrega. 

Para acceder a Socios de Ventas, ir a:
> Inicio > Ventas > Ventas > Socios de Ventas 

## 1. Creación de un Socio de Ventas

1. Ir al listado de Socios de Ventas y hacer click en Nuevo.
2. Ingresar el nombre del Socio de Ventas y su tasa de comisión.
3. También se puede seleccionar el tipo de Socio de Ventas para identificar si se trata de un Revendedor, Minorista, etc. 
4. Guardar.

<img class="screenshot" alt="Socios Comerciales " src="{{docs_base_url}}/assets/img/selling/sales-partner.png">

## 2. Características
### 2.1 Dirección y Contacto

Se puede ingresar y rastrear la Dirección y los Datos de Contacto del Socio de Ventas. Estos pueden ingresarse en la sección Dirección y Contacto en un Socio de Ventas:

<img class="screenshot" alt="Socios Comerciales  Address" src="{{docs_base_url}}/assets/img/selling/sales-partner-address.png">

### 2.2 Objetivo del Socio de Ventas

Se pueden asignar Socios de Ventas a cada grupo de productos basado en cantidad y monto. Se puede también asignar el Territorio del target, para saber más ir a *Temas relacionados*.
<img class="screenshot" alt="Socios Comerciales  Target" src="{{docs_base_url}}/assets/img/selling/sales-partner-target.png">

### 2.3 Incluir Socios de Ventas en los sitios web

Para incluir a un Socio de Ventas a un sitio web, hay que tildar la casilla "Mostrar en el Sitio Web". Al hacer esto, aparecerá un campo donde se puede adjuntar el logo de la empresa asociada y una breve introducción respecto al socio, además de una descripción opcional para referencias internas. 

<img class="screenshot" alt="Socios Comerciales " src="{{docs_base_url}}/assets/img/selling/sales-partner-website.png">

Para ver el listado de Socios ir a:

https://yourCompanyName.erpnext.com/partners

<img class="screenshot" alt="Socios Comerciales " src="{{docs_base_url}}/assets/img/crm/sales-partner-listing.png">

### 2.4 Monitorear las ventas de los Socios de Ventas

Los Socios de Ventas pueden generar activamente Iniciativas para la empresa o productos/servicios. Para monitorear el desempeño comercial de cada socio se puede utilizar el Código de Referencia y URL. 

Se puede enviar a los Socios de Ventas una URL, como se muestra a continuación, a fin de que la utilicen en su sitio web o campaña comercial. 

Por ejemplo, una URL como esta, que utiliza "sp" como parámetro http://xyz.erpnext.com?sp=speed capturará la infomación de los Socios de Ventas en la Orden de Venta generada a través del Carrito de Compras. 

<img class="screenshot" alt="Socios Comerciales  Referral Code" src="{{docs_base_url}}/assets/img/selling/sales-partner-refrral-code.png">

## 3. Informes de Socios de Ventas

### 3.1 Comisiones de Socios de Ventas

Para obtener información respecto a las comisiones de Socios de Ventas provenientes de Ordenes de Venta.

<img class="screenshot" alt="Socios Comerciales  Target" src="{{docs_base_url}}/assets/img/selling/sales-partner-commission.png">

### 3.2 Transacciones de Socios de Ventas

Para obtener información respecto a las comisiones de Socios de Ventas de acuerdo a los productos vendidos. 

<img class="screenshot" alt="Socios Comerciales  Target" src="{{docs_base_url}}/assets/img/selling/sales-partner-commission-item.png">

### 3.3 Variación del objetivo del Socio de ventas según el grupo de productos 

Este informe permite analizar la diferencia entre el objetivo del Socio de Ventas y su desempeño de acuerdo a información proveniente de Ordenes de Venta/Facturas de Venta/Notas de Entrega. El usario podrá ver este informe de acuerdo a la periodicidad que elija: mensual, bimestral, cuatrimestral o anual.

<img class="screenshot" alt="Socios Comerciales  Target" src="{{docs_base_url}}/assets/img/selling/sales-partner-target-variance.png">

## Temas relacionados
1. [Asignación de objetivos a Vendedores](/docs/user/manual/es/selling/sales-person-target-allocation)
2. [¿Cómo registrar comisiones de Socios de Ventas en ERPNext?](https://support.erpnext.com/kb/selling/how-to-give-commission-to-sales-partner)
