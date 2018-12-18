---
title: tipo de recurso windows10VpnConfiguration
description: Proporcionando las configuraciones de este perfil puede indicar el dispositivo de Windows 10 (escritorio o móvil) para conectarse al extremo VPN que desee. Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo VPN que puede realizar la conexión VPN transparente para el usuario final.
author: tfitzmac
ms.openlocfilehash: 1dbbdb5a7065214ab6a290215f2c6016f8ad74bb
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27340701"
---
# <a name="windows10vpnconfiguration-resource-type"></a>tipo de recurso windows10VpnConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Proporcionando las configuraciones de este perfil puede indicar el dispositivo de Windows 10 (escritorio o móvil) para conectarse al extremo VPN que desee. Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo VPN que puede realizar la conexión VPN transparente para el usuario final.

Hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista windows10VpnConfigurations](../api/intune-deviceconfig-windows10vpnconfiguration-list.md)|colección de [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md)|Propiedades de la lista y relaciones de los objetos [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) .|
|[Obtener windows10VpnConfiguration](../api/intune-deviceconfig-windows10vpnconfiguration-get.md)|[windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md)|Leer las propiedades y las relaciones del objeto [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) .|
|[Crear windows10VpnConfiguration](../api/intune-deviceconfig-windows10vpnconfiguration-create.md)|[windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md)|Crear un nuevo objeto [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) .|
|[Eliminar windows10VpnConfiguration](../api/intune-deviceconfig-windows10vpnconfiguration-delete.md)|Ninguno|Elimina un [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md).|
|[Actualizar windows10VpnConfiguration](../api/intune-deviceconfig-windows10vpnconfiguration-update.md)|[windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md)|Actualizar las propiedades de un objeto [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) .|

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
|connectionName|String|Nombre de la conexión que se muestra al usuario. Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)|
|servidores|colección de [servidor de VPN](../resources/intune-deviceconfig-vpnserver.md)|Lista de servidores VPN en la red. Asegúrese de que los usuarios finales pueden tener acceso a estas ubicaciones de red. Esta colección puede contener un máximo de 500 elementos. Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)|
|customXml|Binario|Comandos XML personalizados que configura la conexión VPN. (Matriz de bytes codificada UTF8) Se hereda de [windowsVpnConfiguration](../resources/intune-deviceconfig-windowsvpnconfiguration.md)|
|profileTarget|[windows10VpnProfileTarget](../resources/intune-deviceconfig-windows10vpnprofiletarget.md)|Tipo de perfil de destino. Los valores posibles son: `user`, `device` y `autoPilotDevice`.|
|connectionType|[windows10VpnConnectionType](../resources/intune-deviceconfig-windows10vpnconnectiontype.md)|Tipo de conexión. Los valores posibles son: `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `automatic`, `ikEv2`, `l2tp`, `pptp`, `citrix` y `paloAltoGlobalProtect`.|
|enableSplitTunneling|Boolean|Habilitar túnel dividido.|
|enableAlwaysOn|Boolean|Habilitar siempre en el modo.|
|enableDeviceTunnel|Boolean|Habilitar túnel de dispositivo.|
|enableDnsRegistration|Boolean|Habilitar el registro de dirección IP con DNS interno.|
|dnsSuffixes|Colección String|Especificar sufijos DNS para agregar a la lista de búsqueda DNS para enrutar correctamente los nombres cortos.|
|authenticationMethod|[windows10VpnAuthenticationMethod](../resources/intune-deviceconfig-windows10vpnauthenticationmethod.md)|Método de autenticación. Los valores posibles son: `certificate`, `usernameAndPassword` y `customEapXml`.|
|rememberUserCredentials|Boolean|Recuerde que las credenciales de usuario.|
|enableConditionalAccess|Boolean|Habilite el acceso condicional.|
|enableSingleSignOnWithAlternateCertificate|Boolean|Habilitar sesión único (SSO) con certificado alternativa.|
|singleSignOnEku|[ExtendeKeyUsage](../resources/intune-deviceconfig-extendedkeyusage.md)|Single sign-on extendido clave (EKU).|
|singleSignOnIssuerHash|String|Hash de emisor de inicio de sesión único.|
|eapXml|Binario|Protocolo de autenticación extensible (EAP) XML. (Matriz de bytes codificada UTF8)|
|proxyServer|[windows10VpnProxyServer](../resources/intune-deviceconfig-windows10vpnproxyserver.md)|Servidor proxy.|
|associatedApps|colección de [windows10AssociatedApps](../resources/intune-deviceconfig-windows10associatedapps.md)|Aplicaciones asociadas. Esta colección puede contener un máximo de 10 000 elementos.|
|onlyAssociatedAppsCanUseConnection|Boolean|Sólo las aplicaciones asociadas pueden utilizar conexión (VPN por aplicación).|
|windowsInformationProtectionDomain|String|Dominio de protección de información de Windows (curso) para asociar a esta conexión.|
|trafficRules|colección de [vpnTrafficRule](../resources/intune-deviceconfig-vpntrafficrule.md)|Reglas de tráfico. Esta colección puede contener un máximo de 1000 elementos.|
|rutas|colección de [vpnRoute](../resources/intune-deviceconfig-vpnroute.md)|Rutas (opcionales para los proveedores de terceros). Esta colección puede contener un máximo de 1000 elementos.|
|dnsRules|colección de [vpnDnsRule](../resources/intune-deviceconfig-vpndnsrule.md)|Reglas de DNS. Esta colección puede contener un máximo de 1000 elementos.|

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
|identityCertificate|[windowsCertificateProfileBase](../resources/intune-deviceconfig-windowscertificateprofilebase.md)|Certificado de identidad para la autenticación de cliente al método de autenticación es el certificado.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windows10VpnConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10VpnConfiguration",
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
  "connectionName": "String",
  "servers": [
    {
      "@odata.type": "microsoft.graph.vpnServer",
      "description": "String",
      "address": "String",
      "isDefaultServer": true
    }
  ],
  "customXml": "binary",
  "profileTarget": "String",
  "connectionType": "String",
  "enableSplitTunneling": true,
  "enableAlwaysOn": true,
  "enableDeviceTunnel": true,
  "enableDnsRegistration": true,
  "dnsSuffixes": [
    "String"
  ],
  "authenticationMethod": "String",
  "rememberUserCredentials": true,
  "enableConditionalAccess": true,
  "enableSingleSignOnWithAlternateCertificate": true,
  "singleSignOnEku": {
    "@odata.type": "microsoft.graph.extendedKeyUsage",
    "name": "String",
    "objectIdentifier": "String"
  },
  "singleSignOnIssuerHash": "String",
  "eapXml": "binary",
  "proxyServer": {
    "@odata.type": "microsoft.graph.windows10VpnProxyServer",
    "automaticConfigurationScriptUrl": "String",
    "address": "String",
    "port": 1024,
    "bypassProxyServerForLocalAddress": true
  },
  "associatedApps": [
    {
      "@odata.type": "microsoft.graph.windows10AssociatedApps",
      "appType": "String",
      "identifier": "String"
    }
  ],
  "onlyAssociatedAppsCanUseConnection": true,
  "windowsInformationProtectionDomain": "String",
  "trafficRules": [
    {
      "@odata.type": "microsoft.graph.vpnTrafficRule",
      "name": "String",
      "protocols": 1024,
      "localPortRanges": [
        {
          "@odata.type": "microsoft.graph.numberRange",
          "lowerNumber": 1024,
          "upperNumber": 1024
        }
      ],
      "remotePortRanges": [
        {
          "@odata.type": "microsoft.graph.numberRange",
          "lowerNumber": 1024,
          "upperNumber": 1024
        }
      ],
      "localAddressRanges": [
        {
          "@odata.type": "microsoft.graph.iPv4Range",
          "lowerAddress": "String",
          "upperAddress": "String"
        }
      ],
      "remoteAddressRanges": [
        {
          "@odata.type": "microsoft.graph.iPv4Range",
          "lowerAddress": "String",
          "upperAddress": "String"
        }
      ],
      "appId": "String",
      "appType": "String",
      "routingPolicyType": "String",
      "claims": "String"
    }
  ],
  "routes": [
    {
      "@odata.type": "microsoft.graph.vpnRoute",
      "destinationPrefix": "String",
      "prefixSize": 1024
    }
  ],
  "dnsRules": [
    {
      "@odata.type": "microsoft.graph.vpnDnsRule",
      "name": "String",
      "servers": [
        "String"
      ],
      "proxyServerUri": "String"
    }
  ]
}
```





