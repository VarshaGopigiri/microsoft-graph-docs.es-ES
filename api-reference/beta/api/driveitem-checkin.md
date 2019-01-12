---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Proteger archivos
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: fb62dc05c60e26a6d1d6683913eeec0403d1c41c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27950812"
---
# <a name="check-in-changes-to-a-driveitem-resource"></a>Insertar cambios en el repositorio en un recurso DriveItem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Inserte un recurso DriveItem que se ha extraído del repositorio, lo que hace que la versión del documento esté disponible para otros usuarios.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.ReadWrite, Files.ReadWrite.All    |
|Aplicación | Files.ReadWrite.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/checkin
POST /groups/{groupId}/drive/items/{itemId}/checkin
POST /me/drive/items/{item-id}/checkin
POST /sites/{siteId}/drive/items/{itemId}/checkin
POST /users/{userId}/drive/items/{itemId}/checkin
```

### <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.


|   Nombre    | Valor  |                                                Descripción                                                |
| :-------- | :----- | :-------------------------------------------------------------------------------------------------------- |
| checkInAs | string | Opcional. El estado deseado del documento una vez completada la operación de inserción. Puede ser `published` o no especificarse. |
| comment   | string | Un comentario de inserción asociado a la versión.                                                   |

## <a name="example"></a>Ejemplo

Este ejemplo inserta un archivo identificado por `{item-id}` en el repositorio.

<!-- { "blockType": "request", "name": "checkin-item", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /drives/{drive-id}/items/{item-id}/checkin
Content-Type: application/json

{
  "comment": "Updating the latest guidelines"
}
```

## <a name="response"></a>Respuesta

Si se realiza correctamente, la llamada API devuelve `204 No content`.

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No content
```

### <a name="remarks"></a>Comentarios


[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
