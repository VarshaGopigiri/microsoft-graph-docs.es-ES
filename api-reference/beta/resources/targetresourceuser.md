---
title: tipo de recurso targetResourceUser
description: Indica el objeto de usuario que se ha agregado, actualiza o elimina los administradores como parte de la actividad de auditoría. Deriva el recurso targetResource.
ms.openlocfilehash: 632d0551b3aba434c3309c8c874947708eb9a9f5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086431"
---
# <a name="targetresourceuser-resource-type"></a>tipo de recurso targetResourceUser
Indica el objeto de usuario que se ha agregado, actualiza o elimina los administradores como parte de la actividad de auditoría. Deriva el recurso [targetResource](targetresource.md) .


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|userPrincipalName|String|Indica el identificador único del usuario. Hace referencia al identificador de usuario para un usuario específico.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.targetResourceUser"
}-->

```json
{
  "userPrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "targetResourceUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->