---
title: tipo de recurso androidWiFiConfiguration
description: Proporcionando las configuraciones de este perfil puede indicar el dispositivo Android para conectarse al extremo de Wi-Fi deseado. Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo de Wi-Fi que puede hacer que la conexión Wi-Fi transparente para el usuario final. Este perfil proporciona los tipos de seguridad limitado y más sencillo que el perfil de empresa Wi-Fi.
author: tfitzmac
ms.openlocfilehash: a243bbd6e8fe132291b514c77ff85d820b824b92
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350410"
---
# <a name="androidwificonfiguration-resource-type"></a>tipo de recurso androidWiFiConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Proporcionando las configuraciones de este perfil puede indicar el dispositivo Android para conectarse al extremo de Wi-Fi deseado. Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo de Wi-Fi que puede hacer que la conexión Wi-Fi transparente para el usuario final. Este perfil proporciona los tipos de seguridad limitado y más sencillo que el perfil de empresa Wi-Fi.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista androidWiFiConfigurations](../api/intune-deviceconfig-androidwificonfiguration-list.md)|colección de [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md)|Propiedades de la lista y relaciones de los objetos [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md) .|
|[Obtener androidWiFiConfiguration](../api/intune-deviceconfig-androidwificonfiguration-get.md)|[androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md)|Leer las propiedades y las relaciones del objeto [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md) .|
|[Crear androidWiFiConfiguration](../api/intune-deviceconfig-androidwificonfiguration-create.md)|[androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md)|Crear un nuevo objeto [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md) .|
|[Eliminar androidWiFiConfiguration](../api/intune-deviceconfig-androidwificonfiguration-delete.md)|Ninguno|Elimina un [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md).|
|[Actualizar androidWiFiConfiguration](../api/intune-deviceconfig-androidwificonfiguration-update.md)|[androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md)|Actualizar las propiedades de un objeto [androidWiFiConfiguration](../resources/intune-deviceconfig-androidwificonfiguration.md) .|

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
|networkName|String|Nombre de red|
|SSID|String|Esto es el nombre de la red Wi-Fi que se difunde a todos los dispositivos.|
|connectAutomatically|Boolean|Conectar automáticamente cuando esta red esté en el intervalo. Si se establece en true omitirá el símbolo del sistema del usuario y el dispositivo se conecte automáticamente a la red Wi-Fi.|
|connectWhenNetworkNameIsHidden|Boolean|Cuando se establece en true, este perfil fuerza el dispositivo para conectarse a una red que no difundir su SSID para todos los dispositivos.|
|wiFiSecurityType|[androidWiFiSecurityType](../resources/intune-deviceconfig-androidwifisecuritytype.md)|Indica si el extremo de Wi-Fi utiliza un tipo de EAP en función de seguridad. Los valores posibles son: `open` y `wpaEnterprise`.|

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
  "@odata.type": "microsoft.graph.androidWiFiConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidWiFiConfiguration",
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
  "wiFiSecurityType": "String"
}
```





