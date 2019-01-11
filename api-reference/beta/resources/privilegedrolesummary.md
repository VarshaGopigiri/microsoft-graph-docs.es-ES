---
title: tipo de recurso privilegedRoleSummary
description: Las estadísticas de resumen para un rol determinado.
localization_priority: Normal
ms.openlocfilehash: b74b562a992f7795f3ae8e317608f1e370bc2a4e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858621"
---
# <a name="privilegedrolesummary-resource-type"></a>tipo de recurso privilegedRoleSummary

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Las estadísticas de resumen para un rol determinado.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener privilegedRoleSummary](../api/privilegedrolesummary-get.md) | [privilegedRoleSummary](privilegedrolesummary.md) |Leer las propiedades y las relaciones del objeto privilegedRoleSummary.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|elevatedCount|int32|El número de usuarios que tienen el rol asignado y la función está activado.|
|id|string| El identificador único para el rol. Solo lectura.|
|managedCount|int32|El número de usuarios que tienen el rol asignado, pero la función se desactiva.|
|mfaEnabled|boolean|**true** si la activación de la función requiere MFA. **false** si la activación de la función no requiere MFA.|
|status|string| Los valores posibles son: `ok` y `bad`. El valor depende de la relación entre (managedCount / usersCount). Si la proporción es menor que un umbral predefinido, `ok` se devuelve. De lo contrario, `bad` se devuelve.|
|usersCount|int32|El número de usuarios que están asignados a la función.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedRoleSummary"
}-->

```json
{
  "elevatedCount": 1024,
  "id": "string (identifier)",
  "managedCount": 1024,
  "mfaEnabled": true,
  "status": "string",
  "usersCount": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRoleSummary resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
