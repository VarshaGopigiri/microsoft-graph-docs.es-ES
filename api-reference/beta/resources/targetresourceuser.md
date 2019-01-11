---
title: tipo de recurso targetResourceUser
description: Indica el objeto de usuario que se ha agregado, actualiza o elimina los administradores como parte de la actividad de auditoría. Deriva el recurso targetResource.
localization_priority: Normal
ms.openlocfilehash: 9c71ead1b358b72a1b531abac56018fa71d084e8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831932"
---
# <a name="targetresourceuser-resource-type"></a>tipo de recurso targetResourceUser
Indica el objeto de usuario que se ha agregado, actualiza o elimina los administradores como parte de la actividad de auditoría. Deriva el recurso [targetResource](targetresource.md) .


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|userPrincipalName|Cadena|Indica el identificador único del usuario. Hace referencia al identificador de usuario para un usuario específico.|

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
