---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Image
ms.openlocfilehash: c9e647ef630e8822d835aec1bd72b9f3c18f2e3e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088199"
---
# <a name="image-resource-type"></a>Tipo de recurso Image

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **Image** agrupa en una sola estructura las propiedades relacionadas con la imagen. Si un [**DriveItem**](driveitem.md) tiene una faceta de **image** no null, el elemento representa una imagen de mapa de bits.

**Nota:** Si el servicio no puede determinar el ancho y el alto de la imagen, puede que el recurso **image** esté vacío.

## <a name="json-representation"></a>Representación JSON

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.image" } -->
```json
{
  "width": 100,
  "height": 200
}
```

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo  | Descripción                                |
|:-----------|:------|:-------------------------------------------|
| **height** | Int32 | Opcional. Ancho o alto de la imagen en píxeles. Solo lectura. |
| **width**  | Int32 | Opcional. Ancho de la imagen en píxeles. Solo lectura.  |

## <a name="remarks"></a>Comentarios

En OneDrive para la Empresa, este recurso se devuelve en los elementos que se esperan que sean imágenes en función de la extensión de archivo.

Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).


<!-- {
  "type": "#page.annotation",
  "description": "The image facet describes properties of an image like width and height",
  "keywords": "image,width,height,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Image"
} -->
