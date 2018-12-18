---
title: Tipo de recurso mediaContentRatingIreland
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 68d5e0e9454fadde550988f46c1104733a9de013
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359475"
---
# <a name="mediacontentratingireland-resource-type"></a>Tipo de recurso mediaContentRatingIreland

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|movieRating|[ratingIrelandMoviesType](../resources/intune-deviceconfig-ratingirelandmoviestype.md)|Películas de clasificación seleccionado para Irlanda. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove12`, `agesAbove15`, `agesAbove16` y `adults`.|
|tvRating|[ratingIrelandTelevisionType](../resources/intune-deviceconfig-ratingirelandtelevisiontype.md)|Clasificación de TV seleccionada para Irlanda. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `children`, `youngAdults`, `parentalSupervision` y `mature`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingIreland"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingIreland",
  "movieRating": "String",
  "tvRating": "String"
}
```



