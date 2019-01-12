---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Restaurar una versión anterior de un elemento de lista de SharePoint
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: b7c81022ebcb4f7afe02520c48f7cfbf103b2943
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983005"
---
# <a name="restore-a-previous-version-of-a-listitem"></a>Restaurar una versión anterior de un objeto ListItem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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

<!-- { "blockType": "request", "name": "restore-item-version-listItem", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /sites/{site-id}/items/{item-id}/versions/{version-id}/restoreVersion
```

## <a name="response"></a>Respuesta

Si se realiza correctamente, la llamada API devuelve `204 No content`.

<!-- { "blockType": "response" } -->

```http
HTTP/1.1 204 No content
```

<!-- {
  "type": "#page.annotation",
  "description": "Create a copy of an existing item.",
  "keywords": "copy existing item",
  "section": "documentation",
  "tocPath": "Items/Copy"
} -->
