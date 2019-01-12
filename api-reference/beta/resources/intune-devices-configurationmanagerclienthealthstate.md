---
title: tipo de recurso configurationManagerClientHealthState
description: Estado de mantenimiento de cliente de administrador de configuración
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 4d202b5f672977e8bb1a5fe05ba56937005825ff
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981745"
---
# <a name="configurationmanagerclienthealthstate-resource-type"></a>tipo de recurso configurationManagerClientHealthState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Estado de mantenimiento de cliente de administrador de configuración
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|state|[configurationManagerClientState](../resources/intune-devices-configurationmanagerclientstate.md)|Estado de cliente de administrador de configuración actual. Los valores posibles son: `unknown`, `installed`, `healthy`, `installFailed`, `updateFailed` y `communicationError`.|
|errorCode|Int32|Código de error de estado de error.|
|lastSyncDateTime|DateTimeOffset|Elija la última sincronización de fo de fecha y hora con la administración del Administrador de configuración.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.configurationManagerClientHealthState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.configurationManagerClientHealthState",
  "state": "String",
  "errorCode": 1024,
  "lastSyncDateTime": "String (timestamp)"
}
```





