---
title: Tipo de recurso settingTemplateValue
description: Representa una definición de configuración de plantilla individual, incluido el valor predeterminado de la configuración, en caso de que la configuración no tenga instancias.
ms.openlocfilehash: 00e424e36338855d8ef603d06c7a9ee52a99c621
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032080"
---
# <a name="settingtemplatevalue-resource-type"></a>Tipo de recurso settingTemplateValue

Representa una definición de configuración de plantilla individual, incluido el valor predeterminado de la configuración, en caso de que la configuración no tenga instancias.

### <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------------|:--------|:----------|
|defaultValue|String| Valor predeterminado para la configuración. |
|description|String| Descripción de la configuración. |
|nombre|String| Nombre de la configuración. |
|tipo|String| Tipo de la configuración. |

### <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.settingTemplateValue"
}-->

```json
{
  "defaultValue": "String",
  "description": "String",
  "name": "String",
  "type": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "settingTemplateValue resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->