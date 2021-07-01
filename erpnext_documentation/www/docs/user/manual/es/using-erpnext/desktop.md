<!-- add-breadcrumbs -->
# Escritorio 

**En el momento en que el Usuario ingresa al sistema, podrá ver una Pantalla de Inicio donde todos los Módulos y Dominios se verán en forma de tarjetas.**

![New Desktop](/docs/assets/img/using-erpnext/desktop/desktop.png)

Estas tarjetas pueden clasificarse en cuatro categorías, véase:

- **Módulos**: Estos son los módulos aplicables a todo ámbito disponibles en ERPNext, que son comunes a todos los tipos de negocios. Módulos como Recursos Humanos, CRM, Compras, Ventas, etc, se encuentran en esta categoría.
- **Ámbitos**: Aquí se pueden encontrar todos los módulos específicos de un ámbito, como Educación y Fabricación. Se puede aprender más respecto a módulos de industrias específicas [aquí](/docs/user/manual/en#3-industry-specific-modules).
- **Lugares**: Lugares es donde se pueden encontrar funciones que no son específicas a una industria en particular y que no se requieren en las operaciones del día a día de la empresa. Funciones como Sitio Web, Tableros y Mercado, pueden encontrarse aquí. 
- **Administración**: Aquí se pueden encontrar módulos relacionados a la configuración y administración de ERPNext.

Estas tarjetas permiten una mejor navegación con accesos directos en el menú desplegable. Se puede personalizar dicho menú para añadir o eliminar vínculos a varios DocType para ese Módulo.

![Desktop Dropdown](/docs/assets/img/using-erpnext/desktop/desktop-dropdown.png)

También se puede reordenar, mostrar u ocultar estas tarjetas de módulo. 

![Drag and Drop](/docs/assets/img/using-erpnext/desktop/drag-and-drop.gif)

## Página de Módulo

Haciendo click en cualquier tarjeta de módulo se irá a la página del módulo. Aquí el usuario puede navegar a través de todos los doctypes, informes y configuraciones asociadas a ese módulo en particular. 

Por ejemplo, así es como se ve la página del módulo de Contabilidad. 

![Accounts Module](/docs/assets/img/using-erpnext/desktop/accounts-module-page.png)

### Navegando la Página

Algunos links de estos módulos pueden estar en gris, de esta forma, si se hace click en esos links no se abrirá ninguna página. Se marcan así porque hay un documento, del que dependen, que debe ser creado primero. Por ejemplo, se debe crear una Factura de Venta antes de acceder al registro de venta. Al utilizar cualquiera de estos links se mostrará una ventana emergente guiando al usuario al documento del que dependen. 

![Muted Link in Module Page](/docs/assets/img/using-erpnext/desktop/module-link-hover.png)

También podrá verse un indicador de color antes de algunos links. Estos indicadores se utilizan para informar al usuario si algun documento abierto o urgente debe ser visto. 

![Color Indicators](/docs/assets/img/using-erpnext/desktop/color-indicator.png)

* El indicador **rojo** en el ejemplo anterior indicaba que hay tareas abiertas o atrasadas en la lista. 
* De manera similiar, un indicador **azul** significa que no hay tareas abiertas. 
* Un indicador **naranja** significa que no se ha accedido al informe o que no hay un documento creado en el doctype correspondiente. 

{siguiente}