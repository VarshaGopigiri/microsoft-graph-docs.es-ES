---
title: tipo de recurso androidWorkProfileEnterpriseWiFiConfiguration
description: Proporcionando las configuraciones de este perfil puede indicar el dispositivo Android perfil de trabajo para conectarse al extremo de Wi-Fi que desee. Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo de Wi-Fi que puede hacer que la conexión Wi-Fi transparente para el usuario final.
author: tfitzmac
ms.openlocfilehash: 9626ae3ce49dc474f80b4c83b978a4a7ed655239
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27306135"
---
# <a name="androidworkprofileenterprisewificonfiguration-resource-type"></a>tipo de recurso androidWorkProfileEnterpriseWiFiConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Proporcionando las configuraciones de este perfil puede indicar el dispositivo Android perfil de trabajo para conectarse al extremo de Wi-Fi que desee. Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo de Wi-Fi que puede hacer que la conexión Wi-Fi transparente para el usuario final.

Hereda de [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista androidWorkProfileEnterpriseWiFiConfigurations](../api/intune-deviceconfig-androidworkprofileenterprisewificonfiguration-list.md)|colección de [androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md)|Propiedades de la lista y relaciones de los objetos [androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md) .|
|[Obtener androidWorkProfileEnterpriseWiFiConfiguration](../api/intune-deviceconfig-androidworkprofileenterprisewificonfiguration-get.md)|[androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md)|Leer las propiedades y las relaciones del objeto [androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md) .|
|[Crear androidWorkProfileEnterpriseWiFiConfiguration](../api/intune-deviceconfig-androidworkprofileenterprisewificonfiguration-create.md)|[androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md)|Crear un nuevo objeto [androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md) .|
|[Eliminar androidWorkProfileEnterpriseWiFiConfiguration](../api/intune-deviceconfig-androidworkprofileenterprisewificonfiguration-delete.md)|Ninguno|Elimina un [androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md).|
|[Actualizar androidWorkProfileEnterpriseWiFiConfiguration](../api/intune-deviceconfig-androidworkprofileenterprisewificonfiguration-update.md)|[androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md)|Actualizar las propiedades de un objeto [androidWorkProfileEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofileenterprisewificonfiguration.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|supportsScopeTags|Boolean|Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito. No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito. Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure. Esta propiedad es de sólo lectura. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|networkName|String|Nombre de red se hereda de [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)|
|SSID|String|Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos. Se hereda de [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)|
|connectAutomatically|Boolean|Conectar automáticamente cuando esta red esté en el intervalo. Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi. Se hereda de [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)|
|connectWhenNetworkNameIsHidden|Boolean|Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos. Se hereda de [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md)|
|wiFiSecurityType|[androidWiFiSecurityType](../resources/intune-deviceconfig-androidwifisecuritytype.md)|Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad. Se hereda de [androidWorkProfileWiFiConfiguration](../resources/intune-deviceconfig-androidworkprofilewificonfiguration.md). Los valores posibles son: `open` y `wpaEnterprise`.|
|eapType|[androidEapType](../resources/intune-deviceconfig-androideaptype.md)|Indica el tipo de protocolo EAP establecido en el extremo de Wi-Fi (enrutador). Los valores posibles son: `eapTls`, `eapTtls` y `peap`.|
|authenticationMethod|[wiFiAuthenticationMethod](../resources/intune-deviceconfig-wifiauthenticationmethod.md)|Indica el método de autenticación que se debe usar cuando se configura el tipo de EAP PEAP o EAP-TTLS el cliente (dispositivo). Los valores posibles son: `certificate` y `usernameAndPassword`.|
|innerAuthenticationProtocolForEapTtls|[nonEapAuthenticationMethodForEapTtlsType](../resources/intune-deviceconfig-noneapauthenticationmethodforeapttlstype.md)|Método no EAP para la autenticación (Inner identidad) cuando el tipo de EAP es EAP-TTLS y Authenticationmethod es el nombre de usuario y contraseña. Los valores posibles son: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap` y `microsoftChapVersionTwo`.|
|innerAuthenticationProtocolForPeap|[nonEapAuthenticationMethodForPeap](../resources/intune-deviceconfig-noneapauthenticationmethodforpeap.md)|Método no EAP para la autenticación (Inner identidad) cuando el tipo de EAP es PEAP y Authenticationmethod es el nombre de usuario y contraseña. Los valores posibles son: `none` y `microsoftChapVersionTwo`.|
|outerIdentityPrivacyTemporaryValue|String|Habilitar privacidad de identidad (identidad externa) cuando se configura el tipo de EAP a EAP-TTLS o PEAP. La cadena proporcionada aquí se usa para el nombre de usuario de los usuarios individuales de la máscara cuando intenten conectarse a la red Wi-Fi.|

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
|rootCertificateForServerValidation|[androidWorkProfileTrustedRootCertificate](../resources/intune-deviceconfig-androidworkprofiletrustedrootcertificate.md)|Certificado raíz de confianza para la validación de servidor cuando se configura el tipo de EAP para EAP-TLS, EAP-TTLS o PEAP. Éste es el certificado presentado por el extremo de Wi-Fi cuando el dispositivo intenta conectarse al extremo de Wi-Fi. El dispositivo (o usuario) debe aceptar este certificado para continuar con el intento de conexión.|
|identityCertificateForClientAuthentication|[androidWorkProfileCertificateProfileBase](../resources/intune-deviceconfig-androidworkprofilecertificateprofilebase.md)|Certificado de identidad para la autenticación de cliente cuando se configura el tipo de EAP para EAP-TLS, EAP-TTLS (con autenticación de certificados) o PEAP (con la autenticación de certificado). Éste es el certificado presentado por el cliente al extremo de Wi-Fi. El servidor de autenticación esté sentado detrás del extremo de Wi-Fi debe aceptar este certificado para establecer una conexión Wi-Fi correcta.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidWorkProfileEnterpriseWiFiConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidWorkProfileEnterpriseWiFiConfiguration",
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
  "networkName": "String",
  "ssid": "String",
  "connectAutomatically": true,
  "connectWhenNetworkNameIsHidden": true,
  "wiFiSecurityType": "String",
  "eapType": "String",
  "authenticationMethod": "String",
  "innerAuthenticationProtocolForEapTtls": "String",
  "innerAuthenticationProtocolForPeap": "String",
  "outerIdentityPrivacyTemporaryValue": "String"
}
```





