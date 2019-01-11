---
title: 'Usar la API de Microsoft Graph para trabajar con Project Roma '
description: 'Roma de proyecto es una iniciativa de Microsoft para crear una plataforma que permite a los programadores de la aplicación crear grandes experiencias entre el dispositivo. Roma Project permite diferentes capacidades que se conectan los distintos servicios y los extremos de cliente cuando los signos de usuario con el mismo Microsoft cuenta o trabajan o escuela cuenta. Esto le permite implementar experiencias entre el dispositivo y multiplataforma que se centran en las tareas de usuario en lugar de dispositivos. '
localization_priority: Normal
ms.openlocfilehash: 9f3b923bff5bad93036a1784090c8ce00763650f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830005"
---
# <a name="use-the-microsoft-graph-api-to-work-with-project-rome"></a>Usar la API de Microsoft Graph para trabajar con Project Roma 

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

[Roma de proyecto](https://developer.microsoft.com/en-us/windows/project-rome) es una iniciativa de Microsoft para crear una plataforma que permite a los programadores de la aplicación crear grandes experiencias entre el dispositivo. Roma Project permite diferentes capacidades que se conectan los distintos servicios y los extremos de cliente cuando los signos de usuario con el mismo Microsoft cuenta o trabajan o escuela cuenta. Esto le permite implementar experiencias entre el dispositivo y multiplataforma que se centran en las tareas de usuario en lugar de dispositivos. 

Tres funciones principales de Project Roma se exponen a través de Microsoft Graph que le ayudarán a habilitar grandes experiencias de dispositivo cruzado: actividades, dispositivos y notificaciones. 

## <a name="activities"></a>Actividades

Actividades en Microsoft Graph habilitar compromiso de usuario de unidad con sus aplicaciones en dispositivos y plataformas. Una actividad es la unidad de contratación de usuario y se compone de tres componentes:

- Un vínculo profundo
- Una representación visual
- Los metadatos de contenido que describe la actividad, con el [https://schema.org/](https://schema.org/) shared vocabulario

Cuando se crea una sesión de una aplicación, se agrega un elemento de historial a la actividad para reflejar el período de contratación de usuario. Cada vez que un usuario reengages con una actividad, se agrega un nuevo elemento de historial a la actividad para acumular compromiso de usuario.

Cuando una aplicación publica los objetos de actividad de usuario, el objeto se mostrará en algunas de las nuevas superficies de la interfaz de usuario de Windows; Por ejemplo, las notificaciones de Cortana y escala de tiempo. Puede especificar metadatos enriquecidos (para permitir actividades se presenten en el contexto de derecho) y elementos visuales enriquecidos (con el marcado de la [Tarjeta de adaptable](https://adaptivecards.io/) ) en los objetos de actividad.

Puede usar las siguientes API de gráfico de Microsoft para crear y recuperar las actividades del usuario:

- [Crear o reemplazar la actividad](../api/projectrome-put-activity.md)
- [Obtener las actividades](../api/projectrome-get-activities.md)
- [Obtener actividades recientes](../api/projectrome-get-recent-activities.md)
- [Eliminar una actividad](../api/projectrome-delete-activity.md)
- [Crear o reemplazar un elemento de historial](../api/projectrome-put-historyitem.md)
- [Eliminar un elemento de historial](../api/projectrome-delete-historyitem.md)

## <a name="devices"></a>Dispositivos

Puede usar las API de Roma de Project en Microsoft Graph para que:

- Descubrir y conectarse a dispositivos del usuario
- Iniciar aplicaciones en esos dispositivos de forma remota
- Enviar mensajes a las aplicaciones en esos dispositivos

Con estas API, puede crear aplicaciones que creación experiencias enriquecidas que sobrepasar un único dispositivo. Por ejemplo, puede ampliar la aplicación para iniciar en una pantalla más grande. O bien, puede crear una experiencia complementaria para una aplicación en otro de los dispositivos del usuario.

Puede usar las siguientes API de gráfico de Microsoft para comunicarse con otros dispositivos de Windows:

- [Lista de dispositivos del usuario](../api/user-list-devices.md)
- [Enviar un comando a un dispositivo](../api/send-device-command.md)
- [Obtener el estado del comando](../api/get-device-command-status.md)

## <a name="notifications"></a>Notificaciones

Puede usar las API de notificaciones en Microsoft Graph para entregar notificaciones a través de varios extremos que ha iniciado sesión en el mismo usuario en. Puede dirigir un usuario directamente al registrar las notificaciones en lugar de preocuparse acerca de las direcciones o canales de dispositivo. De esta forma, puede centrarse en el diseño de los escenarios de notificación derecho en un humanos centrada, en lugar de una manera centrada en el dispositivo. 

Puede publicar una notificación visual directa o una notificación de datos sin procesar. Cuando se envía una notificación de datos sin procesar a un extremo del dispositivo, a continuación, puede usar el [SDK de cliente](https://github.com/Microsoft/project-rome) (Microsoft Graph notificaciones SDK para Windows, proyecto Roma SDK para iOS y Android) para recibir y administrar las notificaciones. Cuando se entrega una notificación visual directa a un extremo del dispositivo, muestra la notificación nativa específicos de la plataforma para el usuario. 

Para obtener información detallada, vea [crear y enviar una notificación](../api/projectrome-notification-post.md).

