---
title: Tipo de recurso windowsPhone81CustomConfiguration
description: Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso windowsPhone81CustomConfiguration.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 47c371e6b3eb978c7a829e3b14a41515a4ac354e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952366"
---
# <a name="windowsphone81customconfiguration-resource-type"></a>Tipo de recurso windowsPhone81CustomConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso windowsPhone81CustomConfiguration.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windowsPhone81CustomConfigurations](../api/intune-deviceconfig-windowsphone81customconfiguration-list.md)|Colección [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md).|
|[Obtener windowsPhone81CustomConfiguration](../api/intune-deviceconfig-windowsphone81customconfiguration-get.md)|[windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md)|Lea las propiedades y las relaciones del objeto [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md).|
|[Crear windowsPhone81CustomConfiguration](../api/intune-deviceconfig-windowsphone81customconfiguration-create.md)|[windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md)|Cree un objeto [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md).|
|[Eliminar windowsPhone81CustomConfiguration](../api/intune-deviceconfig-windowsphone81customconfiguration-delete.md)|Ninguna|Elimina un [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md).|
|[Actualizar windowsPhone81CustomConfiguration](../api/intune-deviceconfig-windowsphone81customconfiguration-update.md)|[windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md)|Actualice las propiedades de un objeto [windowsPhone81CustomConfiguration](../resources/intune-deviceconfig-windowsphone81customconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|omaSettings|Colección [omaSetting](../resources/intune-deviceconfig-omasetting.md)|Configuración de OMA. Esta colección puede contener un máximo de 1000 elementos.|

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
  "@odata.type": "microsoft.graph.windowsPhone81CustomConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsPhone81CustomConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "omaSettings": [
    {
      "@odata.type": "microsoft.graph.omaSetting",
      "displayName": "String",
      "description": "String",
      "omaUri": "String",
      "value": 1024
    }
  ]
}
```



