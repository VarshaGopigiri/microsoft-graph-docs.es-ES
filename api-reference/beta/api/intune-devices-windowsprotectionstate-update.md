---
title: Actualizar windowsProtectionState
description: Actualizar las propiedades de un objeto windowsProtectionState.
author: tfitzmac
ms.openlocfilehash: 8bdbe3d1841eb29f7616edcc5063cd025f282974
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308711"
---
# <a name="update-windowsprotectionstate"></a>Actualizar windowsProtectionState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualizar las propiedades de un objeto [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementManagedDevices.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsMalwareInformation/{windowsMalwareInformationId}/windowsDevicesProtectionState/{windowsProtectionStateId}
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/windowsProtectionState
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Aceptar|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|El identificador único para el objeto de estado de protección de dispositivo. Esto es el identificador de dispositivo del dispositivo|
|malwareProtectionEnabled|Boolean|Protección contra malware está habilitado o no|
|deviceState|[windowsDeviceHealthState](../resources/intune-devices-windowsdevicehealthstate.md)|Estado del equipo (como clean o pendiente de examen completo o pendientes reinicio etcetera). Los valores posibles son: `clean`, `fullScanPending`, `rebootPending`, `manualStepsPending`, `offlineScanPending`, `critical`.|
|realTimeProtectionEnabled|Boolean|¿Protección en tiempo real está habilitada o no?|
|networkInspectionSystemEnabled|Boolean|¿Sistema de control de red habilitado o no?|
|quickScanOverdue|Boolean|¿Rápido examinar vencidas o no?|
|fullScanOverdue|Boolean|¿Total de examen vencida o no?|
|signatureUpdateOverdue|Boolean|¿Firma caducada o no?|
|rebootRequired|Boolean|¿Es necesario reiniciar o no?|
|fullScanRequired|Boolean|¿Examen completo o no necesario?|
|engineVersion|String|Versión del motor de actual extremo protección|
|signatureVersion|String|Versión actual de las definiciones de malware|
|antiMalwareVersion|String|Actual de protección contra malware versión|
|lastQuickScanDateTime|DateTimeOffset|Fecha y hora último análisis rápido|
|lastFullScanDateTime|DateTimeOffset|Fecha y hora último análisis rápido|
|lastQuickScanSignatureVersion|String|Última versión de firma de análisis rápido|
|lastFullScanSignatureVersion|String|Última versión de firma de examen completo|
|lastReportedDateTime|DateTimeOffset|Último estado de mantenimiento de dispositivo el tiempo notificado|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/windowsMalwareInformation/{windowsMalwareInformationId}/windowsDevicesProtectionState/{windowsProtectionStateId}
Content-type: application/json
Content-length: 804

{
  "malwareProtectionEnabled": true,
  "deviceState": "fullScanPending",
  "realTimeProtectionEnabled": true,
  "networkInspectionSystemEnabled": true,
  "quickScanOverdue": true,
  "fullScanOverdue": true,
  "signatureUpdateOverdue": true,
  "rebootRequired": true,
  "fullScanRequired": true,
  "engineVersion": "Engine Version value",
  "signatureVersion": "Signature Version value",
  "antiMalwareVersion": "Anti Malware Version value",
  "lastQuickScanDateTime": "2016-12-31T23:58:27.5900669-08:00",
  "lastFullScanDateTime": "2017-01-01T00:01:44.9405639-08:00",
  "lastQuickScanSignatureVersion": "Last Quick Scan Signature Version value",
  "lastFullScanSignatureVersion": "Last Full Scan Signature Version value",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 914

{
  "@odata.type": "#microsoft.graph.windowsProtectionState",
  "id": "1ac6ea5a-ea5a-1ac6-5aea-c61a5aeac61a",
  "malwareProtectionEnabled": true,
  "deviceState": "fullScanPending",
  "realTimeProtectionEnabled": true,
  "networkInspectionSystemEnabled": true,
  "quickScanOverdue": true,
  "fullScanOverdue": true,
  "signatureUpdateOverdue": true,
  "rebootRequired": true,
  "fullScanRequired": true,
  "engineVersion": "Engine Version value",
  "signatureVersion": "Signature Version value",
  "antiMalwareVersion": "Anti Malware Version value",
  "lastQuickScanDateTime": "2016-12-31T23:58:27.5900669-08:00",
  "lastFullScanDateTime": "2017-01-01T00:01:44.9405639-08:00",
  "lastQuickScanSignatureVersion": "Last Quick Scan Signature Version value",
  "lastFullScanSignatureVersion": "Last Full Scan Signature Version value",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00"
}
```





