---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Foto
ms.openlocfilehash: 391eafd84ab1abd4670c953720ff7097e060bfd3
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23267069"
---
# <a name="photo-resource-type"></a>Tipo de recurso Photo

El recurso **photo** proporciona propiedades de foto y cámara, por ejemplo, los metadatos EXIF, en un [driveItem](driveitem.md).

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.photo"
}-->

```json
{
  "cameraMake": "string",
  "cameraModel": "string",
  "exposureDenominator": 1000.0,
  "exposureNumerator": 1.0,
  "fNumber": 1.8,
  "focalLength": 22.5,
  "iso": 100,
  "takenDateTime": "String (timestamp)"
}
```

## <a name="properties"></a>Propiedades

| Propiedad                | Tipo           | Descripción
|:------------------------|:---------------|:----------------------------------
| **takenDateTime**       | DateTimeOffset | Representa la fecha y hora en que se tomó la foto. Solo lectura.
| **cameraMake**          | String         | Fabricante de la cámara. Solo lectura.
| **cameraModel**         | String         | Modelo de la cámara. Solo lectura.
| **fNumber**             | Doble         | Valor punto F de la cámara. Solo lectura.
| **exposureDenominator** | Double         | Denominador de la fracción de tiempo de exposición de la cámara. Solo lectura.
| **exposureNumerator**   | Double         | Numerador de la fracción de tiempo de exposición de la cámara. Solo lectura.
| **focalLength**         | Doble         | Distancia focal de la cámara. Solo lectura.
| **iso**                 | Int32          | Valor ISO de la cámara. Solo lectura.

## <a name="remarks"></a>Comentarios

OneDrive para la Empresa y SharePoint solo devuelven la propiedad **takenDateTime**.

Para obtener más información sobre las facetas de un DriveItem, consulte [DriveItem](driveitem.md).
<!-- {
  "type": "#page.annotation",
  "description": "The photo facet provides details about the camera and settings on the camera for photos.",
  "keywords": "camera make,camera model, exposure, f-stop, iso",
  "section": "documentation",
  "tocPath": "Facets/Photo"
} -->
