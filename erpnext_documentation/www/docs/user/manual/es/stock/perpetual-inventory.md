<!-- add-breadcrumbs -->
# Inventario Perpetuo

De acuerdo con el sistema de inventario perpetuo, se realiza un registro contable por cada transacción de inventario. De otra forma, se realiza en intervalos de tiempo más largos como mensualmente, o cuatrimestralmente. Cada almacén está relacionado con una cuenta principal. 

Al recibir productos en un almacén en particular, el balance en la Cuenta almacén aumentará. De forma similar, cuando se envían productos desde el almacén, se registrará un gasto, y el balance de la Cuenta de almacén se reducirá. 

### 1. Activación del inventario perpetuo

1. Activar Inventario Perpetuo:

    **Inicio > Contabilidad > Compañía > Habilitar Inventario Perpetuo**

    <img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-1.png">
    
    Tener en cuenta que si se deshabilita el inventario perpetuo, los usuarios deberán administrar los registros contables de forma manual. 
1. Configurar las siguientes cuentas predeterminadas para cada Compañía si todavía no fueron configuradas. Estas cuentas son creadas automáticamente en las nuevas cuentas de ERPNext.

    * Cuenta de Inventario Predeterminada (Activo)
    * Productos Recibidos Pero No Facturados (Pasivo)
    * Cuenta de Ajuste de Inventario (Gasto)
    * Gastos Incluidos en la Valoración (Gasto)
    * Centro de Costos

1. Si el usuario quiere configurar una cuenta individual para cada almacén, crear cuenta principal para cada cuenta. Ir a: 

    **Contabilidad > Plan de Cuentas > Compañía > Aplicación de Fondos (Activos) > Activos Corrientes > Activos de Inventario > *Crear una nueva cuenta con el mismo nombre que el almacén***

    Ahora, ir a un almacén y vincular esta cuenta al almacén. Esto ayuda a filtrar y ver informes en base a los almacenes. 

1. Para transacciones de inventario, los registros son realizados en el libro contable en relación a la Cuenta Principal configurada en el almacén. Si el usuario no configuró esta cuenta para el almacén, entonces el sistema obtiene la cuenta principal desde el almacén principal. Si no se configuró una Cuenta para el almacén principal, entonces el sistema toma la cuenta (Cuenta de Inventario Predeterminada) desde la configuración de la Compañía. 

* * *

### 2. Ejemplo

Considérese el siguiente Plan de Cuentas y configuración de almacén para la empresa: 

Plan de Cuentas:

* Activos (Débito)
    * Activos Corrientes
        * Cuentas por Cobrar
            * Deudores
        * Activos de inventario
            * Tiendas
            * Productos Finales
            * Trabajo en Curso
        * Activos Impositivos
            * IVA
* Pasivos (Crédito)
    * Pasivos Corrientes
        * Cuentas a Pagar
            * Acreedores
        * Pasivos de inventario
            * Productos Recibidos Pero No Facturados
        * Pasivos Impositivos
            * Impuesto sobre Servicios
* Ingresos (Crédito)
    * Ingreso Directo
        * Cuenta de Ventas
* Gastos (Débito)
    * Gastos Directos
        * Gastos de inventario
            * Costo de Bienes Vendidos
            * Gastos Incluidos en la Valoración
            * Ajuste de Inventario
    * Gastos Indirectos
        * Gastos de Envío
        * Derechos Aduaneros

#### 2.1 Almacén - Configuración de Cuenta

  * Tiendas
  * Trabajo en Curso
  * Productos Finales

#### 2.2 Recibo de Compra

Suponiendo que se compraron _10 unidades_ del producto "RM0001" a _$200_ y _5 unidades_ del producto "Base Plate" a **$100** del proveedor "Arcu Vel Quam Fabricators". A continuación están los detalles del Recibo de Compra:

**Proveedor:** Arcu Vel Quam Fabricators

**Productos:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Producto</th>
            <th>Almacén</th>
            <th>Cantidad</th>
            <th>Precio</th>
            <th>Monto</th>
            <th>Monto de Valoración</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Tienda</td>
            <td>10</td>
            <td>200</td>
            <td>2000</td>
            <td>2250</td>
        </tr>
    </tbody>
</table>
<p><strong>Impuestos:</strong>
</p>
<table class="table table-bordered">
    <thead>
        <tr>
            <th>Cuenta</th>
            <th>Monto</th>
            <th>Categoría</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Gastos de Envío</td>
            <td>100</td>
            <td>Total y Valoración</td>
        </tr>
        <tr>
            <td>IVA (10%)</td>
            <td>200</td>
            <td>Total</td>
        </tr>
        <tr>
            <td>Derechos Aduaneros</td>
            <td>150</td>
            <td>Valoración</td>
        </tr>
    </tbody>
</table>

**Mayor de Inventario**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-receipt-sl-1.png">

**Libro Contable**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-receipt-gl-2.png">

