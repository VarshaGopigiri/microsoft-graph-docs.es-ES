---
title: " tipo de recurso controlScore"
description: Este recurso contiene una puntuación de inquilinos y una descripción para un control individual.
ms.openlocfilehash: 67059c1a7382416411709f02c609c90b20a673b4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084476"
---
#  <a name="controlscore-resource-type"></a>tipo de recurso controlScore

Este recurso contiene una puntuación de inquilinos y una descripción para un control individual.

|Nombre |Tipo |Descripción |
|:--|:--|:--|
|   controlName |   String  |   Nombre único de control |
|   score   |   Doble  |  Inquilino de lograr la puntuación para el control (día a día varía, dependiendo de las operaciones del inquilino en el control). |
|   controlCategory |   String  |  Categoría de acción de control (identidad, datos, dispositivos, aplicaciones, infraestructura). |
|   descripción |   String  |  Descripción del control. |

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
