---
title: Crear importedAppleDeviceIdentityResult
description: Crear un nuevo objeto importedAppleDeviceIdentityResult.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 52b1e2364b2bfb2168b97da3e212bffdad67845c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27983663"
---
# <a name="create-importedappledeviceidentityresult"></a>Crear importedAppleDeviceIdentityResult

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Crear un nuevo objeto [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) .
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementServiceConfig.ReadWrite.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Authorization|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto importedAppleDeviceIdentityResult.

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el importedAppleDeviceIdentityResult.

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|serialNumber|String|Número de serie del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|requestedEnrollmentProfileId|String|Administración de identificador de perfil de inscripción tenga la intención de aplicar al dispositivo durante la inscripción siguiente Inherited de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|requestedEnrollmentProfileAssignmentDateTime|DateTimeOffset|El perfil de tiempo de inscripción se asignó al dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|isSupervised|Booleano|Indica si el dispositivo de Apple es supervisado. Obtener más información se encuentra en: https://support.apple.com/en-us/HT202837 se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|discoverySource|[discoverySource](../resources/intune-enrollment-discoverysource.md)|Origen de detección del dispositivo de Apple. Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md). Los valores posibles son: `unknown`, `adminImport` y `deviceEnrollmentProgram`.|
|createdDateTime|DateTimeOffset|Crear fecha hora del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|lastContactedDateTime|DateTimeOffset|Última vez fecha ponerse en contacto del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|descripción|String|La descripción del dispositivo Inherited desde [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md)|
|enrollmentState|[enrollmentState](../resources/intune-enrollment-enrollmentstate.md)|El estado del dispositivo en Intune se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md). Los valores posibles son: `unknown`, `enrolled`, `pendingReset`, `failed`, `notContacted`, `blocked`.|
|platform|[plataforma](../resources/intune-enrollment-platform.md)|La plataforma del dispositivo. Se hereda de [importedAppleDeviceIdentity](../resources/intune-enrollment-importedappledeviceidentity.md). Los valores posibles son: `unknown`, `ios`, `android`, `windows`, `windowsMobile`, `macOS`.|
|status|Booleano|Estado de identidad de dispositivo importada|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [importedAppleDeviceIdentityResult](../resources/intune-enrollment-importedappledeviceidentityresult.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
POST https://graph.microsoft.com/beta/deviceManagement/depOnboardingSettings/{depOnboardingSettingId}/importedAppleDeviceIdentities
Content-type: application/json
Content-length: 522

{
  "@odata.type": "#microsoft.graph.importedAppleDeviceIdentityResult",
  "serialNumber": "Serial Number value",
  "requestedEnrollmentProfileId": "Requested Enrollment Profile Id value",
  "requestedEnrollmentProfileAssignmentDateTime": "2017-01-01T00:02:32.8167841-08:00",
  "isSupervised": true,
  "discoverySource": "adminImport",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios",
  "status": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 630

{
  "@odata.type": "#microsoft.graph.importedAppleDeviceIdentityResult",
  "id": "557cfb4a-fb4a-557c-4afb-7c554afb7c55",
  "serialNumber": "Serial Number value",
  "requestedEnrollmentProfileId": "Requested Enrollment Profile Id value",
  "requestedEnrollmentProfileAssignmentDateTime": "2017-01-01T00:02:32.8167841-08:00",
  "isSupervised": true,
  "discoverySource": "adminImport",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "lastContactedDateTime": "2016-12-31T23:58:44.2908994-08:00",
  "description": "Description value",
  "enrollmentState": "enrolled",
  "platform": "ios",
  "status": true
}
```





