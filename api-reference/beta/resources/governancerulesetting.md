---
title: tipo de recurso governanceRuleSetting
description: Representa las reglas que consta de la configuración de las funciones.
localization_priority: Normal
ms.openlocfilehash: 7554c96daec70a95cde5ab0c3faedfba74764cff
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894260"
---
# <a name="governancerulesetting-resource-type"></a>tipo de recurso governanceRuleSetting

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa las reglas que consta de la configuración de las funciones.


## <a name="properties"></a>Propiedades
|Propiedad      | Tipo         |Description|
|:-------------|:-------------|:----------|
|ruleIdentifier|Cadena        |El identificador de la regla. Por ejemplo, ``ExpirationRule`` y ``MfaRule``.|
|ajustes       |Cadena        |La configuración de la regla. El valor es una cadena JSON con una lista de pares de en el formato de Parameter_Name:Parameter_Value. Por ejemplo: `{"permanentAssignment":false,"maximumGrantPeriodInMinutes":129600}`|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.governanceRuleSetting"
}-->


```json
{
  "ruleIdentifier": "String",
  "setting": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceRuleSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
