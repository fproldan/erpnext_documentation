<!-- add-breadcrumbs -->
# Entradas contables

El concepto de contabilidad se explica con el siguiente ejemplo: Se toma a 
"Tea Stall" como compañía y se observa cómo registrar entradas contables
para el negocio. 

 Juan (propietario de Tea Stall) invierte $25000 para iniciar el negocio.

![A&L](/docs/assets/old_images/erpnext/assets-1.png)

## 1. Inversión
Juan invierte $25000 en la compañía, con la esperanza de obtener alguna
ganancia. En otras palabras, la compañía es responsable del pago de $25000 a Juan en 
el futuro. Así, la cuenta "Juan" es una cuenta de pasivo y es un crédito. El balance de
efectivo de la compañía incrementará debido a la inversión. "Caja" es un activo de
la compañía y será debitado.

La compañía necesita equipos (cocina, tetera, pocillos, etc) y materia prima (té, 
azúcar, leche, etc) de inmediato. Se decide comprarlos en una tienda cercana "Super Bazaar"
que pertenece a un amigo y le concede cierto crédito. Los equipos cuestan $2800 y la
materia prima vale $2200. La compañía paga $2000 de un total de $5000. Esto puede ser registrado en ERPNext por medio de una [Entrada de pago](/docs/user/manual/es/accounts/payment-entry).
  
![A&L](/docs/assets/old_images/erpnext/assets-2.png)

## 2. Activos
Los equipos son "Activos fijos" (porque tienen una larga vida útil) y la materia prima es "Activo corriente" (porque es usada en la 
operación diaria del negocio). Entonces, "Equipos" y "Existencias disponibles" deben
ser debitadas para incrementar su valor. La compañía pagó $2000, entonces la cuenta
"Caja" debe ser reducida en dicha cantidad, es decir, debe ser crédito. Además, dado que la
compañía tiene la obligación de pagar $3000 a "Super Bazaar", dicha cuenta debe tener
un crédito de $3000.

Juan (quien está pendiente de todas las entradas) decide anotar las ventas al finalizar
cada día, de tal manera que pueda analizar las ventas diarias. Al finaliza el primer
día, Tea Stall vende 325 tazas de té, lo cual da una venta neta de $1625. El propietario
registra feliz su primer día de ventas.

![A&L](/docs/assets/old_images/erpnext/assets-3.png)

## 3. Ingresos
Los ingresos fueron anotados en la cuenta "Ventas de Té", la cual se 
debita para incrementar el valor y la misma cantidad se acredita de la cuenta
"Caja". Digamos que, hacer 325 tazas de té cuesta $800, entonces la 
cuenta "Existencias disponibles" debe ser reducida (crédito) en $800 y el gasto
debe ser registado en la cuenta "Costos de bienes vendidos" en la misma cantidad.

Al finalizar el mes, la compañía paga el alquiler del local ($5000) y el salario de
un empleado ($8000), quien trabajó desde el primer día.

![A&L](/docs/assets/old_images/erpnext/assets-4.png)

## 4. Registro de ganancias

A medida que avanza el mes, la compañía compra más materia prima para el negocio.
Después de un mes se anotan las ganancias en el "Libro de Balance" y en el "Estado de Pérdidas y Ganancias". Ya que las ganancias pertenecen a Juan y no a
la compañía, se considera que son una obligación (la compañía tiene
que pagárselas a Juan). Cuando el Libro de Balance no está balanceado, por ejemplo: el
débito no es igual al crédito, la ganancia aún no ha sido registrada. Para hacerlo, las cuentas de ganancia y pérdidas deben ser reinicializadas. La ganancia/pérdida es tranferida a la cuenta de activo y el estado de pérdidas y ganancias comienza de cero. Esto se realiza creando un [Cierre de período](/docs/user/manual/es/accounts/period-closing-voucher).

![A&L](/docs/assets/old_images/erpnext/assets-5.png)

**Explicación**: Las ventas y gastos netos de la compañía son $40000 y $20000 respectivamente.
Por lo tanto, la compañía tuvo una ganancia de $20000. Para registrar esa ganancia,
la cuenta "Pérdidas y Ganancias" debe ser debitada y la cuenta "Capital"
debe ser acreditada. El balance neto de caja es $44000 y queda alguna materia
prima que vale $1000.


### Temas relacionados
1. [Entrada de pago](/docs/user/manual/es/accounts/payment-entry)
1. [Pagos adelantados](/docs/user/manual/es/accounts/advance-payment-entry)

