---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: CommentAction
localization_priority: Normal
ms.openlocfilehash: 952a86161047ab869238feaba50b8ad4d8ce0658
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845601"
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

| Nombre de la propiedad    | Tipo                       | Descripción
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
