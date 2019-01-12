---
title: tipo de recurso audioSourceLevel
description: Configuración de nivel para otros orígenes.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 79ad56c11e8b277a1354ffc3a6292a0434466c8a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27947655"
---
# <a name="audiosourcelevel-resource-type"></a>tipo de recurso audioSourceLevel

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Configuración de nivel para otros orígenes.

## <a name="properties"></a>Propiedades

| Propiedad               | Tipo    | Descripción                                                                                         |
| :--------------------- | :------ | :---------------------------------------------------------------------------------------------------|
| duckOthers             | Booleano | Permite que este origen agacha otros orígenes mientras está activa. Si se establece en true, nivel de sobra se ha establecido.|
| nivel                  | Int64   | Nivel de la fuente de sobra si `duckOthers` está establecida en `true`.                                     |
| participante            | Cadena  | La secuencia de audio participantes de origen.                                                                |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.audioSourceLevel"
}-->
```json
{
  "duckOthers": true,
  "level": 100,
  "participant": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "audioSourceLevel resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
