---
title: 'Usar la API de notificaciones de Microsoft Graph para habilitar las experiencias de notificaciones centradas en las personas '
description: 'Las notificaciones son la forma más eficaz de hacer que los usuarios vuelvan a participar. Pueden llamar la atención de los usuarios y traerlos a la aplicación de nuevo. En un entorno con gran variedad de dispositivos, los usuarios pueden acceder a las aplicaciones y servicios desde cualquier lugar y en distintas plataformas y dispositivos donde las aplicaciones estén disponibles. '
ms.openlocfilehash: 7ff36d7e0d406cb7918e2999812e3c756ae3b5bc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092814"
---
# <a name="using-the-notifications-api-in-microsoft-graph-to-enable-human-centric-notification-experiences"></a>Usar la API de notificaciones de Microsoft Graph para habilitar las experiencias de notificaciones centradas en las personas 

Las notificaciones son la forma más eficaz de hacer que los usuarios vuelvan a participar. Pueden llamar la atención de los usuarios y traerlos a la aplicación de nuevo. En un entorno con gran variedad de dispositivos, los usuarios pueden acceder a las aplicaciones y servicios desde cualquier lugar y en distintas plataformas y dispositivos donde las aplicaciones estén disponibles. 

Los escenarios de notificaciones deben diseñarse centrados en las personas; el objetivo principal es siempre notificar al usuario, esté donde esté. Las soluciones de notificación existentes ofertadas por grandes plataformas son excelentes a la hora de dirigirse a los dispositivos. Las notificaciones de Microsoft Graph son mejores en este sentido, ya que permiten dirigirse a los usuarios. Las notificaciones de Microsoft Graph se encargan del trabajo pesado, como la asignación entre los usuarios y los puntos de conexión, la sincronización del estado de notificaciones en los diferentes puntos de conexión de los usuarios y mucho más. 

## <a name="why-integrate-with-microsoft-graph-notifications"></a>¿Por qué integrar con las notificaciones de Microsoft Graph?
### <a name="deliver-notifications-to-a-user-across-different-endpoints"></a>Entrega notificaciones a un usuario en diferentes puntos de conexión
Como parte de Microsoft Graph, la API de notificaciones permite entregar notificaciones a una cuenta de Microsoft o a una profesional o educativa (Azure AD). La plataforma distribuye esta notificación a todos los puntos de conexión de los usuarios, incluidos UWP de Windows, iOS y Android. 

### <a name="manage-notifications-across-endpoints"></a>Administrar las notificaciones en todos los puntos de conexión
La API de notificaciones de Microsoft Graph permite actualizar el estado de una notificación y sincronizar ese estado en todos los puntos de conexión. Por ejemplo, cuando un usuario realiza una acción en una notificación desde un dispositivo, puede actualizar el estado de dicha notificación (por ejemplo, marcarla como leída o descartarla) y el mismo cambio de estado se distribuirá a todos los otros puntos de conexión. La API de notificaciones de Microsoft Graph realiza el seguimiento del estado de las notificaciones de los usuarios de forma centralizada, lo que garantiza que las notificaciones se administren solo una vez y se descarten en los demás puntos de conexión.

### <a name="retrieve-notification-history"></a>Recuperar el historial de notificaciones
Puede usar la API de notificaciones para recuperar el historial de notificación en función de la fecha de expiración que defina (hasta un máximo de 30 días). Las notificaciones marcadas como leídas o descartadas todavía se pueden recuperar del historial, lo que habilita las vistas en la aplicación del historial de notificaciones y otros escenarios. 

## <a name="integrating-with-the-notifications-api-in-microsoft-graph"></a>Integración con la API de notificaciones de Microsoft Graph

Puede integrar las aplicaciones con las notificaciones de Microsoft Graph siguiendo estos sencillos pasos: incorpore la aplicación a través del Centro de desarrollo de Windows, use el método [Crear notificación](/graph/api/projectrome-notification-post?view=graph-rest-beta) para publicar notificaciones y use el SDK del Proyecto Roma para recibir y administrar notificaciones en los clientes de la aplicación.  

Para obtener más información sobre cómo publicar notificaciones de usuario a través de Microsoft Graph, consulte la [referencia de API de notificaciones](/graph/api/resources/notifications-api-overview?view=graph-rest-beta).
 
Para obtener más información sobre cómo recibir y administrar las notificaciones mediante la integración con el SDK del Proyecto Roma, consulte la [documentación del SDK del Proyecto Roma](https://docs.microsoft.com/es-ES/windows/project-rome/) 

## <a name="see-also"></a>Vea también

- [Experiencias entre dispositivos en Microsoft Graph](cross-device-concept-overview.md)
- [Centro de desarrollo del Proyecto Roma](https://aka.ms/projectrome)
