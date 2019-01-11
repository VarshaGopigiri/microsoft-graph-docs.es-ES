---
title: " tipo de recurso controlScore"
description: Este recurso contiene una puntuación de inquilinos y una descripción para un control individual.
localization_priority: Normal
ms.openlocfilehash: d8c2d73205f00a9dd5f2f28fcee3c33778bb3276
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891472"
---
#  <a name="controlscore-resource-type"></a>tipo de recurso controlScore

Este recurso contiene una puntuación de inquilinos y una descripción para un control individual.

|Nombre |Tipo |Description |
|:--|:--|:--|
|   controlName |   Cadena  |   Nombre único de control |
|   score   |   Doble  |  Inquilino de lograr la puntuación para el control (día a día varía, dependiendo de las operaciones del inquilino en el control). |
|   controlCategory |   Cadena  |  Categoría de acción de control (identidad, datos, dispositivos, aplicaciones, infraestructura). |
|   descripción |   Cadena  |  Descripción del control. |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.controlScore"
}-->

```json
{
  "controlName": "String",
  "score": "String",
  "controlCategory": "String",
  "description": "String"
}

```


<!-- {
  "type": "#page.annotation",
  "description": "controlScore resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
