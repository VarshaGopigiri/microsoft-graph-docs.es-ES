---
title: Tipo de recurso mediaContentRatingJapan
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2b1ab45a91fb617412742481639a0203624bc11d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27945926"
---
# <a name="mediacontentratingjapan-resource-type"></a>Tipo de recurso mediaContentRatingJapan

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|movieRating|[ratingJapanMoviesType](../resources/intune-deviceconfig-ratingjapanmoviestype.md)|Películas de clasificación seleccionado para Japón. Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove15`, `agesAbove18`.|
|tvRating|[ratingJapanTelevisionType](../resources/intune-deviceconfig-ratingjapantelevisiontype.md)|Clasificación de TV seleccionada para Japón. Los valores posibles son: `allAllowed`, `allBlocked` y `explicitAllowed`.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingJapan"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingJapan",
  "movieRating": "String",
  "tvRating": "String"
}
```



