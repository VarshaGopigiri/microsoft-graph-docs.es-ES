---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Copiar un archivo o carpeta
ms.openlocfilehash: 453a407775f6dc3b7afa8cb5d4d122f351c0a75f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031171"
---
# <a name="copy-a-driveitem"></a>Copiar un objeto DriveItem

Crea de forma asincrónica una copia de un objeto [driveItem][item-resource] (incluidos los elementos secundarios), en un nuevo elemento primario o con un nuevo nombre.

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
POST /drives/{driveId}/items/{itemId}/copy
POST /groups/{groupId}/drive/items/{itemId}/copy
POST /me/drive/items/{item-id}/copy
POST /sites/{siteId}/drive/items/{itemId}/copy
POST /users/{userId}/drive/items/{itemId}/copy
```

### <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.


| Nombre            | Valor                                          | Descripción                                                                                                 |
|:----------------|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| parentReference | [ItemReference](../resources/itemreference.md) | Opcional. Referencia al elemento primario en que se creará la copia.                                         |
| name            | string                                         | Opcional. El nuevo nombre de la copia. Si no se proporciona, se usará el mismo nombre que el original.    |

**Nota:** El valor _parentReference_ debe incluir los parámetros `driveId` y `id` para la carpeta de destino.

## <a name="example"></a>Ejemplo

Este ejemplo copia un archivo identificado por `{item-id}` en una carpeta identificada con un valor `driveId` y `id`.
La nueva copia del archivo se denominará `contoso plan (copy).txt`.

<!-- { "blockType": "request", "name": "copy-item", "scopes": "files.readwrite", "tags": "service.graph", "target": "action" } -->

```http
POST /me/drive/items/{item-id}/copy
Content-Type: application/json

{
  "parentReference": {
    "driveId": "6F7D00BF-FC4D-4E62-9769-6AEA81F3A21B",
    "id": "DCD0D3AD-8989-4F23-A5A2-2C086050513F"
  },
  "name": "contoso plan (copy).txt"
}
```

## <a name="response"></a>Respuesta

Devuelve detalles sobre cómo [supervisar el progreso](/graph/long-running-actions-overview) de la copia tras aceptar la solicitud.

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 202 Accepted
Location: https://contoso.sharepoint.com/_api/v2.0/monitor/4A3407B5-88FC-4504-8B21-0AABD3412717
```

El valor del encabezado `Location` proporciona una dirección URL para un servicio que devolverá el estado actual de la operación de copia.
Puede usar esta información para [determinar cuándo ha finalizado la copia](/graph/long-running-actions-overview).

### <a name="remarks"></a>Comentarios

En muchos casos, la operación de copia se realiza de forma asincrónica. La respuesta de la API solo indicará que la operación de copia se ha aceptado o rechazado, debido a que el nombre de archivo de destino ya está en uso.

[item-resource]: ../resources/driveitem.md

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
