---
title: Actualizar macOSEnterpriseWiFiConfiguration
description: Actualizar las propiedades de un objeto macOSEnterpriseWiFiConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a5dcf7400bd0f8efbdc57751c15c5666e4478529
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27808424"
---
# <a name="update-macosenterprisewificonfiguration"></a>Actualizar macOSEnterpriseWiFiConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Actualizar las propiedades de un objeto [macOSEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-macosenterprisewificonfiguration.md) .
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
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [macOSEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-macosenterprisewificonfiguration.md) .

La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [macOSEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-macosenterprisewificonfiguration.md).

|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|supportsScopeTags|Booleano|Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito. No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito. Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure. Esta propiedad es de sólo lectura. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|networkName|Cadena|Nombre de red se hereda de [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)|
|SSID|Cadena|Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos. Se hereda de [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)|
|connectAutomatically|Booleano|Conectar automáticamente cuando esta red esté en el intervalo. Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi. Se hereda de [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)|
|connectWhenNetworkNameIsHidden|Booleano|Conectar cuando la red no sea de difusión su nombre (SSID). Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos. Se hereda de [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)|
|wiFiSecurityType|[wiFiSecurityType](../resources/intune-deviceconfig-wifisecuritytype.md)|Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad. Se hereda de [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md). Los valores posibles son: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.|
|proxySettings|[wiFiProxySetting](../resources/intune-deviceconfig-wifiproxysetting.md)|Tipo de proxy para esta conexión Wi-Fi Inherited desde [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md). Los valores posibles son: `none`, `manual` y `automatic`.|
|proxyManualAddress|Cadena|Nombre de host DNS o dirección IP del servidor proxy cuando se selecciona la configuración manual. Se hereda de [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)|
|proxyManualPort|Int32|Puerto del servidor proxy cuando se selecciona la configuración manual. Se hereda de [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)|
|proxyAutomaticConfigurationUrl|Cadena|URL de la secuencia de la configuración automática de servidor proxy cuando se selecciona la configuración automática. Normalmente, esta dirección URL es la ubicación del archivo PAC (configuración automática de Proxy). Se hereda de [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)|
|preSharedKey|Cadena|Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA. Se hereda de [macOSWiFiConfiguration](../resources/intune-deviceconfig-macoswificonfiguration.md)|
|eapType|[eapType](../resources/intune-deviceconfig-eaptype.md)|Protocolo de autenticación extensible (EAP). Indica el tipo de protocolo EAP establecido en el extremo de Wi-Fi (enrutador). Los valores posibles son: `eapTls`, `leap`, `eapSim`, `eapTtls`, `peap`, `eapFast`.|
|eapFastConfiguration|[eapFastConfiguration](../resources/intune-deviceconfig-eapfastconfiguration.md)|Opción de configuración de EAP-FAST cuando EAP-FAST es el tipo de EAP seleccionado. Los valores posibles son: `noProtectedAccessCredential`, `useProtectedAccessCredential`, `useProtectedAccessCredentialAndProvision` y `useProtectedAccessCredentialAndProvisionAnonymously`.|
|trustedServerCertificateNames|Colección String|Los nombres de certificado de servidor de confianza cuando se configura el tipo de EAP a FAST/EAP-TLS o TTLS o PEAP. Esto es el nombre común que se usa en los certificados emitidos por su entidad emisora de certificados de confianza (CA). Si proporciona esta información, puede omitir el cuadro de diálogo de confianza dinámica que se muestra en los dispositivos de los usuarios finales cuando se conectan a esta red Wi-Fi.|
|authenticationMethod|[wiFiAuthenticationMethod](../resources/intune-deviceconfig-wifiauthenticationmethod.md)|Método de autenticación cuando se configura el tipo de EAP PEAP o EAP-TTLS. Los valores posibles son: `certificate` y `usernameAndPassword`.|
|innerAuthenticationProtocolForEapTtls|[nonEapAuthenticationMethodForEapTtlsType](../resources/intune-deviceconfig-noneapauthenticationmethodforeapttlstype.md)|Método no EAP para la autenticación (Inner identidad) cuando el tipo de EAP es EAP-TTLS y Authenticationmethod es el nombre de usuario y contraseña. Los valores posibles son: `unencryptedPassword`, `challengeHandshakeAuthenticationProtocol`, `microsoftChap` y `microsoftChapVersionTwo`.|
|outerIdentityPrivacyTemporaryValue|Cadena|Habilitar privacidad de identidad (identidad externa) cuando se configura el tipo de EAP a EAP-TTLS, EAP-FAST o PEAP. Esta propiedad enmascara los nombres de usuario con el texto que escriba. Por ejemplo, si usa 'anonymous', cada usuario que se autentica con esta conexión Wi-Fi con su nombre de usuario real se muestra como 'anonymous'.|



## <a name="response"></a>Respuesta
Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [macOSEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-macosenterprisewificonfiguration.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1078

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "networkName": "Network Name value",
  "ssid": "Ssid value",
  "connectAutomatically": true,
  "connectWhenNetworkNameIsHidden": true,
  "wiFiSecurityType": "wpaPersonal",
  "proxySettings": "manual",
  "proxyManualAddress": "Proxy Manual Address value",
  "proxyManualPort": 15,
  "proxyAutomaticConfigurationUrl": "https://example.com/proxyAutomaticConfigurationUrl/",
  "preSharedKey": "Pre Shared Key value",
  "eapType": "leap",
  "eapFastConfiguration": "useProtectedAccessCredential",
  "trustedServerCertificateNames": [
    "Trusted Server Certificate Names value"
  ],
  "authenticationMethod": "usernameAndPassword",
  "innerAuthenticationProtocolForEapTtls": "challengeHandshakeAuthenticationProtocol",
  "outerIdentityPrivacyTemporaryValue": "Outer Identity Privacy Temporary Value value"
}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1257

{
  "@odata.type": "#microsoft.graph.macOSEnterpriseWiFiConfiguration",
  "id": "7a6f9a2e-9a2e-7a6f-2e9a-6f7a2e9a6f7a",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "networkName": "Network Name value",
  "ssid": "Ssid value",
  "connectAutomatically": true,
  "connectWhenNetworkNameIsHidden": true,
  "wiFiSecurityType": "wpaPersonal",
  "proxySettings": "manual",
  "proxyManualAddress": "Proxy Manual Address value",
  "proxyManualPort": 15,
  "proxyAutomaticConfigurationUrl": "https://example.com/proxyAutomaticConfigurationUrl/",
  "preSharedKey": "Pre Shared Key value",
  "eapType": "leap",
  "eapFastConfiguration": "useProtectedAccessCredential",
  "trustedServerCertificateNames": [
    "Trusted Server Certificate Names value"
  ],
  "authenticationMethod": "usernameAndPassword",
  "innerAuthenticationProtocolForEapTtls": "challengeHandshakeAuthenticationProtocol",
  "outerIdentityPrivacyTemporaryValue": "Outer Identity Privacy Temporary Value value"
}
```





