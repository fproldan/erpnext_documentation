<!-- add-breadcrumbs -->
# Creación Automática de Solicitud de Material

Para prevenir faltantes de existencias se puede registrar un Nivel mínimo de stock. Cuando el nivel de existencias está por debajo de este nivel, el gerente de compras es notificado y recibe instrucciones para iniciar el proceso de compra para el producto.

En ERPNext, se puede actualizar el Nivel mínimo de stock y la Cantidad mínima para ordenar en el Producto. Si el mismo producto tiene un nivel mínimo de stock diferente, también se puede actualizar el nivel y cantidad de pedido en base a almacenes. 

<img alt="reorder level" class="screenshot" src="{{docs_base_url}}/assets/img/articles/reorder-request-1.png">

Con el nivel mínimo de stock también se puede definir cuáles serán los pasos a seguir. Es decir, si iniciar una nueva compra o transferir desde otro almacén. De acuerdo con lo que se configure en el Producto, el objetivo será actualizado a su vez en la Solicitud de Material.

<img alt="reorder level next action" class="screenshot" src="{{docs_base_url}}/assets/img/articles/reorder-request-2.png">

Cuando las existencias del producto alcanzan el nivel mínimo de stock, se crea automáticamente una Solicitud de Material. Se puede habilitar esta función desde: 

`Almacén > Configuración > Configuración de Inventarios`

<img alt="active auto-material request" class="screenshot" src="{{docs_base_url}}/assets/img/articles/reorder-request-3.png">

Se creará una Solicitud de Material individual para cada producto. El usuario con el rol de Gerente de Compras recibirá una alerta por correo electrónico respecto a estas Solicitudes de Materiales. 

Si la creación automática de la Solicitud de Material falla, el usuario con el rol de Gerente de Compras será informado respecto al error. Uno de los mensajes de error más frecuentes es:

**Ocurrió un error para ciertos productos al crear Solicitud de Material en base al Nivel mínimo de stock.**
**Fecha 01-04-2016 no perteneciente a un Año Fiscal.**

Uno de los motivos de error puede ser el Año Fiscal. Hacer click [aquí](/docs/user/manual/en/accounts/articles/fiscal-year-error) para aprender más sobre esto.
<!-- markdown -->
