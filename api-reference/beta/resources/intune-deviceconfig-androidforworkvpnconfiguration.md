---
title: tipo de recurso androidForWorkVpnConfiguration
description: Proporcionando las configuraciones de este perfil puede indicar a los dispositivos Android para conectarse al extremo VPN que desee. Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo VPN que puede realizar la conexión VPN transparente para el usuario final.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7447e090e4ea9a85f4baeb24bf1f97d2a3d824fd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912264"
---
# <a name="androidforworkvpnconfiguration-resource-type"></a>tipo de recurso androidForWorkVpnConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Proporcionando las configuraciones de este perfil puede indicar a los dispositivos Android para conectarse al extremo VPN que desee. Mediante la especificación de los tipos de seguridad y el método de autenticación esperen por el extremo VPN que puede realizar la conexión VPN transparente para el usuario final.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista androidForWorkVpnConfigurations](../api/intune-deviceconfig-androidforworkvpnconfiguration-list.md)|colección de [androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md)|Propiedades de la lista y relaciones de los objetos [androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md) .|
|[Obtener androidForWorkVpnConfiguration](../api/intune-deviceconfig-androidforworkvpnconfiguration-get.md)|[androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md)|Leer las propiedades y las relaciones del objeto [androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md) .|
|[Crear androidForWorkVpnConfiguration](../api/intune-deviceconfig-androidforworkvpnconfiguration-create.md)|[androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md)|Crear un nuevo objeto [androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md) .|
|[Eliminar androidForWorkVpnConfiguration](../api/intune-deviceconfig-androidforworkvpnconfiguration-delete.md)|Ninguno|Elimina un [androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md).|
|[Actualizar androidForWorkVpnConfiguration](../api/intune-deviceconfig-androidforworkvpnconfiguration-update.md)|[androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md)|Actualizar las propiedades de un objeto [androidForWorkVpnConfiguration](../resources/intune-deviceconfig-androidforworkvpnconfiguration.md) .|

## <a name="properties"></a>Propiedades
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
|connectionName|Cadena|Nombre de la conexión que se muestra al usuario.|
|connectionType|[androidForWorkVpnConnectionType](../resources/intune-deviceconfig-androidforworkvpnconnectiontype.md)|Tipo de conexión. Los valores posibles son: `ciscoAnyConnect`, `pulseSecure`, `f5EdgeClient`, `dellSonicWallMobileConnect`, `checkPointCapsuleVpn`, `citrix`.|
|role|Cadena|Función de tipo de conexión se establece en impulsos seguro.|
|dominio kerberos|Cadena|Dominio Kerberos cuando se establece el tipo de conexión a impulsos seguro.|
|servidores|colección de [servidor de VPN](../resources/intune-deviceconfig-vpnserver.md)|Lista de servidores VPN en la red. Asegúrese de que los usuarios finales pueden tener acceso a estas ubicaciones de red. Esta colección puede contener un máximo de 500 elementos.|
|huella digital|Cadena|Huella es una cadena que se usará para comprobar el servidor VPN puede ser de confianza, que sólo es aplicable al tipo de conexión es VPN Check Point con cápsula.|
|customData|colección [keyValue](../resources/intune-deviceconfig-keyvalue.md)|Datos personalizados al tipo de conexión se establece en Citrix. Esta colección puede contener un máximo de 25 elementos.|
|customKeyValueData|Colección [keyValuePair](../resources/intune-shared-keyvaluepair.md)|Datos personalizados al tipo de conexión se establece en Citrix. Esta colección puede contener un máximo de 25 elementos.|
|authenticationMethod|[vpnAuthenticationMethod](../resources/intune-deviceconfig-vpnauthenticationmethod.md)|Método de autenticación. Los valores posibles son: `certificate` y `usernameAndPassword`.|

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
|identityCertificate|[androidForWorkCertificateProfileBase](../resources/intune-deviceconfig-androidforworkcertificateprofilebase.md)|Certificado de identidad para la autenticación de cliente al método de autenticación es el certificado.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.androidForWorkVpnConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.androidForWorkVpnConfiguration",
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
  "role": "String",
  "realm": "String",
  "servers": [
    {
      "@odata.type": "microsoft.graph.vpnServer",
      "description": "String",
      "address": "String",
      "isDefaultServer": true
    }
  ],
  "fingerprint": "String",
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
  "authenticationMethod": "String"
}
```





