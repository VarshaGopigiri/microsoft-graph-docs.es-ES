---
title: tipo de recurso attributeMapping
description: Define cómo deben flujo de valores para el atributo de destino determinada durante la sincronización.
localization_priority: Normal
ms.openlocfilehash: 6c7a6367684b3e11013355b6d4726afe3346dab9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825280"
---
# <a name="attributemapping-resource-type"></a>tipo de recurso attributeMapping

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Define cómo deben flujo de valores para el atributo de destino determinada durante la sincronización.

## <a name="properties"></a>Propiedades

| Propiedad                  | Tipo                      | Descripción    |
|:--------------------------|:--------------------------|:---------------|
|defaultValue               | String                    |Valor que se usará en caso de que la propiedad de **origen** se evalúa a predeterminado `null`. Opcional.|
|exportMissingReferences    |Cadena                     |Solo para uso interno.|
|flowBehavior               |attributeFlowBehavior      |Define cuándo se debe exportar este atributo en el directorio de destino. Los valores posibles son: `FlowWhenChanged` y `FlowAlways`. El valor predeterminado es `FlowWhenChanged`. |
|Tasa                   |attributeFlowType          |Define cuándo debe actualizarse este atributo en el directorio de destino. Los valores posibles son: `Always` (valor predeterminado), `ObjectAddOnly` (sólo cuando se crea un objeto nuevo), `MultiValueAddOnly` (sólo cuando el cambio va a agregar nuevos valores a un atributo de varios valores). |
|matchingPriority           |Int32                      |Si es mayor que 0, se usará este atributo para llevar a cabo a una coincidencia inicial de los objetos entre los directorios de origen y de destino. El motor de sincronización intentará buscar el objeto que coincida con el atributo con el valor más bajo de coincidencia prioridad en primer lugar. Si no se ha encontrado el atributo con la siguiente prioridad coincidente se va a usar y así sucesivamente un hasta que se encuentra coincidencia o se dejan no más atributos coincidentes. Sólo los atributos que se espera que tienen valores únicos, como correo electrónico, deben usarse como atributos coincidentes.|
|source                     |[attributeMappingSource](synchronization-attributemappingsource.md)     | Define cómo debe ser un valor extrajo (o transforma) desde el objeto de origen. |
|/TargetAttributeName        |Cadena                     |Nombre del atributo en el objeto de destino. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attributeMapping"
}-->

```json
{
  "defaultValue": "String",
  "exportMissingReferences": true,
  "flowBehavior": "String",
  "flowType": "String",
  "matchingPriority": 1024,
  "source": {"@odata.type": "microsoft.graph.attributeMappingSource"},
  "targetAttributeName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attributeMapping resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
