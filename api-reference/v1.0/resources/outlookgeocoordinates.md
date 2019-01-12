---
title: Tipo de recurso outlookGeoCoordinates
description: Coordenadas geográficas, elevación y su grado de precisión para una ubicación geográfica.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 59b5055118cd4a213d59fdcb4921544e3b84608e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976495"
---
# <a name="outlookgeocoordinates-resource-type"></a>Tipo de recurso outlookGeoCoordinates

Coordenadas geográficas, elevación y su grado de precisión para una ubicación geográfica.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.outlookGeoCoordinates"
}-->

```json
{
  "accuracy": 1024.13,
  "altitude": 1024.13,
  "altitudeAccuracy": 1024.13,
  "latitude": 1024.13,
  "longitude": 1024.13
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|accuracy|double|Exactitud de la latitud y longitud. Por ejemplo, la precisión puede medirse en metros, como que la latitud y longitud tienen una precisión de 50 metros.|
|altitude|double|Altitud de la ubicación.|
|altitudeAccuracy|double|Exactitud de la altitud.|
|latitude|double|Latitud de la ubicación.|
|longitude|double|Longitud de la ubicación.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookGeoCoordinates resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
