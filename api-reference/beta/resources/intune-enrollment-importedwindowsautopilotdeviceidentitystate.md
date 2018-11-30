---
title: Tipo de recurso importedWindowsAutopilotDeviceIdentityState resource type
description: Todavía no documentado
ms.openlocfilehash: cdb13df520d109ddcc49e2637652499186ac9f24
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087980"
---
# <a name="importedwindowsautopilotdeviceidentitystate-resource-type"></a>Tipo de recurso importedWindowsAutopilotDeviceIdentityState resource type

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|deviceImportStatus|[importedWindowsAutopilotDeviceIdentityImportStatus](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityimportstatus.md)|Estado del dispositivo detectado por el servicio de directorio de dispositivo (DDS). Los valores posibles son: `unknown`, `pending`, `partial`, `complete` y `error`.|
|deviceRegistrationId|Cadena|Identificador del registro del dispositivo para el dispositivo agregado correctamente notificado por el servicio de directorio de dispositivo (DDS).|
|deviceErrorCode|Int32|Código de error de dispositivo detectado por el servicio de directorio de dispositivo (DDS).|
|deviceErrorName|Cadena|Nombre de error de dispositivo detectado por el servicio de directorio de dispositivo (DDS).|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentityState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityState",
  "deviceImportStatus": "String",
  "deviceRegistrationId": "String",
  "deviceErrorCode": 1024,
  "deviceErrorName": "String"
}
```





