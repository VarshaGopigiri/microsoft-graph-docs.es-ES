---
title: Actualizar macOSCompliancePolicy
description: Actualice las propiedades de un objeto macOSCompliancePolicy.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 09bba9c19d912d1d4065f390ed35cc209f1879a0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27886768"
---
# <a name="update-macoscompliancepolicy"></a>Actualizar macOSCompliancePolicy

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualice las propiedades de un objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md).
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
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md).

En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).|
|passwordRequired|Booleano|Si quiere requerir o no una contraseña.|
|passwordBlockSimple|Booleano|Indica si se van a bloquear las contraseñas simples.|
|passwordExpirationDays|Int32|Número de días antes de que expire la contraseña. Valores válidos de 1 a 65535|
|passwordMinimumLength|Int32|Longitud mínima de la contraseña. Valores válidos de 4 a 14|
|passwordMinutesOfInactivityBeforeLock|Int32|Minutos de inactividad antes de que sea necesaria una contraseña.|
|passwordPreviousPasswordBlockCount|Int32|Número de contraseñas anteriores que bloquear. Valores válidos de 1 a 24.|
|passwordMinimumCharacterSetCount|Int32|Número de juegos de caracteres necesarios en la contraseña.|
|passwordRequiredType|[requiredPasswordType](../resources/intune-deviceconfig-requiredpasswordtype.md)|Tipo de contraseña necesaria. Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.|
|osMinimumVersion|Cadena|Versión mínima de iOS.|
|osMaximumVersion|Cadena|Versión máxima de iOS.|
|systemIntegrityProtectionEnabled|Booleano|Requiere que los dispositivos hayan habilitado la protección de integridad del sistema.|
|deviceThreatProtectionEnabled|Booleano|Requiere que los dispositivos hayan habilitado la protección contra amenazas de dispositivo.|
|deviceThreatProtectionRequiredSecurityLevel|[deviceThreatProtectionLevel](../resources/intune-deviceconfig-devicethreatprotectionlevel.md)|Exigir que el nivel de riesgo mínimo de Mobile Threat Protection informe del no cumplimiento. Los valores posibles son: `unavailable`, `secured`, `low`, `medium`, `high` y `notSet`.|
|storageRequireEncryption|Booleano|Exige el cifrado en dispositivos Mac OS.|
|firewallEnabled|Booleano|Si el firewall se debe habilitar o no.|
|firewallBlockAllIncoming|Booleano|Corresponde a la opción "Bloquear todas las conexiones entrantes".|
|firewallEnableStealthMode|Booleano|Corresponde a "Habilitar modo silencioso".|



## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSCompliancePolicy](../resources/intune-deviceconfig-macoscompliancepolicy.md) actualizado en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}
Content-type: application/json
Content-length: 849

{
  "@odata.type": "#microsoft.graph.macOSCompliancePolicy",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "systemIntegrityProtectionEnabled": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "storageRequireEncryption": true,
  "firewallEnabled": true,
  "firewallBlockAllIncoming": true,
  "firewallEnableStealthMode": true
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1021

{
  "@odata.type": "#microsoft.graph.macOSCompliancePolicy",
  "id": "ddbadff3-dff3-ddba-f3df-baddf3dfbadd",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "passwordRequired": true,
  "passwordBlockSimple": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeLock": 5,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordMinimumCharacterSetCount": 0,
  "passwordRequiredType": "alphanumeric",
  "osMinimumVersion": "Os Minimum Version value",
  "osMaximumVersion": "Os Maximum Version value",
  "systemIntegrityProtectionEnabled": true,
  "deviceThreatProtectionEnabled": true,
  "deviceThreatProtectionRequiredSecurityLevel": "secured",
  "storageRequireEncryption": true,
  "firewallEnabled": true,
  "firewallBlockAllIncoming": true,
  "firewallEnableStealthMode": true
}
```



