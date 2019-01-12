---
title: tipo de recurso iosVppAppRevokeLicensesActionResult
description: Define los resultados de acciones en iOS aplicaciones Vpp, contiene propiedades heredadas para ActionResult.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 13bc69a0c04eb7b9742f6c549fd1ae976cf25561
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986995"
---
# <a name="iosvppapprevokelicensesactionresult-resource-type"></a>tipo de recurso iosVppAppRevokeLicensesActionResult

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Define los resultados de acciones en iOS aplicaciones Vpp, contiene propiedades heredadas para ActionResult.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|userId|Cadena|Identificador de usuario asociado con la acción.|
|managedDeviceId|Cadena|DeviceId asociado con la acción.|
|totalLicensesCount|Int32|Un recuento del número de licencias para el que se ha intentado establecer revoke.|
|failedLicensesCount|Int32|Un recuento del número de licencias para qué revoke no se pudo.|
|actionFailureReason|[vppTokenActionFailureReason](../resources/intune-shared-vpptokenactionfailurereason.md)|El motivo del error de acción de licencias revoke. Los valores posibles son: `none`, `appleFailure`, `internalError`, `expiredVppToken` y `expiredApplePushNotificationCertificate`.|
|actionName|cadena|Nombre de acción|
|actionState|[actionState](../resources/intune-shared-actionstate.md)|Estado de la acción. Los valores posibles son: `none`, `pending`, `canceled`, `active`, `done`, `failed` y `notSupported`.|
|startDateTime|DateTimeOffset|Hora a la que se inició la acción|
|lastUpdatedDateTime|DateTimeOffset|Hora en la que se actualizó por última vez el estado de la acción|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iosVppAppRevokeLicensesActionResult"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVppAppRevokeLicensesActionResult",
  "userId": "String",
  "managedDeviceId": "String",
  "totalLicensesCount": 1024,
  "failedLicensesCount": 1024,
  "actionFailureReason": "String",
  "actionName": "String",
  "actionState": "String",
  "startDateTime": "String (timestamp)",
  "lastUpdatedDateTime": "String (timestamp)"
}
```





