<!-- add-breadcrumbs -->
# Búsqueda Global

**La Búsqueda Global es una poderosa operación de procesamiento de texto en ERPNext que ayudará en la búsqueda de un Tipo de Documento o Documento en particular.**

Para cada secuencia de una palabra particular o conjunto de caracteres, se obtendrá un resultado de búsqueda.

### Utilizar la Barra Inteligente para Búsqueda Global

![Tree Master Renaming](/docs/assets/img/using-erpnext/using-global-search-2.gif)

La Búsqueda Global ayuda a los usuarios a encontrar información rápidamente. Se encuentra en la esquina superior derecha en ERPNext. Al ingresar algunos caracteres en la Barra de Búsqueda se mostrarán resultados para varios tipos de registros diferentes (Contacto, Cliente, Asuntos, etc.) relacionados con esa palabra clave. También se pueden personalizar los campos en los cuales se basará la búsqueda. 

También se pueden ingresar muchas palabras claves separadas por & para encontrar los resultados deseados. Por ejemplo: 

- La entrada "apple & iPod" puede devolver documentos con un campo que contenga Apple y otro que contenga iPod (Vendedor y producto).
- La entrada "iPhone & iPod" puede devolver documentos que contengan ambos productos iPhone y iPod (tabla de productos secundarios).
- La entrada "iPhone & negro" puede devolver un producto con una descripción que contenga ambas palabras (campo de texto largo).
- La entrada "foo & bar" puede devolver cualquier documento con etiquetas asignadas para foo y bar (campo de texto largo especial _etiquetasdeusuario).

### Habilitar Búsqueda Global para campos en un Doctype

![Tree Master Renaming](/docs/assets/img/using-erpnext/using-global-search-1.gif)

