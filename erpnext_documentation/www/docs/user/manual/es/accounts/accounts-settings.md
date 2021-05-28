<!-- add-breadcrumbs -->
# Configuración de cuentas

ERPNext da la posibilidad de configurar y restringir ciertas acciones dentro del módulo de contabilidad.

![Account Settings]({{docs_base_url}}/assets/img/accounts/account-settings.png)

## 1. Cuentas congeladas hasta
Se congelan las transacciones hasta la fecha especificada. Nadie puede crear/modificar entradas contables, salvo el rol seleccionado a continuación.

## 2. Rol que permite definir cuentas congeladas y editar asientos congelados
Los usuarios con este rol tienen permiso para congelar cuentas y crear/modificar entradas contables contra cuentas congeladas.

## 3. Determinar la categoría de impuestos de la dirección de
La [Categoría de impuesto](/docs/user/manual/es/accounts/tax-category) puede establecerse en la dirección. Una dirección puede ser de envío o de facturación. En este campo se define desde qué tipo de dirección se tomará la Categoría de impuesto.

## 4. Porcentaje permitido de sobrefacturación
Porcentaje por el cual se puede sobrefacturar transacciones. Por ejemplo, si el valor de la orden es de $100 por un producto y el porcentaje especificado en este campo es de 10%, entonces está permitido facturar con un precio de $110.

## 5. Rol que tiene permitido sobrefacturar
Los usuarios que posean este rol pueden facturar sobrepasando el procentaje permitido.

## 6. Controlador de créditos
Aquí se selecciona el rol que tiene permitido crear transacciones que exceden el límite de crédito establecido. El límite de crédito puede determinarse por cliente.

## 7. Comprobar número de factura único por proveedor
Al tildar esta opción no se permitirá la creación de Facturas de compra con el mismo 'Factura de proveedor No.'. Esto es útil para evitar entradas duplicadas. 

## 8. Realizar pago mediante asiento contable
Al tildar esta opción, si un usuario realiza un pago desde una factura, el sistema generará un Asiento contable en lugar de una Entrada de pago.

## 9. Desvinculación de pago en la cancelación de la factura
Al tildar esta opción, el sistema desvinculará el pago contra la Factura cancelada. Por defecto, si una Entrada de pago está validada, la Factura vinculada no puede ser cancelada hasta que la Entrada de pago sea igualmente cancelada. Al desvincularse, es posible cancelar y corregir las Facturas. Por su parte, los pagos quedan desvinculados y son considerados pagos adelantados.

## 10. Desvinculación de pago adelantado en la cancelación de la orden
Similar a la opción anterior, esta configuración desvincula cualquier pago adelantado hecho sobre Ordenes de venta o de compra. 

## 11. Entrada automática de depreciación de bienes
Cuando esta opción está tildada, se creará automáticamente una entrada contable por depreciación de bienes en la primera fecha especificada. Por ejemplo, se puede programar la creación de una entrada de depreciación anual por los próximos 3 o 4 años dependiendo del número de depreciaciones registradas especificado en el master de bienes. Para más detalles, visitar la página [Depreciación de bienes](/docs/user/manual/en/asset/asset-depreciation).

## 12. Permitir centro de costo en entrada de cuenta de balance
Si esta opción está tildada, se podrá registrar entradas en cuentas de la Hoja de balance hechas contra Centro de costos. Por defecto el Centro de costos está sólo disponible para cuentas de ganancia o pérdida.

## 13. Añadir automáticamente Impuestos y cargos desde la Plantilla de impuestos
Habilitando esta opción se completará automáticamente la tabla de Impuestos de las transacciones con los valores correspondientes según la [Plantilla de impuestos](/docs/user/manual/es/accounts/item-tax-template) del Producto seleccionado.

## 14. Traer automáticamente Términos de pago
Habilitar esta configuración hará que se traigan automáticamente los Términos de pago del Proveedor. 

## 15. Ajustes de impresión

![Account Settings]({{docs_base_url}}/assets/img/accounts/account-settings-1.png)

* **Mostrar impuesto incluído en la impresión**: los impuestos incluídos serán mostrados en la vista de impresión.
* **Mostrar cronograma de pago en la impresión**: el cronograma de pagos generado por los [Términos de pago](/docs/user/manual/es/accounts/payment-terms) estará visible en la impresión.

## 16. Permitir Tipos de cambio obsoletos
Esta opción debería estar destildada si se desea validar la vigencia del Tipo de cambio en transacciones de exportación. En ese caso, el campo Tipo de cambio será de sólo lectura.

Días Pasados es el número de días usado para decidir si un Cambio de divisas ya no es válido. Este campo se muestra sólo cuando 'Permitir Tipos de Cambio Obsoletos' está **deshabilitado**. Entonces, si Días Pasados es igual a 10, se considerarán válidos tipos de cambio de hasta 10 días de antigüedad. Si 'Permitir Tipos de Cambio Obsoletos' está tildado, no hay límite de antigüedad para los Tipos de cambio.

Si la opción está tildada, los Tipos de cambio serán traídos en el siguiente orden:

* Último Tipo de cambio entre los Cambios de divisa
* Si no se encuentra ningún Cambio de divisa será tomado el último Tipo de cambio del mercado

Si la opción está destildada, los Tipos de cambio serán traídos en el siguiente orden:

* Último Tipo de cambio entre los Cambios de divisa con antigüedad menor a "Días Pasados"
* Si no se encuentra ningún Cambio de divisa será tomado el último Tipo de cambio del mercado


## 17. Utilice el formato de Flujo de fondos personalizado
Seleccionando esta opción se podrá personalizar la información presentada en el reporte de Flujo de fondos. Para saber más, [visitar esta página](/docs/user/manual/en/accounts/articles/how-to-customise-cash-flow-report).
