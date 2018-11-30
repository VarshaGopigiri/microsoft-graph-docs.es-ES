---
title: tipo de recurso iosScepCertificateProfile
description: perfil de certificado SCEP iOS.
ms.openlocfilehash: 590672e873382fda048749622282be45315dbca4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084919"
---
# <a name="iosscepcertificateprofile-resource-type"></a>tipo de recurso iosScepCertificateProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

perfil de certificado SCEP iOS.

Hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista iosScepCertificateProfiles](../api/intune-deviceconfig-iosscepcertificateprofile-list.md)|colección de [iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md)|Propiedades de la lista y relaciones de los objetos [iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md) .|
|[Obtener iosScepCertificateProfile](../api/intune-deviceconfig-iosscepcertificateprofile-get.md)|[iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md)|Leer las propiedades y las relaciones del objeto [iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md) .|
|[Crear iosScepCertificateProfile](../api/intune-deviceconfig-iosscepcertificateprofile-create.md)|[iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md)|Crear un nuevo objeto [iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md) .|
|[Eliminar iosScepCertificateProfile](../api/intune-deviceconfig-iosscepcertificateprofile-delete.md)|Ninguno|Elimina un [iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md).|
|[Actualizar iosScepCertificateProfile](../api/intune-deviceconfig-iosscepcertificateprofile-update.md)|[iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md)|Actualizar las propiedades de un objeto [iosScepCertificateProfile](../resources/intune-deviceconfig-iosscepcertificateprofile.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|supportsScopeTags|Booleano|Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito. No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito. Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure. Esta propiedad es de sólo lectura. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|renewalThresholdPercentage|Int32|Porcentaje de umbral de renovación de certificado. Válido valores heredada de 1 a 99 de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)|
|subjectNameFormat|[appleSubjectNameFormat](../resources/intune-deviceconfig-applesubjectnameformat.md)|Formato de nombre de sujeto de certificado. Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md). Los valores posibles son: `commonName`, `commonNameAsEmail`, `custom`, `commonNameIncludingEmail`, `commonNameAsIMEI`, `commonNameAsSerialNumber`.|
|subjectAlternativeNameType|[subjectAlternativeNameType](../resources/intune-deviceconfig-subjectalternativenametype.md)|Tipo de nombre alternativo del sujeto del certificado. Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md). Los valores posibles son: `none`, `emailAddress`, `userPrincipalName`, `customAzureADAttribute` y `domainNameService`.|
|certificateValidityPeriodValue|Int32|Valor para el período de validez del certificado. Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)|
|certificateValidityPeriodScale|[certificateValidityPeriodScale](../resources/intune-deviceconfig-certificatevalidityperiodscale.md)|Escala para el período de validez del certificado. Se hereda de [iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md). Los valores posibles son: `days`, `months` y `years`.|
|scepServerUrls|Colección String|Direcciones URL del servidor SCEP.|
|subjectNameFormatString|String|Formato personalizado para usar con SubjectNameFormat = personalizada. Ejemplo: CN = {{EmailAddress}}, E = {{EmailAddress}}, OU = Users de la empresa, O = Contoso Corporation, L = Redmond, ST = WA, C = US|
|keyUsage|[keyUsages](../resources/intune-deviceconfig-keyusages.md)|Uso de la clave SCEP. Los valores posibles son: `keyEncipherment` y `digitalSignature`.|
|keySize|[keySize](../resources/intune-deviceconfig-keysize.md)|Tamaño de la clave SCEP. Los valores posibles son: `size1024` y `size2048`.|
|extendedKeyUsages|colección de [ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)|Configuración de clave (EKU) extendida. Esta colección puede contener un máximo de 500 elementos.|
|subjectAlternativeNameFormatString|String|Cadena personalizada que define el atributo AAD.|
|certificateStore|[certificateStore](../resources/intune-deviceconfig-certificatestore.md)|Certificado del almacén de destino. Los valores posibles son: `user` y `machine`.|
|customSubjectAlternativeNames|colección de [customSubjectAlternativeName](../resources/intune-deviceconfig-customsubjectalternativename.md)|Configuración de Alterantive nombre de sujeto personalizado. Esta colección puede contener un máximo de 500 elementos.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|groupAssignments|colección de [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)|La lista de asignaciones de grupo para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|asignaciones|Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|La lista de tareas para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatuses|Colección [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Estado de instalación de configuración del dispositivo por dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|userStatuses|Colección [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|Estado de instalación de configuración de dispositivo por usuario. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|Información general sobre el estado de dispositivos de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|Información general sobre el estado de usuarios de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Resumen de dispositivo sobre el estado de configuración de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|rootCertificate|[iosTrustedRootCertificate](../resources/intune-deviceconfig-iostrustedrootcertificate.md)|Certificado raíz de confianza.|
|managedDeviceCertificateStates|colección de [managedDeviceCertificateState](../resources/intune-deviceconfig-manageddevicecertificatestate.md)|Estado de certificado para dispositivos|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosScepCertificateProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosScepCertificateProfile",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "roleScopeTagIds": [
    "String"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "renewalThresholdPercentage": 1024,
  "subjectNameFormat": "String",
  "subjectAlternativeNameType": "String",
  "certificateValidityPeriodValue": 1024,
  "certificateValidityPeriodScale": "String",
  "scepServerUrls": [
    "String"
  ],
  "subjectNameFormatString": "String",
  "keyUsage": "String",
  "keySize": "String",
  "extendedKeyUsages": [
    {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "String",
      "objectIdentifier": "String"
    }
  ],
  "subjectAlternativeNameFormatString": "String",
  "certificateStore": "String",
  "customSubjectAlternativeNames": [
    {
      "@odata.type": "microsoft.graph.customSubjectAlternativeName",
      "sanType": "String",
      "name": "String"
    }
  ]
}
```





