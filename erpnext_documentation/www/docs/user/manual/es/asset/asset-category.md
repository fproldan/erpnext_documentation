 <!-- add-breadcrumbs -->
# Categoría de Activo

**Una Categoría de Activos clasifica los diferentes activos de una Empresa.**

El primer paso para administrar los activos es crear una Categoría de Activos basada en el tipo de activos. Por ejemplo, todas las computadoras de escritorio y portátiles pueden ser parte de una Categoría de Activos llama "Equipos Electrónicos". 

En Categoría de Activos se pueden configurar: un método predeterminado de depreciación, su periodicidad y las cuentas vinculadas a depreciación, las cuáles se aplicarán a todos los activos que se encuentren dentro de esa categoría.

> **Observación:** También se pueden configurar Cuentas relacionadas a depreciación y Centros de Costo predeterminados en la Compañía. 

Para acceder al listado de Categoría de Activos ir a: 
> Inicio > Bienes > Bienes > Categoría de Activos

## 1. Creación de una Categoría de Activos
1. Ingresar un Nombre para la Categoría de Activos
1. Hacer click en "Permitir Contabilidad de Capital en Proceso" si se desea mantener un registro de los activos bajo una hoja de cálculo temporaria en vez de en la cuenta de activo correspondiente. Para saber más, [visitar esta página](/docs/user/manual/es/asset/purchasing-an-asset).
1. Guardar.

    ![Asset Category](/docs/assets/img/asset/asset-category.png)

### 1.1 Opciones de Depreciación
1. **Habilitar la contabilidad del capital de trabajo en curso**: Al tildar esta opción, los registros contables para activos dentro de esta categoría que no estén en uso son realizados dentro de la cuenta de Capital en Proceso de Trabajo. Esto sucede cuando se es dueño del Activo, pero éste no está siendo usado aún, es decir, cuando la "Fecha disponible para usar" se configura en una fecha posterior. Si se utilizan todos los activos de forma inmediata, deshabilitar esta opción. Al hacerlo, la cuenta de Capital en Proceso de Trabajo será pasada por alto. 

## 2. Características
### 2.1 Detalle del Libro de finanzas
Se puede vincular un Libro de finanzas si se registran las depreciaciones de forma diferente. Se pueden ingresar los siguientes campos: 

* **Método de Depreciación**: Elegir un método de depreciación a través del cuál se registrará la depreciación de los activos de esta categoría. Para saber más, [visitar esta página](/docs/user/manual/es/asset/asset-depreciation).
* **Frecuencia de la Depreciación (Meses)**: El número de meses dentro de los cuáles se registrará la depreciación. El activo puede ser descartado luego de este período.
* **Número Total de Depreciaciones**: El número de depreciaciones a ser registrado en el período de tiempo seleccionado.
* **Tasa de Depreciación**: La tasa de depreciación aplicada a lo largo del período de tiempo seleccionado. Ésta se calculará en base al Método de Depreciación seleccionado.

### 2.2 Cuentas

Pueden configurarse los siguientes detalles de cuenta para registrar los valores de activos en los libros contables:  

* Compañía
* Cuenta de Activo Fijo
* Cuenta de Depreciación Acumulada 
* Cuenta de Gastos de Depreciación
* Cuenta de Capital de trabajo en progreso

## 3. Temas Relacionados
1. [Activos](/docs/user/manual/es/asset/asset)
