---
title: Crear o reemplazar un historyItem
description: Crear un nuevo o reemplazar un elemento de historial existente para una actividad de usuario existente.
ms.openlocfilehash: a33c5cb295ce0cd954c37154bc85eac0322937e0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032196"
---
# <a name="create-or-replace-a-historyitem"></a>Crear o reemplazar un historyItem

Crear un nuevo o reemplazar un elemento de historial existente para una actividad de usuario existente.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).


|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | UserActivity.ReadWrite.CreatedByApp    |
|Delegado (cuenta personal de Microsoft) | UserActivity.ReadWrite.CreatedByApp    |
|Aplicación | No admitida. |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
PUT /me/activities/{id}/historyItems/{id}
```

Identificador debe ser un GUID.

## <a name="request-headers"></a>Encabezados de solicitud

|Nombre | Tipo | Descripción|
|:----|:-----|:-----------|
|Authorization | string | {token} de portador. Obligatorio.|

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcionar una representación JSON de un objeto [historyItem](../resources/projectrome-historyitem.md) .

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve el `201 Created` código de respuesta si se ha creado la historyItem o `200 OK` si se ha sustituido el historyItem.

## <a name="example"></a>Ejemplo

#### <a name="request"></a>Solicitud

Aquí tiene un ejemplo de la solicitud.

<!-- {
    "blockType": "ignored",
    "name": "upsert_historyItem"
} -->

```http
PUT https://graph.microsoft.com/v1.0/me/activities/{activity-id}/historyItems/{item-id}
Content-type: application/json
Content-length: 364

{
    "startedDateTime": "2015-02-11T20:54:04.3457274+00:00",
    "userTimezone": "Africa/Casablanca",
    "lastActiveDateTime": "2015-02-11T20:54:04.3457274+00:00"
}
```

#### <a name="response"></a>Respuesta

Aquí tiene un ejemplo de la respuesta.

<!-- {
    "blockType": "ignored",
    "truncated": true,
    "@odata.type": "microsoft.graph.activityHistoryItem"
} -->

```http
HTTP/1.1 200 OK
Content-Type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#users('user%40contoso.com')/activities('13881113971988980728')/historyItems/$entity",
    "status": "updated",
    "userTimezone": "Africa/Casablanca",
    "createdDateTime": "2018-02-26T20:28:22.14Z",
    "lastModifiedDateTime": "2018-02-26T20:28:22.155Z",
    "id": "9d0b74e4-4b41-43ea-b34d-f9c1bf9f809c",
    "startedDateTime": "2018-02-26T20:54:04.345Z",
    "lastActiveDateTime": "2018-02-26T20:54:24.345Z",
    "expirationDateTime": "2018-03-28T20:28:22.14Z",
    "activeDurationSeconds": 20
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Upsert historyitem",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->