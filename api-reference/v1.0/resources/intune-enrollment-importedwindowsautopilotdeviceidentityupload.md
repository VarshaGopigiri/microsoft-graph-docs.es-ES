---
title: tipo de recurso importedWindowsAutopilotDeviceIdentityUpload
description: Importe los dispositivos de piloto automático de windows mediante carga.
ms.openlocfilehash: 6c22fed9fdd0a4caf103021e193b56f30aa6c094
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030264"
---
# <a name="importedwindowsautopilotdeviceidentityupload-resource-type"></a>tipo de recurso importedWindowsAutopilotDeviceIdentityUpload

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Importe los dispositivos de piloto automático de windows mediante carga.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista importedWindowsAutopilotDeviceIdentityUploads](../api/intune-enrollment-importedwindowsautopilotdeviceidentityupload-list.md)|colección de [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md)|Propiedades de la lista y relaciones de los objetos [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .|
|[Obtener importedWindowsAutopilotDeviceIdentityUpload](../api/intune-enrollment-importedwindowsautopilotdeviceidentityupload-get.md)|[importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md)|Leer las propiedades y las relaciones del objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .|
|[Crear importedWindowsAutopilotDeviceIdentityUpload](../api/intune-enrollment-importedwindowsautopilotdeviceidentityupload-create.md)|[importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md)|Crear un nuevo objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .|
|[Eliminar importedWindowsAutopilotDeviceIdentityUpload](../api/intune-enrollment-importedwindowsautopilotdeviceidentityupload-delete.md)|Ninguno|Elimina un [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md).|
|[Actualizar importedWindowsAutopilotDeviceIdentityUpload](../api/intune-enrollment-importedwindowsautopilotdeviceidentityupload-update.md)|[importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md)|Actualizar las propiedades de un objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityupload.md) .|
|[autopilotDeviceStream (función)](../api/intune-enrollment-importedwindowsautopilotdeviceidentityupload-autopilotdevicestream.md)|String|Crear una solicitud de carga con la secuencia de dispositivo de piloto automático en ella.|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|El GUID para el objeto|
|createdDateTimeUtc|DateTimeOffset|Fecha y hora cuando se crea la entidad.|
|status|[importedWindowsAutopilotDeviceIdentityUploadStatus](../resources/intune-enrollment-importedwindowsautopilotdeviceidentityuploadstatus.md)|Estado de la carga. Los valores posibles son: `noUpload`, `pending`, `complete` y `error`.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|deviceIdentities|Colección [importedWindowsAutopilotDeviceIdentity](../resources/intune-enrollment-importedwindowsautopilotdeviceidentity.md)|Colección de todos los dispositivos de piloto automático como parte de esta carga.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentityUpload"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityUpload",
  "id": "String (identifier)",
  "createdDateTimeUtc": "String (timestamp)",
  "status": "String"
}
```



