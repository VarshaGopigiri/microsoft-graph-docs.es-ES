---
title: tipo de recurso mobileAppTroubleshootingAppPolicyCreationHistory
description: Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.
ms.openlocfilehash: 7ca80443351e5c1b1232dc050cdf721ab7389351
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089465"
---
# <a name="mobileapptroubleshootingapppolicycreationhistory-resource-type"></a>tipo de recurso mobileAppTroubleshootingAppPolicyCreationHistory

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Elemento de historial de contenidos en el evento de solución de problemas de aplicación móvil.

Hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|occurrenceDateTime|DateTimeOffset|Tiempo que se produjo el elemento de historial. Se hereda de [mobileAppTroubleshootingHistoryItem](../resources/intune-troubleshooting-mobileapptroubleshootinghistoryitem.md)|
|runState|[runState](../resources/intune-shared-runstate.md)|Estado del elemento. Los valores posibles son: `unknown`, `success` y `fail`.|
|errorCode|String|Código de error para el error, vacío si no hay error.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppTroubleshootingAppPolicyCreationHistory"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppTroubleshootingAppPolicyCreationHistory",
  "occurrenceDateTime": "String (timestamp)",
  "runState": "String",
  "errorCode": "String"
}
```





