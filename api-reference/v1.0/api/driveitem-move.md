---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Mover un archivo o carpeta
localization_priority: Normal
ms.openlocfilehash: 1112ff8a75502b763c6bf3937596248ab5b52ff9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836256"
---
# <a name="move-a-driveitem-to-a-new-folder"></a>Mover un objeto DriveItem a una carpeta nueva

Para mover un objeto DriveItem a un nuevo elemento primario, la aplicación solicita actualizar la **parentReference** del objeto DriveItem que se moverá.

Este es un caso especial del método [Update](driveitem-update.md).
La aplicación puede mover un elemento a un nuevo contenedor y actualizar otras propiedades del elemento en una sola solicitud.

No se pueden mover elementos entre [Drives](../resources/drive.md) con esta solicitud.

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
PATCH /drives/{drive-id}/items/{item-id}
PATCH /groups/{group-id}/drive/{item-id}
PATCH /me/drive/items/{item-id}
PATCH /sites/{site-id}/drive/items/{item-id}
PATCH /users/{user-id}/drive/items/{item-id}
```

## <a name="optional-request-headers"></a>Encabezados de solicitud opcionales

| Nombre          | Tipo   | Descripción                                                                                                                                                         |
|:--------------|:-------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| if-match      | String | Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide la eTag actual en la carpeta, se devuelve una respuesta `412 Precondition Failed`. |

## <a name="request-body"></a>Cuerpo de la solicitud

En el cuerpo de la solicitud, proporcione el nuevo valor de la propiedad **parentReference**. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

**Nota:** Al mover elementos a la raíz de una unidad, la aplicación no puede usar la sintaxis `"id:" "root"`.
La aplicación debe proporcionar el identificador real de la carpeta raíz para la referencia primaria.

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo

En este ejemplo, se mueve un elemento especificado mediante {item-id} a una carpeta en la unidad del usuario con el identificador `new-parent-folder-id`.

<!-- { "blockType": "request", "name": "move-item", "scopes": "files.readwrite", "tags": "service.graph" } -->

```http
PATCH /me/drive/items/{item-id}
Content-type: application/json

{
  "parentReference": {
    "id": "{new-parent-folder-id}"
  },
  "name": "new-item-name.txt"
}
```

### <a name="response"></a>Respuesta

En el ejemplo siguiente se muestra la respuesta de esta solicitud de movimiento.

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.driveItem", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "id": "0123456789abc",
  "name": "new-item-name.txt",
  "parentReference":
  {
    "driveId": "11231001",
    "path": "/drive/root:/Documents",
    "id": "1231203102!1011"
  }
}
```

## <a name="error-responses"></a>Respuestas de error

Vea [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.

[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Move an item to another location or rename the item.",
  "keywords": "move,rename,mv,change location",
  "section": "documentation",
  "tocPath": "Items/Move"
} -->
