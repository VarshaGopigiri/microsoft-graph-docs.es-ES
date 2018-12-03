---
title: tipo de recurso managedDeviceCertificateState
description: Todavía no documentado
ms.openlocfilehash: 17128f812eca82f01d6d2fa632f11c6640d18fc6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089822"
---
# <a name="manageddevicecertificatestate-resource-type"></a>tipo de recurso managedDeviceCertificateState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista managedDeviceCertificateStates](../api/intune-deviceconfig-manageddevicecertificatestate-list.md)|colección de [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md)|Propiedades de la lista y relaciones de los objetos [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) .|
|[Obtener managedDeviceCertificateState](../api/intune-deviceconfig-manageddevicecertificatestate-get.md)|[managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md)|Leer las propiedades y las relaciones del objeto [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) .|
|[Crear managedDeviceCertificateState](../api/intune-deviceconfig-manageddevicecertificatestate-create.md)|[managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md)|Crear un nuevo objeto [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) .|
|[Eliminar managedDeviceCertificateState](../api/intune-deviceconfig-manageddevicecertificatestate-delete.md)|Ninguno|Elimina un [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md).|
|[Actualizar managedDeviceCertificateState](../api/intune-deviceconfig-manageddevicecertificatestate-update.md)|[managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md)|Actualizar las propiedades de un objeto [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|devicePlatform|[devicePlatformType](../resources/intune-shared-deviceplatformtype.md)|Plataforma de dispositivo. Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `androidWorkProfile`.|
|certificateKeyUsage|[keyUsages](../resources/intune-deviceconfig-keyusages.md)|Uso de la clave. Los valores posibles son: `keyEncipherment` y `digitalSignature`.|
|certificateValidityPeriodUnits|[certificateValidityPeriodScale](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|Unidades del período de validez. Los valores posibles son: `days`, `months` y `years`.|
|certificateIssuanceState|[certificateIssuanceStates](../resources/intune-deviceconfig-certificateissuancestates.md)|Estado de emisión. Los valores posibles son: `unknown`, `challengeIssued`, `challengeIssueFailed`, `requestCreationFailed`, `requestSubmitFailed`, `challengeValidationSucceeded`, `challengeValidationFailed`, `issueFailed`, `issuePending`, `issued`, `responseProcessingFailed`, `responsePending`, `enrollmentSucceeded`, `enrollmentNotNeeded`, `revoked`, `removedFromCollection`, `renewVerified`, `installFailed`, `installed` , `deleteFailed`, `deleted`, `renewalRequested`, `requested`.|
|certificateKeyStorageProvider|[keyStorageProviderOption](../resources/intune-deviceconfig-keystorageprovideroption.md)|Proveedor de almacenamiento de claves. Los valores posibles son: `useTpmKspOtherwiseUseSoftwareKsp`, `useTpmKspOtherwiseFail`, `usePassportForWorkKspOtherwiseFail` y `useSoftwareKsp`.|
|certificateSubjectNameFormat|[subjectNameFormat](../resources/intune-deviceconfig-subjectnameformat.md)|Formato de nombre de sujeto. Los valores posibles son: `commonName`, `commonNameIncludingEmail`, `commonNameAsEmail`, `custom`, `commonNameAsIMEI`, `commonNameAsSerialNumber`, `commonNameAsAadDeviceId`, `commonNameAsIntuneDeviceId` y `commonNameAsDurableDeviceId`.|
|certificateSubjectAlternativeNameFormat|[subjectAlternativeNameType](../resources/intune-deviceconfig-subjectalternativenametype.md)|Formato de nombre alternativo de sujeto. Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.|
|certificateRevokeStatus|[certificateRevocationStatus](../resources/intune-deviceconfig-certificaterevocationstatus.md)|Revocar el estado. Los valores posibles son: `none`, `pending`, `issued`, `failed` y `revoked`.|
|certificateProfileDisplayName|String|Nombre para mostrar de perfil de certificado|
|deviceDisplayName|String|Nombre para mostrar del dispositivo|
|userDisplayName|String|Nombre para mostrar del usuario.|
|certificateExpirationDateTime|DateTimeOffset|Fecha de caducidad del certificado|
|certificateLastIssuanceStateChangedDateTime|DateTimeOffset|Último cambio de estado de emisión de certificado|
|lastCertificateStateChangeDateTime|DateTimeOffset|Último cambio de estado de emisión de certificado|
|certificateIssuer|String|Emisor|
|certificateThumbprint|String|Huella digital|
|númeroSerieCertificado|String|Número de serie|
|certificateKeyLength|Int32|Longitud de clave|
|certificateEnhancedKeyUsage|String|Uso mejorado de clave|
|certificateValidityPeriod|Int32|Período de validez|
|certificateSubjectNameFormatString|String|Cadena de formato de nombre de sujeto para formatos de nombre de sujeto personalizado|
|certificateSubjectAlternativeNameFormatString|String|Cadena de formato de nombre alternativo de sujeto para formatos personalizados|
|certificateIssuanceDateTime|DateTimeOffset|Fecha de emisión|
|certificateErrorCode|Int32|Código de error|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceCertificateState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceCertificateState",
  "id": "String (identifier)",
  "devicePlatform": "String",
  "certificateKeyUsage": "String",
  "certificateValidityPeriodUnits": "String",
  "certificateIssuanceState": "String",
  "certificateKeyStorageProvider": "String",
  "certificateSubjectNameFormat": "String",
  "certificateSubjectAlternativeNameFormat": "String",
  "certificateRevokeStatus": "String",
  "certificateProfileDisplayName": "String",
  "deviceDisplayName": "String",
  "userDisplayName": "String",
  "certificateExpirationDateTime": "String (timestamp)",
  "certificateLastIssuanceStateChangedDateTime": "String (timestamp)",
  "lastCertificateStateChangeDateTime": "String (timestamp)",
  "certificateIssuer": "String",
  "certificateThumbprint": "String",
  "certificateSerialNumber": "String",
  "certificateKeyLength": 1024,
  "certificateEnhancedKeyUsage": "String",
  "certificateValidityPeriod": 1024,
  "certificateSubjectNameFormatString": "String",
  "certificateSubjectAlternativeNameFormatString": "String",
  "certificateIssuanceDateTime": "String (timestamp)",
  "certificateErrorCode": 1024
}
```





