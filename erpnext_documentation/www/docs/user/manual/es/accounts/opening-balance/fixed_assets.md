<!-- add-breadcrumbs -->
# Actualización de Activos fijos

Para poder importar los activos fijos primero es necesario crearlos y luego crear un Asiento contable para actualizar el Balance general.

## 1. Creación de un Activo

Se debe crear un Activo por cada bien de la compañía que no esté totalmente amortizado.

Para crear un nuevo Activo:

1. Crear un [Producto](/docs/user/manual/en/stock/item) con la opción "Es activo fijo" tildada.
1. Ir a **Bienes > Activo > Nuevo**.
1. Ingresar el Nombre de activo.
1. Ingresar el Código del producto.
1. Ingresar Ubicación.
1. Ingresar Fecha de compra.
1. Ingresar Importe Bruto de Compra.
1. Tildar **Es Activo Existente**.
1. Guardar.

    <img class="screenshot" alt="Stock Asset Ledger" src="{{docs_base_url}}/assets/img/accounts/asset_opening_balance.png">

> Para conocer más sobre Activos, visitar esta [página](/docs/user/manual/en/asset/asset).

## 2. Creación del Asiento contable para actualizar las cuentas

Al crear un Activo con el tilde de "Es Activo Existente", el Balance general no es actualizado. Se deberá actualizar el valor mediante un Asiento contable.

Para crear un nuevo Asiento contable:

1. Ir a **Contabilidad > Maestros y cuentas > Asiento contable > Nuevo**
1. Ingresar Fecha de Contabilización.
1. Seleccionar las cuentas de activos fijos correspondientes en la columna Cuenta e ingresar el valor en la columna Debe.
1. Seleccionar la cuenta de "Apertura temporaria" en la columna Cuenta e ingresar el importe en la columna Haber.
1. Seleccionar "Sí" en el campo "De apertura".

<img class="screenshot" alt="Stock Asset Ledger" src="{{docs_base_url}}/assets/img/accounts/journal_entry_for_fixed_asset_opening_balance.png">

{next}
