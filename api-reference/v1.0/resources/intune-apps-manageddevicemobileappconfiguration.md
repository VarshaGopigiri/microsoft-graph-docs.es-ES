---
title: Tipo de recurso managedDeviceMobileAppConfiguration
description: Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8e2ad71a4927f2b0156d085bad54cf59d45f97c8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27811651"
---
# <a name="manageddevicemobileappconfiguration-resource-type"></a>Tipo de recurso managedDeviceMobileAppConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Una clase abstracta para la configuración de aplicaciones móviles para dispositivos inscritos.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedDeviceMobileAppConfigurations](../api/intune-apps-manageddevicemobileappconfiguration-list.md)|Colección [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).|
|[Obtener managedDeviceMobileAppConfiguration](../api/intune-apps-manageddevicemobileappconfiguration-get.md)|[managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md)|Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfiguration](../resources/intune-apps-manageddevicemobileappconfiguration.md).|
|[Acción assign](../api/intune-apps-manageddevicemobileappconfiguration-assign.md)|Ninguno|Todavía no documentado|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad.|
|targetedMobileApps|Colección string|La aplicación asociada.|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto.|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo.|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez.|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo.|
|versión|Int32|Versión de la configuración del dispositivo.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md)|La lista de asignaciones de grupo para la configuración de la aplicación.|
|deviceStatuses|colección de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md)|Lista de ManagedDeviceMobileAppConfigurationDeviceStatus.|
|userStatuses|Colección [managedDeviceMobileAppConfigurationUserStatus](../resources/intune-apps-manageddevicemobileappconfigurationuserstatus.md)|Lista de ManagedDeviceMobileAppConfigurationUserStatus.|
|deviceStatusSummary|[managedDeviceMobileAppConfigurationDeviceSummary](../resources/intune-apps-manageddevicemobileappconfigurationdevicesummary.md)|Resumen del estado del dispositivo de la configuración de aplicaciones|
|userStatusSummary|[managedDeviceMobileAppConfigurationUserSummary](../resources/intune-apps-manageddevicemobileappconfigurationusersummary.md)|Resumen del estado del usuario de la configuración de aplicaciones|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfiguration",
  "id": "String (identifier)",
  "targetedMobileApps": [
    "String"
  ],
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024
}
```



