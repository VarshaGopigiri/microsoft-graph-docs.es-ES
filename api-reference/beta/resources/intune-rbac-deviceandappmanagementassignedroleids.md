---
title: tipo de recurso deviceAndAppManagementAssignedRoleIds
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1ae87f1a8430ef2539fe10e813390b0fbd68b267
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846343"
---
# <a name="deviceandappmanagementassignedroleids-resource-type"></a>tipo de recurso deviceAndAppManagementAssignedRoleIds

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|roleDefinitionIds|Colección Guid|Identificadores de definición de rol para las definiciones de roles asignados a un usuario específicas.|
|roleAssignmentIds|Colección Guid|Identificadores de asignación de rol para las asignaciones de roles asignados a un usuario específicas.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceAndAppManagementAssignedRoleIds"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementAssignedRoleIds",
  "roleDefinitionIds": [
    "Guid"
  ],
  "roleAssignmentIds": [
    "Guid"
  ]
}
```





