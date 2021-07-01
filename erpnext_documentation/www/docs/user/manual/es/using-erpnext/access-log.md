# Registro de Acceso

**El Registro de Acceso es una función de seguridad que almacena todas las exportaciones de datos realizadas por todos los usuarios en el sistema.**

Es una herramienta para Administradores del Sistema que les permite rastrear qué archivos fueron accedidos o exportados por usuarios en el sistema. Esto resulta útil para rastrear toda la información sensible de la empresa como transacciones o información financiera. 

Los Registros de Acceso se crean en los siguientes casos:

 - Impresión de todos los Formularios e Informes 
 - Descargas de archivos privados
 - Exportaciones en formatos XLSX/CSV

En ERPNext, el Registro de Acceso está disponible para Administradores del Sistema y puede ser accedido a través de la Búsqueda Global o de: 

> Inicio > Usuarios > Registros > Registros de Acceso

![Access Log](/docs/assets/img/using-erpnext/using-access-log-3.png)

En el caso de que se cree un registro de acceso por la exportación de un Informe, se generará un botón de **Mostrar Informe** en el registro respectivo. Al hacer click en ese botón, puede verse el informe exportado junto con los filtros configurados. 

![Access Log](/docs/assets/img/using-erpnext/using-access-log-1.png)

De forma similar, se generará un botón de **Mostrar Documento** en el caso de eventos relacionados directamente a documentos como Impresión y descarga de Archivos Privados. 

![Access Log](/docs/assets/img/using-erpnext/using-access-log-2.png)

Eventos como la [Impresión Directa](/docs/user/manual/en/setting-up/print/raw-printing) guardan la información junto con la plantilla elegida para el documento. 

![Access Log](/docs/assets/img/using-erpnext/using-acces-log-4.png)
