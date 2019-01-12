---
title: Usar la API de REST de notificaciones en Microsoft Graph
description: Puede usar las notificaciones de la API de Microsoft Graph para enviar notificaciones de inserción a un usuario. Simplemente una cuenta de usuario para enviar una notificación de destino, y la plataforma le ofrecerá la notificación a todos los extremos de dispositivo. Las solicitudes de la API de notificaciones se realizan en nombre de un usuario a través de permisos delegados y el [permiso de notificación]( /graph/permissions_reference), que se puede usar con puede ser cuentas de Microsoft o las cuentas de trabajo o escuela.
localization_priority: Priority
ms.prod: project-rome
ms.openlocfilehash: 68a20b655eecea7d5afb82677178593b094a9cc3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931499"
---
# <a name="use-the-notifications-rest-api-in-microsoft-graph"></a>Usar la API de REST de notificaciones en Microsoft Graph

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Puede usar las notificaciones de la API de Microsoft Graph para enviar notificaciones de inserción a un usuario. Simplemente una cuenta de usuario para enviar una notificación de destino, y la plataforma le ofrecerá la notificación a todos los extremos de dispositivo. Las solicitudes de la API de notificaciones se realizan en nombre de un usuario a través de [permisos delegados](/graph/permissions-reference#delegated-permissions-application-permissions-and-effective-permissions) y el [permiso de notificación]( /graph/permissions_reference), que se puede usar con puede ser cuentas de Microsoft o las cuentas de trabajo o escuela.
Este tipo de notificación centrado en el usuario está representado por el recurso de [notificación](../resources/projectrome-notification.md) y se almacena en Microsoft Graph. A continuación, se accede a y administrado por la aplicación de publicación a través de las [API de SDK de Project Roma](https://github.com/Microsoft/project-rome). 

## <a name="next-steps"></a>Pasos siguientes
- Consulte el [recurso de notificación](../resources/projectrome-notification.md) y crear notificaciones para integrarse con los usuarios. 
- Pruebe la API en el [Probador de Graph](https://developer.microsoft.com/graph/graph-explorer).
