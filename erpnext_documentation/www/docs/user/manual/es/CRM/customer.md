<!-- add-breadcrumbs -->
# Cliente

**Un cliente, conocido también como comprador o consumidor, es quien recibe los bienes, servicios, productos o ideas desde un vendedor, a cambio de una retribución monetaria.**

A cada cliente debe asignársele una identificación única. El nombre del cliente puede ser la identificación o se puede configurar la generación de series de identificación en las [Configuraciones de Venta](/docs/user/manual/en/selling/selling-settings).

Para acceder al listado de Clientes ir a:

> Inicio > CRM > Flujo de Ventas > Cliente

O

> Inicio > Ventas > Ventas > Cliente

## 1. Creación de un Cliente

1. Ir al listado de Cliente y hacer click en Nuevo.
1. Ingresar el Nombre Completo del Cliente.
1. En el campo Tipo seleccionar Individual si el cliente es una persona o Compañía si el cliente respresenta a una Organización.
1. Seleccionar una [Categoría de Clientes](/docs/user/manual/es/CRM/customer-group). Individuo, Comercial, Sin Fines de Lucro y Gobierno están disponibles de forma predeterminada. Se pueden crear grupos adicionales de ser necesario. 
1. Seleccionar el Territorio, la Condicion de IVA, el Tipo de documento y el CUIT/CUIL correspondiente.
1. Si el cliente se crea desde una iniciativa, se puede seleccionar a la misma en el campo Desde Iniciativa. 
1. Guardar.

    <img class="screenshot" alt="Create Customer" src="{{docs_base_url}}/assets/img/crm/create-customer.gif">

Se pueden desactivar Ordenes de venta y facturas de venta desde un cliente haciendo click en la opción "Deshabilitado".

También se pueden cargar los detalles del cliente a través de la [Herramienta de Importación de Datos](/docs/user/manual/es/setting-up/data/data-import).

## 2. Características

El flujo general de transacciones para un cliente es como se muestra a continuación: 

<img class="screenshot" alt="Customer" src="{{docs_base_url}}/assets/img/crm/customer-to selling-flowchart.jpeg">

### 2.1 Configuración de Percepciones

