# Cheques de tercero

Se recibe un cheque de tercero cuando alguna entidad, como un Cliente, paga con dicho cheque.

A continuación se detalla el ciclo de vida de un cheque en el sistema.

## 1. Recepción de un pago con cheque de tercero

Al recibir un cheque de un tercero, este debe registrarse en el sistema de forma tal que se cancele la deuda que la entidad tenga con la empresa.

Los cheques pueden crearse de dos maneras:

### 1.1. Creación desde la Entrada de pago

Es la forma de creación más usual. 

   1. En la Entrada de pago, seleccionar "Recibir/Recibido" en Tipo de pago (opción por defecto).
   2. Elegir Método de pago: Cheque.
   3. En la tabla Cheques añadir una fila y, luego de hacer click en la celda Cheque, seleccionar "Crear: Cheque".
   4. Seleccionar Tipo de Cheque, indicar Nro de Cheque, Importe, Fecha de Pago, Banco y Sucursal. Fecha de emisión no es un dato obligatorio.
   5. Guardar.
    
Luego de Guardar y Validar la Entrada de pago, el cheque quedará en estado En mano.

Estos pasos también aplican para el uso de un cheque creado desde el listado, caso que se verá a continuación. La única diferencia es que, en lugar de crearlo (paso 3), se lo debe seleccionar entre el listado de cheques.

El ingreso del cheque en sistema trae aparejado la creación de un asiento contable, el cual se genera al realizar la Entrada de pago.

### 1.2. Creación desde el listado

Es la forma de creación de cheques en sistema que permitirá luego aplicarlos a distintas operaciones.

   1. Ir al listado de Cheques en *Inicio > Contabilidad > Cheques > Cheque* y hacer click en Nuevo.
   2. Completar los datos correspondientes.
   3. Guardar.
    
Así el cheque se creará con estado En mano.

> Importante: El cheque aparece como tal en sistema pero aún sin impacto contable. Por lo tanto, deberá ser ingresado en la Entrada de pago/Asiento contable, según corresponda, para registrar su impacto contable.

## 2. Pago con cheque de tercero

Es posible utilizar el cheque recibido para pagar, por ejemplo, a un Proveedor.

Para esto se deberá seleccionar en la tabla Cheques de la Entrada de pago de Tipo: Pagar y Método de pago: Cheque, el cheque de tercero que se desea usar. Los valores disponibles se muestran en el desplegable.

Una vez Guardada y Validada esta Entrada de pago, el cheque pasará a estado Entregado.

## 3. Depósito de cheque de tercero

Es posible depositar los cheques de terceros recibidos en la cuenta bancaria de la firma.

Hay dos opciones para reflejar en el sistema el depósito de un cheque recibido con estado En mano. 

La primera consiste en ingresar al mismo y hacer click en *Acciones > Depositar*.
Esto llevará a la creación de un Asiento contable de tipo Cheque Depositado, donde la cuenta de débito por defecto será la definida como Cuenta de Depósitos en la Compañía.
Las cuentas contables que el sistema arroja por defecto pueden modificarse al momento de contabilización de la operación. 

