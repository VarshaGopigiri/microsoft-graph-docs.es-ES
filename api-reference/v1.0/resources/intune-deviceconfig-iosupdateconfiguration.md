---
title: Tipo de recurso iosUpdateConfiguration
description: Configuración de actualización de iOS, le permite configurar el intervalo de horas de la semana para instalar actualizaciones de iOS
ms.openlocfilehash: 9c04f0a5866fcbbb62397e0d4e8e04d038648484
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032726"
---
# <a name="iosupdateconfiguration-resource-type"></a>Tipo de recurso iosUpdateConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de actualización de iOS, le permite configurar el intervalo de horas de la semana para instalar actualizaciones de iOS

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[iosUpdateConfigurations](../api/intune-deviceconfig-iosupdateconfiguration-list.md)|Colección [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md).|
|[Obtener iosUpdateConfiguration](../api/intune-deviceconfig-iosupdateconfiguration-get.md)|[iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md)|Lea las propiedades y las relaciones del objeto [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md).|
|[Crear iosUpdateConfiguration](../api/intune-deviceconfig-iosupdateconfiguration-create.md)|[iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md)|Cree un objeto [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md).|
|[Eliminar iosUpdateConfiguration](../api/intune-deviceconfig-iosupdateconfiguration-delete.md)|Ninguna|Elimina un [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md).|
|[Actualizar iosUpdateConfiguration](../api/intune-deviceconfig-iosupdateconfiguration-update.md)|[iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md)|Actualice las propiedades de un objeto [iosUpdateConfiguration](../resources/intune-deviceconfig-iosupdateconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|activeHoursStart|TimeOfDay|Inicio de horas activas (las horas activas son el intervalo de tiempo en que no se deberían instalar actualizaciones)|
|activeHoursEnd|TimeOfDay|Fin de horas activas (las horas activas son el intervalo de tiempo en que no se deberían instalar actualizaciones)|
|scheduledInstallDays|colección de [dayOfWeek](../resources/intune-deviceconfig-dayofweek.md)|Días de la semana para los que se configuran las horas activas. Esta colección puede contener un máximo de 7 elementos.|
|utcTimeOffsetInMinutes|Int32|Diferencia horaria UTC indicada en minutos|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
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
  "@odata.type": "microsoft.graph.iosUpdateConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iosUpdateConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "activeHoursStart": "String (time of day)",
  "activeHoursEnd": "String (time of day)",
  "scheduledInstallDays": [
    "String"
  ],
  "utcTimeOffsetInMinutes": 1024
}
```



<!-- {
  "type": "#page.annotation",
  "suppressions": [
     "Warning: /api-reference/v1.0/resources/intune-deviceconfig-iosupdateconfiguration.md/microsoft.graph.iosUpdateConfiguration/scheduledInstallDays:
      Inconsistent types between parameter (String) and table (Object)"
  ],
}
-->
