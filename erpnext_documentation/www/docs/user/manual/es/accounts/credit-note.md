<!-- add-breadcrumbs -->
# Nota de Crédito


## 1. Nota de Crédito contra Factura de venta

**Una Nota de Crédito es un documento enviado por el vendedor al Cliente notificando que se generó un crédito en su cuenta contra los bienes devueltos por el comprador.**

La Nota de crédito se genera por el valor de los bienes devueltos por el Cliente, el cual puede ser menor o igual al monto total de la Orden. 

### 1.1. Creación de Notas de Crédito

Se puede hacer una Nota de Crédito contra la Factura de venta o directamente desde una factura de ventas nueva tildando la opción Es una Nota de Crédito (en este caso se debe completar manualmente el campo Comprobante asociado). Tener en cuenta que para crear una Nota de Crédito la factura debe estar pagada mediante una [Entrada de pago](/docs/user/manual/es/accounts/payment-entry).

1. Ir a la Factura de venta deseada y hacer click en **Crear > Devolución/Nota de Crédito**.
    ![Credit Note from Invoice](/docs/assets/img/accounts/credit-note-from-invoice.png)
1. Los detalles del Cliente y del Producto serán traídos de la Factura de Venta.
1. Si el Cliente pagó, de forma parcial o completa, se debe hacer la Entrada de pago contra la factura original.
1. Guardar y validar.
    <img class="screenshot" alt="Sales Invoice" src="{{docs_base_url}}/assets/img/accounts/credit-note.png">

La cantidad y el precio del producto serán negativos ya que es una devolución.

#### 1.1.1 Impacto contable de la Nota de crédito
Una vez que la Entrada de pago es creada contra la Factura de venta original, el monto será agregado en la cuenta del Cliente con signo negativo de forma que en su próxima compra el valor se ajuste automáticamente. 

Esta es la forma en que el balance general es afectado al registrarse el pago de una factura devuelta:
![Credit Note Ledger](/docs/assets/img/accounts/credit-note-ledger.png)

Se encontrará más información en la página de [Facturas de venta](/docs/user/manual/es/accounts/sales-invoice).

### 1.2. Ejemplo

Un cliente compró caños PVC por $3000 + impuestos, pero al recibir sus productos notó que estaban dañados. Al efectuarse la devolución de los mismos se debe generar en el sistema una Nota de crédito.


## 2. Nota de Crédito contra Factura de compra

**Una Nota de Crédito es un documento enviado al proveedor notificando que se ha registrado un crédito respecto a los bienes devueltos al mismo.**

El monto de la Nota de Crédito será igual al valor de los productos devueltos. En algunos casos, los vendedores envían Notas de Crédito que deberán ser tratadas como cualquier otra factura.

### 2.1. Creación de una Nota de Crédito

Se puede hacer una Nota de Crédito contra la Factura de compra o directamente desde la misma sin referencia tildando la opción Es una Nota de Crédito.

1. Ir a la Factura de compra correspondiente y hacer click en **Crear > Retorno / Nota de Crédito**.
 ![Debit Note from Invoice](/docs/assets/img/accounts/debit-note-from-invoice.png)
1. Los detalles del proveedor y del producto serán traídos desde la Factura.
1. Si se había realizado el pago por la compra, ya sea de forma completa o parcial, se deberá generar una Entrada de pago contra la factura original.
1. Guardar y validar.
 <img class="screenshot" alt="Sales Invoice" src="{{docs_base_url}}/assets/img/accounts/debit-note.png">

Los demás pasos son similares a los de una [Factura de compra](/docs/user/manual/en/accounts/purchase-invoice).

#### 2.1.1 Impacto contable de la Nota de Crédito
Una vez que el pago es creado contra la factura original, el monto será agregado a la cuenta del Proveedor con signo negativo de forma que en la próxima compra al mismo, el valor se ajuste automáticamente. 

Esta es la forma en que el balance general es afectado al registrarse el pago de una factura devuelta:
![Debit Note Ledger](/docs/assets/img/accounts/debit-note-ledger.png)

Más información al respecto en la página de [Factura de compra](/docs/user/manual/en/accounts/purchase-invoice).

### 2.2. Ejemplo
Se realizó la compra de algodón por $2400 + impuestos; pero al recibir los productos se nota que el producto no está en condiciones. Al devolverlo, se debe generar la Nota de Crédito en el sistema.


### 3. Temas relacionados
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Nota de Débito](/docs/user/manual/es/accounts/debit-note)
1. [Devoluciones de ventas](/docs/user/manual/es/stock/sales-return)
