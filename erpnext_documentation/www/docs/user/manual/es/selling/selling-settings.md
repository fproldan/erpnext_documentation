# Configuración de Ventas

La Configuración de Ventas es donde se pueden definir las propiedades y validaciones que luego serán aplicadas a las transacciones involucradas en el ciclo de ventas.

A continuación se ven las opciones disponibles dentro de la Configuración de Ventas en ERPNext.

<img class="screenshot" alt="Selling Settings" src="{{docs_base_url}}/assets/img/selling/selling-settings.png">

Para acceder a la Configuración de Ventas ir a:
> Inicio > Ventas > Configuración > Configuración de Ventas

## 1. Nomenclatura
### 1.1 Nombrar cliente por

Cuando un cliente es guardado, se genera una identificación única para ese cliente.

La configuración predeterminada genera esa identificación utilizando el "Nombre del Cliente". Si, en cambio, se prefiere guardar un cliente utilizando una secuencia hay que seleccionar "Secuencias e identificadores". De esa forma, los clientes se verían así - "CUST00001, CUST00002, CUST00003...", etc.

Se puede configurar una Nomenclatura de clientes desde:

**Configuración > Datos > Secuencias e identificadores**

### 1.2 Nombrar campañas por

Al igual que para los clientes, se puede configurar la nomenclatura para las Campañas. De forma predeterminada, la campaña se guardará bajo el Nombre de Campaña. 

## 2. Configuración predeterminada
### 2.1 Categoría de clientes y territorio predeterminados

Seleccionar una Categoría de Clientes predeterminada que será actualizada automáticamente al crear un nuevo Cliente. 

Las Cotizaciones pueden ser creadas tanto para Clientes como para Iniciativas. Cuando una Cotización realizada a una Iniciativa se convierte en Orden de Venta, el sistema intenta convertirla en Cliente. Al crear un Cliente en la base de datos, los valores para Categoría de Clientes y Territorio son tomados de la Configuración de Ventas. Si no se encuentran valores predeterminados para Categoría de Clientes o Territorio, se recibirá un mensaje de validación que solicitará el mencionado Categoría de Clientes o Territorio. También es posible convertir una Iniciativa en Cliente de forma manual. 

### 2.2 Lista de Precios predeterminada

La Lista de Precios establecida en este campo será utilizada de forma automática en el campo de Lista de Precios de las transacciones de venta como Cotización, Orden de Venta, Nota de Entrega, y Factura de Venta. 

### 2.3 Cerrar Oportunidad transcurrida determinada cantidad de días

Si hay muchas Oportunidades con un estado distinto a Abierto, las mismas serán cerradas automáticamente luego de transcurridos los días establecidos en este campo.

### 2.4 Días de validez de Cotizaciones

Las cotizaciones realizadas para los clientes solo son válidas durante una cierta cantidad de días. En la Cotización se puede actualizar de forma manual la Fecha de Validez. De forma predeterminada, la misma será establecida en 30 días desde la fecha de realización de la Cotización. Se puede cambiar esa cantidad de días en este campo de acuerdo a las características del negocio. 

### 2.5 Canal de Venta por Defecto

En este campo se puede especificar el Canal de ventas que aparecerá por defecto al crear una nueva Orden de venta.

## 3. Configuración de requisitos
### 3.1 Se requiere Orden de venta para la creación de Facturas de venta y Notas de entrega

Si se desea que sea obligatoria la creación de una Orden de Venta antes de crear una Factura de Venta, hay que seleccionar "Si" en este campo. De forma predeterminada este campo estará en "No". 

Esta configuración puede ser cambiada para un cliente en particular tildando la opción "Permitir la creación de Facturas de venta sin Orden de venta" en el perfil del cliente. 

<img alt="Sales Order Required" class="screenshot" src="{{docs_base_url}}/assets/img/selling/so-required.png">

### 3.2 Se requiere Nota de entrega para la creación de Facturas de venta

Para que sea obligatoria la creación de una Nota de Entrega antes de generar la Factura de Venta este campo debería configurarse en "Si". De forma preestablecida se encontrará en "No". 

Esta configuración puede ser cambiada para un cliente en particular haciendo click en la opción "Permitir la creación de Facturas de venta sin Nota de entrega" en el perfil del cliente.

<img alt="Delivery Note Required" class="screenshot" src="{{docs_base_url}}/assets/img/selling/dn-required.png">

### 3.3 Frecuencia de Actualización de Ventas
Esta es la frecuencia con la cual se actualizarán el avance de los proyectos y los detalles de las transacciones de una empresa. De forma predeterminada, esta actualización se dará con Cada Transacción, sin embargo, si la frecuencia de transacciones es muy alta, también se puede configurar la actualización para que se realice de forma Diaria o Mensual. 

## 4. Otras configuraciones
### 4.1 Mantener mismo precio durante todo el ciclo de ventas

El sistema de forma predeterminada validará si el precio del producto cambia a lo largo del cliclo de venta (ej: en una Nota de entrega/Factura de venta respecto a la Orden de venta desde la cual se creó).

Se puede configurar en el campo "Acción si no se mantiene el mismo precio" la acción que el sistema deberá realizar si el precio no es el mismo:

* Detener: ERPNext generará un mensaje de error que impedirá continuar con el ciclo de venta.
* Advertir: el sistema permitirá guardar la transacción pero mostrará un mensaje de advertencia.

Si se seleccionó "Detener", se puede determinar un valor en el campo "Rol autorizado para anular la acción de detener", permitiendo solo a usuarios con este rol continuar con el ciclo de venta.

### 4.2 Permitir al usuario editar el Precio del Producto

La tabla de productos en las transacciones de venta contiene un campo llamado Precio de la lista de precios. Este campo está configurado de forma preestablecida para no permitir ediciones en todas las transacciones de venta. Esto es para asegurar que el precio de un producto será obtenido del registro de Precio de Producto y que el usuario no pueda editarlo. 

Si resulta necesario editar el Precio de Producto obtenido de la Lista de Precios, esta opción debería estar destildada.

### 4.3 Permitir que el producto sea añadido varias veces en una transacción

Este es un campo de validación que impide que un producto sea añadido más de una vez en una transacción cuando se encuentra destildada. En algunos casos esto puede resultar necesario, por ende, si es así, tildar esta opción. 

### 4.4 Permitir múltiples Ordenes de venta contra la Orden de compra de un cliente

Al crear una Orden de Venta, se puede actualizar el Número y la Fecha de la Orden de Compra recibida del cliente. Se podrá crear solo una Orden de Venta por cada Número y Fecha. Sin embargo, si se desea permitir la creación de múltiples Ordenes de Venta por cada Número de Orden de Compra se deberá tildar esta opción. 

### 4.5 Validar el precio de venta del producto frente al precio de compra o la tasa de valoración

Al realizar una venta es importante saber que no se está incurriendo en pérdidas. Al validar este campo, el Precio de Venta del Producto será comparado con su precio de compra o valuación. Si el precio de venta del producto es menor que el precio de compra se recibirá un aviso si esta opción está tildada.

### 4.6 Ocultar el número de identificación fiscal del cliente en las transacciones de ventas

Debido a las reglamentaciones, la mayoría de los clientes poseen una Identificación Fiscal única. A su vez, la misma debe ser utilizada en las transacciones de venta. Sin embargo, si se desea se puede deshabilitar tildando esta opción.
