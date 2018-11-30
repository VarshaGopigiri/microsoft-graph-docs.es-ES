---
title: tipo de recurso deviceAndAppManagementAssignedRoleIds
description: Todavía no documentado
ms.openlocfilehash: 9d9fbf9bc6dcfa422316a236dfd890369d069c2f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087476"
---
# <a name="deviceandappmanagementassignedroleids-resource-type"></a>tipo de recurso deviceAndAppManagementAssignedRoleIds

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Todavía no documentado
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
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





