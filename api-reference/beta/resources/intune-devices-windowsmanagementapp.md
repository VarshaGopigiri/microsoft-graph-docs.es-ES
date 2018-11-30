---
title: tipo de recurso windowsManagementApp
description: Entidad de aplicación de administración de Windows.
ms.openlocfilehash: b1c5c673e755f87328574113c4a0b0088c033d0f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089899"
---
# <a name="windowsmanagementapp-resource-type"></a>tipo de recurso windowsManagementApp

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Entidad de aplicación de administración de Windows.
## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Obtener windowsManagementApp](../api/intune-devices-windowsmanagementapp-get.md)|[windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md)|Leer las propiedades y las relaciones del objeto [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) .|
|[Actualizar windowsManagementApp](../api/intune-devices-windowsmanagementapp-update.md)|[windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md)|Actualizar las propiedades de un objeto [windowsManagementApp](../resources/intune-devices-windowsmanagementapp.md) .|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|String|Identificador único para la aplicación de administración de Windows|
|availableVersion|String|Versión disponible de Windows management app.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|healthSummary|[windowsManagementAppHealthSummary](../resources/intune-devices-windowsmanagementapphealthsummary.md)|Mantenimiento de resumen para la aplicación de administración de Windows.|
|healthStates|colección de [windowsManagementAppHealthState](../resources/intune-devices-windowsmanagementapphealthstate.md)|La lista de Estados de mantenimiento para la aplicación de administración de Windows instalada.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsManagementApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsManagementApp",
  "id": "String (identifier)",
  "availableVersion": "String"
}
```





