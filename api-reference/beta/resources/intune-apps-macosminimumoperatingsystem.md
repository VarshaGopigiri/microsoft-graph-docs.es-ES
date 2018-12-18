---
title: tipo de recurso macOSMinimumOperatingSystem
description: El sistema operativo mínimo necesario para una aplicación de Mac OS.
author: tfitzmac
ms.openlocfilehash: ff9d4e3fc375f17d7b3c3efdd4af16cd7e87ceb6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354778"
---
# <a name="macosminimumoperatingsystem-resource-type"></a>tipo de recurso macOSMinimumOperatingSystem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El sistema operativo mínimo necesario para una aplicación de Mac OS.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|v10_7|Boolean|Mac OS 10.7 o posterior.|
|v10_8|Boolean|Mac OS 10,8 o posterior.|
|v10_9|Boolean|Mac OS 10.9 o posterior.|
|v10_10|Boolean|Mac OS 10.10 o posterior.|
|v10_11|Boolean|Mac OS 10.11 o posterior.|
|v10_12|Boolean|Mac OS 10.12 o posterior.|
|v10_13|Boolean|Mac OS 10.13 o posterior.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.macOSMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.macOSMinimumOperatingSystem",
  "v10_7": true,
  "v10_8": true,
  "v10_9": true,
  "v10_10": true,
  "v10_11": true,
  "v10_12": true,
  "v10_13": true
}
```





