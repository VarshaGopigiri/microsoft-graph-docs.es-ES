---
title: Crear deviceComplianceSettingState
description: Cree un objeto deviceComplianceSettingState.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: e7c79676eac77cebe645c0c26785421dd0dc278b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959091"
---
# <a name="create-devicecompliancesettingstate"></a>Crear deviceComplianceSettingState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Cree un objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementConfiguration.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceSettingState.

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceSettingState.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad|
|platformType|[deviceType](../resources/intune-shared-devicetype.md)|Tipo de plataforma del dispositivo. Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.|
|ajustes|String|El nombre de la clase de configuración y el nombre de propiedad.|
|settingName|String|El nombre de configuración que se está notificando|
|deviceId|Cadena|El identificador del dispositivo que se está notificando|
|deviceName|String|El nombre del dispositivo que se está notificando|
|userId|Cadena|El identificador del usuario que se está notificando|
|userEmail|String|La dirección de correo electrónico del usuario que se está notificando|
|userName|String|El nombre de usuario que se está notificando|
|userPrincipalName|String|El nombre principal de usuario que se está notificando|
|deviceModel|Cadena|El modelo de dispositivo que se está notificando|
|estado|[complianceStatus](../resources/intune-shared-compliancestatus.md)|El estado de cumplimiento de la configuración. Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.|
|complianceGracePeriodExpirationDateTime|DateTimeOffset|La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceSettingState](../resources/intune-deviceconfig-devicecompliancesettingstate.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}/deviceComplianceSettingStates
Content-type: application/json
Content-length: 549

{
  "@odata.type": "#microsoft.graph.deviceComplianceSettingState",
  "platformType": "windowsRT",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "deviceId": "Device Id value",
  "deviceName": "Device Name value",
  "userId": "User Id value",
  "userEmail": "User Email value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "deviceModel": "Device Model value",
  "state": "notApplicable",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 598

{
  "@odata.type": "#microsoft.graph.deviceComplianceSettingState",
  "id": "9905f955-f955-9905-55f9-059955f90599",
  "platformType": "windowsRT",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "deviceId": "Device Id value",
  "deviceName": "Device Name value",
  "userId": "User Id value",
  "userEmail": "User Email value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "deviceModel": "Device Model value",
  "state": "notApplicable",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00"
}
```





