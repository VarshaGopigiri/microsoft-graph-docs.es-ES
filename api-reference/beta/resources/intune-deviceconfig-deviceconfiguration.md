---
title: Tipo de recurso deviceConfiguration
description: Configuración de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 497d382b5b4b1a16c67144883be2b3d82362c4d4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957595"
---
# <a name="deviceconfiguration-resource-type"></a>Tipo de recurso deviceConfiguration

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Configuración de dispositivos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar deviceConfigurations](../api/intune-deviceconfig-deviceconfiguration-list.md)|Colección [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|[Obtener deviceConfiguration](../api/intune-deviceconfig-deviceconfiguration-get.md)|[deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|Lea las propiedades y las relaciones del objeto [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).|
|[Acción assign](../api/intune-deviceconfig-deviceconfiguration-assign.md)|Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|Todavía no documentado|
|[acción windowsPrivacyAccessControls](../api/intune-deviceconfig-deviceconfiguration-windowsprivacyaccesscontrols.md)|Ninguno|Todavía no documentado|
|[acción assignedAccessMultiModeProfiles](../api/intune-deviceconfig-deviceconfiguration-assignedaccessmultimodeprofiles.md)|Ninguno|Todavía no documentado|
|[acción getTargetedUsersAndDevices](../api/intune-deviceconfig-deviceconfiguration-gettargetedusersanddevices.md)|colección de [deviceConfigurationTargetedUserAndDevice](../resources/intune-deviceconfig-deviceconfigurationtargeteduseranddevice.md)|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Clave de la entidad.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|roleScopeTagIds|Colección String|Lista de etiquetas de ámbito para esta instancia de entidad.|
|supportsScopeTags|Booleano|Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito. No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito. Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure. Esta propiedad es de sólo lectura.|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto.|
|descripción|String|Descripción proporcionada por el administrador de la configuración del dispositivo.|
|displayName|String|Nombre proporcionado por el administrador de la configuración del dispositivo.|
|versión|Int32|Versión de la configuración del dispositivo.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|groupAssignments|colección de [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)|La lista de asignaciones de grupo para el perfil de configuración del dispositivo.|
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
  "roleScopeTagIds": [
    "String"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024
}
```





