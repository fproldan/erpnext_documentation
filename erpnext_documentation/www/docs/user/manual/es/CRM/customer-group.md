<!-- add-breadcrumbs -->
# Categoría de Clientes

**Una Categoría de Clientes es un conjunto de clientes que, de alguna forma, son similares.**

Estas categorías permiten organizar a los clientes. Generalmente, los clientes se agrupan de acuerdo al segmento de mercado basado en el dominio en que opera una empresa. Las Categorías de Clientes se crean de forma jerárquica en ERPNext. Se puede crear una categoría de clientes principal y luego añadir sub-categorías.

Se puede definir un listado de precios que será aplicado de forma automática a todos los clientes que pertenezcan a determinada categoría. También se puede realizar un análisis de tendencias para cada categoría. Las categorías Individuo, Comercial y Gobierno son creadas de forma predeterminada. Se pueden añadir otras categorías de clientes de acuerdo con lo que se requiera: como minorista, mayorista, etc.

### 1. Creación de una Categoría de Clientes
1. Ir a **CRM > Configuraciones > Categoría de Clientes**.
1. Hacer click en una categoría principal de clientes como "Todos los grupos de clientes".
1. Hacer click en "Agregar hijo".
2. Ingresar el "Nombre de la categoría de cliente".
3. Seleccionar la casilla de verificación "Nodo de Grupo" si se desea añadir sub grupos de clientes bajo este. 
4. Hacer click en "Crear".

<img class="screenshot" alt="Customer Group Tree" src="{{docs_base_url}}/assets/img/crm/customer-group-tree.png">

> Consejo: Si se considera que esto es mucho trabajo, se puede dejar todo en Categoría de Clientes Predeterminado. Sin embargo, todo este esfuerzo dará sus frutos cuando se empiecen a realizar informes. Un ejemplo de informe de muestra se encuentra a continuación: 

<img class="screenshot" alt="Customer Group report" src="{{docs_base_url}}/assets/img/crm/sales-analytics-customer.gif">

### 2. Características

#### 2.1 Asignar Límite de Crédito, Lista de Precios Predeterminada y Plantilla de Condiciones de Pago Predeterminada 

Se puede asignar el límite de crédito, la [Lista de Precios](/docs/user/manual/es/stock/price-lists), y las [Condiciones de Pago](/docs/user/manual/es/accounts/payment-terms) y todo esto será automáticamente aplicado cuando un cliente perteneciente a una categoría de clientes es seleccionado en transacciones de venta como [Orden de Venta](/docs/user/manual/es/selling/sales-order) y [Factura de Venta](/docs/user/manual/es/accounts/sales-invoice).

#### 2.2 Cuenta por Cobrar Predeterminada

No es necesario crear una cuenta por separado para cada cliente en ERPNext. Leer [Cuenta por Cobrar Común](/docs/user/manual/en/accounts/articles/common-receivable-account) para más detalles.

Si se necesita una cuenta por cobrar por separado para un cliente, se puede añadir en la sección "Cuenta por Cobrar Predeterminada".

#### 3. Temas Relacionados
1. [Cliente](/docs/user/manual/es/CRM/customer)
1. [Lista de Precios](/docs/user/manual/es/stock/price-lists)
1. [Condiciones de Pago](/docs/user/manual/es/accounts/payment-terms)

{siguiente}
