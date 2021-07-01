<!-- add-breadcrumbs -->

# Facturas entre compañías

**Las facturas entre compañías son realizadas entre organizaciones que pertenecen al mismo grupo.**

Además de poder crear facturas de compra y de venta para una sola compañía, se pueden crear facturas vinculadas entre sí para múltiples organizaciones.

Por ejemplo, se puede crear una Factura de compra para una compañía "ABC", una Factura de venta contra dicha factura para la compañía "XYZ" y vincularlas.

## 1. Creación de Facturas entre compañías

### 1.1 Configuración
1. Ir a: **Contabilidad > Maestros > Clientes**.
1. Seleccionar el Cliente correspondiente.
1. Tildar la opción **"Es Cliente Interno"**

 <img class="screenshot" alt="Internal Customer" src="{{docs_base_url}}/assets/img/accounts/make-internal-customer.png">

4. Agregar la Compañía a la cual representa el Cliente en el campo **"Representa a la Compañía"**. Esta es la compañía para la cual se crearán las facturas de venta, considerese compañía "B".
1. En la tabla **"Permitido para realizar transacciones con"** agregar la compañía para la cual se van a crear la facturas de compra (compañía "A"). 
1. Al crear una factura de compra para la compañía A, esta se vinculará a la factura de venta para la compañía A creada usando este Cliente interno de la compañía B.
1. A continuación se debe hacer algo similar para configurar el Proveedor.
1. Ir a: **Contabilidad > Maestros > *Seleccionar el Proveedor***
1. Tildar la opción **"Es un Proveedor Interno"**.
1. En el campo **"Representa a la Compañía"**, agregar la compañía que se seleccionó en la tabla **"Permitido para realizar transacciones con"** del Cliente.
1. En la tabla **"Permitido para realizar transacciones con"** del Proveedor, seleccionar la compañía a la cual representa el Cliente. Esta es la compañía contra la cual se va a realizar la factura de compra.

 <img class="screenshot" alt="Internal Supplier" src="{{docs_base_url}}/assets/img/accounts/make-internal-supplier.png">

### 1.2 Creación de la factura
1. Crear una nueva [Factura de venta](/docs/user/manual/es/accounts/sales-invoice) completando los campos necesarios.
1. Se debe recordar seleccionar el cliente que es Cliente Interno y la compañía para la cual está comprando.
1. Guardar y validar.

 <img class="screenshot" alt="Inter company invoice" src="{{docs_base_url}}/assets/img/accounts/make-inter-company-invoice.png">

4. Antes de hacer una *Factura entre compañías* se debe realizar lo siguiente:
    1. Los precios para la compra y para la venta entre compañías deberían estar sincronizados.
    1. Ir a **Almacén > Lista de precios**, crear una nueva lista para transacciones entre compañías.
    1. Tildar tanto la opción "Compras" como "Ventas" en esta nueva lista.
    1. Ir a **Compras > Proveedor > *Proveedor Interno***, en la sección Divisa y listas de precios, seleccionar la lista de precios recién creada.
    1. Hacer lo mismo para el Cliente interno.
1. Al validar la factura, debajo del botón **Crear** aparecerá **Factura entre compañías**. Al hacer click se redirigirá a una nueva Factura de compra.
1. Aquí, el proveedor y la compañía serán automáticamente traídos dependiendo de la compañía que se haya seleccionado en la factura de venta.
> ***Recordar**: solo puede haber un único Cliente o Proveedor interno por compañía.*
7. Al validar la factura, ambas quedan vinculadas entre sí. *Al cancelar alguna de las facturas se las desvinculará automáticamente.*

> Nota: Una factura entre compañías solo afectará la contabilidad pero no el stock. Esto es porque ambas compañías pertenecen al mismo grupo.

Se puede seguir el mismo proceso para crear una Factura de compra y luego vincularla a la nueva Factura de venta.

### 2. Temas relacionados
1. [Factura de venta](/docs/user/manual/es/accounts/sales-invoice)
1. [Factura de compra](/docs/user/manual/es/accounts/purchase-invoice)
1. [Asiento contable entre compañías](/docs/user/manual/es/accounts/inter-company-journal-entry)
