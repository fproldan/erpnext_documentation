<!-- add-breadcrumbs -->
# Sistema de Puntos de Energía 

**El Sistema de Puntos de Energía es un sistema de puntuación/karma que puede ser habilitado para uso de la empresa.**

Este sistema puede utilizarse para rastrear el desempeño de cada usuario.

> Para habilitar el Sistema de Puntos de Energía ir a **Configuraciones de Puntos de Energía** > y hacer click en **Habilitar**.

## 1. Utilización del Sistema de Puntos de Energía

Para comenzar a utilizar este sistema es necesario crear algunas Reglas de Puntos de Energía (ver sección 3 Creación de Reglas de Puntos de Energía) para que los usuarios pueden recibir puntos de energía de acuerdo con las actividades que realicen.

## 2. Reglas de Puntos de Energía

Las Reglas de Puntos de Energía almacenan la información respecto a la actividad y el valor de puntos a ser asignados.

Las Reglas tienen los siguientes campos:

 * **DocType de Referencia:** tipo de documento sobre el cual se quiere aplicar la regla, por ejemplo: Tarea, Tarea Pendiente, Ticket, etc.
 * **Para Evento de Documento:** opciones: Guardar, Validar, Cancelar, y Personalizar.
    **Observación:** si la opción "Personalizar" está seleccionada, entonces el campo "Condiciones" se vuelve obligatorio.
 * **Puntos:** puntos a asignar.
 * **Adjudicar puntos a los usuarios asignados:** si esta opción se encuentra tildada, los usuarios asignados al documento de referencia recibirán puntos. Por ejemplo, si los usuarios Rema y Jai son asignados a una tarea en particular, entonces ambos recibirán puntos cuando el documento cumpla la condición.
 * **Campo de usuario:** campo del cual será seleccionado el usuario, por ejemplo puede usarse: "Resuelto Por", "Modificado Por", "Propietario", etc. Si se selecciona "Modificado Por", la última persona en cumplir la condición del documento recibirá los puntos.
 * **Campo multiplicador:** campo que almacena el valor del multiplicador. Este campo puede tener valores numéricos y decimales que pueden multiplicarse por los puntos definidos en la regla.
    Por ejemplo: 2 (multiplicador) * 10 (puntos configurados en la regla) = 20 puntos
 * **Condición:** condición para asignar los puntos.
    Ejemplo: `estado.documento == "Cerrado"`. La condición establecida más arriba verificará si el campo `estado` en el documento es "Cerrado", de ser así, se asignarán los puntos al usuario.
 * **Aplicar solo una vez:** la regla se aplicará una sola vez por documento.

> **Observación:** Los Campos de Usuario y Multiplicador son tomados desde el doctype de referencia. 

## 3. Creación de Reglas de Puntos de Energía

> Buscar **Regla de Puntos de Energía** > crear nueva Regla de Puntos de Energía 

Ver el siguiente ejemplo de una regla:

<img class="screenshot" src="/docs/assets/img/setup/energy-point-system/issue-closed-rule.png">

La captura de pantalla de más arriba es la regla para **Cerrar Ticket**. De esta forma, cuando un usuario cierra el ticket, el/ella recibirá **10** puntos.

Otros casos pueden ser tratados de forma similar.

Suponiendo que se quiere crear una regla según la cual un usuario consigue puntos al completar una tarea, esto puede hacerse creando la siguiente regla:

<img class="screenshot" src="/docs/assets/img/setup/energy-point-system/task-complete-rule.png">


## 4. Características

### 4.1 Asignación Automática de Puntos

De acuerdo con las reglas de puntos de energía creadas, los usuarios recibirán puntos de forma automática al completar actividades que son rastreadas utilizando el Sistema de Puntos.

### 4.2 Sistema de Revisiones

El sistema de revisiones puede utilizarse para "Apreciar" o "Criticar" el trabajo de alguien.

Ver el siguiente GIF para el proceso de revisión:

<img class="screenshot" src="/docs/assets/img/setup/energy-point-system/review-system.gif">

Para realizar revisiones, el usuario debe tener puntos de revisión que pueden ser asignados por el Administrador de Sistema a través de **Configuraciones de Puntos de Energía**.

También se puede configurar la asignación automática de puntos de revisión desde "Configuraciones de Puntos de Energía":
<img class="screenshot" src="/docs/assets/img/setup/energy-point-system/auto-review-point-allocation.png">

### 4.3 Tabla de Posiciones

Ir a Inicio Social > Tabla de Posiciones (barra de navegación lateral)

La Tabla de Posiciones muestra la posición del usuario en la empresa. 

<img class="screenshot" src="/docs/assets/img/setup/energy-point-system/leaderboard.png">

## 5. Temas Relacionados
1. [Rastreador de Objetivos](/docs/user/manual/es/automation/milestone-tracker)
