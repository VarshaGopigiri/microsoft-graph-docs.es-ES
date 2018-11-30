---
title: tipo de recurso dailySchedule
description: Programación diaria de ejecución de una secuencia de comandos de administración de dispositivo periódica.
ms.openlocfilehash: 5d517b0bcd15f041b934a0ca936075bc6d3d3741
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088813"
---
# <a name="dailyschedule-resource-type"></a>tipo de recurso dailySchedule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Programación diaria de ejecución de una secuencia de comandos de administración de dispositivo periódica.

Hereda de [runSchedule](../resources/intune-devices-runschedule.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|interval|Int32|Intervalo en número de días|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.dailySchedule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.dailySchedule",
  "interval": 1024
}
```





