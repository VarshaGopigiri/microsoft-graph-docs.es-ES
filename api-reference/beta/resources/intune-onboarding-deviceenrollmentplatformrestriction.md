---
title: Tipo de recurso deviceEnrollmentPlatformRestriction
description: Restricciones de inscripción específicas de la plataforma
ms.openlocfilehash: 823eecc37dc8ee4536d5cb63213f2bb80ca5138d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089275"
---
# <a name="deviceenrollmentplatformrestriction-resource-type"></a>Tipo de recurso deviceEnrollmentPlatformRestriction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

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





