---
title: Tipo de recurso del usuario
description: Representa un objeto de usuario de Azure Active Directory.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8a2cf2ee8798a02eeea7be3b1c7493c6b1b1ddb6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27827471"
---
# <a name="user-resource-type"></a>Tipo de recurso del usuario

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Representa un objeto de usuario de Azure Active Directory.

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Los usuarios de la lista](../api/intune-shared-user-list.md) de objetos.|Colección [user](../resources/intune-shared-user.md)|Enumere las propiedades y las relaciones de los objetos [user](../resources/intune-shared-user.md).|
|Objeto [obtener el usuario](../api/intune-shared-user-get.md) .|Colección [user](../resources/intune-shared-user.md)|Lea las propiedades y las relaciones del objeto [user](../resources/intune-shared-user.md).|
|Objeto de [usuario de crear](../api/intune-shared-user-create.md) .|Colección [user](../resources/intune-shared-user.md)|Cree un objeto [user](../resources/intune-shared-user.md).|
|[Eliminar el usuario](../api/intune-shared-user-delete.md).|Ninguna|Elimina un [user](../resources/intune-shared-user.md).|
|Objeto de [usuario de actualización](../api/intune-shared-user-update.md) .|[user](../resources/intune-shared-user.md)|Actualice las propiedades de un objeto [user](../resources/intune-shared-user.md).|
|**Administración de dispositivos**|
|[Acción removeAllDevicesFromManagement](../api/intune-shared-user-removealldevicesfrommanagement.md)|Ninguna|Retirar todos los dispositivos de la administración para este usuario|
|**Administración de aplicaciones móviles (MAM)**|
|[Función getManagedAppDiagnosticStatuses](../api/intune-shared-user-getmanagedappdiagnosticstatuses.md)|Colección [getManagedAppDiagnosticStatus](../resources/intune-mam-managedappdiagnosticstatus.md)|Obtiene estados de validación de diagnósticos de un usuario determinado.|
|[Función getManagedAppPolicies](../api/intune-shared-user-getmanagedapppolicies.md)|Colección [managedAppPolicy](../resources/intune-mam-managedapppolicy.md)|Obtiene las restricciones de aplicaciones de un usuario determinado.|
|[Acción wipeManagedAppRegistrationsByDeviceTag](../api/intune-shared-user-wipemanagedappregistrationsbydevicetag.md)|Ninguna|Emite una operación de borrado en un registro de la aplicación con la etiqueta del dispositivo especificado.|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único del usuario.|
|**Incorporación de redes**|
|deviceEnrollmentLimit|Int32|El límite del número máximo de dispositivos que el usuario puede inscribir. Los valores permitidos son 5 o 1000.|


## <a name="relationships"></a>Relaciones
|Relación|Tipo|Description|
|:---|:---|:---|
|**Administración de dispositivos**|
|managedDevices|Colección [managedDevice](../resources/intune-devices-manageddevice.md)|Los dispositivos administrados asociados al usuario.|
|**Administración de aplicaciones móviles (MAM)**|
|managedAppRegistrations|Colección [managedAppRegistration](../resources/intune-mam-managedappregistration.md)|Cero o más registros de administración de aplicaciones administradas que pertenecen al usuario.|
|**Solución de problemas**|
|deviceManagementTroubleshootingEvents|Colección [deviceManagementTroubleshootingEvent](../resources/intune-troubleshooting-devicemanagementtroubleshootingevent.md)|La lista de eventos de solución de problemas para este usuario.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.directoryObject",
  "openType": true,
  "@odata.type": "microsoft.graph.user"
}
--> 
``` json
{
  "@odata.type": "#microsoft.graph.user",
  "id": "String (identifier)",
  "deviceEnrollmentLimit": 5
}
```

<!-- {
  "type": "#page.annotation",
  "suppressions": [
    "Warning: Resource microsoft.graph.user is defined in multiple files: /api-reference/v1.0/resources/intune_shared_user.md, /api-reference/v1.0/resources/user.md",
  ]
}-->
