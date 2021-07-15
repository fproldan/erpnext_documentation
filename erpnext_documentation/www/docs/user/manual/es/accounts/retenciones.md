# Retenciones

Una retención es un monto que se retiene cuando se realiza una operación de pago/cobro a cuenta de algún impuesto, dependiendo de las condiciones impositivas de la Compañía y del Cliente/Proveedor.

## Retenciones emitidas

Las retenciones emitidas de **Ingresos brutos** y de **Ganancias** se calcularán **automáticamente** en el momento de emisión de la Entrada de pago, dependiendo de las características impositivas del Proveedor. Las retenciones emitidas de IVA y de Seguridad social se deben agregar manualmente.

### 1. Configuración

### 1.1 Configuración para Ingresos brutos

#### 1.1.1 Compañía

Ir a *Inicio > Contabilidad > Maestros contables > Compañía* e ingresar a la Compañía que se desee configurar.

Dentro de la sección **Datos fiscales** se deberá tildar la opción **Agente de Retención IIBB** y completar los campos **CIT ARBA** y **Ambiente ARBA** (si correspondiese).

#### 1.1.2 Impuestos de Retención

Ir a *Inicio > Contabilidad > Configuración Factura Electrónica > Impuesto de Retención* y hacer click en Nuevo.

  - **Nombre**: nombre identificable del impuesto, por ejemplo, Ingresos Brutos Santa Fe.
  - **Compañía**: la cual hará uso del impuesto, permite tener diferentes configuraciones de impuesto por Compañía.
  - **Categoría**: es el tipo de impuesto, ya sea Ingresos Brutos, Ganancias, IVA o Seguridad Social. Es importante categorizar correctamente el impuesto.
  - **Código de Tipo de Impuesto**: según documentación de AFIP. Se utiliza para reportes.
  - **Código de impuesto**: según documentación de AFIP. Se utiliza para reportes.
  - **Jurisdicción**: jurisdicción por la cual corresponde retener. Se configurará un impuesto de retención por cada jurisdicción ante la cual se actúe como agente.
  - **Descripción**: descripción opcional del impuesto.

**Cuentas**

  - **Cuenta de Venta / Cuenta de Compra**: son las cuentas que se utilizarán en las deducciones al momento de efectuar una retención Emitida / Sufrida.
  - **Centro de costos**: centro de costos que aplicará en la deducción.

**Configuración General**

   - **Alícuota**: alícuota general a retener del impuesto, se utilizará cuando el proveedor no tenga una actividad específica que determine otra alícuota.
   - **Mínimo imponible**: monto del pago a partir del cual se aplicará el impuesto, si el monto del pago (sin deducciones) es inferior no se efectúa retención.
   - **Base Imponible**: especifica cómo se calcula la base, las opciones son: 
     * **Neto**: toma como base imponible para el cálculo de la retención el monto de la factura libre de impuestos.  
     * **Total**: toma como base imponible el valor final de la factura, posterior a los cargos e impuestos. 
     * **Porcentaje sobre neto**: sobre el valor neto de la factura, utiliza solo un porcentaje como base imponible. 
   - **Porcentaje**: este campo solo aparece si en el campo *Base Imponible* se eligió *Porcentaje sobre el neto* y nos permite determinar cuál será el porcentaje del neto que se tomará como base imponible del impuesto.
   - **Retención mínima**: permite especificar una retención mínima. Luego de realizado el cálculo de la retención, si ésta no supera el monto especificado en el campo Retención mínima, la retención no se aplica.
   - **Tipo de cálculo**: existen tres métodos de cálculo:
      * **Por monto de pago**: en Entradas de pago parciales, calcula la retención del pago total, pero solo se efectúa la retención por la proporción del pago que se está cancelando. De esta forma, al cancelarse el saldo de la factura, también se efectuará el saldo de retención.
       * **Por comprobante**: en Entradas de pago que incluyen más de una factura, excluirá del cálculo de la base imponible aquellas facturas cuyo monto sea inferior al mínimo imponible.
      * **Por pago**: en Entradas de pago parciales, efectúa la retención por el total del monto a pagar y no por el pago parcial. De esta forma, al cancelarse el saldo restante no se hará retención, dado que se retuvo en su totalidad.

 **Actividades**
   - **Actividad**: determinada actividad de la jurisdicción.
   - **Alícuota**: alícuota definida para la actividad.
   - **Regimen SIRCAR**: regimen SIRCAR al cual corresponde la actividad. Dato no obligatorio pero necesario para que la retención aparezca en el [Reporte SIRCAR](/docs/user/manual/es/accounts/reporte-sircar).

#### 1.1.3 Proveedor

Ir a *Inicio > Contabilidad > Proveedor > Proveedor* e ingresar al que se desee configurar.

En la sección **Configuración de Retenciones** se debe especificar:

**Impuestos de Retención**
- **Compañía**: indica qué Compañía hará uso de este impuesto.
- **Impuesto**: impuesto de retención a aplicar al Proveedor.
- **Actividad**: actividad (definida dentro del impuesto de retención) que aplica para el Proveedor. En el caso de que no se tenga una actividad definida para el Proveedor dejar en blanco y se tomará la alícuota general del impuesto.
- **Categoría de Impuesto**: campo de sólo lectura que indica el tipo de impuesto del impuesto elegido, en este caso Ingresos Brutos.
- **Porcentaje Exento**: porcentaje de exención del impuesto.
- **Fecha hasta de exención**: fecha de fin de la exención del impuesto, si se deja en blanco no tiene fecha de fin.

