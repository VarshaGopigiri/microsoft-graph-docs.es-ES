---
title: tipo de recurso windowsManagementAppHealthState
description: Entidad de estado de mantenimiento de aplicación de Windows management.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 23381aed47ade8f42937f6bc48cfff33b36d1fa7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875302"
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
|id|Cadena|Identificador único para el estado de mantenimiento de aplicación de administración de Windows|
|healthState|[healthState](../resources/intune-devices-healthstate.md)|Estado de mantenimiento de aplicación de administración de Windows. Los valores posibles son: `unknown`, `healthy` y `unhealthy`.|
|installedVersion|Cadena|La versión instalada de aplicación de administración de Windows.|
|lastCheckInDateTime|DateTimeOffset|Aplicación de administración de Windows última hora de protección.|
|deviceName|Cadena|Nombre del dispositivo con Windows está instalada la aplicación de administración.|
|deviceOSVersion|Cadena|Versión de sistema operativo de Windows 10 del dispositivo con Windows está instalada la aplicación de administración.|

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





