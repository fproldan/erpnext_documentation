# Percepciones

Una percepción es un valor adicional que se aplica a una factura a cuenta de algún impuesto, dependiendo de las condiciones impositivas de la empresa y del cliente.

Para acceder a Percepciones ir a 

> Inicio > Contabilidad > Configuración de Factura Electrónica > Impuesto de Percepción



Se recomienda tener previamente configuradas las cuentas de impuestos para las percepciones sufridas, así como para las recibidas, en el Plan de Cuentas de la empresa. 



## 2. Percepciones emitidas

Las percepciones emitidas se calcularán automáticamente en el momento de emisión de la factura de venta, dependiendo de las características impositivas del cliente.

### 2. 1. Creación de un impuesto de percepción

1. Se deberá ingresar en la configuración de la Compañía y tildar el checkbox *Agente de Percepción*.

2. Deberá ingresarse a Impuesto de Percepción y hacer click en *Nuevo Impuesto de Percepción*. 
3. Deberán cargarse los campos correspondientes y hacer click en *Guardar*. 
4. Deberá ingresarse en el Maestro del cliente y, dentro del apartado *Configuración de Percepciones*, completando las filas que correspondan de acuerdo a las percepciones aplicables al mismo. 

### 2. 2. Carga del impuesto de percepción

* **Nombre**: Se deberá asignar un nombre para el impuesto. Por ejemplo, Percepción IIBB Santa Fe. 
* **Cuenta de Venta**: Es la cuenta contable en la que impactarán las percepciones. Deberá definirse en el tipo de cuenta bajo el subtipo *Impuesto*.
* **Categoría**: Las categorías admitidas por el sistema son IVA e IIBB. Si las percepciones fuesen por otros conceptos impositivos deberán ingresarse manualmente.
* **Jurisdicción**: Como en muchos casos (a excepción de IVA) se trata de impuestos provinciales, en jurisdicción deberá elegirse aquella que corresponda.

* **Configuración General**: En el apartado deberán completarse la *Alícuota*, *Percepción Mínima* (en caso de que aplique, será el valor mínimo a percibir, independientemente del monto y alícuota), y *Mínimo imponible* (en caso de que aplique, es el monto a partir del cual comienzan a aplicarse las percepciones, tal que no aplique para importes inferiores al mismo). 

  Si las alícuotas de la percepción son proporcionadas a través del padrón, dado que se determina una alícuota para cada contribuyente en particular, no se deben completar los campos del apartado Configuración General. A continuación, se verá que esta información se vuelca directamente en el maestro del cliente.

* **Actividades**: En caso de que las percepciones difieran por actividad, en la tabla de Actividades deberán detallarse las distintas actividades y la alícuota que a cada una aplica.

### 2. 3. Carga del impuesto de percepción en el maestro del Cliente

En el maestro del Cliente, dentro del apartado **Configuración de Percepciones**, deberán cargarse los impuestos de percepción que correspondan, agregando las filas necesarias para esto. 

Si la información respecto a la alícuota es levantada de un padrón, entonces en la edición de la fila deberán completarse los campos *Alícuota Percepción*, *Fecha Desde* y *Fecha Hasta*.

### 2. 4. Emisión de factura con percepción

Realizadas estas configuraciones, en la emisión de una factura de venta debería aparecer de manera automática, en el apartado *Impuestos y Cargos sobre Ventas*, por defecto la percepción que al cliente seleccionado aplique.



## 3. Percepciones sufridas

Las percepciones sufridas deberán ingresarse de manera manual en el momento en el cual se ingrese la factura de compra. Esto se debe a que tienen que coincidir exactamente el importe ingresado en sistema con el de la factura recibida del proveedor.

### 3. 1. Carga del impuesto de percepción en la factura de compra

Dentro de la factura de compra, en el apartado *Impuestos y Cargos sobre Compras*, deberá ingresarse una nueva fila en la cual se completarán los datos correspondientes a la percepción que el proveedor ha efectuado. Los campos obligatorios son los siguientes:

* **Tipo**: Deberá completarse con la opción correspondiente del desplegable. En general, en Argentina los distintos impuestos aplican sobre el total neto, salvo que se indique lo contrario. Se puede ver también en el detalle de la factura de compra.
* **Encabezado de cuenta**: Cuenta sobre la cual impactará la percepción sufrida. 
* **Precio**: Porcentaje correspondiente a la percepción. 

Haciendo click en *Editar* pueden configurarse una serie de aspectos adicionales de las percepciones. Entre algunos, se puede determinar el *Impuesto* al que pertenecen, así como la *Jurisdicción* y el *Centro de Costos* en caso de corresponder. 

Los restantes apartados de la factura de compra no sufren modificaciones, debiendo completarse de acuerdo a lo indicado en la documentación de Factura de Compra.

