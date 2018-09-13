# <a name="use-the-microsoft-graph-api-to-work-with-project-rome"></a>Usar la API de Microsoft Graph para trabajar con Project Rome

[Project Rome](https://developer.microsoft.com/en-us/windows/project-rome) es una iniciativa de Microsoft para crear una plataforma de experiencias multidispositivo. Project Rome permite que una aplicación en un cliente o servicio local interactúe con las aplicaciones y los servicios de un host remoto cuando el usuario inicia sesión con la misma cuenta de Microsoft que se utiliza para iniciar sesión en el dispositivo del cliente. Esto le permite programar experiencias multidispositivo y multiplataforma que se centran en las tareas de usuario y no en los dispositivos.

Mediante Microsoft Graph se expone un componente clave para permitir estas experiencias: las actividades.

## <a name="activities"></a>Actividades

Las actividades de Microsoft Graph le permiten fomentar el compromiso del usuario con sus aplicaciones en distintos dispositivos y plataformas. Una actividad es la unidad de compromiso del usuario y consta de tres componentes:

- Un vínculo profundo
- Una representación visual
- Metadatos de contenido que describen la actividad, con el [http://schema.org/](http://schema.org/) vocabulario compartido

Cuando una aplicación crea una sesión, se agrega un elemento de historial a la actividad para reflejar el período de compromiso del usuario. Cada vez que un usuario se vuelve a comprometer con una actividad, se agrega un nuevo elemento de historial a la actividad para acumular el compromiso del usuario.

Cuando una aplicación publica objetos de actividad de usuario, el objeto se mostrará en algunas de las nuevas superficies de la interfaz de usuario de Windows; Por ejemplo, la escala de tiempo y las notificaciones de Cortana. Puede especificar metadatos enriquecidos (para permitir que las actividades se presenten en el contexto adecuado) y elementos visuales enriquecidos (con la marcación de la [Tarjeta de adaptable](http://adaptivecards.io/) ) en los objetos de actividad.

Puede usar las siguientes API de Microsoft Graph para crear y recuperar las actividades del usuario:

- [Crear o reemplazar una actividad](../api/projectrome_put_activity.md)
- [Obtener actividades](../api/projectrome_get_activities.md)
- [Obtener actividades recientes](../api/projectrome_get_recent_activities.md)
- [Eliminar una actividad](../api/projectrome_delete_activity.md)
- [Crear o reemplazar un elemento de historial](../api/projectrome_put_historyitem.md)
- [Eliminar un elemento de historial](../api/projectrome_delete_historyitem.md)