En esta sección se deben especificar los Impuestos de percepción a los que está sujeto el Cliente, si corresponde. Para más información visitar [Configuración de Percepciones](/docs/user/manual/es/accounts/configuracion-de-percepciones#23-configuración-del-impuesto-de-percepción-en-el-cliente).

### 2.2 Divisa y Listas de Precios Predeterminadas

ERPNext permite [Múltiples Monedas](/docs/user/manual/es/accounts/multi-currency-accounting) y [Listas de Precio](/docs/user/manual/es/stock/price-lists).

Se puede configurar la moneda predeterminada a ser utilizada para este cliente en las órdenes de venta y facturas de venta seleccionando la moneda adecuada en Moneda de Facturación. 

De forma similar, se puede configurar el listado de precios predeterminado a ser utilizado para este cliente en órdenes de venta y facturas de venta seleccionando la moneda adecuada en Lista de Precios Predeterminada.

### 2.3 Múltiples Contactos y Direcciones

[Contactos](/docs/user/manual/es/CRM/contact) y [Direcciones](/docs/user/manual/es/CRM/address) se almacenan de forma separada para que se puedan adjuntar muchos Contactos y Direcciones al cliente.

### 2.4 Permitir creación de Factura de Venta sin Orden de Venta y Nota de Envío 

Si las opciones "Orden de venta requerida" o "Nota de entrega requerida" se encuentran configuradas como "Si" en las [Configuraciones de Venta](/docs/user/manual/es/selling/selling-settings), estas pueden anularse para un cliente en particular habilitando las opciones "Permitir la creación de facturas de venta sin orden de venta" o "Permitir la creación de facturas de venta sin nota de entrega" en el Cliente. 

<img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/selling/customer-so-dn-required.png">

### 2.5 Contabilidad

A diferencia de otros sistemas contables, no es necesario crear una cuenta por separado para cada cliente. 
De forma predeterminada se creará una cuenta unificada denominada **Deudores**.

Sin embargo, si se necesita específicamente una cuenta por separado para un cliente, primero se debe crear la misma dentro de Cuentas por Cobrar en el [Plan de Cuentas](/docs/user/manual/es/accounts/chart-of-accounts.html) y luego añadirla en la sección CONTABILIDAD del cliente.

> Consejo Avanzado: ERPNext permite la creación de [Asientos contables entre compañías](/docs/user/manual/es/accounts/inter-company-journal-entry). Se pueden utilizar los mismos registros de cliente en múltiples empresas. Como una cuenta es específica de una empresa, se debe seleccionar la empresa y la cuenta correspondiente en la sección CONTABILIDAD si se decide tener una cuenta por separado para un cliente.

### 2.6 Límite de Crédito y Condiciones de Pago

Se puede configurar el límite de crédito ingresando el monto en el campo "Límite de Crédito". Leer [Límite de Crédito](/docs/user/manual/es/accounts/credit-limit) para más detalles.

Se pueden seleccionar las [Condiciones de Pago](/docs/user/manual/es/accounts/payment-terms) predeterminadas a ser aplicadas en órdense de venta y facturas de venta en el campo "Plantilla Predeterminada de Condiciones de Pago".

### 2.7 Equipo y Socio de Ventas

Si se tiene uno o más [Vendedores](/docs/user/manual/es/CRM/sales-person) encargados de administrar la venta al cliente, éstos pueden ser añadidos en la sección EQUIPO DE VENTAS. Si muchos vendedores están involucrados, se puede dividir la contribución entre todos ellos. Tener en cuenta que la suma de todas las contribuciones de los vendedores debe ser igual a 100%. 

Ver [Vendedores en Transacciones de Venta](/docs/user/manual/es/selling/articles/sales-persons-in-the-sales-transactions) para más detalles.

Un [Socio de ventas](/docs/user/manual/es/selling/sales-partner) es un tercero distribuidor/concesionario/comisionista/afiliado/revendedor que facilita la venta de productos o servicios de una empresa, a cambio de una comisión. 
Si la venta de productos de la empresa se realiza a través de un socio, éste puede ser incluido en el campo "Socio de ventas" y mencionar la "Tasa de Comisión" para calcular la comisión. 

### 2.8 Programa de Fidelidad

Si se desea ofrecer un [Programa de lealtad](/docs/user/manual/es/accounts/loyalty-program) al cliente, configurarlo en el campo Programa de Fidelidad. 

### 2.9 Ver Libro Contable y Cuentas por Cobrar

Hacer click en el botón Libro Contable para ver todas las transacciones contables con el cliente. 

Hacer click en Cuentas por Cobrar para ver los detalles de todas las facturas pendientes. 

### 2.10 Configurar Id del Cliente, Categoría de cliente predeterminada, Territorio y Lista de Precios

Se puede configurar cómo se generará la identificación única para el cliente en [Configuraciones de Venta](/docs/user/manual/es/selling/selling-settings).

* **Secuencias e identificadores**: Si se desea que se genere una identidad única para cada cliente de acuerdo con una serie de nombres, seleccionar "Secuencias e identificadores" en "Nombrar cliente por".

* **Nombre del Cliente**: Si se desea usar el mismo nombre del cliente como id, seleccionar "Nombre del Cliente" en "Nombrar cliente por". En este caso, si se crean dos clientes con nombres idénticos, se añadirá el sufijo **- 1** al segundo cliente.

<img class="screenshot" alt="Customer" src="{{docs_base_url}}/assets/img/crm/customer-with-identical-names.png">

Se puede configurar el grupo de clientes predeterminado, territorio y lista de precios en [Configuraciones de Venta](/docs/user/manual/es/selling/selling-settings).


### 3. Temas Relacionados
1. [Categoría de Cliente](/docs/user/manual/es/CRM/customer-group)
1. [Cotización](/docs/user/manual/es/selling/quotation)
1. [Lista de Precios](/docs/user/manual/es/stock/price-lists)
1. [Contacto](/docs/user/manual/es/CRM/contact)
1. [Diferencia entre Iniciativa, Contacto y Cliente](/docs/user/manual/es/CRM/articles/difference_between_lead_contact_and_customer)
