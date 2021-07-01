<!-- add-breadcrumbs -->
# Informes Preparados

Muchas veces, al generar un informe que utiliza un gran volumen de datos, por ejemplo, un informe de Libro Mayor para todo el año, puede suceder que se reciba el siguiente mensaje de error: **Tiempo de espera agotado**. Esto ocurre cuando hay muchos datos a procesar y presentar en la página del informe, pero no hay suficientes recursos en el servidor, lo cual resulta en una desconexión.

Para procesar mejor esos informes, ERPNext ofrece Informes Preparados. Cuando un informe se configura como Informe Preparado, se generará a través de un [Trabajo en Segundo Plano](https://frappe.io/docs/user/en/guides/app-development/running-background-jobs), y una vez que esté listo, se encontrará disponible para que los usuarios lo vean. 

## Configuración de Informes Preparados

1. Ir a [Permisos de Rol Para Página y Reporte](/docs/user/manual/es/setting-up/users-and-permissions/role-permission-for-page-and-report).
1. En el campo "Establecer Rol Para" seleccionar **Reporte**.
1. En el campo "Reporte" seleccionar el informe para el cual se desea habilitar/deshabilitar el informe preparado.
1. Utilizar la casilla de verificación **Deshabilitar informe preparado** para habilitar/deshabilitar el informe preparado. Si la opción está tildada, la opción de informe preparado será deshabilitada para el informe seleccionado. 
1. Hacer click en **Actualizar**.

<img alt="Setup Prepared Report" class="screenshot" src="{{docs_base_url}}/assets/img/articles/set-prep-report.gif">

## Uso de un Informe Preparado

1. Abrir dicho reporte (por ejemplo Libro Mayor) y aplicar todos los filtros necesarios.
1. Si la opción de informe preparado está habilitada para ese informe, se verá un botón de **Generar Informe**. Hacer click allí.
 
    <img alt="Generate Prepared Report" class="screenshot" src="{{docs_base_url}}/assets/img/articles/prepared-report-generate.png">
    
1. Se verá una notificación en la parte inferior izquierda de la pantalla que diga "Informe iniciado. Rastrear su estado _aquí_"
 
    <img alt="Prepared Report Initiated" class="screenshot" src="{{docs_base_url}}/assets/img/articles/prepared-report-bg.png">
    
1. Se puede esperar en esa pantalla o hacer click en el _aquí_ del mensaje para abrir la página para el informe. Esto abrirá una nueva página para el informe:
    
    <img alt="Prepared Report Queued" class="screenshot" src="{{docs_base_url}}/assets/img/articles/prepared-report-queued.png">
    
    Como se puede ver, la página del informe tiene el estado de "En Espera". Una vez que el informe esté listo, se verá un botón de **Mostrar Informe** en el cual se puede hacer click para ver el informe:
    
     <img alt="Prepared Report Initiated" class="screenshot" src="{{docs_base_url}}/assets/img/articles/prepared-report-page.png">
     
1. Como el Informe Preparado también es un doctype, para ver la lista de Informes Preparados se puede utilizar el [Administrador de Permisos de Rol](/docs/user/manual/es/setting-up/users-and-permissions/role-based-permissions) para dar acceso al mismo.
