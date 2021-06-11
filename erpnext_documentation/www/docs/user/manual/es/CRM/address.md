<!-- add-breadcrumbs -->
# Dirección

Se pueden registrar las direcciones asociadas con una Iniciativa, un Cliente, Proveedor, Accionista, Socio de ventas o Almacén. 

También se puede agregar una Dirección como un registro independiente sin vincularla a ninguna de las entidades mencionadas anteriormente.

Para acceder al listado de Direcciones ir a:
> Inicio > CRM > Dirección

## 1. Creación de una Dirección

1. Ir al listado de Dirección y hacer click en Nuevo. 
1. Seleccionar el Tipo de Dirección.
1. Ingresar los detalles en Dirección línea 1, Dirección línea 2, Ciudad/Pueblo, Provincia/Jurisdicción, Partido/Departamento, Provincia/Estado
y País. 
1. Ingresar Correo Electrónico, Teléfono y Fax. 
1. Ingresar el vínculo de DocType y vínculo de Nombre para vincular esta dirección a un cliente, proveedor, etc.
4. Guardar.
    <img class="screenshot" alt="Contact" src="{{docs_base_url}}/assets/img/crm/address.png">

También se puede ingresar una Dirección desde el registro de un Cliente o Proveedor haciendo click en el botón "Nueva Dirección" como se muestra a continuación. 

<img class="screenshot" alt="Contact" src="{{docs_base_url}}/assets/img/crm/address-from-supp.png">

Para Importar muchas direcciones desde una hoja de cálculo, utilizar la [Herramienta de Importación de Datos](/docs/user/manual/en/setting-up/data/data-import).

---
## 2. Características

### 2.1 Vincular una Dirección a Muchas Entidades 

Una dirección puede vincularse a múltiples clientes o múltiples proveedores. 

<img class="screenshot" alt="Contact" src="{{docs_base_url}}/assets/img/crm/link_address_to_multipl_entities.png">

### 2.2 Título de la Dirección

Si la dirección no se encuentra vinculada a ninguna entidad, se deberá ingresar un título de forma manual.

Si la dirección está vinculada a una entidad como un cliente o proveedor, el título se genera automáticamente en un formato como el siguiente: "Nombre de la Entidad-Tipo de Dirección".

<img class="screenshot" alt="Contact" src="{{docs_base_url}}/assets/img/crm/address_title_generation.png">

### 2.3 Dirección de Facturación y de Envío Preferida 

Si se selecciona "Dirección de envío preferida", la dirección se añadirá automáticamente en el campo Dirección de Envío en las transacciones como Orden de Venta, Factura de Venta y Nota de Envío. 

De forma similar, si se selecciona "Dirección de facturación preferida", la dirección se añadirá automáticamente en el campo Dirección de Facturación en transacciones como Orden de Venta, Factura de Venta y Nota de Envío. 

### 3. Temas Relacionados
1. [Cliente](/docs/user/manual/es/CRM/customer)
1. [Proveedor](/docs/user/manual/es/buying/supplier)
1. [Socio de ventas](/docs/user/manual/es/selling/sales-partner)
