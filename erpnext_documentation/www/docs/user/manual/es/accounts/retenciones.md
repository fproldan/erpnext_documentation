# Retenciones

Una retención es un valor adicional que se aplica a una factura a cuenta de algún impuesto, dependiendo de las condiciones impositivas de la Compañía y del Cliente/Proveedor.

## Retenciones emitidas

Las retenciones emitidas se calcularán automáticamente en el momento de emisión de la Entrada de pago, dependiendo de las características impositivas del Proveedor.

### 1. Configuración

### 1.1 Configuración para Ingresos brutos

#### 1.1.1 Compañía

Ir a *Inicio > Contabilidad > Maestros contables > Compañía* e ingresar a la Compañía que se desee configurar.

Dentro de la sección **Datos fiscales** se deberá tildar la opción **Agente de Retención IIBB** y completar los campos **CIT ARBA** y **Ambiente ARBA**.

#### 1.1.2 Impuestos de Retención
  - Nombre: nombre identificable del impuesto, por ejemplo, Ingresos Brutos Santa Fe.
  - Compañía: la cual hará uso del impuesto, nos permite tener diferentes configuraciones por impuesto por Compañía.
  - Categoría: es el tipo de impuesto, ya sea Ingresos Brutos, Ganancias, IVA, Seguridad Social. Es importante categorizar correctamente el impuesto.
  - Código de Tipo de Impuesto: según documentación de AFIP. Se utiliza para reportes.
  - Código de impuesto: según documentación de AFIP. Se utiliza para reportes.
  - Jurisdicción: jurisdicción por la cual corresponde retener. Se configurará un impuesto de retención por cada jurisdicción ante la cual se actúe como agente.
  - Descripción:  descripción opcional del impuesto.

Configuración General
   - Alícuota: alícuota general a retener del impuesto, se utilizará cuando el proveedor no tenga una actividad específica que determine una alícuota.
   - Mínimo imponible: monto del pago a partir del cual se aplicará el impuesto, si el monto del pago (sin deducciones) es inferior no se efectúa retención.
   - Base Imponible: especifica cómo se calcula la base, las opciones son: 
     - Neto: Toma como base imponible para el cálculo de la retención el monto de la factura libre de impuestos.  
     - Total: Toma como base imponible el valor final de la factura, posterior a los cargos e impuestos. 
     - Porcentaje sobre neto: Sobre el valor neto de la factura, utiliza solo un porcentaje como base imponible. 
   - Porcentaje: este campo solo aparece si en el campo Base Imponible se eligió Porcentaje sobre el neto y nos permite determinar cual será el porcentaje del neto que se tomará como base imponible del impuesto.
   - Retención mínima: permite especificar una retención mínima. Luego de realizado el cálculo de la retención, si ésta no supera el monto especificado en el campo Retención mínima, la retención no se aplica.
   - Tipo de cálculo: existen tres métodos de cálculo:
      - Por monto de pago: En entradas de pago parciales, calcula la retención del pago total, pero solo se efectúa la retención por la proporción del pago que se está cancelando. De esta forma, al cancelarse el saldo de la factura, también se efectuará el saldo de retención 
       - Por comprobante: En entradas de pago que incluyen mas de una factura, excluirá del cálculo de la base imponible aquellas facturas cuyo monto sea inferior al mínimo imponible 
      - Por pago: En entradas de pago parciales, efectúa la retención por el total del monto a pagar y no por el pago parcial. De esta forma, al cancelarse el saldo restante no se hará retención, dado que se retuvo en su totalidad 

 Actividades
   - Actividad: determinada actividad de la jurisdicción
   - Alícuota: alícuota definida para la actividad
 
Cuentas
  - Cuenta de Venta / Cuenta de Compra: son las cuentas que se utilizaran en las deducciones al momento de efectuar una retención Emitida / Sufrida
  - Centro de costos: 

#### 1.1.3 Proveedor

En la sección **Configuración de Retenciones** se debe especificar:

Impuestos de Retención
- Compañía
- Impuesto
- Actividad
- Categoría de Impuesto
- Porcentaje Exento
- Fecha hasta de exención
- Predeterminado
Alícuotas desde Padrón
- Alícuota Retención
- Fecha Desde
- Fecha Hasta

Porcentajes por Convenio Multilateral
- Jurisdicción
- Porcentaje


### 1.2 Configuración para Ganancias

### 1.2.1 Compañía

Dentro de la sección **Datos fiscales** se deberá tildar la opción **Agente de Retención Ganancias**.

### 1.2.2 Impuestos de Retención
  - Nombre: 
  - Compañía: 
  - Categoría: 
  - Código de Tipo de Impuesto: 
 
 
Cuentas
  - Cuenta de Venta / Cuenta de Compra
  - Centro de costos

### 1.2.3 Escala de ganancias

- Importe Desde
- Importe Hasta
- Importe Fijo
- Porcentaje
- Importe Excedente

### 1.2.4 Alícuota monto ganancias

- Código de Régimen
- Concepto referencia
- Anexo referencia
- Montos no sujetos a retención

Inscripto
- Retención mínima Inscripto
- Porcentaje Inscripto
o
- Usa escala

No Inscripto
- Retención mínima No Inscripto
- Porcentaje No Inscripto

### 1.2.5 Proveedor

En la sección **Configuración de Retenciones** se debe especificar:

- Ganancias
- Régimen de ganancias

Impuestos de Retención
- Compañía
- Impuesto
- Actividad
- Categoría de Impuesto
- Porcentaje Exento
- Fecha hasta de exención
- Predeterminado
Alícuotas desde Padrón
- Alícuota Retención
- Fecha Desde
- Fecha Hasta

---

### 2. Emisión de retenciones

### 2.1 Entrada de pago



### 2.2 Retención

---

### 3. Reportes de retenciones

### 3.1 Libro de IVA Digital



### 3.2 SIRCAR



### 3.3 SICORE


***
