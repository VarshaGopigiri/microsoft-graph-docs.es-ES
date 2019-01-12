---
title: Tipo de recurso deviceConfigurationUserOverview
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9c20471630b2ab888af96a33b1e24eced26d3015
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27926305"
---
# <a name="deviceconfigurationuseroverview-resource-type"></a>Tipo de recurso deviceConfigurationUserOverview

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceConfigurationUserOverview](../api/intune-deviceconfig-deviceconfigurationuseroverview-get.md)|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|Lea las propiedades y las relaciones del objeto [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md).|
|[Actualizar deviceConfigurationUserOverview](../api/intune-deviceconfig-deviceconfigurationuseroverview-update.md)|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|Actualice las propiedades de un objeto [deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|pendingCount|Int32|Número de usuarios pendientes|
|notApplicableCount|Int32|Número de usuarios no es aplicable.|
|successCount|Int32|Número de usuarios correctos|
|errorCount|Int32|Número de usuarios con error|
|failedCount|Int32|Número de usuarios erróneos|
|lastUpdateDateTime|DateTimeOffset|Última hora de actualización|
|configurationVersion|Int32|Versión de la directiva para esa información general|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationUserOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationUserOverview",
  "id": "String (identifier)",
  "pendingCount": 1024,
  "notApplicableCount": 1024,
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```



