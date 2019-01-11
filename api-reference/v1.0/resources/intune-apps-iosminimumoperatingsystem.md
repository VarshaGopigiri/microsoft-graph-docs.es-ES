---
title: Tipo de recurso iosMinimumOperatingSystem
description: Contiene las propiedades del sistema operativo mínimo necesario para una aplicación móvil de iOS.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7243b337a53cca31054f99ae807e5c17cdd3e372
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876274"
---
# <a name="iosminimumoperatingsystem-resource-type"></a>Tipo de recurso iosMinimumOperatingSystem

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



