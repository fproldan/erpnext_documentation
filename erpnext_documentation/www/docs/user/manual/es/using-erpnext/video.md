<!-- add-breadcrumbs -->
# Video

**Pueden añadirse videos tanto desde Vimeo como de YouTube, utilizando el DocType de videos.**

Se pueden añadir videos con sus respectivas URL, descripciones, miniaturas, etc. Algunos usos que pueden darse a esta función son guardar material de cursos educativos y hacer un seguimiento del uso personal de YouTube. 

Para acceder a Videos, ir a:

> Inicio > Utilidades > Video

## 1. Creación de un Video

1. Ir al listado de Video y hacer click en Nuevo.
2. Ingresar el título del Video.
3. Selecccionar el Proveedor. El Proveedor de Video predeterminado es YouTube.
4. Ingresar la URL para acceder al Video.
5. Si se desea, se puede ingresar una fecha de publicación y la duración del Video en días-horas-minutos-segundos. 
6. También se debe ingresar alguna descripción para el mismo.
7. Guardar.

Luego de guardar, se podrá agregar una imagen o miniatura para el Video.
![Video](/docs/assets/img/education/video-after-save.png)

También se puede ver el video en el Documento luego de guardarlo. 
![Video](/docs/assets/img/education/video-watch.gif)

## 2. Características

### 2.1 Rastrear Estadísticas de Video a través de YouTube

Las estadísticas de Video de YouTube pueden rastrearse y analizarse. Esto es útil para conocer el conteo de espectadores y su participación en un Video que se haya publicado. 

Para esto, primero se debe habilitar el Seguimiento de YouTube en **Configuraciones de Video**:
> Ajustes de video > Habilitar el seguimiento de YouTube 

Una vez habilitado esto, se harán visibles los campos **Clave de API** y **Frecuencia**.
![Video](/docs/assets/img/education/video-settings.png)

**Clave de API** : Se puede generar una clave de API en la [Consola de Desarrolladores de Google](https://console.developers.google.com/). Para conocer los pasos para generarla ver [Información de YouTube respecto a Documentación de Datos API](https://developers.google.com/youtube/v3/getting-started).

**Frecuencia**: Se puede elegir la frecuencia con la cual el sistema actualizará automáticamente las estadísticas. Las opciones disponibles son: cada 30 minutos, 1 hora o Diariamente (una vez por día).

Mas allá de la actualización automática, las estadísticas se actualizan al Guardar. Por ende todos los videos creados o actualizados **luego** de habilitar el Seguimiento de YouTube, actualizarán sus estadísticas al ser Guardados. 
![Video](/docs/assets/img/education/video-stats.png)

### 2.2 Informe de Interacciones de YouTube

El Informe de Interacciones de YouTube, provee una visión consolidada de la participación de espectadores en todos los videos. El gráfico de barras brinda un análisis visual de los Me Gusta versus las Vistas. 

Se pueden filtrar los datos del informe por rango de Fecha de Publicación. 
![Video](/docs/assets/img/education/youtube-interactions.png)

> **Observación** : El límite para pedir datos API de forma **gratuita** era de 10.000 pedidos en septiembre de 2020. ERPNext actualiza automáticamente hasta 50 videos en un pedido. De forma similar, para 100 videos necesitaría 2 pedidos.<br>
Asumiendo que se actualizan 100 videos **por hora** (frecuencia = 1 hour):<br>
>
- se enviarán 2 pedidos por hora<br>
- 48 pedidos por día<br>

> Tener en cuenta configurar la frecuencia acordemente.

{siguiente}
