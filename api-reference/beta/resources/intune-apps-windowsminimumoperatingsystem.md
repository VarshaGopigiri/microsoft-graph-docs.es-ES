---
title: Tipo de recurso windowsMinimumOperatingSystem
description: El sistema operativo mínimo necesario para una aplicación móvil de Windows.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 672bceca692702b4d108b8538626c2b767ffdf56
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27814521"
---
# <a name="windowsminimumoperatingsystem-resource-type"></a>Tipo de recurso windowsMinimumOperatingSystem

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

El sistema operativo mínimo necesario para una aplicación móvil de Windows.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|v8_0|Booleano|Windows versión 8.0 o posterior.|
|v8_1|Booleano|Windows versión 8.1 o posterior.|
|v10_0|Booleano|Windows versión 10.0 o posterior.|
|v10_1607|Booleano|Windows 1607 10 o posterior.|
|v10_1703|Booleano|Windows 1703 10 o posterior.|
|v10_1709|Booleano|Windows 1709 10 o posterior.|
|v10_1803|Booleano|Windows 1803 10 o posterior.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsMinimumOperatingSystem"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsMinimumOperatingSystem",
  "v8_0": true,
  "v8_1": true,
  "v10_0": true,
  "v10_1607": true,
  "v10_1703": true,
  "v10_1709": true,
  "v10_1803": true
}
```





