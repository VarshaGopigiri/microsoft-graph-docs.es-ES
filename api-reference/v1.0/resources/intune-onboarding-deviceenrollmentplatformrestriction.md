---
title: Tipo de recurso deviceEnrollmentPlatformRestriction
description: Restricciones de inscripción específicas de la plataforma
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: ce30b9ff24067fb2bfec17ad85d3c8827cc6b798
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816005"
---
# <a name="deviceenrollmentplatformrestriction-resource-type"></a>Tipo de recurso deviceEnrollmentPlatformRestriction

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Restricciones de inscripción específicas de la plataforma
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|platformBlocked|Booleano|Impedir que la plataforma se inscriba|
|personalDeviceEnrollmentBlocked|Booleano|Impedir que los dispositivos de propiedad personal se inscriban|
|osMinimumVersion|cadena|Versión de sistema operativo mínima compatible|
|osMaximumVersion|cadena|Versión de sistema operativo máxima compatible|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestriction",
  "platformBlocked": true,
  "personalDeviceEnrollmentBlocked": true,
  "osMinimumVersion": "String",
  "osMaximumVersion": "String"
}
```



