<!-- add-breadcrumbs -->
# Tipo de cambio

En ERPNext, mediante el Tipo de cambio se almacenan tasas de cambio generadas manualmente. Por defecto, el sistema trae automáticamente los cambios de divisas actualizados del mercado. Sin embargo, se pueden guardar y usar cambios de divisas fijos. Para esto se debe tildar la opción "Permitir Tipos de Cambio Obsoletos" en la Configuración de cuentas para poder utilizar tasas de cambio almacenadas en el Tipo de cambio.

Para acceder a la lista de Cambios de divisa, ir a:
> Inicio > Contabilidad > Multimoneda > Tipo de cambio

## 1. Creación de Tipo de cambio
1. Ir a la lista de Tipo de cambio y hacer click en Nuevo.
1. Ingresar una fecha desde la cual este Tipo de cambio será válido. Los Cambios con fecha más cercana serán usados en las transacciones.
1. Seleccionar los valores correspondientes para los campos "Desde Moneda" y "A moneda".
1. Ingresar el Valor de cambio, por ejemplo, si 1 USD = 65 ARS entonces ingresar 65.
1. Determinar si el Cambio aplica a ventas, compras o ambas.
1. Guardar.

    ![Currency Exchange](/docs/assets/img/accounts/currency-exchange.png)

## 2. Temas relacionados
1. [Revalorización del tipo de cambio](/docs/user/manual/es/accounts/exchange-rate-revaluation)
1. [Contabilidad con múltiples divisas](/docs/user/manual/es/accounts/multi-currency-accounting)
