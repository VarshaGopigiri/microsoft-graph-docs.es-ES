---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: GeoCoordinates
ms.openlocfilehash: 61fc7c117d2da961b1b6d581e21db27d7afe3f31
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="geocoordinates-resource-type"></a>Tipo de recurso GeoCoordinates

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

## <a name="remarks"></a>Comentarios

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).

<!-- {
  "type": "#page.annotation",
  "description": "The location facet provides geographic location related properties for an item",
  "keywords": "location,geographic,item,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Location"
} -->
