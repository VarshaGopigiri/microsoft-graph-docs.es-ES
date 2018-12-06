---
title: Usar la API de fuente de actividades en Microsoft Graph para facilitar experiencias multidispositivo
description: Al usar las actividades, estas experiencias de Microsoft pueden facilitar la interacción con la aplicación. También puede mostrar actividades en las aplicaciones para ayudar a los usuarios a continuar con lo que estaban haciendo en cualquier dispositivo y desde cualquier plataforma, como Windows, Android y iOS.
ms.openlocfilehash: 768326a5a18962f28aebe2e66b7dbd2a95b1a7bb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27092765"
---
# <a name="using-the-activity-feed-api-in-microsoft-graph-to-enable-cross-device-experiences"></a>Usar la API de fuente de actividades en Microsoft Graph para facilitar experiencias multidispositivo

Las actividades mejoran la productividad de los usuarios, ya que les permiten reanudar rápidamente tareas importantes en la aplicación desde varios dispositivos. Microsoft mejora la productividad de los usuarios con sus aplicaciones mediante experiencias como Windows Timeline, Conjuntos de Windows, “Continúa desde donde lo dejaste” de Cortana y Microsoft Launcher, que usan la tecnología de la fuente de actividades. Al usar las actividades, estas experiencias de Microsoft pueden facilitar la interacción con la aplicación. También puede mostrar actividades en las aplicaciones para ayudar a los usuarios a continuar con lo que estaban haciendo en cualquier dispositivo y desde cualquier plataforma, como Windows, Android y iOS.

## <a name="why-integrate-with-activities"></a>¿Por qué integrar con las actividades?
### <a name="enable-experiences-that-flow-seamlessly-between-windows-android-linux-and-ios-devices"></a>Facilitar experiencias fluidas entre dispositivos con Windows, Android, Linux y iOS 
Las aplicaciones excelentes permiten a los usuarios realizar trabajos excelentes: facilitan una amplia variedad de escenarios de creatividad, productividad y entretenimiento. Volver a una tarea puede ser complicado, especialmente si el usuario quiere continuarla en otro dispositivo o plataforma. Al incorporar las actividades a las aplicaciones, puede ayudar a los usuarios a volver rápidamente a tareas recientes en la pantalla que tengan a su disposición: pueden cambiar de la web a un dispositivo móvil y de ahí a un equipo de escritorio, y hacer el cambio contrario. Con los elementos del historial, los usuarios pueden ver fácilmente las actividades que usaron más recientemente, cuándo y durante cuánto tiempo.   

Cada actividad de usuario representa un único destino dentro de la aplicación: una página de producto, un programa de televisión, un documento o una campaña actual en un juego. Solo necesita un vínculo profundo para reanudar la actividad de la aplicación. Use la característica [Obtener actividades recientes](/graph/api/projectrome-get-recent-activities?view=graph-rest-1.0) para crear una lista de los productos vistos recientemente para su aplicación de compras, o bien una lista de lectura actual de libros y artículos de noticias. 

### <a name="create-richer-activities-for-any-experience-with-adaptive-cards"></a>Crear actividades enriquecidas para cualquier experiencia con tarjetas adaptables
Cuando las actividades se representan en las experiencias de Microsoft, como Windows Timeline, se muestran mediante el marco [Tarjeta adaptable](https://adaptivecards.io/), que le permite crear tarjetas enriquecidas y atractivas para presentar las actividades de la aplicación. También puede usar el SDK de Tarjetas adaptables para representar tarjetas enriquecidas en su aplicación. Si no proporciona una tarjeta adaptable para cada actividad, crearemos automáticamente una tarjeta de actividad sencilla basada en el nombre y el icono de la aplicación, el campo de título (obligatorio) y el campo de descripción (opcional). 

### <a name="let-microsoft-help-drive-app-usage-with-features-that-reach-hundreds-of-millions-of-customers"></a>Dejar que Microsoft impulse el uso de la aplicación con características que llegan a cientos de millones de clientes
La integración con las actividades de usuario no solo permite a los usuarios reanudar fácilmente las actividades en la aplicación, sino que también permite obtener acceso a un creciente conjunto de experiencias de Microsoft para Windows, iOS y Android (experiencias diseñadas para mejorar la productividad de los usuarios y facilitar la interacción de los usuarios con la aplicación en todos los dispositivos). Con Microsoft Graph, puede facilitar la integración con las actividades de usuario solo una vez y, con ello, llegar a cientos de millones de consumidores y a decenas de millones de clientes en organizaciones que usan Windows y en productos de Microsoft para dispositivos con iOS y Android.

![Captura de pantalla de Windows Timeline](https://winblogs.azureedge.net/win/2017/05/22-591a3ec9833f4.jpg)

## <a name="see-also"></a>Vea también

- [Experiencias multidispositivo en Microsoft Graph](cross-device-concept-overview.md)
- [Usar la API de fuente de actividades para reanudar la actividad de un usuario en varios dispositivos](/graph/api/resources/activity-feed-api-overview?view=graph-rest-1.0)
- [Publicar actividades y elementos del historial con una solicitud con una inserción profunda](/graph/api/projectrome-put-activity?view=graph-rest-1.0#example-2---deep-insert)
- [Más información sobre el proyecto Rome](https://aka.ms/projectrome)