La segunda opción consiste en realizar el depósito desde la Conciliación bancaria. Se sugiere revisar la documentación de [Conciliación bancaria](/docs/user/manual/es/accounts/bank-reconciliation#conciliación-de-cheques-de-terceros-desde-la-herramienta-de-conciliación-bancaria), en particular, el apartado de cheques.

Al Validar el asiento, el cheque pasará a estado Depositado.

## 4. Cobro de cheque de tercero

Existe la posibilidad de cobrar por ventanilla, en efectivo, un cheque de terceros. De acuerdo a la normativa vigente, aplican ciertas limitaciones.  

Para reflejar en el sistema el cobro de un cheque recibido En mano se puede ingresar al mismo y hacer click en *Acciones > Cobrar*.
Esto llevará a la creación de un Asiento contable de tipo Cheque Cobrado, donde la cuenta de débito por defecto será la definida como Cuenta de Cobros en la Compañía. 

Las cuentas contables que el sistema arroja por defecto pueden modificarse al momento de contabilización de la operación. 

Al Validar el asiento, el cheque pasará a estado Cobrado.

## 5. Vencimiento de un cheque de tercero

En el supuesto caso de que se tenga un cheque recibido En mano y supere el plazo de pago, es decir, se exceda en más de 30 días corridos la Fecha de pago; este pasará a estado Vencido. El sistema corre un proceso automático diario mediante el cual va cambiando los estados para aquellos cheques que correspondan. 

Se deberán realizar las gestiones comerciales correspondientes y registrar las mismas en el sistema, según corresponda; lo que a continuación se detallará. 

### 5.1. Actualización de fecha
Si el vencimiento resultó de un error en la selección de la Fecha de pago, es posible actualizarla haciendo click en *Acciones > Actualizar Fecha de pago*. Así se puede seleccionar una fecha posterior y el cheque volverá a estado En mano.

### 5.2. Reemplazo de cheque por nuevo cheque o por otra forma de pago
Existen situaciones en las cuales un cheque vencido puede ser reemplazado, ya que el Cliente decide entregar uno nuevo en su lugar. En estos casos, se puede crear el nuevo cheque desde el listado de cheques, y seleccionar el cheque vencido en el campo Reemplaza a. Así el cheque Vencido pasará a estado Reemplazado y se tendrá el nuevo cheque con estado En mano.

En el caso de que se reemplace el cheque por otra forma de pago, se debe hacer click en *Acciones > Reemplazar*, lo que cambiará el estado del cheque a Reemplazado y ya no estará disponible para futuras transacciones. Al hacer esto se puede añadir un comentario en el cheque aclarando la razón del reemplazo, a modo informativo. 
Como la transacción implicó un cambio en la composición del activo de la empresa, deberá realizarse además el Asiento contable correspondiente. Por ejemplo, en el caso de que un cheque en mano sea reemplazado por efectivo, la cuenta Valores a Depositar (Activo) disminuye por el importe correspondiente al cheque, mientras que la cuenta Caja aumenta por el mismo valor.

### 5.3. Rechazo de cheque vencido
También se puede optar por rechazar el cheque vencido, lo cual registrará la deuda del Cliente en el sistema.
Para esto ingresar al cheque y hacer click en *Acciones > Rechazar Vencido*. Esto llevará a la creación de un Asiento contable de tipo Cheque Rechazado, donde la cuenta de débito por defecto será la definida como Cuenta de Cheques Rechazados en la Compañía. Al Validar el asiento, el cheque pasará a estado Rechazado. Es importante crear la Nota de débito con el producto Cheque rechazado para volver a generar la deuda del Cliente ya que el pago queda anulado.

### 5.4. Cobro de cheque vencido
Por más que el cheque esté vencido, el sistema permite registrar el cobro del mismo. Esta facultad está dada por la posibilidad de que exista un desfasaje temporal entre el movimiento diario de Bancos y el momento en el cual se realiza la conciliación de las cuentas bancarias. Para esto hacer click en *Acciones > Cobrar* y validar el Asiento de cobro explicado [anteriormente](/docs/user/manual/es/accounts/cheque-de-tercero.md#4-cobro-de-cheque-de-tercero).


## 6. Rechazo de cheque de tercero

Se puede registrar en el sistema el rechazo de cheques en estado Vencido (explicado anteriormente), Depositado o Entregado. A continuación se detallan los últimos dos casos.

### 6.1. Rechazo de cheque depositado

Un cheque depositado en la cuenta bancaria de la empresa puede ser rechazado por diferentes motivos: falta de fondos, defectos formales, plazos vencidos, etc.

Hay dos opciones para reflejar en sistema el rechazo de un cheque depositado en la cuenta bancaria. 

La primera consiste en ingresar al cheque y hacer click en *Acciones > Rechazar Depositado*. Esto llevará a la creación de un Asiento contable de tipo Cheque Rechazado, donde la cuenta de débito por defecto será la definida como Cuenta de Cheques Rechazados en la Compañía. Al Validar el asiento, el cheque pasará a estado Rechazado. Es importante crear la Nota de débito con el producto Cheque rechazado para volver a generar la deuda del Cliente ya que el pago queda anulado.

La segunda opción consiste en realizar el depósito desde la conciliación bancaria. Se sugiere revisar la documentación de [Conciliación bancaria](/docs/user/manual/es/accounts/bank-reconciliation#conciliación-de-cheques-de-terceros-desde-la-herramienta-de-conciliación-bancaria), en particular, el apartado de cheques.

Al Validar el asiento, el cheque pasará a estado Cobrado.

### 6.2. Rechazo de cheque entregado

Un cheque entregado a un tercero (por ejemplo, a un proveedor) puede ser rechazado por diferentes motivos: falta de fondos, defectos formales, plazos vencidos, etc.

Para esto ingresar al cheque y hacer click en *Acciones > Rechazar Entregado*. En este caso no se debe crear el asiento de rechazo, sino que se debe cargar la Nota de Débito del proveedor al cual se le entregó el cheque y generar la Nota de débito con el producto Cheque rechazado para volver a generar la deuda del Cliente ya que el pago queda anulado.

## 7. Reemplazo de cheque de tercero

Existen situaciones en las cuales un cheque puede ser reemplazado, ya sea por motivos comerciales (cheque en mano), como también porque el cheque se haya vencido y el Cliente decida entregar uno nuevo en su lugar (cheque vencido, caso visto anteriormente) o porque el cheque fue rechazado. En todos los casos se debe seguir los pasos indicados [anteriormente](/docs/user/manual/es/accounts/cheque-de-tercero.md#52-reemplazo-de-cheque).

Si el reemplazo es por efectivo Como la transacción implicó un cambio en la composición del activo de la empresa, deberá realizarse además el Asiento contable correspondiente. Por ejemplo, en el caso de que un cheque en mano sea reemplazado por efectivo, la cuenta Valores a Depositar (Activo) disminuye por el importe correspondiente al cheque, mientras que la cuenta Caja aumenta por el mismo valor.
