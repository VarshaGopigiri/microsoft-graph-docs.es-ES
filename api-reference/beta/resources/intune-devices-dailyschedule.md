---
title: tipo de recurso dailySchedule
description: Programación diaria de ejecución de una secuencia de comandos de administración de dispositivo periódica.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d0f4f258afe1de65bd8fecf32d9df387716a2c6d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987716"
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





