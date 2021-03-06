---
title: tipo de recurso windowsManagementAppHealthState
description: Entidad de estado de mantenimiento de aplicación de Windows management.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 8cf679cf1a5ac86c47354db2fc9f800647d309c1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976474"
---
# <a name="windowsmanagementapphealthstate-resource-type"></a>tipo de recurso windowsManagementAppHealthState

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad de estado de mantenimiento de aplicación de Windows management.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Lista windowsManagementAppHealthStates](../api/intune-devices-windowsmanagementapphealthstate-list.md)|colección de [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md)|Propiedades de la lista y relaciones de los objetos [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) .|
|[Obtener windowsManagementAppHealthState](../api/intune-devices-windowsmanagementapphealthstate-get.md)|[windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md)|Leer las propiedades y las relaciones del objeto [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) .|
|[Crear windowsManagementAppHealthState](../api/intune-devices-windowsmanagementapphealthstate-create.md)|[windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md)|Crear un nuevo objeto [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) .|
|[Eliminar windowsManagementAppHealthState](../api/intune-devices-windowsmanagementapphealthstate-delete.md)|Ninguno|Elimina un [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md).|
|[Actualizar windowsManagementAppHealthState](../api/intune-devices-windowsmanagementapphealthstate-update.md)|[windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md)|Actualizar las propiedades de un objeto [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único para el estado de mantenimiento de aplicación de administración de Windows|
|healthState|[healthState](../resources/intune-devices-healthstate.md)|Estado de mantenimiento de aplicación de administración de Windows. Los valores posibles son: `unknown`, `healthy` y `unhealthy`.|
|installedVersion|String|La versión instalada de aplicación de administración de Windows.|
|lastCheckInDateTime|DateTimeOffset|Aplicación de administración de Windows última hora de protección.|
|deviceName|String|Nombre del dispositivo con Windows está instalada la aplicación de administración.|
|deviceOSVersion|String|Versión de sistema operativo de Windows 10 del dispositivo con Windows está instalada la aplicación de administración.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsManagementAppHealthState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsManagementAppHealthState",
  "id": "String (identifier)",
  "healthState": "String",
  "installedVersion": "String",
  "lastCheckInDateTime": "String (timestamp)",
  "deviceName": "String",
  "deviceOSVersion": "String"
}
```





