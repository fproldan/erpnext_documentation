<!-- add-breadcrumbs -->
# Centro de costos distribuido

**Un Centro de costos distribuido es un Centro de costos compuesto por múltiples Centros de costos, cada uno de ellos con un porcentaje correspondiente.**

Un negocio puede tener un Centro de costos principal y otros varios que dependen de él. Como resulta complejo actualizar el pesupuesto, la ganancia y la pérdida de cada Centro de costos secundario de forma manual por cada transacción donde se utilice el Centro de costos prncipal, esta funcionalidad ayuda a automatizar este proceso de entradas manuales.
Por ejemplo, si los Centros de costos 'B' y 'C' dependen de 'A' en un 20% y 80% respectivamente, se puede considerar a 'A' como un Centro de costos distribuido. Esto ayuda a reflejar los ingresos, gastos y presupuesto de 'A' en base a los porcentajes de 'B' y 'C'.

En ERPNext se puede crear Centros de costos distribuidos y usarlos en transacciones y reportes.

## 1. Creación de un Centro de costos distribuido
1. Ir al listado de Centro de costos, hacer click en Nuevo.
1. Ingresar el nombre del Centro de costos.
1. Seleccionar el Centro de costos principal.
1. Tildar la opción **Habilitar Centro de costos distribuido**: al hacer esto aparecerá la tabla de Centros de costos secundarios. Aquí se deberán seleccionar Centros de costos deseados y asignarle su porcentaje.
1. Una vez que esté todo listo, hacer click en Guardar.

  <img class="screenshot" alt="Distributed Cost Center" src="{{docs_base_url}}/assets/img/accounts/distributed_cost_center.png">

Los siguientes reportes serán automáticamente actualizados al filtrar por Centro de costos:

  * [Reportes contables](/docs/user/manual/es/accounts/accounting-reports)
    * Estados financieros
    * Variación de presupuesto
    * Balance general
  * [Cuenta de Resultados](/docs/user/manual/en/accounts/articles/tracking-project-profitability-using-cost-center)

### 2. Temas relacionados
1. [Centro de costos](/docs/user/manual/es/accounts/cost-center)
