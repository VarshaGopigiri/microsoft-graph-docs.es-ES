---
title: tipo de recurso managedDeviceCleanupSettings
description: Definir la regla cuando el administrador desea que los dispositivos limpiar.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 334b561ffa19d4161553f761ce65b7da7d9dbcfa
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961900"
---
# <a name="manageddevicecleanupsettings-resource-type"></a>tipo de recurso managedDeviceCleanupSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Definir la regla cuando el administrador desea que los dispositivos limpiar.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|deviceInactivityBeforeRetirementInDays|Cadena|Número de días cuando el dispositivo no ha contactado Intune.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.managedDeviceCleanupSettings"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceCleanupSettings",
  "deviceInactivityBeforeRetirementInDays": "String"
}
```





