---
title: Tipo de recurso settingTemplateValue
description: Representa una definición de configuración de plantilla individual, incluido el valor predeterminado de la configuración, en caso de que la configuración no tenga instancias.
localization_priority: Normal
ms.openlocfilehash: e941630ab72363db1c4be40079cf2af9e40ff002
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811868"
---
# <a name="settingtemplatevalue-resource-type"></a>Tipo de recurso settingTemplateValue

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una definición de configuración de plantilla individual, incluido el valor predeterminado de la configuración, en caso de que la configuración no tenga instancias.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|defaultValue|string|Valor predeterminado para la configuración. Solo lectura.|
|description|string|Descripción de la configuración. Solo lectura.|
|name|string|Nombre de la configuración. Solo lectura.|
|type|string|Tipo de la configuración. Solo lectura.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.settingTemplateValue"
}-->

```json
{
  "defaultValue": "string",
  "description": "string",
  "name": "string",
  "type": "string"
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
