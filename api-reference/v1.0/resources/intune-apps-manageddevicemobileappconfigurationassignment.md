---
title: Tipo de recurso managedDeviceMobileAppConfigurationAssignment
description: Contiene las propiedades usadas para asignar una configuración de la aplicación MDM a un grupo.
ms.openlocfilehash: 810d28bfb5ca176bd1ab8c3f3fc0d4f885bf3b56
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032214"
---
# <a name="manageddevicemobileappconfigurationassignment-resource-type"></a>Tipo de recurso managedDeviceMobileAppConfigurationAssignment

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Contiene las propiedades usadas para asignar una configuración de la aplicación MDM a un grupo.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar managedDeviceMobileAppConfigurationAssignments](../api/intune-apps-manageddevicemobileappconfigurationassignment-list.md)|Colección [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md)|Enumere las propiedades y las relaciones de los objetos [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).|
|[Obtener managedDeviceMobileAppConfigurationAssignment](../api/intune-apps-manageddevicemobileappconfigurationassignment-get.md)|[managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md)|Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).|
|[Crear managedDeviceMobileAppConfigurationAssignment](../api/intune-apps-manageddevicemobileappconfigurationassignment-create.md)|[managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md)|Cree un objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).|
|[Eliminar managedDeviceMobileAppConfigurationAssignment](../api/intune-apps-manageddevicemobileappconfigurationassignment-delete.md)|Ninguna|Elimina un [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).|
|[Actualizar managedDeviceMobileAppConfigurationAssignment](../api/intune-apps-manageddevicemobileappconfigurationassignment-update.md)|[managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md)|Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationAssignment](../resources/intune-apps-manageddevicemobileappconfigurationassignment.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único de la entidad.|
|target|[deviceAndAppManagementAssignmentTarget](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|Destino de asignación al que está asignada la directiva de términos y condiciones.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managedDeviceMobileAppConfigurationAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



