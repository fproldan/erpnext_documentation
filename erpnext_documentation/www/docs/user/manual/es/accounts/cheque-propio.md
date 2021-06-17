# Cheque propio

Se registra un cheque propio en el sistema cuando se emite el mismo. 

## 1. Prerrequisitos

Para poder operar con cheques es necesario realizar las siguientes [Configuraciones](/docs/user/manual/es/accounts/configuraciones-cheques).

## 2. Operaciones con cheques propios

A continuación se detalla el ciclo de vida de un cheque propio en el sistema.

### 2.1. Pago con un cheque propio

### 2.1.1. Creación desde la Entrada de pago

Normalmente el cheque propio se registra en el sistema al realizar un pago, por ejemplo, a un Proveedor.

   1. En la Entrada de pago, seleccionar "Pagar" en Tipo de pago (opción por defecto si se crea el pago desde una Factura).
   2. Elegir Método de pago: Cheque.
   3. En la tabla Cheques añadir una fila y, luego de hacer click en la celda Cheque, seleccionar **Crear: Cheque**.
   4. Seleccionar Tipo de Cheque, Chequera, Importe, Fecha de Pago y, de forma opcional, Fecha de Emisión. Esto es cuando se elige una chequera común. Si la chequera es electrónica se deberá completar el campo Nro de Cheque Electrónico y Nro de Operación (opcional).
   5. Guardar.
    
Luego de Validar la Entrada de pago, el cheque pasará a estado **Entregado**.

> IMPORTANTE:
> - La chequera, así como si se trata de un cheque propio o de terceros, se definen para la Entrada de pago. Por lo tanto, si se utilizan dos o más chequeras, distintas, o bien si se trata de operaciones que incolucren cheques propios y de terceros, deberán emitirse dos o más Entradas de Pago (según corresponda). 

### 2.1.2. Creación desde el listado

También es posible crear el cheque propio desde el listado de cheques para usarlo luego en la operación que corresponda.

1. Ir al listado de Cheques en *Inicio > Contabilidad > Cheques > Cheque* y hacer click en Nuevo.
2. Completar los datos correspondientes.
3. Guardar.

Así el cheque se creará con estado **En mano**.

> IMPORTANTE: el cheque aparece como tal en sistema pero aún sin impacto contable. Por lo tanto, deberá ser ingresado en la Entrada de pago/Asiento contable, según corresponda, para registrar su impacto contable.

### 2.2 Anulación de un cheque propio

En el caso de que el cheque propio haya quedado con estado En mano (no esté vinculado a ninguna transacción validada) y se desee que el sistema no lo tenga en cuenta para futuras operaciones, se puede ingresar al mismo y hacer click en *Acciones > Anular*. Luego de confirmar la acción el cheque pasará a estado **Anulado** y ya no podrá ser utilizado.

### 2.3 Depósito de cheque propio

El caso más común es que se entregue el cheque a un tercero y este lo deposite en su cuenta; aunque también es posible depositar en la cuenta de la Compañía un cheque que quedó con estado En mano.

