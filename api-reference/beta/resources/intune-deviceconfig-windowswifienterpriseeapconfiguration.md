---
title: tipo de recurso windowsWifiEnterpriseEAPConfiguration
description: Esta entidad ofrece descripciones de los métodos declarados, propiedades y relaciones expuestas por el CSP Wifi.
ms.openlocfilehash: 5ed685d5dc25b3adea2a11a632c66dbe68fbebf5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085552"
---
# <a name="windowswifienterpriseeapconfiguration-resource-type"></a>tipo de recurso windowsWifiEnterpriseEAPConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Esta entidad ofrece descripciones de los métodos declarados, propiedades y relaciones expuestas por el CSP Wifi.

Hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista windowsWifiEnterpriseEAPConfigurations](../api/intune-deviceconfig-windowswifienterpriseeapconfiguration-list.md)|colección de [windowsWifiEnterpriseEAPConfiguration](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md)|Propiedades de la lista y relaciones de los objetos [windowsWifiEnterpriseEAPConfiguration](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md) .|
|[Obtener windowsWifiEnterpriseEAPConfiguration](../api/intune-deviceconfig-windowswifienterpriseeapconfiguration-get.md)|[windowsWifiEnterpriseEAPConfiguration](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md)|Leer las propiedades y las relaciones del objeto [windowsWifiEnterpriseEAPConfiguration](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md) .|
|[Crear windowsWifiEnterpriseEAPConfiguration](../api/intune-deviceconfig-windowswifienterpriseeapconfiguration-create.md)|[windowsWifiEnterpriseEAPConfiguration](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md)|Crear un nuevo objeto [windowsWifiEnterpriseEAPConfiguration](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md) .|
|[Eliminar windowsWifiEnterpriseEAPConfiguration](../api/intune-deviceconfig-windowswifienterpriseeapconfiguration-delete.md)|Ninguno|Elimina un [windowsWifiEnterpriseEAPConfiguration](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md).|
|[Actualizar windowsWifiEnterpriseEAPConfiguration](../api/intune-deviceconfig-windowswifienterpriseeapconfiguration-update.md)|[windowsWifiEnterpriseEAPConfiguration](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md)|Actualizar las propiedades de un objeto [windowsWifiEnterpriseEAPConfiguration](../resources/intune-deviceconfig-windowswifienterpriseeapconfiguration.md) .|

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
|preSharedKey|String|Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|wifiSecurityType|[wiFiSecurityType](../resources/intune-deviceconfig-wifisecuritytype.md)|Especificar el tipo de seguridad Wifi. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md). Los valores posibles son: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.|
|meteredConnectionLimit|[meteredConnectionLimitType](../resources/intune-deviceconfig-meteredconnectionlimittype.md)|Especificar el tipo de límite de conexión intencionadas para la conexión wifi. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md). Los valores posibles son: `unrestricted`, `fixed` y `variable`.|
|SSID|String|Especifique el SSID de la conexión wifi. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|networkName|String|Especifique el nombre de la configuración de red. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|connectAutomatically|Booleano|Especifique si la conexión wifi debe conectarse automáticamente cuando en el rango. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|connectToPreferredNetwork|Booleano|Especifique si la conexión wifi debe conectarse a redes más preferidas cuando ya está conectado a éste.  Requiere ConnectAutomatically sea true. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|connectWhenNetworkNameIsHidden|Booleano|Especifique si la conexión wifi debe conectarse automáticamente incluso cuando el SSID no sea de difusión. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|proxySetting|[wiFiProxySetting](../resources/intune-deviceconfig-wifiproxysetting.md)|Especificar la configuración del proxy para la configuración de Wi-Fi Inherited desde [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md). Los valores posibles son: `none`, `manual` y `automatic`.|
|proxyManualAddress|String|Especifique la dirección IP del servidor proxy. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|proxyManualPort|Int32|Especifique el puerto del servidor proxy. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|proxyAutomaticConfigurationUrl|String|Especifique la dirección URL de la secuencia de comandos de configuración de servidor proxy. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|forceFIPSCompliance|Booleano|Especifique si debe forzarse la compatibilidad con FIPS. Se hereda de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|
|networkSingleSignOn|[networkSingleSignOnType](../resources/intune-deviceconfig-networksinglesignontype.md)|Especifique el inicio de sesión único de red en tipo. Los valores posibles son: `disabled`, `prelogon` y `postlogon`.|
|maximumAuthenticationTimeoutInSeconds|Int32|Especificar el tiempo de espera de autenticación máximo (en segundos).  Intervalo válido: 1-120|
|promptForAdditionalAuthenticationCredentials|Booleano|Especifique si la conexión wifi debe solicitar las credenciales de autenticación adicional.|
|enablePairwiseMasterKeyCaching|Booleano|Especifique si la conexión wifi debe habilitar el almacenamiento en caché de clave maestra en pares.|
|maximumPairwiseMasterKeyCacheTimeInMinutes|Int32|Especificar el tiempo de caché máximo clave maestra en pares (en minutos).  Intervalo válido: 5-1440|
|maximumNumberOfPairwiseMasterKeysInCache|Int32|Especifique el número máximo de claves maestras en pares en memoria caché.  Intervalo válido: 1-255|
|enablePreAuthentication|Booleano|Especifique si se debe habilitar la autenticación previa.|
|maximumPreAuthenticationAttempts|Int32|Especifique el número máximo de intentos de autenticación previa.  Intervalo válido: 1-16|
|eapType|[eapType](../resources/intune-deviceconfig-eaptype.md)|Protocolo de autenticación extensible (EAP). Indica el tipo de protocolo EAP establecido en el extremo de Wi-Fi (enrutador). Los valores posibles son: `eapTls`, `leap`, `eapSim`, `eapTtls`, `peap`, `eapFast`.|
|trustedServerCertificateNames|Colección String|Especifique los nombres de certificado de servidor de confianza.|
|authenticationMethod|[wiFiAuthenticationMethod](../resources/intune-deviceconfig-wifiauthenticationmethod.md)|Especifique el método de autenticación. Los valores posibles son: `certificate` y `usernameAndPassword`.|
|innerAuthenticationProtocolForEAPTTLS|[nonEapAuthenticationMethodForEapTtlsType](../resources/intune-deviceconfig-noneapauthenticationmethodforeapttlstype.md)|Especificar el protocolo de autenticación interna para EAP TTLS. Los valores posibles son: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap` y `microsoftChapVersionTwo`.|
|outerIdentityPrivacyTemporaryValue|String|Especifique la cadena que va a reemplazar los nombres de usuario para privacidad cuando se utiliza EAP TTLS o PEAP.|

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
|rootCertificatesForServerValidation|colección de [windows81TrustedRootCertificate](../resources/intune-deviceconfig-windows81trustedrootcertificate.md)|Especifique el certificado raíz para la validación del servidor.|
|identityCertificateForClientAuthentication|[windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)|Especificar certificado de identidad para la autenticación de cliente.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsWifiEnterpriseEAPConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsWifiEnterpriseEAPConfiguration",
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
  "preSharedKey": "String",
  "wifiSecurityType": "String",
  "meteredConnectionLimit": "String",
  "ssid": "String",
  "networkName": "String",
  "connectAutomatically": true,
  "connectToPreferredNetwork": true,
  "connectWhenNetworkNameIsHidden": true,
  "proxySetting": "String",
  "proxyManualAddress": "String",
  "proxyManualPort": 1024,
  "proxyAutomaticConfigurationUrl": "String",
  "forceFIPSCompliance": true,
  "networkSingleSignOn": "String",
  "maximumAuthenticationTimeoutInSeconds": 1024,
  "promptForAdditionalAuthenticationCredentials": true,
  "enablePairwiseMasterKeyCaching": true,
  "maximumPairwiseMasterKeyCacheTimeInMinutes": 1024,
  "maximumNumberOfPairwiseMasterKeysInCache": 1024,
  "enablePreAuthentication": true,
  "maximumPreAuthenticationAttempts": 1024,
  "eapType": "String",
  "trustedServerCertificateNames": [
    "String"
  ],
  "authenticationMethod": "String",
  "innerAuthenticationProtocolForEAPTTLS": "String",
  "outerIdentityPrivacyTemporaryValue": "String"
}
```





