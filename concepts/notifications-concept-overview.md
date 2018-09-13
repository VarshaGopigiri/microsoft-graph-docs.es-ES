# <a name="using-the-notifications-api-in-microsoft-graph-to-enable-human-centric-notification-experiences"></a>Uso de la API de notificaciones de Microsoft Graph para permitir experiencias de notificación centradas en las personas 

Las notificaciones son la forma más eficaz de volver a involucrar a los usuarios. Se puede captar la atención de los usuarios y hacer que vuelvan a la aplicación. En un mundo de múltiples dispositivos, los usuarios pueden tener acceso a las aplicaciones y los servicios desde cualquier lugar, en distintas plataformas y distintos dispositivos donde están presentes las aplicaciones. 

Los escenarios de notificación deben diseñarse de manera que se "centren en las personas" y el objetivo principal es notificar al usuario dondequiera que se encuentre. Las soluciones de notificación existentes que proporcionan las principales plataformas son excelentes cuando los dispositivos son el objetivo. Las notificaciones de Microsoft Graph mejoran esta situación, ya que le permiten tener a los usuarios como objetivo. Las notificaciones de Microsoft Graph realizan el trabajo difícil, incluidas la asignación de usuarios a puntos de conexión, la sincronización de estado de notificación en los distintos puntos de conexión de los usuarios, y mucho más. 

## <a name="why-integrate-with-microsoft-graph-notifications"></a>¿Por qué realizar la integración con las notificaciones de Microsoft Graph?
### <a name="deliver-notifications-to-a-user-across-different-endpoints"></a>Entregar notificaciones a un usuario en distintos puntos de conexión
Como parte de Microsoft Graph, la API de notificaciones le permite tener como objetivo una cuenta de Microsoft o una cuenta profesional o educativa (Azure AD) a la que entregar una notificación. La plataforma distribuye esta notificación a los puntos de conexión de todos los usuarios, incluidos Windows UWP, Android e iOS. 

### <a name="manage-notifications-across-endpoints"></a>Administrar notificaciones en múltiples puntos de conexión
La API de notificaciones de Microsoft Graph le permite actualizar el estado de una notificación y sincronizar ese estado en todos los puntos de conexión. Por ejemplo, cuando un usuario actúa respecto a una notificación en un dispositivo, puede actualizar el estado de esa notificación (por ejemplo, marcándola como leída o descartada) y el mismo cambio de estado se distribuirá a todos los otros puntos de conexión. La API de notificaciones de Microsoft Graph realiza un seguimiento del estado de las notificaciones de los usuarios de forma centralizada, lo que facilita garantizar que las notificaciones se gestionan una sola vez y se descartan en todas las ubicaciones.

### <a name="retrieve-notification-history"></a>Recuperar el historial de notificaciones
Puede usar la API de notificaciones para recuperar el historial de notificaciones de acuerdo con un tiempo de caducidad que defina (hasta 30 días). Las notificaciones marcadas como leídas o descartadas añun se pueden recuperar del historial, habilitando las vistas en la aplicación del historial de notificaciones y otros escenarios. 

## <a name="integrating-with-the-notifications-api-in-microsoft-graph"></a>Integración con la API de notificaciones de Microsoft Graph

Puede integrar las aplicaciones con las notificaciones de Microsoft Graph con unos pasos sencillos: incorporar la aplicación mediante el centro para desarrolladores de Windows, usar el método [Crear notificación](../api-reference/beta/api/projectrome_notification_post.md) para publicar las notificaciones y usar el SDK de Project Rome para recibir y administrar las notificaciones en los clientes de la aplicación.  

Para obtener más información acerca de cómo publicar las notificaciones de usuario mediante Microsoft Graph, consulte la [Referencia de la API de notificaciones](../api-reference/beta/resources/notifications-api-overview.md).
 
Para obtener más información sobre cómo recibir y administrar las notificaciones mediante la integración con el SDK de Project Rome, consulte la [documentación del SDK de Project Rome](https://docs.microsoft.com/en-us/windows/project-rome/) 

## <a name="see-also"></a>Consulte también

- [Experiencias multidispositivo en Microsoft Graph](cross-device-concept-overview.md)
- [Centro para desarrolladores de Project Rome](http://aka.ms/projectrome)