Alícuotas desde Padrón (estos datos son completados automátcamente al realizarse la primera retención con impuestos de jurisdicciones que usan padrón)
- **Alícuota Retención**: alícuota con la cual se calculará la retención.
- **Fecha Desde**: fecha de inicio de vigencia.
- **Fecha Hasta**: fecha de fin de vigencia.

**Porcentajes por Convenio Multilateral**
- **Jurisdicción**: jurisidicción en la que opera el proveedor y sobre la cual se es agente de retención.
- **Porcentaje**: coeficiente unificado de retención de dicha jurisdicción.

---

### 1.2 Configuración para Ganancias

#### 1.2.1 Compañía

Ir a *Inicio > Contabilidad > Maestros contables > Compañía* e ingresar a la Compañía que se desee configurar.

Dentro de la sección **Datos fiscales** se deberá tildar la opción **Agente de Retención Ganancias**.

#### 1.2.2 Impuestos de Retención

Ir a *Inicio > Contabilidad > Configuración Factura Electrónica > Impuesto de Retención* y hacer click en Nuevo.

  - **Nombre**: nombre identificable del impuesto, por ejemplo, Retención de ganancias.
  - **Compañía**: la cual hará uso del impuesto, permite tener diferentes configuraciones de impuesto por Compañía.
  - **Categoría**: es el tipo de impuesto, ya sea Ingresos Brutos, Ganancias, IVA o Seguridad Social. Es importante categorizar correctamente el impuesto.
  - **Código de Tipo de Impuesto**: según documentación de AFIP. Se utiliza para reportes.
  - **Descripción**: descripción opcional del impuesto.
 
**Cuentas**
  - **Cuenta de Venta / Cuenta de Compra**: son las cuentas que se utilizarán en las deducciones al momento de efectuar una retención Emitida / Sufrida.
  - **Centro de costos**: centro de costos que aplicará en la deducción.

Estos mismos campos son los que se deben completar para los Impuestos de retención de IVA y de Seguridad social, por más que el cálculo de estos tipos de retención no sea automático. 

#### 1.2.3 Escala de ganancias

Ir a *Inicio > Contabilidad > Configuración Factura Electrónica > Escala de Ganancias* y hacer click en Nuevo.

Aquí se deben cargar las escalas tomando como referencia el [Anexo de la RG830](https://www.afip.gob.ar/noticias/documentos/anexo16052018.pdf) que serán necesarias para la "Alícuota monto ganancias".

#### 1.2.4 Alícuota monto ganancias

Ir a *Inicio > Contabilidad > Configuración Factura Electrónica > Alícuota Monto Ganancias* y hacer click en Nuevo.

Cada documento "Alícuota monto ganancias" representa un régimen en el cual la compañía retiene, tomando como referencia el [Anexo de la RG830](https://www.afip.gob.ar/noticias/documentos/anexo16052018.pdf).

Para los Inscriptos puede ser necesario usar una escala, las cuales se explican en la sección anterior.

#### 1.2.5 Proveedor

Ir a *Inicio > Contabilidad > Proveedor > Proveedor* e ingresar al que se desee configurar.

En la sección **Configuración de Retenciones** se debe especificar:

- **Ganancias**: situación frente al impuesto (lo completa el padrón de AFIP en caso de ser posible).
- **Régimen de ganancias**: se retendrá sobre el régimen indicado.

---


### 2. Emisión de retenciones

#### 2.1 Entrada de pago

Después de guardar la Entrada de Pago, si la Compañía es Agente de retención de Ingresos brutos o de Ganancias, aparecerá arriba a la derecha el botón **Generar retenciones**. Al hacer click aquí se ejecutará el cálculo automático y aparecerá la tabla de Retenciones y la de Deducciones o Pérdida con los impuestos y montos correspondientes.

Además, de ser necesario, es posible agregar manualmente a la tabla de Retenciones los impuestos de IVA y de Seguridad social con sus montos correspondientes.

Luego de validar la Entrada de Pago se guardarán efectivamente las Retenciones, las cuales pueden encontrarse en *Inicio > Contabilidad > Configuración Factura Electrónica > Retención*.

Si se cancela una Entrada de Pago con retenciones, las mismas serán también canceladas, y no aparecerán en los reportes.

#### 2.2 Retención

Ir a *Inicio > Contabilidad > Configuración Factura Electrónica > Retención*

Por cada retención generada se crea un documento, el cual posee los siguientes datos:
  - Datos del Impuesto de retención y vínculo al mismo.
  - Datos del Régimen y vínculo al mismo en el caso de retenciones de Ganancias.
  - Fecha en la que se generó.
  - Importe base, Alícuota Aplicada (en retenciones de Ingresos brutos o Ganancias) y Monto.

En todas las retenciones hay un botón arriba a la derecha para "Ver Entrada de Pago", el cual lleva a la transacción en la que se generó.

---

## Retenciones sufridas

Las retenciones sufridas de cualquier tipo se deben agregar manualmente en las Entradas de pago generadas contra Facturas de venta.

Luego de guardar la Entrada de pago se debe agregar los impuestos que corresponda retener con sus datos correspondientes.

Al igual que con las retenciones emitidas, estas se guardan efectivamente una vez validada la Entrada de pago. Se las puede ver en el listado de retenciones, todas ellas llevan el nombre de "SUFRIDAS".

También son canceladas al cancelarse la Entrada de pago.

---

## Reportes de retenciones

Las retenciones generadas se muestran en los siguientes reportes:

  - [Reporte SIRCAR](/docs/user/manual/es/accounts/reporte-sircar)
  - [Reporte SICORE](/docs/user/manual/es/accounts/reporte-sicore)
  - [Informe de retenciones](/docs/user/manual/es/accounts/informe-de-retenciones)
