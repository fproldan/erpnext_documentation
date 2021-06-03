# Configuraciones de cheques

Para hacer uso del módulo de Cheques, es necesario configurar los siguientes aspectos:

* **Chequera**
* **Cuenta y producto para cheques rechazados**
* **Cuentas por defecto**
* **Método de pago tipo Cheque**

## 1. Chequera

Para crear cheques propios se necesita tener en el sistema al menos una chequera.

Para acceder al listado de Chequeras ir a:
> Inicio > Contabilidad > Cheques > Chequera

### Creación de una nueva chequera
1. Ir al listado de Chequera y hacer click en Nuevo.
2. Ingresar un Nombre, el Banco y la Sucursal al cual pertenece.
3. Seleccionar el Tipo:
    * **Manual**: para este tipo de chequera se debe especificar el Nro Desde y Nro Hasta. Al primer cheque creado en el sistema se le asignará el Nro Desde, al segundo el Nro desde + 1, y así sucesivamente hasta llegar al Nro Hasta, momento en el cual la chequera será Deshabilitada.
    * **Electrónica**: la numeración de los cheques generados con este tipo de chequera es dado por el banco y se ingresa en la creación del mismo.
4. Guardar.

## 2. Cuenta y producto para cheques rechazados

Para representar el rechazo de un cheque en el sistema se debe contar con:

* **Cuenta Cheque rechazado**: se debe crear en el Plan de cuentas de la Compañía, en el ACTIVO, una cuenta denominada "Cheques rechazados" de tipo **Temporal**. Así, una vez rechazado el cheque y generada la Nota de débito correspondiente, la cuenta mostrará saldo cero. Para mayor información acerca del Plan de Cuentas presione [aquí](...) -> *colocamos link de acceso a la docu de plan de cuentas y creación de cuentas*. 
* **Producto Cheque rechazado**: este producto no debe tener tildada la opción "Mantener stock", debe indicarse que es un producto tanto de venta como de compra, y se deberá colocar la cuenta "Cheque rechazado" en Ingreso por Defecto y Gastos por Defecto en la tabla "Valores Predeterminados de Ventas, Compras y Contabilidad". Este producto se utilizará que para generar las Notas de débito (propias y de proveedores) provenientes del rechazo de cheques. Para mayor información acerca de Producto presione [aquí](...) -> *colocamos link de acceso a la docu de producto y alta de producto*. 

## 3. Cuentas por defecto

Se deberán especificar en la [Compañía](docs/user/manual/es/setting-up/company-setup) las cuentas que serán tomadas por defecto para las diferentes transacciones que se relizarán involucrando cheques (recepción, pago, cobro, depósito, rechazo, etc.).
(Imagen con las cuentas a setear)

## 4. Método de pago tipo Cheque

Para registrar Entradas de pago con cheque se necesita tener al menos un método de pago de este tipo. Para crear uno ingresar a *Inicio > Contabilidad > Configuración > Método de pago*, hacer click en Nuevo, "Editar en pantalla completa" y en el campo Tipo seleccionar "Cheque".
