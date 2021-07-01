<!-- add-breadcrumbs -->
# Límite de crédito

**El límite de crédito define el monto máximo de crédito que se ofrece a cada Cliente.**

En términos generales es el monto máximo que una institución financiera u otro prestamista está dispuesto a otorgar a un deudor por una línea de crédito en particular. En el caso de un Cliente, es el monto máximo de bienes o servicios que puede obtener sin realizar el pago de forma inmediata.

Esta valor se puede definir en el Cliente, Categoría de Cliente y en la Compañía.
Al validar una Orden o Factura de venta, se controlará si este límite es sobrepasado.

El orden de precedencia para este control es el siguiente:

* Límite de crédito del Cliente
* Límite de crédito de la Categoría de Cliente
* Límite de crédito de la Compañía


## 1. Configuración del Límite de crédito
1. Ir a: **Ventas > Clientes > Cliente**.
1. En la sección "LÍMITE DE CRÉDITO Y CONDICIONES DE PAGO", establecer el "Límite de Crédito" deseado.
1. Si se deja este valor en 0, no tendrá efecto alguno.
1. Guardar.

    <img class="screenshot" alt="Credit Limit" src="{{docs_base_url}}/assets/img/accounts/customer-credit-limit.png">

## 2. Características
### 2.1 Controlador de créditos
Se puede dar permiso a usuarios con un rol específico para saltearse esta validación y poder generar Ordenes o Facturas de venta incluso cuando el Cliente llegó a su límite de crédito.

Para definir el rol de Controlador de créditos:

1. Ir a: **Contabilidad > Configuración > Configuración de cuentas**
1. Seleccionar el rol deseado en el campo Controlador de créditos.

<img class="screenshot" alt="Credit Limit" src="{{docs_base_url}}/assets/img/accounts/credit_controller_role.png">

### 2.2 Evitar el control de límite de crédito en la Orden de Venta

Para Clientes específicos se puede configurar para que este control se realice solo sobre el acumulado de Facturas de venta y no se tenga en cuenta a las Ordenes de venta. Para esto se debe tildar la opción "Evitar el control de límite de crédito en la Orden de Venta" en la sección correspondiente dentro del Cliente.

<img class="screenshot" alt="Customer Credit Limit" src="{{docs_base_url}}/assets/img/accounts/customer-credit-limit-bypass.png">


### 2.3 Límite de Crédito por Categoría de Cliente
Para establecer este límite por Categoría de clientes:

1. Ir a **Ventas > Clientes > Categoría de cliente**.
1. Abrir la categoría deseada y establecer el valor en el campo Límite de crédito.

### 2.4 Límite de Crédito por Compañía
Al definir este valor en la Compañía, todos los Clientes de la misma tendrán el mismo Límite de crédito.

Para establecer este límite por Compañía:

1. Ir a **Contabilidad > Empresa y Contabilidad > Compañía**.
1. Abrir la Compañía y completar el campo Límite de Crédito.

### 3. Temas relacionados
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Cliente](/docs/user/manual/es/CRM/customer)
