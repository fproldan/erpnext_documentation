<!-- add-breadcrumbs -->
# Descuento de facturas

**El Descuento de facturas es la práctica de usar las facturas de venta impagas como garantía para préstamos a corto plazo generado por un banco o entidad financiera.**

Para acceder la lista de Descuento de facturas, ir a:
> Inicio > Contabilidad > Banco y pagos > Descuento de facturas

## 1. Prerrequisitos

Se debe crear las siguientes cuentas para poder registrar transacciones de descuento de facturas.

* **Préstamo a corto plazo:** una cuenta bajo "Pasivo corriente" > "Préstamos (Pasivos)".
* **Cuenta de cargos bancarios:** una cuenta de gasto para cargos impuestos por el banco.
* **Cuenta de cobro de crédito:** una cuenta de control de tipo "A cobrar".
* **Cuenta de cobro de descuento:** una cuenta a cobrar para facturas que fueron descontadas.
* **Cuenta de cobro impagas:** una cuenta a cobrar para facturas que fueron descontadas y continúan impagas luego de haber finalizado el período del préstamo.

## 2. Creación de Transacciones de descuento de facturas

1. Ir al listado de Descuentos de facturas y hacer click en Nuevo.
1. Ingresar la Fecha de Contabilización y la Fecha de inicio del préstamo. Ingresar el Periodo de préstamo (días).
1. Seleccionar facturas ya sea manualmente en la tabla o haciendo click en el botón "Obtener facturas" arriba a la derecha.
1. Seleccionar la cuenta de Préstamo a corto plazo, cuenta bancaria y cuenta de cargos bancarios.
1. Seleccionar Cuenta de cobro de crédito, Cuenta de cobro de descuento y Cuenta de cobro impagas.
1. Guardar y validar.
1. Luego de validar el Descuento de factura, hacer click en **Desembolso del préstamo**.

  <img class="screenshot" alt="Lead" src="{{docs_base_url}}/assets/img/accounts/invoice_discounting.png">
  
8. Se llevará a un [Asiento contable](/docs/user/manual/es/accounts/journal-entry), el cual debe ser guardado y validado.

  ![Journal Entry](/docs/assets/img/accounts/invoice-discounting-je.png)
  
## 2. Funcionalidades

### 2.1 Importar facturas
Hacer click en "Obtener facturas" para importarlas. Se puede importar filtrando por ciertos criterios:

* Facturas creadas contra un Cliente específico.
* Rango de fechas en el cual las facturas fueron creadas.
* Monto mínimo y máximo.

Se pueden especificar múltiples filtros combinados.

### 2.2 Cierre del préstamo
Cuendo se paga el préstamo al final del período del mismo o antes de esa fecha, se lo puede actualizar haciendo click en el botón "Cerrar préstamo".

  ![Journal Entry](/docs/assets/img/accounts/invoice-discounting-disbursed.png)
  
El sistema preparará el Asiento contable. Revisar y validar.

### 2.3 Actualizar automáticamente las cuentas al final del período del préstamo
Si el préstamo no fue pagado al fin del período, el sistema creará un Asiento contable para cambiar el valor de "Cuenta de cobro de descuento" a "Cuenta de cobro impagas". Esto permitirá rastrear las facturas que fueron descontadas y continúan impagas.
