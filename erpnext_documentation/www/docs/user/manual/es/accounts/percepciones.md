# Configuración de Percepciones

Una percepción es un valor adicional que se aplica a una factura a cuenta de algún impuesto, dependiendo de las condiciones impositivas de la Compañía y del Cliente/Proveedor.

## 1. Percepciones emitidas

Las percepciones emitidas se calcularán automáticamente en el momento de emisión de la Factura de Venta, dependiendo de las características impositivas del Cliente.

### 1.1. Configuraciones generales

1. Ingresar en la configuración de la **Compañía**, tildar la opción *Agente de Percepción* y seleccionar las Jurisdicciones correspondientes.
2. Crear los **Impuestos de Percepción** necesarios (más información en la sección siguiente). 
3. Ingresar en el **Cliente** y, dentro del apartado *Configuración de Percepciones*, completar las filas que correspondan de acuerdo a las percepciones aplicables al mismo. 

### 1.2. Creación de un Impuesto de Percepción

Ingresar a *Inicio > Contabilidad > Configuración de Factura Electrónica > Impuesto de Percepción* y hacer click en Nuevo. Completar los campos correspondientes:

* **Nombre**: Se deberá asignar un nombre para el impuesto. Por ejemplo, Percepción IIBB Santa Fe. 
* **Cuenta de Venta**: Es la cuenta contable en la que impactarán las percepciones. Deberá definirse en el tipo de cuenta bajo el subtipo *Impuesto*.
* **Categoría**: Las categorías admitidas por el sistema son IVA e IIBB. Si las percepciones fuesen por otros conceptos impositivos deberán ingresarse manualmente.
* **Jurisdicción**: Como en muchos casos (a excepción de IVA) se trata de impuestos provinciales, en Jurisdicción deberá elegirse aquella que corresponda.
* **Centro de Costos**: centro de costos en el cual se registrará el impuesto.
* **Código de Impuesto**: dato informativo para ser usado en reportes.
* **Código de Tipo de Impuesto**: dato informativo para ser usado en reportes.
* **Descripción**: dato informativo.

* **Configuración General**: En este apartado deberá completarse la:
  * **Alícuota**: valor que se utilizará en el cálculo de la percepción.
  * **Percepción Mínima**: en caso de que aplique, será el valor mínimo a percibir.
  * **Mínimo imponible**: es el monto a partir del cual comienzan a aplicarse las percepciones, tal que no aplique para importes inferiores al mismo. 

  Si las alícuotas de la percepción son proporcionadas a través del padrón, dado que se determina una alícuota para cada contribuyente en particular, no se deben completar los campos del apartado Configuración General sino que esta información se establece directamente en el Cliente.

* **Actividades**: En caso de que las percepciones difieran por actividad, en esta tabla deberán detallarse las distintas actividades y la alícuota que aplica a cada una de ellas.

### 1.3. Configuración del impuesto de percepción en el Cliente

En el Cliente, dentro del apartado Configuración de Percepciones, deberán seleccionarse los **Impuestos de percepción** que correspondan, agregando las filas necesarias para esto.
* **Impuesto**: impuesto al cual aplica.
* **Actividad**: se puede especificar una actividad específica.
* **Porcentaje Exento**: el Cliente puede estar exento de percepciones por un período determinado. Aquí se puede ingresar el porcentaje de excención.
* **Fecha Hasta de Exención**: fecha hasta la cual se aplicará la exención.

Si la información respecto a la alícuota es tomada desde un padrón, entonces en la edición de la fila deberán completarse los campos **Alícuota Percepción**, **Fecha Desde** y **Fecha Hasta**.

Si corresponde se debe completar la tabla **Porcentajes por Convenio Multilateral**, especificando las distintas Jurisdicciones con sus Porcentajes de percepción.

### 1.4. Emisión de comprobante con percepción

#### 1.4.1. Factura de venta con percepción

Realizadas estas configuraciones, al guardar una Factura de venta aparecerá de manera automática, en el apartado *Impuestos y Cargos sobre Ventas*, por defecto la percepción que aplique al Cliente seleccionado (puede aplicar más de una por Cliente).

#### 1.4.2. Cotización/Orden de venta con percepción

Es posible generar (de forma opcional) la percepción en la etapa de Cotización o de creación de Orde de venta. Para esto se debe hacer click en *Acciones > Calcular Percepciones* luego de guardar el documento. 

## 2. Percepciones sufridas

Las percepciones sufridas deberán ingresarse de forma manual en la creación de la Factura de compra. Esto se debe a que tienen que coincidir exactamente el importe ingresado en sistema con el de la factura recibida del proveedor.

### 2.1. Carga del impuesto de percepción en la Factura de compra

Dentro de la factura de compra, en el apartado *Impuestos y Cargos sobre Compras*, deberá ingresarse una nueva fila en la cual se completarán los datos correspondientes a la percepción que el proveedor ha efectuado. Los campos obligatorios son los siguientes:

* **Tipo**: Deberá completarse con la opción correspondiente del desplegable. En general, los distintos impuestos aplican sobre el total neto, salvo que se indique lo contrario. Se puede ver también en el detalle de la factura de compra.
* **Encabezado de cuenta**: Cuenta sobre la cual impactará la percepción sufrida. 
* **Precio**: Porcentaje correspondiente a la percepción. 

Haciendo click en *Editar* pueden configurarse una serie de aspectos adicionales de las percepciones. Entre algunos, se puede determinar el *Impuesto* al que pertenecen, así como la *Jurisdicción* y el *Centro de Costos* en caso de corresponder. 

Los restantes apartados de la Factura de compra no sufren modificaciones, debiendo completarse de acuerdo a lo indicado en la [documentación](docs/user/manual/es/accounts/purchase-invoice).

