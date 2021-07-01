<!-- add-breadcrumbs -->
# Migrar a Inventario Perpetuo

La Valoración de Inventario Perpetuo se encuentra activada en el sistema de forma predeterminada. 

Para los usuarios que actualmente estén utilizando sistemas de valuación de inventario periódicas y deseen cambiar a sistemas de valuación de inventario perpetuo, seguir los pasos explicados a continuación. 

### 1. Migrar a Inventario Perpetuo

1. Para activar el Inventario Perpetuo, hay que asegurarse que la Cuenta de Existencias Disponibles está sincronizada con el valor de las existencias reales que se encuentran en el Almacén. Para sincronizarla se debe crear un asiento en el libro diario, por la diferencia que exista, con la cuenta de gastos (generalmente utilizada en Factura de Compra) como contrapartida. 

 Por ejemplo, cuando el inventario perpetuo está desactivado, se debe tener la Cuenta de Gastos (Costo de los Bienes Vendidos) registrada a través de las Facturas de Compra. Al activar el inventario perpetuo, se debe crear un asiento en el libro diario para mover el valor de las existencias desde la cuenta de gastos hacia la de existencias disponibles. 

  Cr. Cuenta de Gastos ......... XXX
  
  Dr. Cuenta de Existencias Disponibles ... XXX

  También puede funcionar al revés si se selecciona la cuenta de existencias disponibles en la Factura de Compra. 

2. Antes de habilitar el Inventario Perpetuo, asegurarse que las Cuentas de Existencias están vinculadas al Almacén existente. La cuenta de existencias para un Almacén puede ser configurada en tres niveles.

  * En el Almacén
  * En la sección Almacén Principal
  * Cuenta Predeterminada de Existencias Disponibles en la configuración de la Compañía, si sólo se mantiene una cuenta de Existencias Disponibles para todos los Almacene.
  
3. Asiento de Libro Diario para actualizar la cuenta de Existencias Recibidas pero no Facturadas.

La cuenta "Inventario entrante no facturado" es una cuenta de ajuste que refleja el valor de las existencias para las cuáles se emitió Recibo de Compra pero todavía no se emitió Factura de Compra. Debería crearse un asiento en el libro diario para actualizar el valor de Recibos de compra pendientes de Facturación en la cuenta "Inventario entrante no facturado".

Para saber el valor de las existencias recibidas pero no facturadas, puede utilizarse el informe "Productos Recibidos Pendientes de Facturación" en el módulo de Contabilidad.

 Crear un asiento contable de la siguiente forma para actualizar el valor en la cuenta Inventario entrante no facturado.

  Cr. Inventario entrante no facturado ........... XXX
  
  Dr. Cuenta de Gastos .................. XXX

4. Configurar las siguientes cuentas predeterminadas para cada Empresa 

  * Inventario entrante no facturado
  * Cuenta de Ajuste de Existencias
  * Gastos de valoración
  * Centro de Costos
  * Activar Inventario Perpetuo

5. Ir a: **Inicio > Contabilidad > Compañía**
    
    <img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-1.png">

#### 2. Temas relacionados
1. [Contabilidad de Inventario de Existencias](/docs/user/manual/es/stock/accounting-of-inventory-stock)
1. [Inventario Perpetuo](/docs/user/manual/es/stock/perpetual-inventory)
