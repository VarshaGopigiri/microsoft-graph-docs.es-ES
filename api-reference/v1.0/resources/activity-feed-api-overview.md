---
title: Usar la API de REST de fuente de actividades
description: 'Puede usar la actividad de fuente API en Microsoft Graph para reanudar actiity de un usuario en dispositivos y plataformas. Solicitudes de API de fuentes de actividades se realizan en nombre de un usuario a través de permisos delegados y el permiso de actividad de usuario, que se puede usar con cuentas personales o trabajos y escolar. '
ms.openlocfilehash: 25b7af22671256a6dd48536a7da232f16251184f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029086"
---
# <a name="use-the-activity-feed-rest-api"></a>Usar la API de REST de fuente de actividades

Puede usar la actividad de fuente API en Microsoft Graph para reanudar actiity de un usuario en dispositivos y plataformas. Solicitudes de API de fuentes de actividades se realizan en nombre de un usuario a través de [permisos delegados](/graph/permissions-reference#delegated-permissions-application-permissions-and-effective-permissions) y el [permiso de actividad de usuario](/graph/permissions-reference), que se puede usar con cuentas personales o trabajos y escolar. 

Las actividades del usuario representadas por el recurso de [actividad](https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/projectrome_activity) y se organizan en una fuente basada en la hora representada por la colección me / actividades. 
<!-- Add missing content.
Each activity represents a unique... 
-->
## <a name="what-makes-a-great-user-activity"></a>¿Qué hace que sea una actividad de usuario excelente?

Las actividades del usuario acaba no iniciar aplicaciones — son vínculos profundos en contenido específico dentro de la aplicación. Las actividades de usuario crear no sólo puede utilizarse en su propia aplicación, pero también aparecerán en Cortana y escala de tiempo de Windows: tiende a más reengagement de aplicación y hacer que sea más fácil para los usuarios a seguir utilizando la aplicación en varios dispositivos.  

### <a name="what-should-become-an-activity"></a>¿Qué deben convertirse en una actividad? 

Debido a que cada aplicación es diferente, es copia de seguridad a cada desarrollador de aplicaciones a comprender la mejor forma de asignar acciones dentro de la aplicación a las actividades del usuario. Por ejemplo, juegos podrían crear una actividad para cada campaña, aplicaciones de creación de documento es posible que crear una actividad para cada documento único y aplicaciones de línea de negocio podrían crear una actividad para cada flujo de trabajo. 

Aplique las siguientes directrices como definir activitites en su aplicación:

**Hacer:** Registre una sola actividad para un grupo de acciones de usuario relacionados. Si la aplicación se usa para una secuencia de contenido relacionado, probablemente tiene sentido para registrar una actividad único para la sesión de contratación todo.  

*Escenarios de lista de reproducción:* Esto es especialmente importante para las listas de reproducción de música o programas de TV: una actividad de usuario solo se puede actualizar para mostrar el progreso. En este caso, tendrá una actividad de usuario único con varios [elementos del historial](https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/projectrome_historyitem) que representa los períodos de compromiso a través de varios días o semanas.  

**Hacer:** Almacenar datos de usuario a la nube. Si desea admitir actividades entre el dispositivo, debe asegurarse de que se almacena el contenido necesario para esta actividad vuelva a atraer a una ubicación en la nube. Por ejemplo, si publica una actividad cada vez que un usuario edita un documento, el documento debe almacenarse en la nube en lugar de hacerlo localmente en el dispositivo del usuario con el fin de habilitar reengagement entre el dispositivo.  

**No:** Crear una actividad de usuario para las acciones que los usuarios no necesitan para reanudar en el futuro. Si la aplicación se usa para llevar a cabo operaciones simples únicas que no se mantienen estado para realizar un seguimiento en el futuro, probablemente no es necesario escribir una actividad de usuario. 

Para ser más precisos, incluso si las actividades del usuario se muestran en la escala de tiempo de Windows, esto no está diseñado como una herramienta de control de versiones: selección de una actividad basados en documentos siempre debe mostrar la versión más reciente de ese documento (incluidos los cambios realizados por otro usuario).

**No:** Crear una actividad de usuario para acciones completadas por *otros usuarios*. Si alguien le envía al usuario un mensaje o @mentions el usuario dentro de la aplicación, no debe escribir una actividad nueva. Estas interacciones se satisfacen exponiendo las notificaciones.  

*Escenarios de colaboración:* Si varias personas trabajan en la misma actividad (por ejemplo, un documento de Word), habrá casos cuando otro usuario ha realizado cambios en el documento después de que se modificó por última vez. En este caso, los desarrolladores de aplicaciones es posible que desee actualizar los elementos visuales en la actividad para reflejar los cambios realizan en el documento. Para ello, la aplicación podría actualizar la actividad existente sin crear un nuevo elemento de historial. 

>**Nota:** Si está publicando actividades para una aplicación web, es importante incluir ambos un `activationURL` y un `fallbackURL` para cada uno de sus actividades. Las actividades iniciará el usuario en la aplicación según lo esperado de experiencias de Microsoft al igual que la escala de tiempo de Windows. 

## <a name="app-interaction-patterns-and-user-activities"></a>Patrones de interacción de la aplicación y las actividades del usuario 
Las actividades de usuario que cree variará en función de la trama de interacción de la aplicación. Aunque cada aplicación es diferente, la mayoría se inscriben en uno de los siguientes patrones de interacción: 

* **Aplicaciones basadas en el documento** : crear una actividad por cada documento con uno o más registros de historial que refleja períodos de uso. Es importante que se debe actualizar su tarjeta de actividad, tal y como se realizan cambios en el documento. 
* **Aplicaciones de reproducción de medios** : crear una actividad por una agrupación lógica de contenido como una lista de reproducción, programa o independiente el contenido. 
* **Juegos** : crear una actividad para cada uno de ellos guarda juego o mundiales. Si su juego es compatible con sólo una única secuencia de niveles, puede escribir la misma actividad a través del tiempo, aunque es posible que desee actualizar su tarjeta para mostrar su progreso o los logros más recientes. 
* **Aplicaciones de utilidad** : si no hay nada dentro de la aplicación y que los usuarios desearán para reanudar, no debe publicar las actividades. Un buen ejemplo es una aplicación simple de un único propósito como la calculadora. 
* **Aplicaciones de línea de negocio** , existen muchas aplicaciones para la administración de tareas sencillas o flujos de trabajo. Crear una actividad para cada flujo de trabajo independiente que tiene acceso a través de la aplicación. Por ejemplo, cada informe de gastos será una actividad independiente, porque es posible que desee haga clic en esa actividad para ver si se ha aprobado.

*Algunas aplicaciones complejas incluyen varios patrones de interacción. Es posible que desee que se deben seguir los patrones de creación de actividad de usuario diferentes para distintos escenarios controlados por la aplicación.*

<!-- Add content or remove H2.
## Common use cases 
-->

## <a name="next-steps"></a>Pasos siguientes

- Consulte el [recurso de la actividad](https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/projectrome_activity) y definir las actividades de su aplicación para ayudar a los usuarios reanudar tareas importantes.
- Explore los ejemplos de [ejemplos de tarjeta adaptable](https://adaptivecards.io/samples/) para ideas realizar sus actividades de **pop**.  
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).

**¿Necesita más ideas?** 

- Vea [cómo experiencias de Microsoft están usando las actividades](https://channel9.msdn.com/events/Build/2017/B8108).
- Obtenga información sobre [la actividad de API de fuente y seleccionar donde quedó](https://channel9.msdn.com/Events/Windows/Windows-Developer-Day-Fall-Creators-Update/WinDev011).
