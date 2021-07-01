<!-- add breadcrumbs -->
# Depreciación de Activos

El sistema crea automáticamente un cronograma para la depreciación de acuerdo con el método de depreciación y otros campos como "Fecha disponible para usar" en el registro de Activos. También es posible crear muchos cronogramas de depreciación para distintos Libros de finanzas. Se debe tildar la opción "Calcular Depreciación" al crear un activo para calcular su depreciación, y añadir registros a la tabla de depreciación del mismo. 

<img class="screenshot" alt="Asset" src="{{docs_base_url}}/assets/img/asset/depreciation-schedule.png">

Tipos de depreciación en ERPNext:

* **Línea Recta**: La depreciación se calcula en línea recta y se _distribuye uniformemente_ a lo largo de la frecuencia seleccionada en meses. Por ejemplo, un activo tiene un valor actual de $1000, luego de la depreciación 5 años después tiene un valor de $500. La línea recta establecería el monto depreciado en $100 para cada año. Este método resulta útil cuando no hay un patrón en particular respecto a cómo se realiza la depreciación durante un período de tiempo. 

* **Saldo doblemente decreciente**: Este también se conoce como el balance 200% decreciente. En este método, se deprecia un 20% del valor existente cada vez. Por ejemplo, si el activo vale $1000, valdrá $800 en el próximo período, luego el 20% de $800 sería $160 por ende el activo valdrá $640, y así hasta que se alcanza el valor final. Si se comienza a mitad de año, se calculará el 10% de depreciación. Este método es útil cuando el activo se deprecia más rápidamente en sus primeros años y luego baja el ritmo de depreciación. 

* **Valor Escrito**: Se establece un porcentaje fijo, y el valor del activo se deprecia en ese porcentaje a lo largo de su vida. El porcentaje fijo siempre es calculado sobre el valor actual del activo. Por ejemplo, si el valor es $1000 y el porcentaje es 10%, a lo largo de 5 años se depreciará un 10% cada año para llegar al valor esperado de $600 al final de la vida útil. Es utilizado para vehículos, por ejemplo, ya que se deprecian más en sus últimos años. 

    | Valor Actual | Depreciación | Valor Registrado |
    | -------------- | ----------- | ------------ |
    | 1000 | 100 | 900 |
    | 900 | 90 | 810 |
    | 810 | 80 | 730 |
    | 730 | 70 | 660 |
    | 660 | 60 | 600 |
    | 600 | 50 | 550 |


* **Manual**: En este método se puede definir manualmente la Fecha Programada y el Monto de Depreciación para cada período. 

## 1. Depreciación programada
En la fecha programada, el sistema crea un registro de depreciación al crear un Asiento contable y ese mismo Asiento es mostrado en la tabla de depreciación a forma de referencia. La Siguiente Fecha de Depreciación y el Valor Actual también se actualizan al realizar el registro de la depreciación. 

<img class="screenshot" alt="Asset" src="{{docs_base_url}}/assets/img/asset/depreciation-entry.png">

## 2. Registros Contables en Depreciación
En el registro de depreciación:

- "Cuenta de Depreciación Acumulada" se acredita y 
- "Cuenta de Gastos de Depreciación" se debita.

Las cuentas relacionadas pueden configurarse en la Categoría de Activos o en la Compañía. 

## 3. Registros automáticos de depreciación
Se puede habilitar el registro automático de la depreciación desde las [Configuraciones de Cuenta](/docs/user/manual/es/accounts/accounts-settings). Esto creará el registro de depreciación de forma automática en la fecha establecida a través del cronograma. De no ser asi, se deberá crear el Asiento de forma manual haciendo click en "Crear > Registro de Depreciación" en la fila correpondiente del Cronograma de Depreciación.

El sistema configurará de forma automática la fecha de finalización del Año Fiscal como la siguiente fecha de depreciación y calculará el monto de depreciación utilizando *pro rata temporis* de acuerdo con la Fecha disponible para usar.

<img class="screenshot" alt="Asset" src="/docs/assets/img/asset/asset_prorated_depreciation.png">

## 4. Ejemplo
Para una mayor comprensión, se muestra en un gráfico de línea el valor neto del activo en diferentes fechas de depreciación.

<img class="screenshot" alt="Asset" src="{{docs_base_url}}/assets/img/asset/asset-graph.png">

### 5. Temas Relacionados
1. [Mantenimiento de Activos](/docs/user/manual/es/asset/asset-maintenance)
1. [Ajuste del valor del Activo](/docs/user/manual/es/asset/asset-value-adjustment)
1. [Desechar un Activo](/docs/user/manual/es/asset/scrapping-an-asset)