Para ambos casos se puede utilizar la [Conciliación bancaria](/docs/user/manual/es/accounts/bank-reconciliation#conciliación-de-cheques-propios-desde-la-herramienta-de-conciliación-bancaria) o mediante la acción *Depositar* del cheque.

En el segundo caso se llevará a la creación de un Asiento contable de tipo Cheque Depositado, donde la cuenta de débito por defecto será la definida como Cuenta de Depósitos en la Compañía. Las cuentas contables que el sistema arroja por defecto pueden modificarse al momento de contabilización de la operación.
Al Validar el asiento, el cheque pasará a estado **Depositado**.

### 2.4 Cobro de cheque propio

El caso más común es que se entregue el cheque a un tercero y este lo cobre; aunque también es posible que quien emitió el cheque vuelva a tenerlo En mano y necesite cobrarlo.

Para ambos casos se puede utilizar la [Conciliación bancaria](/docs/user/manual/es/accounts/bank-reconciliation#conciliación-de-cheques-propios-desde-la-herramienta-de-conciliación-bancaria) o mediante la acción *Cobrar* del cheque.

En el segundo caso se llevará a la creación de un Asiento contable de tipo Cheque Cobrado, donde la cuenta de débito por defecto será la definida como Cuenta de Cobro en la Compañía. Las cuentas contables que el sistema arroja por defecto pueden modificarse al momento de contabilización de la operación.
Al Validar el asiento, el cheque pasará a estado **Cobrado**.

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

Por más que el cheque esté vencido, el sistema permite registrar el cobro del mismo. Esta facultad está dada por la posibilidad de que exista un desfasaje temporal entre el movimiento diario de Bancos y el momento en el cual se realiza la conciliación de las cuentas bancarias. Para esto hacer click en *Acciones > Cobrar* y validar el Asiento de cobro explicado [anteriormente](/docs/user/manual/es/accounts/cheque-propio#4-cobro-de-cheque-propio). Al Validar el asiento, el cheque pasará a estado **Cobrado**.

### 2.6. Rechazo de cheque propio

Se puede registrar en el sistema el rechazo de cheques en estado Vencido (explicado anteriormente), Depositado o Entregado. A continuación se detallan los últimos dos casos.

#### 2.6.1. Rechazo de cheque depositado

Un cheque depositado en la cuenta bancaria de la empresa o de un tercero puede ser rechazado por diferentes motivos: falta de fondos, defectos formales, plazos vencidos, etc.

Hay dos opciones para reflejar en sistema el rechazo de un cheque depositado en la cuenta bancaria. 

La primera consiste en ingresar al cheque y hacer click en *Acciones > Rechazar Depositado*. Esto llevará a la creación de un Asiento contable de tipo Cheque Rechazado, donde la cuenta de débito por defecto será la definida como Cuenta de Cheques Rechazados en la Compañía. Al Validar el Asiento, el cheque pasará a estado **Rechazado**.

> IMPORTANTE: si el cheque había sido entregado, se debe crear la Nota de débito con el producto Cheque rechazado para volver a generar la deuda con el Proveedor ya que el pago queda anulado.

La segunda opción consiste en realizar el depósito desde la conciliación bancaria. Se sugiere revisar la documentación de [Conciliación bancaria](/docs/user/manual/es/accounts/bank-reconciliation#conciliación-de-cheques-de-terceros-desde-la-herramienta-de-conciliación-bancaria), en particular, el apartado de cheques.

#### 2.6.2. Rechazo de cheque entregado

Un cheque entregado a un tercero (por ejemplo, a un proveedor) puede ser rechazado por diferentes motivos: falta de fondos, defectos formales, plazos vencidos, etc.

Para esto ingresar al cheque y hacer click en *Acciones > Rechazar Entregado*. Esto llevará a la creación de un Asiento contable de tipo Cheque Rechazado, donde la cuenta de débito por defecto será la definida como Cuenta de Cheques Rechazados en la Compañía. Al Validar el Asiento, el cheque pasará a estado **Rechazado**.

> IMPORTANTE: se debe crear la Nota de débito con el producto Cheque rechazado para volver a generar la deuda con el Proveedor ya que el pago queda anulado.

### 2.7. Reemplazo de cheque propio

Existen situaciones en las cuales un cheque puede ser reemplazado, ya sea por motivos comerciales (cheque en mano), como también porque el cheque se haya vencido se decide entregar uno nuevo en su lugar (cheque vencido, caso visto anteriormente) o porque el cheque fue rechazado. En todos los casos se debe seguir los pasos indicados [anteriormente](/docs/user/manual/es/accounts/cheque-propio#252-reemplazo-de-cheque).

Si se realiza un **reemplazo por efectivo**, como la transacción implica un cambio en la composición del activo de la empresa, deberá realizarse además el Asiento contable correspondiente.

### 2.8. Transferencia interna con cheques propio

Se puede realizar una Entrada de pago de tipo Transeferencia interna, con Método de pago de tipo Cheque, en el caso de que se desee pasar cheques en estado En mano o Vencido de la cuenta en la que se encuentran a otra, sin afectar el estado del cheque.
