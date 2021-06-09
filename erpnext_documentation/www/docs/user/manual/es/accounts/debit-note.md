<!-- add-breadcrumbs -->
# Nota de débito

**Una Nota de débito es un documento enviado al proveedor notificando que se ha registrado un débito respecto a los bienes devueltos al mismo.**

El monto de la Nota de débito será igual al valor de los productos devueltos. En algunos casos, los vendedores envían Notas de débito que deberán ser tratadas como cualquier otra factura.

## 1. Creación de una Nota de débito

Se puede hacer una Nota de débito contra la Factura de compra o directamente desde la misma sin referencia.

1. Ir a la Factura de compra correspondiente y hacer click en **Crear > Retorno / Nota de Débito**.
 ![Debit Note from Invoice](/docs/assets/img/accounts/debit-note-from-invoice.png)
1. Los detalles del proveedor y del producto serán traídos desde la Factura.
1. Si se había realizado el pago por la compra, ya sea de forma completa o parcial, se deberá generar una Entrada de pago contra la factura original.
1. Guardar y validar.
 <img class="screenshot" alt="Sales Invoice" src="{{docs_base_url}}/assets/img/accounts/debit-note.png">

Los demás pasos son similares a los de una [Factura de compra](/docs/user/manual/en/accounts/purchase-invoice).


### 1.1 Impacto contable de la Nota de débito
Una vez que el pago es creado contra la factura original, el monto será agregado a la cuenta del Proveedor con signo negativo de forma que en la próxima compra al mismo, el valor se ajuste automáticamente. 

Esta es la forma en que el balance general es afectado al registrarse el pago de una factura devuelta:
![Debit Note Ledger](/docs/assets/img/accounts/debit-note-ledger.png)

Más información al respecto en la página de [Factura de compra](/docs/user/manual/en/accounts/purchase-invoice).


## 2. Ejemplo
Se realizó la compra de algodón por $2400 + impuestos; pero al recibir los productos se nota que el producto no está en condiciones. Al devolverlo, se debe generar la Nota de débito en el sistema.

### 3. Temas relacionados
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Nota de crédito](/docs/user/manual/es/accounts/credit-note)
