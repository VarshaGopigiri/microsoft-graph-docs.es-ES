---
title: tipo de recurso audioDuckingConfiguration
description: Parámetros de sobra de otros orígenes (introducir paulatinamente dentro y fuera de otros orígenes).
author: VinodRavichandran
ms.openlocfilehash: e595e2a46f3e8bcbee2bb7ad0e3421216244db71
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380185"
---
# <a name="audioduckingconfiguration-resource-type"></a>tipo de recurso audioDuckingConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Parámetros de sobra de otros orígenes (introducir paulatinamente dentro y fuera de otros orígenes).

## <a name="properties"></a>Propiedades

| Propiedad      | Tipo     | Descripción                                                                     |
| :------------ | :------- | :-------------------------------------------------------------------------------|
| lowerLevel    | Int64    | El volumen de orígenes en por ciento cuando se va a ducked los orígenes.             |
| rampActive    | Int64    | La cantidad de tiempo (en milisegundos) que tarda orígenes ducked "desaparecer". |
| rampInactive  | Int64    | La cantidad de tiempo (en milisegundos) que tarda orígenes ducked a "desaparecer".  |
| upperLevel    | Int64    | El volumen de orígenes en por ciento cuando no se están ducked los orígenes.         |

> **Nota:** Duración de mejorar no puede ser más de 5.000 milisegundos.

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.audioDuckingConfiguration"
}-->
```json
{
  "lowerLevel": 20,
  "rampActive": 1000,
  "rampInactive": 1000,
  "upperLevel": 100
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "audioDuckingConfiguration resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
