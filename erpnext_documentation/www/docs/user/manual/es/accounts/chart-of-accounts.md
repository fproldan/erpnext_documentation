<!-- add-breadcrumbs -->
# Plan de cuentas

**El Plan de cuentas es el listado de cuentas de la organización.**

La estructura general del Plan de cuentas está basada en un sistema contable de doble entrada, el cual se ha convertido en un estándar mundial para cuantificar el estado financiero de una compañía.

El Plan de cuentas es un gráfico de árbol que muestra los nombres de las cuentas (y grupos) que una compañía necesita para administrar la contabilidad. ERPNext crea automáticamente un Plan de cuentas básico con cada compañía, el cual puede ser modificado dependiendo de las necesidades y requerimientos legales de cada una de ellas.

Para cada compañía, el Plan de cuentas determina la forma de clasificar las entradas contables, basándose mayormente en requisitos legales (impuestos, conformidad con regulaciones estatales).

![CoA Tree](/docs/assets/img/accounts/chart-of-accounts-tree.png)

El Plan de cuentas ayuda a responder preguntas como:

 * ¿Cuánto vale la organización?
 * ¿Cuánto se debe?
 * ¿Cuál es la ganancia de la empresa? Por lo tanto, ¿cuánto se paga en impuestos?
 * ¿De cuánto son las ventas?
 * ¿Cuales son los gastos?

Para quienes están a cargo de un negocio, es muy importante saber cuán bien le está yendo económicamente.

Para acceder al Plan de cuentas, ingresar a:
> Inicio > Contabilidad > Maestros > Plan de cuentas

## 1. Creación y edición de cuentas
ERPNext cuenta con un Plan de cuentas estándar por defecto. En lugar de crear/modificar cuentas, se puede utilizar el [Importador de Plan de cuentas](/docs/user/manual/en/setting-up/chart-of-accounts-importer). Tener en cuenta que el Plan de cuentas existente será sobrescrito al usar esta herramienta.

1. Ingresar al Plan de cuentas.
 
 Aquí se puede desplegar grupos de cuentas que contienen otras cuentas. Las opciones son "Agregar hijo" a un grupo, "Editar" o "Eliminar" la cuenta.

 <img class="screenshot" alt="Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/chart-of-accounts-add.gif">

1. La opción de crear una cuenta hija sólo aparece al clickear una cuenta de tipo grupo (carpeta). 
1. Ingresar el nombre para la nueva cuenta.
1. Ingresar un número para la cuenta.
1. Tildar "Es un grupo" si se desea que la cuenta se cree como tal y pueda contener otras cuentas.
1. Determinar el tipo de cuenta. Este dato es importante ya que algunos campos admiten sólo cierto tipo de cuentas.
1. Cambiar la divisa/moneda en caso de que esta cuenta vaya a ser usada para transacciones con determinada moneda. Por defecto se autocompleta este campo con la moneda de la compañía. Para más información, visitar la página [Contabilidad con múltiples divisas](/docs/user/manual/es/accounts/multi-currency-accounting).
1. Click en **Crear**.

Generalmente se deben crear cuentas para:

 * Viajes, salarios, teléfono, etc. dentro de **Egresos**.
 * Impuesto sobre el Valor Añadido (IVA), Impuestos de ventas, Capital, etc. dentro de **Pasivos**.
 * Ventas de productos, ventas de servicios, etc. dentro de **Ingresos**.
 * Inmueble, maquinaria, muebles, etc. dentro de **Activos**.

<img class="screenshot" alt="Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/chart-of-accounts-1.png">

> Tip: cuentas con divisas diferentes son creadas cuando se reciben o realizan pagos desde o hacia paises con distinta moneda. Por ejemplo, si se encuentra en Argentina y se realiza una transacción con Estados Unidos, se deberán crear cuentas como "Deudores US", "Acreedores US", etc.

Estos son los grupos principales de en plan de cuentas:

## 2. Tipos de cuentas
A grandes rasgos las cuentas se clasifican en ingresos, egresos (gastos), activos y pasivos.

### 2.1 Cuentas de la Hoja de balance

Las cuentas de la Hoja de balance son "Aplicación de fondos (Activos)" y "Origen de fondos (Pasivo)", lo cual representa el valor neto de la compañia en un momento determinado.
Cuando se inicia o finaliza un período financiero, la suma de los Activos debe ser igual a la suma de los asivos.

