# Cheques de tercero

Se recibe un cheque de tercero cuando alguna entidad, como un Cliente, paga con dicho cheque.

A continuación se detalla el ciclo de vida de un cheque en el sistema.

## 1. Recepción de un pago con cheque de tercero

Al recibir un cheque de un tercero, este debe registrarse en el sistema de forma tal que se cancele la deuda que la entidad tenga con la empresa.

Los cheques pueden crearse de dos maneras:

### 1.1. Creación desde el listado

   1. Ir al listado de Cheques en *Inicio > Contabilidad > Cheques > Cheque* y hacer click en Nuevo.
   2. Seleccionar Tipo de Cheque, indicar Nro de Cheque, Importe, Fecha de Pago, Banco y Sucursal. Fecha de emisión no es un dato obligatorio.
   3. Guardar.
    
Así el cheque se creará con estado En mano.
> Importante: el cheque deberá ser ingresado en la Entrada de pago a la cual corresponde para registrar su impacto contable.

### 1.2. Creación desde la Entrada de pago

   1. En la Entrada de pago, seleccionar "Recibir/Recibido" en Tipo de pago (opción por defecto).
   2. Elegir Método de pago Cheque.
   3. En la tabla Cheques añadir una fila y, luego de hacer click en la celda Cheque, seleccionar "Crear: Cheque".
   4. Completar los datos correspondientes y hacer click en Guardar.
    
Luego de Guardar y Validar la Entrada de pago, el cheque quedará en estado En mano.

Estos pasos aplican para el uso de un cheque creado desde el listado, solo que en lugar de crearlo se lo debe seleccionar entre el listado de cheques.

## 2. Pago con cheque de tercero

Es posible utilizar el cheque recibido para pagar, por ejemplo, a un Proveedor.

Para esto se deberá seleccionar en la tabla Cheques de la Entrada de pago de Tipo: Pagar y Método de pago: Cheque, el cheque de tercero que se desea usar.
Una vez Guardada y Validada esta Entrada de pago, el cheque pasará a estado Entregado.

## 3. Depósito de cheque de tercero

Para reflejar en el sistema el depósito de un cheque recibido En mano se puede ingresar al mismo y hacer click en *Acciones > Depositar*.
Esto llevará a la creación de un Asiento contable de tipo Cheque Depositado, donde la cuenta de débito por defecto será la definida como Cuenta de Depósitos en la Compañía.
Al Validar el asiento, el cheque pasará a estado Depositado.

## 4. Cobro de cheque de tercero

Para reflejar en el sistema el cobro de un cheque recibido En mano se puede ingresar al mismo y hacer click en *Acciones > Cobrar*.
Esto llevará a la creación de un Asiento contable de tipo Cheque Cobrado, donde la cuenta de débito por defecto será la definida como Cuenta de Cobros en la Compañía.

Al Validar el asiento, el cheque pasará a estado Cobrado.

## 5. Vencimiento de un cheque de tercero

En el supuesto caso de que se tenga un cheque recibido En mano y pase la Fecha de pago, este pasará a estado Vencido.

### 5.1. Actualización de fecha
Si esto sucedió por un error en la selección de la Fecha de pago, es posible actualizarla haciendo click en *Acciones > Actualizar Fecha de pago*. Así se puede seleciconar una fecha futura y el cheque volverá a estado En mano.

### 5.2. Reemplazo de cheque vencido
Por otro lado, si el cheque realmente se venció y el Cliente decide entregar uno nuevo en su lugar, se puede crear el nuevo cheque desde el listado y seleccionar el cheque vencido en el campo Reemplaza a. Así el cheque Vencido pasará a estado Reemplazado y se tendrá el nuevo cheque con estado En mano.
En el caso de que se reemplace el cheque vencido por efectivo, se puede hacer click en *Acciones > Reemplazar*, lo que cambiará el estado del cheque a Reemplazado y ya no estará disponible para futuras transacciones. Al hacer esto se puede añadir un comentario en el cheque aclarando la razón del reemplazo a modo informativo.

### 5.3. Rechazo de cheque vencido
También se puede optar por rechazar el cheque vencido, lo cual registrará la deuda del Cliente en el sistema.
Para esto ingresar al cheque y hacer click en *Acciones > Rechazar Vencido*. Esto llevará a la creación de un Asiento contable de tipo Cheque Rechazado, donde la cuenta de débito por defecto será la definida como Cuenta de Cheques Rechazados en la Compañía. Al Validar el asiento, el cheque pasará a estado Rechazado. Es importante generar la Nota de débito con el producto Cheque rechazado para volver a generar la deuda del Cliente ya que el pago queda anulado.

### 5.4. Cobro de cheque vencido
Por más que el cheque esté vencido, el sistema permite registrar el cobro del mismo. Para esto hacer click en *Acciones > Cobrar* y validar el asiento de cobro explicado [anteriormente](/docs/user/manual/es/accounts/cheque-de-tercero.md#4-cobro-de-cheque-de-tercero).

## 6. Rechazo de cheque de tercero

Se puede registrar en el sistema el rechazo de cheques en estado Vencido, Depositado o Entregado.

### 6.1. Rechazo de cheque depositado
Para esto ingresar al cheque y hacer click en *Acciones > Rechazar Depositado*. Esto llevará a la creación de un Asiento contable de tipo Cheque Rechazado, donde la cuenta de débito por defecto será la definida como Cuenta de Cheques Rechazados en la Compañía. Al Validar el asiento, el cheque pasará a estado Rechazado. Es importante generar la Nota de débito con el producto Cheque rechazado para volver a generar la deuda del Cliente ya que el pago queda anulado.

### 6.2. Rechazo de cheque entregado
Para esto ingresar al cheque y hacer click en *Acciones > Rechazar Entregado*. En este caso no se debe crear el asiento de rechazo, sino que se debe cargar la la Nota de Débito del proveedor al cual se le entregó el cheque y generar la Nota de débito con el producto Cheque rechazado para volver a generar la deuda del Cliente ya que el pago queda anulado.

## 7. Reemplazo de cheque de tercero
El reemplazo de cheques (por otro cheque o por efectivo) se puede realizar no solo para aquellos en estado Vencido, sino también para los En mano o Rechazados. En todos los casos se debe seguir los pasos indicados anteriormente(/docs/user/manual/es/accounts/cheque-de-tercero.md#52-reemplazo-de-cheque-vencido)
