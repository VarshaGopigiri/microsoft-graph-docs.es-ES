---
title: Tipo de recurso outlookItem
description: Aquí tiene una representación JSON del recurso
ms.openlocfilehash: 5f81598b62d2b47230f4a7ce16d17b8056bc9874
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029384"
---
# <a name="outlookitem-resource-type"></a>Tipo de recurso outlookItem



## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "abstract": true,
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.outlookItem"
}-->

```json
{
  "categories": ["string"],
  "changeKey": "string",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedDateTime": "String (timestamp)"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|categories|Colección String|Las categorías asociadas con el elemento|
|changeKey|String|Identifica la versión del elemento. Cada vez que se cambia el elemento, changeKey cambia también. Esto permite a Exchange aplicar los cambios a la versión correcta del objeto. Solo lectura.|
|createdDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|id|String| Solo lectura.|
|lastModifiedDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|

## <a name="relationships"></a>Relaciones
Ninguno

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