> **Una nota de contabilidad**: si uno es nuevo en el tema, se puede llegar a preguntar "¿cómo pueden ser los Activos iguales a los Pasivos? Eso significaría que la compañía no posee nada." Bueno, eso es correcto. Toda la "inversión" hecha en la compañía para comprar activos (como terreno, mebles, máquinas) es realizada por los dueños. Los dueños son una "obligación" de la compañía ya que las ganancias les pertenencen.

> Si una empresa estuviera por cerrar, se necesitaría vender todos los activos y pagar todas las obligaciones (incluyendo ganancias) a los dueños, dejando la compañía en sí con nada.

Todas las cuentas dentro de la Hoja de balance representan un activo que espropiedad de la compañía como "Cuenta bancaria", "Terreno e inmueble", "Muebles" o un pasivo (fondos que la compañía la debe a otros) como "Aporte de los propietarios", "Deuda" etc.

Dos cuentas especiales para tener en consideración son Cuentas por cobrar (dinero que se espera recibir de los Clientes) y Cuentas por pagar (dinero que se debe pagar a los Proveedores) dentro de Activos y Pasivos respectivamente.


### 2.2 Cuentas de pérdida y ganancia

Pérdida y ganancia es el grupo de cuentas dentro de "Ingresos" y "Egresos" que representa las transacciones contables de un determinado período.

A diferencia de las cuentas de la Hoja de balance, las cuentas de pérdida y ganancia no representan el valor neto (activos), sino más bien la cantidad de dinero gastado y obtenido por servicios al cliente durante cierto período. Por lo tanto, el inicio y al final del año fiscal, pasan a ser cero.

En ERPNext es sencillo llevar la cuenta de las pérdidas y ganancias gracias al reporte de Estado de pérdidas y ganancias.

![Profit and Loss Report]({{docs_base_url}}/assets/img/accounts/profit_n_loss_report_1.png)


Nótese que, en el primer día del año no se has registrado pérdidas o ganancias; pero de cualquier forma hay activos, por lo que las cuentas de la hoja de balance nunca vuelven a cero al inicio o final del período.

### 2.3 Grupos y cuentas

Existen dos tipos principales de cuentas en ERPNext: grupos y cuentas. Los grupos pueden tener subgrupos y cuentas dentro de ellos; mientras que las cuentas son nodos hoja del Plan de cuentas y no pueden contener otras.

Las transacciones contables sólo pueden realizarse contra cuentas (no grupos).

<img class="screenshot" alt="Chart of Accounts" src="{{docs_base_url}}/assets/img/accounts/chart-of-accounts-2.png">


### 2.4 Otros tipos de cuentas

En ERPNext, también es posible especificar más información al crear una nueva cuenta, con el objetivo de poder situarla en un escenario como una "Cuenta bancaria" o una "Cuenta de impuestos" sin afectar la estructura del plan de cuentas.

Explicación de los tipos de cuentas:

