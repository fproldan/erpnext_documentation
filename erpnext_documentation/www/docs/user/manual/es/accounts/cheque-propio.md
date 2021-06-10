# Cheque propio

Se registra un cheque propio en el sistema cuando se usa el mismo para realizar un pago.

## 1. Prerrequisitos

Para poder operar con cheques es necesario realizar las siguientes [Configuraciones](/docs/user/manual/es/accounts/configuraciones-cheques).

## 2. Operaciones con cheques propios

A continuación se detalla el ciclo de vida de un cheque propio en el sistema.

### 2.1. Pago con un cheque propio

Normalmente el cheque propio se registra en el sistema al realizar un pago a, por ejemplo, a un Proveedor.

   1. En la Entrada de pago, seleccionar "Pagar" en Tipo de pago (opción por defecto si se crea el pago desde una Factura).
   2. Elegir Método de pago: Cheque.
   3. En la tabla Cheques añadir una fila y, luego de hacer click en la celda Cheque, seleccionar **Crear: Cheque**.
   4. Seleccionar Tipo de Cheque, Chequera, Importe, Fecha de Pago y, de forma opcional, Fecha de Emisión. Esto es cuando se elige una chequera común. Si la chequera es electrónica se deberá completar el campo Nro de Cheque Electrónico y Nro de Operación (opcional).
   5. Guardar.
    
Luego de Validar la Entrada de pago, el cheque pasará a estado **Entregado**.

> IMPORTANTE:
> - No se puede crear una Entrada de pago de dos o más chequeras distintas que tengan dos bancos distintos, ya que solo puede debitar de una cuenta de banco llegada a la fecha. En ese caso se deberá generar una Entrada de pago por cada chequera.
> - No puede en una misma Entrada de pago haber cheques propios y de tercero, ya que se tiene una sola cuenta de destino.

### 2.2 Anulación de un cheque propio

En el caso de que el cheque propio haya quedado con estado En mano (no esté vinculado a ninguna transacción validada) y se desee que el sistema no lo tenga en cuenta para futuras operaciones, se puede ingresar al mismo y hacer click en *Acciones > Anular*. luego de confirmar la acción el cheque pasará a estado **Anulado**.

### 2.3 Depósito de cheque propio



### 2.4 Cobro de cheque propio



### 2.5 Vencimiento de un cheque propio

En el supuesto caso de que se tenga un cheque propio En mano y supere el plazo de pago, es decir, se exceda en más de 30 días corridos la Fecha de pago; este pasará a estado **Vencido**. El sistema corre un proceso automático diario mediante el cual va cambiando los estados para aquellos cheques que correspondan. 

Se deberán realizar las gestiones comerciales correspondientes y registrar las mismas en el sistema, según corresponda; lo que a continuación se detallará. 

#### 2.5.1. Actualización de fecha

Si el vencimiento resultó de un error en la selección de la Fecha de pago, es posible actualizarla haciendo click en *Acciones > Actualizar Fecha de pago*. Así se puede seleccionar una fecha posterior y el cheque volverá a estado **En mano**.

#### 2.5.2. Reemplazo de cheque por nuevo cheque o por otra forma de pago

Existen situaciones en las cuales un cheque vencido puede ser reemplazado, ya que se decide entregar uno nuevo en su lugar. En estos casos, se puede crear el nuevo cheque desde el listado de cheques, y seleccionar el cheque vencido en el campo Reemplaza a. Así el cheque Vencido pasará a estado **Reemplazado** y se tendrá el **nuevo cheque con estado En mano**.

En el caso de que se reemplace el cheque por **otra forma de pago**, se debe hacer click en *Acciones > Reemplazar*, lo que cambiará el estado del cheque a Reemplazado y ya no estará disponible para futuras transacciones. Al hacer esto se puede añadir un comentario en el cheque aclarando la razón del reemplazo, a modo informativo.

> IMPORTANTE: como la transacción implicó un cambio en la composición del activo de la empresa, deberá realizarse además el Asiento contable correspondiente.

#### 2.5.3. Rechazo de cheque vencido

También se puede optar por rechazar el cheque vencido, lo cual registrará la deuda en el sistema.
Para esto ingresar al cheque y hacer click en *Acciones > Rechazar Vencido*. Esto llevará a la creación de un Asiento contable de tipo Cheque Rechazado, donde la cuenta de débito por defecto será la definida como Cuenta de Cheques Rechazados en la Compañía. Al Validar el asiento, el cheque pasará a estado **Rechazado**.

#### 2.5.4. Cobro de cheque vencido



### 2.6. Rechazo de cheque propio



#### 2.6.1. Rechazo de cheque depositado



#### 2.6.2. Rechazo de cheque entregado



### 2.7. Reemplazo de cheque propio