A medida que aumenta el balance de inventario a través del Recibo de Compra, las cuentas "Tienda" son debitadas y una cuenta temporal "Productos Recibidos Pero No Facturados" es acreditada para mantener el sistema contable de partida doble. Al mismo tiempo, el gasto negativo es registrado en la cuenta principal con la categoría de "Valoración" o "Total y Valoración" en la tabla de impuestos y gastos por el monto añadido con fines de valuación para evitar el registro doble de gastos. 

#### 2.3 Factura de Compra

Al recibir una Factura del proveedor para el Recibo de Compra anterior, se realizará una Factura de Compra por lo mismo. Los registros en el Libro Contable son como se muestran a continuación:

**Libro Contable**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-pinv-gl-3.png">

Aquí la cuenta "Productos Recibidos Pero No Facturados" es debitada y anulada por efecto del Recibo de Compra.

#### 2.4 Nota de Entrega

Se tiene una orden de "Utah Automation Services" para enviar 5 unidades del producto "RM0001" a $300. A continuación los detalles de la Nota de Entrega:

**Cliente:** Utah Automation Services

**Productos:**
<table class="table table-bordered">
    <thead>
        <tr>
            <th>Producto</th>
            <th>Almacén</th>
            <th>Cantidad</th>
            <th>Precio</th>
            <th>Monto</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Tiendas</td>
            <td>5</td>
            <td>300</td>
            <td>1500</td>
        </tr>
    </tbody>
</table>
<p><strong>Impuestos:</strong>
</p>
<table class="table table-bordered">
    <thead>
        <tr>
            <th>Cuenta</th>
            <th>Monto</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Impuesto de Servicios</td>
            <td>150</td>
        </tr>
        <tr>
            <td>IVA</td>
            <td>100</td>
        </tr>
    </tbody>
</table>

**Mayor de Inventario**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-dn-sl-4.png">

**Libro Contable**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-dn-gl-5.png">

Cuando un producto es enviado desde el almacén "Tiendas", la cuenta "Tiendas" es acreeditada y un monto equivalente se debita de la cuenta de gastos "Costo de Bienes Vendidos". El monto debitado/acreeditado es igual al monto total de valoración (costo de compra) de los productos vendidos. Y el monto de valoración es calculado de acuerdo al método de valoración elegido (FIFO / Promedio Móvil) o al costo real de los productos seriados. 



    En este ejemplo, tomamos como método de valoración FIFO.
    Tarifa de Valoración  = Precio de Compra + Gastos Incluidos en Valoración
                    = 200 + (250 / 10)
                    = 225
    Monto Total de Valoración  = 220 * 5
                            = 1125



* * *

### 2.5 Facturas de Venta con Actualización de inventario 

Digamos que no se realizó una Nota de Entrega desde la orden anterior sino que se generó una Factura de Venta directamente con la opción "Actualizar Stock". Los detalles de la Factura de Venta son los mismos que los de la Nota de Entrega mostrada más arriba. 

**Mayor de Inventario**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-inv-sl-6.png">

**Libro Contable**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-inv-gl-7.png">

Aquí, además de los registros contables normales para una factura, las cuentas "Tiendas" y "Costo de Bienes Vendidos" también son afectadas en base al monto de valoración. 

#### 2.6 Entrada de Inventario (Recepción de Material)

**Productos:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Producto</th>
            <th>Almacén de Destino</th>
            <th>Cantidad</th>
            <th>Precio</th>
            <th>Monto</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Tiendas</td>
            <td>50</td>
            <td>220</td>
            <td>11000</td>
        </tr>
    </tbody>
</table>

**Mayor de Inventario**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-receipt-sl.png">

**Libro Contable**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-receipt-gl.png">

#### 2.7 Entrada de Inventario (Expedición de Material)

**Productos:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Producto</th>
            <th>Almacén de Origen</th>
            <th>Cantidad</th>
            <th>Precio</th>
            <th>Monto</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Tiendas</td>
            <td>10</td>
            <td>220</td>
            <td>2200</td>
        </tr>
    </tbody>
</table>

**Mayor de Inventario**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-issue-sl.png">

**Libro Contable**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-issue-gl.png">

#### 2.8 Entrada de Inventario (Transferencia de Material)

**Productos:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Producto</th>
            <th>Almacén de Origen</th>
            <th>Almacén de Destino</th>
            <th>Cantidad</th>
            <th>Precio</th>
            <th>Monto</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Tiendas</td>
            <td>Trabajo en Curso</td>
            <td>10</td>
            <td>220</td>
            <td>2200</td>
        </tr>
    </tbody>
</table>

**Mayor de Inventario**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-transfer-sl.png">

**Libro Contable**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-transfer-gl.png">

#### 3. Temas Relacionados
1. [Contabilidad de Existencias en Inventario](/docs/user/manual/es/stock/accounting-of-inventory-stock)
1. [Migrar a Inventario Perpetuo](/docs/user/manual/es/stock/articles/migrate-to-perpetual-inventory)
