---
title: Tipo de recurso settingValue
description: Una configuración que representa un par nombre-valor.
ms.openlocfilehash: b47c5c746117390cfd59db71d832928e482403b9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032673"
---
# <a name="settingvalue-resource-type"></a>Tipo de recurso settingValue

Una configuración que representa un par nombre-valor.

### <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|name|String| Nombre de la configuración (según lo definido por la plantilla [groupSettingTemplate](groupsettingtemplate.md)). |
|value|String| Valor de la configuración. |

### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.settingValue"
}-->

```json
{
  "name": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "settingValue resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->