* **Depreciación acumulada**: en esta cuenta se almacenará el acumulado de depreciaciones de la compañía. Esta cuenta aparece en la Hoja de balance.
* **Activo recibido pero no facturado**: cuenta temporal de pasivo que almacena el valor de los activos recibidos pero todavía no facturados.
* **Banco**: tipo de cuenta con el cual se crearán las demás cuentas de banco. Debe haber al menos un grupo de cuentas de tipo Banco dentro del Plan de cuentas.
* **Efectivo**: tipo de cuenta que aplica para las demás cuentas de efectivo. Debe haber al menos un grupo de cuentas de Efectivo en el Plan de cuentas.
* **Cargos imputables**: cargos adicionales imputables a Productos pueden ser almacenados en cuentas de este tipo. Por ejemplo, "Cargos por flete y envío".
* **Capital de trabajo en progreso**: cargos generados al crear activos fijos son almacenados en estas cuentas. Por ejemplo, costos de construcción de un edificio. En ERPNext los activos son registrados contra este tipo de cuentas cuando todavía no están en uso. 
* **Costo sobre ventas**: una cuenta de este tipo es utilizada para registrar el total acumulado de costos de manufactura/compra de un producto o servicio vendido por la compañía.
* **Depreciación**: cuenta de gastos donde se registra la depreciación de activos fijos. Estas cuentas aparecen en el Estado de resultados.
* **Patrimonio**: este tipo de cuentas representan transacciones con personas que son dueñas del negocio, por ejemplo, accionistas o los mismos dueños.
* **Cuenta de gastos**: este tipo de cuenta representa cualquier fuente de costos o gastos registrados por la compañía.
* **Gastos incluidos en la valoración de activos**: cuenta para registrar los gastos (aparte del costo directo de material de los activos) incluídos en el costo de un activo.
* **Gastos de valoración**: cuenta donde se registran los gastos (aparte del costo directo de material) incluídos en el costo de un producto usado en el inventario perpetuo.
* **Activo Fijo**: cuenta para guardar los costos de activos fijos.
* **Cuenta de ingresos**: esta tipo de cuenta representa cualquier fuente de ingresos o recaudación registrados por la compañía.
* **Pagadero**: tipo de cuenta que representa el monto que la compañía debe a sus proveedores.
* **A cobrar**: tipo de cuenta que representa el monto que los clientes deben a la compañía.
* **Redondeos**: en muchas facturas puede haber un [redondeo](/docs/user/manual/en/accounts/articles/round-off-account-validation) aplicado al importe final. Para un seguimiento preciso, estos valores pueden ser registrados en este tipo de cuentas.
* **Almacén**: grupo de cuentas dentro del cual serán creadas las [cuentas de almacén](/docs/user/manual/en/accounts/articles/warehouse-ledger-link). 
* **Ajuste de existencias**: cuenta de gastos para registrar cualquier asiento de ajuste de stock/inventario. Generalmente se encuentra en el mismo nivel que Costo sobre ventas.
* **Inventario entrante no facturado**: cuenta temporal de pasivo que almacena el valor de stock recibido pero no facturado.
* **Impuesto**: todas las cuentas de impuestos como IVA, entre otros.
* **Temporal**: una cuenta temporal es útil para balancear ingresos y gastos, quedando siempre en cero al finalizar el período.

> **Nota**: al realizar Entradas de pago, la cuenta de banco predeterminada (si está especificada) será tomada en el siguiente orden:
    
> * de la Compañía
> * del Método de pago
> * del Cliente/Proveedor
> * seleccionando manualmente una

### 2.5 Estados financieros
En ERPNext es posible visualizar facilmente estados financieros como Hoja de balance, Cuenta de pérdidas y ganancias y Flujo de fondos.

A continuación se dan ejemplos de estos reportes financieros.:

1. Reporte de Flujo de fondos:
 <img class="screenshot" alt="Cash Flow Report" src="{{docs_base_url}}/assets/img/accounts/cash_flow_report.png">

1. Reporte de Cuenta de pérdidas y ganancias:
 <img class="screenshot" alt="Profit and Loss Report" src="{{docs_base_url}}/assets/img/accounts/profit_n_loss_report.png">
 
1. Reporte de Hoja de balance:
 <img class="screenshot" alt="Balance Sheet Report" src="{{docs_base_url}}/assets/img/accounts/balance_sheet_report.png">

### 2.6 Numeración de cuentas
Un Plan de cuentas estándar está organizado siguiendo un sistema numérico. Cada categoría principal empieza con cierto número, después las sub-categorías comenzarán también con ese número. Por ejemplo, si activos estuvieran clasificados por número comenzando con 1, entonces las cuentas de efectivo serán las 1.1, las cuentas de banco 1.2, cuentas a cobrar 1.3 y así sucesivamente. Esto permite tener espacio para agregar cuentas en el futuro.

Se puede asignar un número durante la creación de la cuenta. También se puede editar un número haciendo click en **Actualizar el nombre / número de la cuenta**. Al hacer esto, el sistema cambia automáticamente el nombre de la cuenta para que contenga el nuevo número.

![Account Number]({{docs_base_url}}/assets/img/accounts/acc-no.png)

### 3. Temas relacionados
1. [Apertura de cuentas](/docs/user/manual/es/accounts/opening-balance)
1. [Configuración de cuentas](/docs/user/manual/es/accounts/accounts-settings)
1. [Asiento contable](/docs/user/manual/es/accounts/journal-entry)
1. [Asiento contable entre compañías](/docs/user/manual/es/accounts/inter-company-journal-entry)
1. [Reportes contables](/docs/user/manual/es/accounts/accounting-reports)
1. [Contabilidad con múltiples divisas](/docs/user/manual/es/accounts/multi-currency-accounting)
