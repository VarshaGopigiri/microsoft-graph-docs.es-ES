---
title: tipo de recurso windowsWifiConfiguration
description: Configuración de dispositivos.
author: tfitzmac
ms.openlocfilehash: 5c8f7df3ef1c80e2d6204ca4acb2996200af5fa2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359188"
---
# <a name="windowswificonfiguration-resource-type"></a>tipo de recurso windowsWifiConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de dispositivos.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista windowsWifiConfigurations](../api/intune-deviceconfig-windowswificonfiguration-list.md)|colección de [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|Propiedades de la lista y relaciones de los objetos [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) .|
|[Obtener windowsWifiConfiguration](../api/intune-deviceconfig-windowswificonfiguration-get.md)|[windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|Leer las propiedades y las relaciones del objeto [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) .|
|[Crear windowsWifiConfiguration](../api/intune-deviceconfig-windowswificonfiguration-create.md)|[windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|Crear un nuevo objeto [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) .|
|[Eliminar windowsWifiConfiguration](../api/intune-deviceconfig-windowswificonfiguration-delete.md)|Ninguno|Elimina un [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md).|
|[Actualizar windowsWifiConfiguration](../api/intune-deviceconfig-windowswificonfiguration-update.md)|[windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md)|Actualizar las propiedades de un objeto [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) .|

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
|preSharedKey|String|Ésta es la clave previamente compartida para la red Wi-Fi Personal WPA.|
|wifiSecurityType|[wiFiSecurityType](../resources/intune-deviceconfig-wifisecuritytype.md)|Especificar el tipo de seguridad Wifi. Los valores posibles son: `open`, `wpaPersonal`, `wpaEnterprise`, `wep`, `wpa2Personal`, `wpa2Enterprise`.|
|meteredConnectionLimit|[meteredConnectionLimitType](../resources/intune-deviceconfig-meteredconnectionlimittype.md)|Especificar el tipo de límite de conexión intencionadas para la conexión wifi. Los valores posibles son: `unrestricted`, `fixed` y `variable`.|
|SSID|String|Especifique el SSID de la conexión wifi.|
|networkName|String|Especifique el nombre de la configuración de red.|
|connectAutomatically|Boolean|Especifique si la conexión wifi debe conectarse automáticamente cuando en el rango.|
|connectToPreferredNetwork|Boolean|Especifique si la conexión wifi debe conectarse a redes más preferidas cuando ya está conectado a éste.  Requiere ConnectAutomatically sea true.|
|connectWhenNetworkNameIsHidden|Boolean|Especifique si la conexión wifi debe conectarse automáticamente incluso cuando el SSID no sea de difusión.|
|proxySetting|[wiFiProxySetting](../resources/intune-deviceconfig-wifiproxysetting.md)|Especificar la configuración para la configuración de Wi-Fi del proxy. Los valores posibles son: `none`, `manual` y `automatic`.|
|proxyManualAddress|String|Especifique la dirección IP del servidor proxy.|
|proxyManualPort|Int32|Especifique el puerto del servidor proxy.|
|proxyAutomaticConfigurationUrl|String|Especifique la dirección URL de la secuencia de comandos de configuración de servidor proxy.|
|forceFIPSCompliance|Boolean|Especifique si debe forzarse la compatibilidad con FIPS.|

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

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsWifiConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsWifiConfiguration",
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
  "forceFIPSCompliance": true
}
```





