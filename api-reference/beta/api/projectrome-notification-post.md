---
title: Crear y enviar una notificación
description: 'Crear y enviar una notificación de identificación de un usuario a través de Microsoft Graph. La notificación se almacena en la notificación de Microsoft Graph fuente almacén y se envía a todos los clientes de la aplicación en todos los extremos de dispositivo que el usuario ha iniciado sesión en.  '
localization_priority: Normal
ms.prod: project-rome
ms.openlocfilehash: d8258e0da04f199a0f40bdb2a2ec85e01d5d5faf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27975935"
---
# <a name="create-and-send-a-notification"></a>Crear y enviar una notificación
> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Crear y enviar una notificación de identificación de un usuario a través de Microsoft Graph. La notificación se almacena en la notificación de Microsoft Graph fuente almacén y se envía a todos los clientes de la aplicación en todos los extremos de dispositivo que el usuario ha iniciado sesión en.  
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Notifications.ReadWrite.CreatedByApp    |
|Delegado (cuenta personal de Microsoft) | Notifications.ReadWrite.CreatedByApp    |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /me/notifications/
```
## <a name="request-headers"></a>Encabezados de solicitud
|Nombre | Tipo | Descripción|
|:----|:-----|:-----------|
|Autorización | string |El encabezado authorization se utiliza para pasar las credenciales del usuario que realiza llamada. Bearer {token}. Obligatorio. |
## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto de [notificación](../resources/projectrome-notification.md) .

## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve el `201 Created` código de respuesta que indica que la notificación se ha creado y almacenados correctamente. 
## <a name="example"></a>Ejemplo
#### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.

```http
POST https://graph.microsoft.com/beta/me/notifications/
Content-type: application/json

{
    "targetHostName": "graphnotifications.sample.windows.com",
    "appNotificationId": "testDirectToastNotification",
    "expirationDateTime": "2018-08-29T23:51:33.000Z",
    "payload": {
        "visualContent": {
            "title": "Hello World!",
            "body": "Notifications are Great!"
        }
    },
    "targetPolicy": {
        "platformTypes": [
        "windows",
        "android"
        ]
    },
    "priority": "High",
    "groupName": "TestGroup",
    "displayTimeToLive": "23"
}
```

#### <a name="response"></a>Respuesta
Este es un ejemplo de la respuesta.

```http
HTTP/1.1 201
Content-Type: application/json
location: https://graph.microsoft.com/beta/me/notifications/518c4fb1-c565-4d67-95c4-bcc3eb8eda1b

{
    "@odata.context": "https://graph.microsoft.com/test872018/$metadata#users('graphNotificationsUser%40contoso.com')/notifications/$entity",
    "appNotificationId": "testDirectToastNotification",
    "displayTimeToLive": 23,
    "expirationDateTime": "2018-08-24T12:31:53.858Z",
    "groupName": "TestGroup",
    "id": "cd5c5e6a-99ce-470a-9982-c47635e73620",
    "priority": "1",
    "payload": {
        "visualContent": {
            "title": "Hello World!",
            "body": "Notifications are Great!"
        }
    }
}
```


