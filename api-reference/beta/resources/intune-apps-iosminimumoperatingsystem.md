---
title: Tipo de recurso iosMinimumOperatingSystem
description: Contiene las propiedades del sistema operativo mínimo necesario para una aplicación móvil de iOS.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: acee063da4c37627027bce2133201943a9194376
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27918941"
---
# <a name="iosminimumoperatingsystem-resource-type"></a>Tipo de recurso iosMinimumOperatingSystem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades del sistema operativo mínimo necesario para una aplicación móvil de iOS.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|v8_0|Booleano|Versión 8.0 o posterior.|
|v9_0|Booleano|Versión 9.0 o posterior.|
|v10_0|Booleano|Versión 10.0 o posterior.|
|v11_0|Booleano|Versión 11.0 o posterior.|
|v12_0|Booleano|Versión 12.0 o posterior.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosMinimumOperatingSystem",
  "v8_0": true,
  "v9_0": true,
  "v10_0": true,
  "v11_0": true,
  "v12_0": true
}
```





