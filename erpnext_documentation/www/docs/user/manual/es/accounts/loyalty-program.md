<!-- add-breadcrumbs -->
# Programa de lealtad

**El Programa de lealtad da la posibilidad de que los Clientes ganen puntos al gastar cierto monto y puedan canjearlos en compras futuras.**

Un Programa de lealtad es una iniciativa de marketing estructurada y a largo plazo que provee un incentivo a los Clientes. Los Programas exitosos están diseñados para motivar a los Clientes a volver a comprar de forma frecuente y evitar competidores.

Para acceder a la lista de Programas de lealtad, ir a:
> Inicio > Retail > Programa de lealtad > Programa de lealtad

## 1. Prerrequisitos
Antes de crear y usar un Programa de lealtad, se recomienda crear lo siguiente:

1. [Cliente](/docs/user/manual/es/CRM/customer)
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)

## 2. Creación de un Programa de lealtad
1. Ir a la lista de Programas de lealtad y hacer click en Nuevo.
1. Ingresar un nombre para el Programa de lealtad.
1. Determinar si es un programa de nivel único o múltiple (oro, plata, etc).
1. Establecer las fechas desde y hasta.
1. Seleccionar la Categoría de Cliente y el Territorio para los cuales se aplicará el programa, por defecto se consideran todos.
1. Para aplicar a todos los Clientes, tildar la opción "Auto Opt In (para todos los clientes)". Si no se tilda esta opción, se deberá seleccionar el Programa de lealtad en los [Clientes](/docs/user/manual/en/accounts/loyalty-program#22-loyalty-points-in-customer) para los cuales se desea aplicar.
1. En la tabla, ingresar:
    * **Nombre de Nivel**: para asignar al Cliente en base a su calificación.
    * **Factor de Recolección**: monto que debe gastar para acumular un Punto de lealtad en ERPNext.
    * **Gasto Total Mínimo**: monto mínimo que se debe gastar para calificar en el nivel.
1. Ingresar el Factor de conversión, por ejemplo, $1.000 = 1 punto.
1. Guardar. 

 <img class="screenshot" alt="Loyalty Program" src="{{docs_base_url}}/assets/img/accounts/loyalty-program.png">

### 2.1 Redención

* **Factor de conversión**: al redimirse los puntos, este factor se usa para convertirlos en dinero. Por ejemplo, si el Cliente posee 100 puntos y 1 punto = $1, entonces el Cliente tendrá $100 a su favor en la siguiente compra.

* **Cuenta de costos**: cuenta desde la cual se ofrecerán los beneficios. Esto es útil para realizar el seguimiento por separado de los beneficios ofrecidos.

* **Período de validez (en días)**: los puntos recolectados expirarán pasada la cantidad de días aquí especificada.

### 2.2 Puntos de lealtad en el Cliente

Se puede asignar un Programa de lealtad en el Cliente.

<img class="screenshot" alt="Loyalty Program 1" src="{{docs_base_url}}/assets/img/accounts/loyalty-program-1.png">

Los **Puntos de lealtad** ganados se pueden ver en el tablero del Cliente.

<img class="screenshot" alt="Loyalty Program 2" src="{{docs_base_url}}/assets/img/accounts/loyalty-program-2.png">

### 2.3 Punto de lealtad
Ir a: **Retail > Programa de fidelidad > Punto de fidelidad**.
Este es simplemente un listado de los Puntos de lealtad registrados, el cual permite ver qué Cliente sumó tal cantidad de puntos contra una determinada factura de venta. Estos registros contienen la información de la factura y del Cliente.

<img class="screenshot" alt="Loyalty Program 3" src="{{docs_base_url}}/assets/img/accounts/loyalty-program-3.png">

## 3. Funcionamiento del Programa de lealtad

### 3.1 Obtención de puntos

* Primero se necesita crear un **Programa de lealtad**.
* Asignar el **Programa de lealtad** al **Cliente**.
* Crear una nueva Factura de venta para el **Cliente** al que se ha asignado el **Programa de lealtad**.
* Para este ejemplo se crea una factura por $3.000. Según el **Programa de lealtad**, por un mínimo de $2.000 será elegible el nivel de Plata con un Factor de Recolección de $300, con lo que el **Cliente** recibirá 10 puntos por su compra.
* Al validar la factura, se creará un registro de **Punto de lealtad**.
* En el **Programa de lealtad** del ejemplo, con un mínimo de $6.000 se accede al nivel Oro. Por lo que, al validar una factura por $3.000, el gasto total del Cliente asciende a $6.000. Así, el **Cliente** pasará automáticamente al nivel Oro.

> Nota: el gasto mínimo del Programa de lealtad no se refiere al valor mínimo de una sola factura, sino que es la suma de los montos de las facturas del Cliente dentro de un mismo Programa de lealtad.

### 3.2 Redención de puntos

* Siguiendo el ejemplo anterior en el que el Cliente obtuvo 10 puntos, al crear una nueva factura, ir a la sección Redención de Puntos de Lealtad y tildar la opción "Canjear Puntos de Lealtad".
 ![Loyalty Program Invoice](/docs/assets/img/accounts/loyalty-program-inv.png)
* Aparecerán los campos "Puntos de lealtad", "Cuenta de Redención" y "Centro de Costos de Redención". La cuenta y el centro de costos serán traídos del **Programa de lealtad** asignado al **Cliente**.
* Los 10 puntos obtenidos estarán disponibles para su uso hasta que llegue la fecha de expiración. Si se intenta usar más puntos que los obtenidos surgirá un mensaje de error.
* Para este ejemplo, se canjearán los 10 puntos. Esto hará que se muestre otro campo indicando el monto calculado usando Puntos de lealtad * Factor de conversión. Así, se restarán $100 del monto de la factura ya que el factor de conversión era de 10.
 ![Loyalty Invoice](/docs/assets/img/accounts/loyalty-program-inv2.png)
* Al validar, se crearán dos registros de **Punto de lealtad**. Uno por la redención, el cual tendrá un valor negativo, y otro por los puntos obtenidos en la factura actual (ya que por el monto acumulado todavía es elegible). El Cliente también ascendió a nivel Oro ya que el gasto total a superar era de $6.000.
 ![Loyalty Point](/docs/assets/img/accounts/loyalty-point-2.png)

> Nota: si se crea una devolución para una factura en la cual se obtuvo puntos, se borrará el registro del Punto de lealtad original y se creará uno nuevo luego de restar el monto devuelto del monto original. Además, al cancelar una factura, su registro de Punto de lealtad será borrado.

### 4. Temas relacionados
1. [Centro de costos](/docs/user/manual/es/accounts/cost-center)
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Cliente](/docs/user/manual/es/CRM/customer)
1. [Categoría de Cliente](/docs/user/manual/es/CRM/customer-group)

