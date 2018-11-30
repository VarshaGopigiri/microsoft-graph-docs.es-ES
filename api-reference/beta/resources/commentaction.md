---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: CommentAction
ms.openlocfilehash: 92dc26945cd591de2ba107907a593159f1e128c9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090831"
---
# <a name="commentaction-resource-type"></a>Tipo de recurso CommentAction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **CommentAction** proporciona información sobre un comentario [activity][] realizado en un elemento.

[activity]: itemactivity.md

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.commentAction"
}-->

```json
{
  "isReply": false,
  "parentAuthor": {"@odata.type": "microsoft.graph.identitySet"},
  "participants": [{"@odata.type": "microsoft.graph.identitySet"}]
}
```

## <a name="properties"></a>Propiedades

| Nombre de propiedad    | Tipo                       | Descripción
|:-----------------|:---------------------------|:-----------------------------
| isReply          | boolean                    | Si es true, esta actividad fue una respuesta a un hilo de comentarios existente.
| parentAuthor     | [identitySet][]            | La identidad del usuario que inició el hilo de comentarios.
| participants     | Colección [identitySet][] | Las identidades de los usuarios que participan en este hilo de comentarios.

[identitySet]: identityset.md

## <a name="remarks"></a>Comentarios

Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.

<!-- {
  "type": "#page.annotation",
  "description": "The CommentAction object provides information about a comment that was made on an item.",
  "keywords": "activities,activity,action,comment",
  "section": "documentation",
  "tocPath": "Resources/CommentAction"
} -->
