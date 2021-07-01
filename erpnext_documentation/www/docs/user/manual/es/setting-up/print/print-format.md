<!-- add-breadcrumbs -->
# Formato de Impresión

**Con el Formato de Impresión se puede configurar cómo se ven los distintos tipos de documentos al imprimir.**

Cada transacción tiene un Formato de Impresión predeterminado llamado "Estándar". Se pueden cambiar los Formatos de Impresión de la siguiente manera:

* Utilizando el formulario de Formato de Impresión
* Utilizando el lenguaje Jinja/JS bajo Formato de Impresión
* Utilizando el [Generador de Formatos de Impresión](/docs/user/manual/es/setting-up/print/print-format-builder) para crear formatos de impresión con UI
* Utilizar Personalizar Formulario para ocultar/mostrar campos

Para acceder al Formato de Impresión ir a:

> Inicio > Configuración > Formato de Impresión

## 1. Creación de un Formato de Impresión
1. Ir al listado de Formato de Impresión y hacer click en Nuevo.
1. Ingresar un nombre y seleccionar el DocType para el cual se utilizará el Formato de Impresión.
1. El Módulo para el cual se aplicará será seleccionado de forma automática.

  ![Print Format menu](/docs/assets/img/setup/print/print-format-menu.png)

4. Guardar.

En Ajustes de Estilo están las opciones para modificar el diseño. Se puede cambiar la fuente, alinear las etiquetas a la izquierda o derecha, añadir encabezados para cada sección, etc.   

Para diseñar el Formato de Impresión utilizando Jinja/JS, tildar la opción "Formato Personalizado". Al hacer esto aparecerá también la opción de [Impresión en bruto](/docs/user/manual/es/setting-up/print/raw-printing).

## 1.1 Utilizar Personalizar Formulario para cambiar los ítems del Formato de Impresión

Los campos de las transacciones y sus tablas secundarias pueden ocultarse/mostrarse utilizando Personalizar Formulario.
Por ejemplo, si se quiere esconder el "Código de Producto" al imprimir una Cotización, se debe ir a Menú > Personalización, seleccionar Producto de Cotización en el campo "Seleccione el Tipo de Formulario".
![Print Format Customize](/docs/assets/img/setup/print/print-format-customize1.png)


En la tabla de campos, expandir al fila "Código de Producto", deslizar hacia abajo y tildar la opción "Ocultar en impresión".
![Print Format Print Hide](/docs/assets/img/setup/print/print-format-customize2.png)

Para saber más, visitar la página [Personalizar Formato de Impresión](/docs/user/manual/es/customize-erpnext/print-format).

Un Formato de Impresión recientemente creado puede seleccionarse en la pantalla de impresión de una transacción. Desde ahí se puede ver cómo se ve y proceder a la impresión. 
![Selecting a Print Format](/docs/assets/img/setup/print/print-format-selection.png)

## 2. Temas Relacionados
1. [Estilo de Impresión](/docs/user/manual/es/setting-up/print/print-style)
1. [Encabezado de Impresión](/docs/user/manual/es/setting-up/print/print-headings)
1. [Membrete](/docs/user/manual/es/setting-up/print/letter-head)
1. [Plantilla de Impresión de Cheques](/docs/user/manual/es/setting-up/print/cheque-print-template)
1. [Inhabilitar Saltos de Línea en Secciones de Formato de Impresión](/docs/user/manual/es/setting-up/articles/print-format-sections)
