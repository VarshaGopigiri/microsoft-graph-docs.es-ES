---
title: Experiencias multidispositivo en Microsoft Graph
description: 'En el mundo actual de varios dispositivos, la forma en que los consumidores usan los dispositivos abarca distintas plataformas y factores de forma: pueden leer las noticias de la mañana en sus tabletas, consultar el correo electrónico en el teléfono al ir al trabajo, y usar el equipo PC de escritorio en la oficina. Por la noche, puede que vean películas en las consolas multimedia del hogar y usen altavoces inteligentes para informarse sobre las noticias del día. El cliente medio usa varios dispositivos y plataformas a lo largo del día. '
localization_priority: Priority
ms.prod: project-rome
ms.openlocfilehash: 85d48d07f06d189f30c8eba9f7f0876353b3ff25
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920690"
---
# <a name="cross-device-experiences-in-microsoft-graph"></a>Experiencias multidispositivo en Microsoft Graph

En el mundo actual de varios dispositivos, la forma en que los consumidores usan los dispositivos abarca distintas plataformas y factores de forma: pueden leer las noticias de la mañana en sus tabletas, consultar el correo electrónico en el teléfono al ir al trabajo, y usar el equipo PC de escritorio en la oficina. Por la noche, puede que vean películas en las consolas multimedia del hogar y usen altavoces inteligentes para informarse sobre las noticias del día. El cliente medio usa varios dispositivos y plataformas a lo largo del día. 

En el pasado, el factor de forma impulsó distintos tipos de comportamiento entre los consumidores. Pero, hoy en día, los consumidores multidispositivo realizan todas sus actividades con todos sus dispositivos. Las tareas realizadas a diario (ya sea en el hogar con la familia o en el trabajo con los compañeros) no están por definición centradas en los dispositivos, sino más bien **centradas en las personas**. Los consumidores quieren ser capaces de usar cualquier pantalla que esté disponible, independientemente del origen de la entrada. En realidad, con frecuencia sienten que cada dispositivo tiene una limitación clara y, para trabajar en varios dispositivos, se necesitan acciones poco naturales, como enviarse a sí mismo un correo electrónico o usar unidades de memoria USB. Los clientes ven la fricción al cambiar entre dispositivos y, a veces, las tareas importantes se pierden debido a este cambio de contexto. Esto también es una complicación para los desarrolladores, ya que, cuando los clientes sienten fricción al usar una aplicación, también disminuye la interacción del cliente con la aplicación.

Microsoft está creando una plataforma para ofrecer experiencias que van más allá de un único dispositivo, ya que pueden armonizarse en varios dispositivos, permitiéndole crear escenarios **centrados en las personas** que se mueven con el usuario y desdibujan las líneas entre sus dispositivos, independientemente del factor de forma o la plataforma. Microsoft Graph ofrece único punto de conexión unificado para ofrecerle acceso a datos de Azure Active Directory y Office 365. Ahora, con Microsoft Graph, también puede obtener acceso a las actividades y dispositivos que pertenecen a sus clientes, y facilitar experiencias enriquecidas centradas en las personas que van más allá de los dispositivos y las plataformas. 

## <a name="why-invest-in-cross-device-experiences"></a>¿Por qué invertir en experiencias multidispositivo?

### <a name="let-customers-pick-up-where-they-leave-off-with-the-activity-feed-api"></a>Permitir que los clientes continúen donde lo dejaron con la API de fuente de actividades 
Con las actividades, puede capturar las tareas únicas para los usuarios de la aplicación que fluyen fácilmente entre cualquier plataforma y dispositivo, lo que les permite reanudar rápidamente su trabajo en la pantalla que prefieran. Con la fuente de actividades, puede crear una visión centrada en las personas de las tareas más importantes para los usuarios, lo que permite reducir la fricción al cambiar de la web al móvil y al equipo PC, y más allá. 

### <a name="build-rich-cross-device-experiences-by-using-the-device-relay-api"></a>Crear experiencias multidispositivo enriquecidas con la API de retransmisión de dispositivos 
Además de los dispositivos Microsoft (equipos PC, Windows Phone, Xbox, IoT, HoloLens y más), la API de retransmisión de dispositivos también expone los dispositivos con iOS y Android. Esto le permite traspasar realmente los límites entre los dispositivos de los usuarios. Puede crear aplicaciones que usen el entorno del usuario y crear experiencias enriquecidas que vayan más allá de un único dispositivo en tiempo real. 

### <a name="engage-users-with-human-centric-cross-device-notifications-preview"></a>Interactuar con los usuarios con notificaciones de varios dispositivos centradas en el individuo (versión preliminar)

Las notificaciones son una de las formas más eficaces y directas de comunicarse e interactuar con los usuarios. 

Con las API de notificaciones de Microsoft Graph, puede ofrecer notificaciones centradas en el individuo en vez de centradas en el dispositivo. Puede dirigirse a un usuario para enviar notificaciones y basarse en el marco de notificaciones de Microsoft Graph para ofrecer las notificaciones para cada punto de conexión en el que el usuario ha iniciado sesión. La administración de notificación de varios dispositivos es sencilla con las API de notificaciones de Microsoft Graph, para que pueda sincronizar las notificaciones de dispositivos de los usuarios y reducir la cantidad de redundancia e interrupción para los usuarios. 

## <a name="api-reference"></a>Referencia de la API
¿Busca la referencia de la API para estos servicios?

- [API para las experiencias en varios dispositivos de Microsoft Graph v1.0](/graph/api/resources/project-rome-overview?view=graph-rest-1.0)
- [API para las experiencias en varios dispositivos de Microsoft Graph beta](/graph/api/resources/project-rome-overview?view=graph-rest-beta)


## <a name="next-steps"></a>Pasos siguientes

- [Usar la API de Microsoft Graph para facilitar experiencias multidispositivo](/graph/api/resources/cross-device-reference-overview?view=graph-rest-1.0)
- [Más información sobre la API de fuente de actividades de Microsoft Graph](activity-feed-concept-overview.md)
- [Más información sobre la API de retransmisión de dispositivos en Microsoft Graph](device-relay-concept-overview.md)
- [Más información sobre la API de notificaciones de Microsoft Graph en Microsoft Graph](notifications-concept-overview.md)
