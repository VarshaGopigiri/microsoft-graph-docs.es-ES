---
title: Tipo de recurso deviceConfiguration
description: Configuración de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1a508a037dbd1271d30a226d9cf62fb0683b53af
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953150"
---
# <a name="deviceconfiguration-resource-type"></a>Tipo de recurso deviceConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceConfigurations](../api/intune-deviceconfig-deviceconfiguration-list.md)|Colección [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|[Obtener deviceConfiguration](../api/intune-deviceconfig-deviceconfiguration-get.md)|[deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|Lea las propiedades y las relaciones del objeto [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|[Acción assign](../api/intune-deviceconfig-deviceconfiguration-assign.md)|Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto.|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo.|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo.|
|versión|Int32|Versión de la configuración del dispositivo.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|La lista de tareas para el perfil de configuración del dispositivo.|
|deviceStatuses|Colección [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Estado de instalación de configuración del dispositivo por dispositivo.|
|userStatuses|Colección [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|Estado de instalación de configuración de dispositivo por usuario.|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|Información general del estado del dispositivo sobre la configuración de dispositivos|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|Información general del estado de los usuarios sobre la configuración de dispositivos|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Resumen de dispositivo del estado de configuración de la configuración de dispositivos|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024
}
```



