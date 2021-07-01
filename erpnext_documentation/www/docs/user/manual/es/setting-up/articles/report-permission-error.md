<!-- add-breadcrumbs -->
# Resolución de Problemas de Errores de Permisos

**Problema:** El usuario tiene asignados roles como Usuario de Cuenta y Administrador de Cuenta. Sin embargo, al acceder al informe de Cuentas por Cobrar, el Usuario recibe un mensaje de error de no permisos en la función territorio. 

<img alt="Report Permission Error" class="screenshot" src="{{docs_base_url}}/assets/img/articles/report-permission-1.png">

**Solución:**

De acuerdo con el sistema de permisos en ERPNext, para que el usuario pueda acceder a un formulario o informe, debe tener por lo menos permiso de lectura sobre todos los campos relacionados con ese formulario/informe. Como el Territorio es un campo relacionado en el informe de Cuentas por Cobrar, es necesario añadir una pauta de permiso para que el Usuario/Administrador de Cuenta posea por lo menos el permiso de lectura sobre Territorio. Se deberán seguir los pasos dados a continuación para resolver el problema:

1.  Los Roles asignados al Usuario son Usuario de Cuenta y Administrador de Cuenta. 

2.  Como se indica en el mensaje de Error, el usuario no tenía permisos sobre territorio. De acuerdo con los permisos predeterminados, ninguno de los roles asignados al Usuario más arriba, tiene permisos sobre Territorio.  

3.  Para resolver este problema, se le asigna al Usuario de Cuenta el permiso para leer Territorio.  

    <img alt="Permission Manager" class="screenshot" src="{{docs_base_url}}/assets/img/articles/report-permission-2.png">

De acuerdo con la actualización de permisos, el Usuario debería poder acceder sin problema al informe de Cuentas por Cobrar.
