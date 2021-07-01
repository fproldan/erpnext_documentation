<!-- add-breadcrumbs -->
# Plantillas de Dirección

**La plantilla de dirección puede almacenar distintos formatos de dirección de acuerdo con la región.**

Cada región tiene su propia forma de definir direcciones. Para administrar muchos formatos de dirección para los Documentos (como Cotizaciones, Facturas de Compra, etc.) se pueden crear **Plantillas de Dirección** basadas en países.

Para acceder a Plantilla de Dirección ir a:
> Inicio > CRM > Plantilla de Dirección

Una Plantilla de Dirección predeterminada es creada cuando se configura el sistema. Se puede editar o crear una nueva plantilla. Esta plantilla predeterminada se aplicará a todos los países si no hay una plantilla específica.

Considérese un cliente de Estados Unidos donde el "Condado" es parte de la dirección. Si se configura condado en la plantilla de dirección para Estados Unidos, entonces se mostrará en el campo dirección y, por ende, en la vista de impresión. Campos como código PIN pueden ser cambiados para mostrarse como código ZIP y campos como condado pueden agregarse utilizando las Plantillas de Dirección. 

> La Plantilla de Dirección verifica el campo "País" en la Dirección para aplicar diferentes plantillas a las transacciones.

## 1. Creación de una Plantilla de Dirección
1. Ir al listado de Plantilla de Dirección y hacer click en Nueva. 
1. Seleccionar un País.
1. Cambiar el CSS y Jinja de ser necesario.
1. Guardar.

### 1.1 Plantillas Jinja
La función para crear plantillas está basada en HTML y en el sistema [Plantillas Jinja](http://jinja.pocoo.org/docs/templates/). Todos los campos (incluyendo los Campos Personalizados) se encontrarán disponibles para crear la plantilla. 

Aquí esta la plantilla Jinja predeterminada:

    {% raw %}{{ address_line1 }}<br>
    {% if address_line2 %}{{ address_line2 }}<br>{% endif -%}
    {{ city }}<br>
    {% if state %}{{ state }}<br>{% endif -%}
    {% if pincode %}PIN:  {{ pincode }}<br>{% endif -%}
    {{ country }}<br>
    {% if phone %}Phone: {{ phone }}<br>{% endif -%}
    {% if fax %}Fax: {{ fax }}<br>{% endif -%}
    {% if email_id %}Email: {{ email_id }}<br>{% endif -%}{% endraw %}

Aquí hay un ejemplo:

<img class="screenshot" alt="Print Heading" src="{{docs_base_url}}/assets/img/setup/print/address-format.png">

### 2. Temas Relacionados
1. [Plantilla de términos y condiciones](/docs/user/manual/es/setting-up/print/terms-and-conditions)
1. [Plantilla de impresión de cheques](/docs/user/manual/es/setting-up/print/cheque-print-template)
