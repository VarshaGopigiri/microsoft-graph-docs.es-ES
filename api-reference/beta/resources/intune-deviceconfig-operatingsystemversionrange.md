---
title: tipo de recurso operatingSystemVersionRange
description: Intervalo de versión del sistema operativo.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: c0b81482ad4b48ad5fe59b1ec0109fcd3bf03f83
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918549"
---
# <a name="operatingsystemversionrange-resource-type"></a>tipo de recurso operatingSystemVersionRange

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Intervalo de versión del sistema operativo.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|description|Cadena|La descripción de este intervalo (por ejemplo, válido 1702 compilaciones)|
|lowestVersion|Cadena|La más baja inclusive versión que contiene este intervalo.|
|highestVersion|Cadena|La versión inclusive más alta que contiene este intervalo.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.operatingSystemVersionRange"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.operatingSystemVersionRange",
  "description": "String",
  "lowestVersion": "String",
  "highestVersion": "String"
}
```





