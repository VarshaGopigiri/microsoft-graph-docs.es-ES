---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: MentionAction
ms.openlocfilehash: be873ba2b5f9bc1fdd387407c1036435dc6f1fc7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086264"
---
# <a name="mentionaction-resource-type"></a>Tipo de recurso MentionAction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **MentionAction** proporciona información sobre un recurso [activity][] que mencionó a usuarios.

[activity]: itemactivity.md

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.mentionAction"
}-->

```json
{
  "mentionees": [{"@odata.type": "microsoft.graph.identitySet"}]
}
```

## <a name="properties"></a>Propiedades

| Nombre de propiedad | Tipo                       | Descripción
|:--------------|:---------------------------|:-----------------------------
| mentionees    | Colección [identitySet][] | Las identidades de los usuarios mencionados en esta acción.

[identitySet]: identityset.md

## <a name="remarks"></a>Comentarios

Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.

<!-- {
  "type": "#page.annotation",
  "description": "The MentionAction object provides information about who was mentioned during an activity.",
  "keywords": "activities,activity,action,mention",
  "section": "documentation",
  "tocPath": "Resources/MentionAction"
} -->
