# Ajuste por inflación

Con esta herramienta es posible hacer el ajuste por inflación de cuentas patrimoniales y de resultados. Permite consultar, evaluar o revertirlo en caso de que no sea correcto. 

## 1. Configuración

### 1.1. Cuentas

Primero es necesario definir en el sistema cuáles son las cuentas No monetarias, que son las que se van a ajustar.

Para esto se debe ingresar a *Inicio > Contabilidad > Plan de Cuentas*, seleccionar la cuenta que se desea ajustar, hacer click Editar y tildar la opción **Genera Ajuste por Inflación**.

Esto se debe hacer por cada cuenta No monetaria que se desea ajustar en el Ajuste por inflación.

### 1.2. Indice RT6

Es necesario crear los índices de cada mes, con el IPC correspondiente.
Para esto ingresar a *Inicio > Contabilidad > Ajuste por inflación > Indice RT6*, hacer click en nuevo e ingresar los datos correspondientes a cada uno de ellos.


## 2. Creación del Ajuste

Una vez completados los pasos anteriores, es posible efectuar el ajuste.

Para crear el ajuste se debe ingresar a  *Inicio > Contabilidad > Ajuste por inflación > Ajuste por inflación* y hacer click en Nuevo.

Completar los siguientes datos:
* **Compañía**: es la compañía a la cual se efectuará el ajuste.
* **Indice**: es el que se tomará para armar el coeficiente y calcular los ajustes.
* **Fecha desde y Fecha hasta**: son las fechas que conformarán el período a ajustar.
* **Cuenta de ajuste**: se debe indicar la cuenta en la que se imputará el ajuste por inflación (generalmente RECPAM / REI ).
* **Fecha de asiento contable**: es la fecha que se imputará el asiento contable generado por ajuste.

> IMPORTANTE:  se requiere que se haya realizado el cierre de cuentas patrimoniales del ejercicio cerrado y la apertura de cuentas del periodo actual para que te muestre correctamente los saldos a ajustar. 

Una vez completado, se debe Guardar y luego Validar. Esto habilitará entonces el botón Crear Ajuste.


Al presionar este botón se accede a una pantalla donde es posible revisar todos los cálculos, antes de que se cree el Asiento contable.

**Pantalla de control**

Aquí se puede revisar por cada cuenta, y en cada mes, el ajuste del período y el saldo que quedaría al cierre.

Por defecto tiene tildado la opción No mostrar valores en cero, la cual omite y oculta cualquier mes de cada cuenta que no tenga movimientos.

También se puede optar por la opción Mostrar solo totales, donde se ven únicamente los totales de cada cuenta.

Es posible descargar este reporte en excel, csv o pdf, para su propio control, desde la opción Menú - Exportar.

Una vez que controlados los resultados, se pasa a generar el Asiento contable presionando el botón Generar ubicado arriba a la derecha.

**Asiento contable**

Se generan los movimientos contables teniendo en cuenta las siguientes consideraciones:

* Se genera un asiento por cada cuenta por el período indicado en los parámetros
* Se le asigna la fecha que configuró al inicio.
* El asiento será de tipo Ajuste por inflación.
* El importe del asiento surge de la columna Ajuste del periodo. El importe de ajuste para la cuenta de partida, se imputa en el mismo signo o columna (debe, haber) en que se encontraba el saldo. La cuenta de contrapartida (REI) se imputa con signo contrario. 


## Consideraciones:

* Si se generó el Ajuste por inflación y quedó en la Pantalla de control, es decir, no se creó todavía el asiento contable, se puede retomar en cualquier momento, dirigiéndose al módulo Factura Electrónica -Informes Estándares - Ajuste por inflación, eligiendo el ajuste que tiene como nombre la fecha del último mes.
* Si se generó el asiento contable de ajuste pero resulta que algún dato era incorrecto, es posible eliminarlo cancelando el Ajuste por inflación que lo generó.

* En el Balance General o Libro Mayor, hay una opción para ocultar los ajustes por inflación del mismo.

* Es posible generar asientos contables de Ajuste por inflación manualmente, en el caso de que los cálculos se realicen por fuera del sistema, teniendo en cuenta solamente de elegir como Tipo de Asiento: Ajuste por inflación.
