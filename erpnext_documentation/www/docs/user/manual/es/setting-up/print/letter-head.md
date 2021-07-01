<!-- add-breadcrumbs -->
# Membrete

**Un Membrete contiene el nombre, logo, dirección y otros datos de la compañía, y se utiliza en la parte superior de los documentos.**

Cada empresa tiene un Membrete predeterminado. Estos Membretes por lo general se configuran como Encabezado y Pie de Página en los documentos. En ERPNext, se pueden capturar estos detalles en el Membrete.

Estos detalles aparecerán en el Formato de Impresión de transacciones como Ordenes de Venta, Facturas de Venta, Recibos de Sueldo, Ordenes de Compra, etc. En ERPNext, el Membrete se utiliza solo para la parte superior del documento, otro contenido ya esta pre formateado y puede ser configurado a través de [Formato de Impresión](/docs/user/manual/es/setting-up/print/print-format) y [Encabezado de Impresión](/docs/user/manual/es/setting-up/print/print-headings).

Para acceder a Membrete ir a:
> Inicio > Configuraciones > Membrete

## 1. Creación de un Membrete
1. Ir al listado de Membrete y hacer click en Nuevo.
1. Ingresar un nombre para el Membrete. Se puede crear un Membrete independiente para diferentes ubicaciones de oficinas.
1. Elegir si se basa en una imagen o HTML.
1. Se pueden ingresar detalles en un Membrete utilizando:

  * Imagen: Hacer click en el botón Adjuntar para subir una imagen. Una vez que la imagen ha sido insertada, se generará automáticamente el HTML para la misma.
  * Otra Información (como Dirección, ID Fiscal, etc.) que se desee incluir en el Membrete. 

    <img class="screenshot" alt="Print Heading" src="{{docs_base_url}}/assets/img/setup/print/letter-head.png">
  
  > Si se desea que este sea el Membrete predeterminado, hacer click en "Membrete Predeterminado".

5. Luego de ingresar los valores en la sección Encabezado y Pie de Página, guardar el Membrete.

Se puede configurar el membrete en base a un HTML para poder realizarle cambios:

![Letter Head based on](/docs/assets/img/setup/print/letter-head-based-on.gif)

Así se ve un Membrete en el formato de impresión de un documento.

<img class="screenshot" alt="Print Heading" src="{{docs_base_url}}/assets/img/setup/print/letter-head-1.png">

> Tener en cuenta que el Pie de Página solo será visible cuando el formato de impresión del documento se vea en PDF. El Pie de Página no será visible en la vista previa de impresión del HTML.

## 2. Temas Relacionados
1. [Plantilla de Dirección](/docs/user/manual/es/setting-up/print/address-template)
1. [Bases y Condiciones](/docs/user/manual/es/setting-up/print/terms-and-conditions)
1. [Plantilla de Impresión de Cheques](/docs/user/manual/es/setting-up/print/cheque-print-template)
1. [Encabezados de Impresión](/docs/user/manual/es/setting-up/print/print-headings)
