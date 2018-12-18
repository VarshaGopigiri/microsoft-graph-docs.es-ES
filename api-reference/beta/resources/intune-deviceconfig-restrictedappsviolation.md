---
title: tipo de recurso restrictedAppsViolation
description: Infracción de perfil de configuración de aplicaciones restringido por dispositivo por usuario
author: tfitzmac
ms.openlocfilehash: cb614bc56f27281198fcecb73bae2b7beddfa266
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27304938"
---
# <a name="restrictedappsviolation-resource-type"></a>tipo de recurso restrictedAppsViolation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Infracción de perfil de configuración de aplicaciones restringido por dispositivo por usuario
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista restrictedAppsViolations](../api/intune-deviceconfig-restrictedappsviolation-list.md)|colección de [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md)|Propiedades de la lista y relaciones de los objetos [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .|
|[Obtener restrictedAppsViolation](../api/intune-deviceconfig-restrictedappsviolation-get.md)|[restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md)|Leer las propiedades y las relaciones del objeto [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .|
|[Crear restrictedAppsViolation](../api/intune-deviceconfig-restrictedappsviolation-create.md)|[restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md)|Crear un nuevo objeto [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .|
|[Eliminar restrictedAppsViolation](../api/intune-deviceconfig-restrictedappsviolation-delete.md)|Ninguno|Elimina un [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md).|
|[Actualizar restrictedAppsViolation](../api/intune-deviceconfig-restrictedappsviolation-update.md)|[restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md)|Actualizar las propiedades de un objeto [restrictedAppsViolation](../resources/intune-deviceconfig-restrictedappsviolation.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único para el objeto. Creados a partir de accountId, deviceId, Id. de directiva y userId|
|userId|String|Identificador único del usuario, debe ser el Guid|
|userName|String|Nombre de usuario|
|managedDeviceId|String|Identificador único de dispositivos administrados, debe ser el Guid|
|deviceName|String|Nombre de dispositivo|
|deviceConfigurationId|String|Identificador único de dispositivo configuración perfil, debe ser el Guid|
|deviceConfigurationName|String|Nombre del perfil de configuración de dispositivo|
|platformType|[policyPlatformType](../resources/intune-deviceconfig-policyplatformtype.md)|Tipo de plataforma. Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile` y `all`.|
|restrictedAppsState|[restrictedAppsState](../resources/intune-deviceconfig-restrictedappsstate.md)|Estado de aplicaciones restringidos. Los valores posibles son: `prohibitedApps` y `notApprovedApps`.|
|restrictedApps|colección de [managedDeviceReportedApp](../resources/intune-deviceconfig-manageddevicereportedapp.md)|Lista de aplicaciones restringidas infringidas|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.restrictedAppsViolation"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.restrictedAppsViolation",
  "id": "String (identifier)",
  "userId": "String",
  "userName": "String",
  "managedDeviceId": "String",
  "deviceName": "String",
  "deviceConfigurationId": "String",
  "deviceConfigurationName": "String",
  "platformType": "String",
  "restrictedAppsState": "String",
  "restrictedApps": [
    {
      "@odata.type": "microsoft.graph.managedDeviceReportedApp",
      "appId": "String"
    }
  ]
}
```





