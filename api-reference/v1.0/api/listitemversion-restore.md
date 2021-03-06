---
title: Restaurar una versión anterior de un objeto ListItem
description: Restaure una versión anterior de un objeto ListItem para que sea la versión actual. Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del elemento.
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 3ba63f56838d07a0031baf613dec8e0847aaf2e6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27963398"
---
# <a name="restore-a-previous-version-of-a-listitem"></a>Restaurar una versión anterior de un objeto ListItem

Restaure una versión anterior de un objeto ListItem para que sea la versión actual. Esto creará una versión con el contenido de la versión anterior, pero conservará todas las versiones existentes del elemento.

## <a name="permissions"></a>Permisos

Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|            Tipo de permiso             |         Permisos (de menos a más privilegiados)          |
| :------------------------------------- | :----------------------------------------------------------- |
| Delegado (cuenta profesional o educativa)     | Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All |
| Delegado (cuenta personal de Microsoft) | N/D                                                          |
| Aplicación                            | Sites.ReadWrite.All, Sites.Manage.All, Sites.FullControl.All |

## <a name="http-request"></a>Solicitud HTTP

<!-- { "blockType": "ignored" } -->

```http
POST /sites/{site-id}/items/{item-id}/versions/{version-id}/restoreVersion
POST /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

### <a name="request-body"></a>Cuerpo de solicitud

No es necesario ningún cuerpo de solicitud.

## <a name="example"></a>Ejemplo

En este ejemplo, se restaura una versión de un recurso listItem identificado por `{item-id}` y `{version-id}`.

<!-- { "blockType": "request", "name": "restore-item-version-listItem", "scopes": "files.readwrite sites.readwrite.all", "target": "action", "tags": "service.graph service.sharepoint" } -->

```http
POST /sites/{site-id}/lists/{list-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

## <a name="response"></a>Respuesta

Si se realiza correctamente, la llamada API devuelve `204 No Content`.

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No Content
```

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
