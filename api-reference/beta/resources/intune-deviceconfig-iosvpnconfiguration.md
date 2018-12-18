---
title: tipo de recurso iosVpnConfiguration
description: Proporcionando las configuraciones de este perfil puede indicar el dispositivo iOS para conectarse al extremo VPN que desee. Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo VPN que puede realizar la conexión VPN transparente para el usuario final.
author: tfitzmac
ms.openlocfilehash: 8dac46c9ef413e3699613b7f3da5a6e19c93c76e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313625"
---
# <a name="iosvpnconfiguration-resource-type"></a>tipo de recurso iosVpnConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Proporcionando las configuraciones de este perfil puede indicar el dispositivo iOS para conectarse al extremo VPN que desee. Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo VPN que puede realizar la conexión VPN transparente para el usuario final.

Hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista iosVpnConfigurations](../api/intune-deviceconfig-iosvpnconfiguration-list.md)|colección de [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md)|Propiedades de la lista y relaciones de los objetos [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) .|
|[Obtener iosVpnConfiguration](../api/intune-deviceconfig-iosvpnconfiguration-get.md)|[iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md)|Leer las propiedades y las relaciones del objeto [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) .|
|[Crear iosVpnConfiguration](../api/intune-deviceconfig-iosvpnconfiguration-create.md)|[iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md)|Crear un nuevo objeto [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) .|
|[Eliminar iosVpnConfiguration](../api/intune-deviceconfig-iosvpnconfiguration-delete.md)|Ninguno|Elimina un [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md).|
|[Actualizar iosVpnConfiguration](../api/intune-deviceconfig-iosvpnconfiguration-update.md)|[iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md)|Actualizar las propiedades de un objeto [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) .|

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
|connectionName|String|Nombre de la conexión que se muestra al usuario. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|connectionType|[appleVpnConnectionType](../resources/intune-deviceconfig-applevpnconnectiontype.md)|Tipo de conexión. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md). Los valores posibles son: `ciscoAnyConnect`, `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `customVpn`, `ciscoIPSec`, `citrix`, `ciscoAnyConnectV2`, `paloAltoGlobalProtect`, `zscalerPrivateAccess`, `f5Access2018`, `citrixSso`, `paloAltoGlobalProtectV2`.|
|loginGroupOrDomain|String|Grupo de inicio de sesión o dominio cuando se establece el tipo de conexión a Dell SonicWALL Mobile conexión. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|role|String|Función de tipo de conexión se establece en impulsos seguro. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|dominio kerberos|String|Dominio Kerberos cuando se establece el tipo de conexión a impulsos seguro. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|servidor|[servidor de VPN](../resources/intune-deviceconfig-vpnserver.md)|Servidor de VPN en la red. Asegúrese de que los usuarios finales pueden tener acceso a esta ubicación de red. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|identificador|String|Identificador proporcionado por el proveedor de VPN cuando se establece el tipo de conexión a VPN personalizado. Por ejemplo: AnyConnect de Cisco usa un identificador de la com.cisco.anyconnect.applevpn.plugin de formulario Inherited desde [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|customData|colección [keyValue](../resources/intune-deviceconfig-keyvalue.md)|Datos personalizados cuando se establece el tipo de conexión a VPN personalizado. Use este campo para habilitar la funcionalidad no admitida por Intune, pero disponible en la solución de VPN. Póngase en contacto con su proveedor de VPN para obtener información sobre cómo agregar estos pares de clave y valor. Esta colección puede contener un máximo de 25 elementos. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|customKeyValueData|Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)|Datos personalizados cuando se establece el tipo de conexión a VPN personalizado. Use este campo para habilitar la funcionalidad no admitida por Intune, pero disponible en la solución de VPN. Póngase en contacto con su proveedor de VPN para obtener información sobre cómo agregar estos pares de clave y valor. Esta colección puede contener un máximo de 25 elementos. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|enableSplitTunneling|Boolean|Enviar todo el tráfico de red a través de VPN. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|authenticationMethod|[vpnAuthenticationMethod](../resources/intune-deviceconfig-vpnauthenticationmethod.md)|Método de autenticación para esta conexión VPN. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md). Los valores posibles son: `certificate` y `usernameAndPassword`.|
|enablePerApp|Boolean|Si se establece en true, crea de carga por aplicación VPN que más adelante se puede asociar con las aplicaciones que pueden desencadenar este conexiones VPN en dispositivo de iOS del usuario final. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|safariDomains|Colección String|Dominios de Safari cuando está habilitada esta VPN por la configuración de la aplicación. Además de las aplicaciones asociadas con esta VPN, dominios de Safari especifiquen aquí también podrá desencadenar esta conexión VPN. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|onDemandRules|colección de [vpnOnDemandRule](../resources/intune-deviceconfig-vpnondemandrule.md)|Reglas de On Demand. Esta colección puede contener un máximo de 500 elementos. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|proxyServer|[vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)|Servidor proxy. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|optInToDeviceIdSharing|Boolean|Participar en uso compartido de identificador del dispositivo a los clientes de vpn de terceros para su uso durante la validación de control de acceso de red. Se hereda de [appleVpnConfiguration](../resources/intune-deviceconfig-applevpnconfiguration.md)|
|tipo de proveedor|[vpnProviderType](../resources/intune-deviceconfig-vpnprovidertype.md)|Tipo de proveedor de VPN por cada aplicación. Los valores posibles son: `notConfigured`, `appProxy` y `packetTunnel`.|
|userDomain|String|Sólo Zscaler. Escriba un dominio estático para rellenar previamente el campo de inicio de sesión con en la aplicación Zscaler. Si se deja vacía, se utilizará el dominio del usuario Azure Active Directory.|
|strictEnforcement|Boolean|Sólo Zscaler. Bloques de tráfico de red hasta que el usuario cierre sesión en la aplicación Zscaler. "True" significa que el tráfico se bloquea.|
|cloudName|String|Sólo Zscaler. Nube de Zscaler que está asignado el usuario.|
|excludeList|Colección String|Sólo Zscaler. Lista de direcciones de red que no se envían a través de la nube de Zscaler.|

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
|identityCertificate|[iosCertificateProfileBase](../resources/intune-deviceconfig-ioscertificateprofilebase.md)|Certificado de identidad para la autenticación de cliente al método de autenticación es el certificado.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.iosVpnConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosVpnConfiguration",
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
  "connectionType": "String",
  "loginGroupOrDomain": "String",
  "role": "String",
  "realm": "String",
  "server": {
    "@odata.type": "microsoft.graph.vpnServer",
    "description": "String",
    "address": "String",
    "isDefaultServer": true
  },
  "identifier": "String",
  "customData": [
    {
      "@odata.type": "microsoft.graph.keyValue",
      "key": "String",
      "value": "String"
    }
  ],
  "customKeyValueData": [
    {
      "@odata.type": "microsoft.graph.keyValuePair",
      "name": "String",
      "value": "String"
    }
  ],
  "enableSplitTunneling": true,
  "authenticationMethod": "String",
  "enablePerApp": true,
  "safariDomains": [
    "String"
  ],
  "onDemandRules": [
    {
      "@odata.type": "microsoft.graph.vpnOnDemandRule",
      "ssids": [
        "String"
      ],
      "dnsSearchDomains": [
        "String"
      ],
      "probeUrl": "String",
      "action": "String",
      "domainAction": "String",
      "domains": [
        "String"
      ],
      "probeRequiredUrl": "String"
    }
  ],
  "proxyServer": {
    "@odata.type": "microsoft.graph.vpnProxyServer",
    "automaticConfigurationScriptUrl": "String",
    "address": "String",
    "port": 1024
  },
  "optInToDeviceIdSharing": true,
  "providerType": "String",
  "userDomain": "String",
  "strictEnforcement": true,
  "cloudName": "String",
  "excludeList": [
    "String"
  ]
}
```





