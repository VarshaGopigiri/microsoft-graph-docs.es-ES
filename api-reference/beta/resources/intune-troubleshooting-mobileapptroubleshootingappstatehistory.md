---
title: tipo de recurso mobileAppTroubleshootingAppStateHistory
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 03a7cd7a67790dca8824b7e446b5add5304c6f0a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917744"
---
# <a name="mobileapptroubleshootingappstatehistory-resource-type"></a>tipo de recurso mobileAppTroubleshootingAppStateHistory

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.

Hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|occurrenceDateTime|DateTimeOffset|Tiempo que se produjo el elemento de historial. Se hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)|
|actionType|[mobileAppActionType](../resources/intune-troubleshooting-mobileappactiontype.md)|Identificador de grupo de seguridad AAD a la que se ha destinado. Los valores posibles son: `unknown`, `installCommandSent`, `installed`, `uninstalled` y `userRequestedInstall`.|
|runState|[runState](../resources/intune-shared-runstate.md)|Estado del elemento. Los valores posibles son: `unknown`, `success` y `fail`.|
|errorCode|String|Código de error para el error, vacío si no hay error.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppTroubleshootingAppStateHistory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppTroubleshootingAppStateHistory",
  "occurrenceDateTime": "String (timestamp)",
  "actionType": "String",
  "runState": "String",
  "errorCode": "String"
}
```





