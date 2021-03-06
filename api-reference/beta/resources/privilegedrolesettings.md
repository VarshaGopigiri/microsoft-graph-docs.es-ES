---
title: tipo de recurso privilegedRoleSettings
description: Representa la configuración de un rol con privilegios.
localization_priority: Normal
ms.openlocfilehash: 971c48ce3ecdd2a219a111f3a11884377e20430c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842745"
---
# <a name="privilegedrolesettings-resource-type"></a>tipo de recurso privilegedRoleSettings

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa la configuración de un rol con privilegios.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener privilegedRoleSettings](../api/privilegedrolesettings-get.md) | [privilegedRoleSettings](privilegedrolesettings.md) |Leer las propiedades y las relaciones del objeto privilegedRoleSettings.|
|[Actualizar privilegedRoleSettings](../api/privilegedrolesettings-update.md) | [privilegedRoleSettings](privilegedrolesettings.md) |Actualizar el objeto privilegedRoleSettings.|
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|elevationDuration|duration|La duración cuando se activa la función.|
|id|string| El identificador único para la configuración de las funciones. Solo lectura.|
|isMfaOnElevationConfigurable|boolean|**true** si mfaOnElevation es configurable. **false** si no se puede configurar mfaOnElevation.|
|lastGlobalAdmin|boolean|Internal que sólo se utiliza.|
|maxElavationDuration|duration|Duración máxima de la función activada.|
|mfaOnElevation|boolean|**true** si MFA se requiere para activar la función. **false** si no es necesario MFA para activar la función.|
|minElevationDuration|duration|Duración mínima de la función activada.|
|notificationToUserOnElevation|boolean|**true** si enviar notificación para el usuario final cuando se activa la función. **false** si no enviar notificación cuando se activa la función.|
|ticketingInfoOnElevation|boolean|**true** si se requiere la información mediante vales cuándo activar la función. **false** si la información mediante vales no se requiere cuando se activa la función.|
|approvalOnElevation|boolean|**true** si se requiere la aprobación cuando se activa la función. **false** si la aprobación no se requiere cuando se activa la función.|
|approverIds|matriz|Lista de identificadores de aprobación, si se necesita aprobación para la activación.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedRoleSettings"
}-->

```json
{
  "elevationDuration": "String (timestamp)",
  "id": "string (identifier)",
  "isMfaOnElevationConfigurable": true,
  "lastGlobalAdmin": true,
  "maxElavationDuration": "String (timestamp)",
  "mfaOnElevation": true,
  "minElevationDuration": "String (timestamp)",
  "notificationToUserOnElevation": true,
  "ticketingInfoOnElevation": true,
  "approvalOnElevation": false,
  "approverIds": []
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRoleSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
