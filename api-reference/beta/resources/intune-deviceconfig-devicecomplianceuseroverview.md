---
title: Tipo de recurso deviceComplianceUserOverview
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 6505cf0d563f129d4a683026f5dc828310c32792
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359391"
---
# <a name="devicecomplianceuseroverview-resource-type"></a>Tipo de recurso deviceComplianceUserOverview

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener deviceComplianceUserOverview](../api/intune-deviceconfig-devicecomplianceuseroverview-get.md)|[deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md)|Lea las propiedades y las relaciones del objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).|
|[Actualizar deviceComplianceUserOverview](../api/intune-deviceconfig-devicecomplianceuseroverview-update.md)|[deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md)|Actualice las propiedades de un objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|pendingCount|Int32|Número de usuarios pendientes|
|notApplicableCount|Int32|Número de usuarios no es aplicable.|
|successCount|Int32|Número de usuarios correctos|
|errorCount|Int32|Número de usuarios con error|
|failedCount|Int32|Número de usuarios erróneos|
|conflictCount|Int32|Número de usuarios en conflicto|
|lastUpdateDateTime|DateTimeOffset|Última hora de actualización|
|configurationVersion|Int32|Versión de la directiva para esa información general|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceComplianceUserOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceComplianceUserOverview",
  "id": "String (identifier)",
  "pendingCount": 1024,
  "notApplicableCount": 1024,
  "successCount": 1024,
  "errorCount": 1024,
  "failedCount": 1024,
  "conflictCount": 1024,
  "lastUpdateDateTime": "String (timestamp)",
  "configurationVersion": 1024
}
```





