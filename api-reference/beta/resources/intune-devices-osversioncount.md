---
title: tipo de recurso osVersionCount
description: Recuento de dispositivos con malware para cada versión del sistema operativo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: de841e679ede22492d26f2a1587e775179c45761
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911843"
---
# <a name="osversioncount-resource-type"></a>tipo de recurso osVersionCount

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Recuento de dispositivos con malware para cada versión del sistema operativo
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|osVersion|Cadena|Versión del sistema operativo|
|deviceCount|Int32|Recuento de dispositivos con malware para la versión del sistema operativo|
|lastUpdateDateTime|DateTimeOffset|Recuento de la marca de hora de la última actualización del dispositivo en UTC|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.osVersionCount"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.osVersionCount",
  "osVersion": "String",
  "deviceCount": 1024,
  "lastUpdateDateTime": "String (timestamp)"
}
```





