---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: GeoCoordinates
ms.openlocfilehash: f9110591ee1e3350979aa2c7785cdebb2d4a584c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086571"
---
# <a name="geocoordinates-resource-type"></a>Tipo de recurso GeoCoordinates

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **GeoCoordinates** proporciona las coordenadas geográficas y la elevación de una ubicación en función de metadatos contenidos en el archivo. Si un [**DriveItem**](driveitem.md) tiene una faceta **location** no null, el elemento representa un archivo que tiene asociada una ubicación conocida.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.geoCoordinates"
}-->

```json
{
  "altitude": 1024.13,
  "latitude": 26.13246,
  "longitude": 24.34616
}
```

## <a name="properties"></a>Propiedades

| Propiedad  | Tipo   | Descripción
|:----------|:-------|:--------------------------------------------------------
| altitude  | Doble | Opcional. Altitud (alto) en pies sobre el nivel del mar del elemento. Solo lectura.
| latitude  | Doble | Opcional. Latitud en formato decimal del elemento. Solo lectura.
| longitude | Doble | Opcional. Longitud en formato decimal del elemento. Solo lectura.

## <a name="remarks"></a>Observaciones

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The location facet provides geographic location related properties for an item",
  "keywords": "location,geographic,item,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Location"
} -->
