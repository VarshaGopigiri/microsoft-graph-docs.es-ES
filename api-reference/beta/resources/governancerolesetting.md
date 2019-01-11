---
title: tipo de recurso governanceRoleSetting
description: " regla y así sucesivamente."
localization_priority: Normal
ms.openlocfilehash: d63685ae1a4383ce7ab245dda0fd7d1207c57f88
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805890"
---
# <a name="governancerolesetting-resource-type"></a>tipo de recurso governanceRoleSetting

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa un conjunto de configuraciones en cada definición de roles que necesite se evalúa cuando se cree o modifique las asignaciones de roles. Por ejemplo, la configuración de las funciones puede incluir regla de "asignación máxima duración", "MFA necesarios en activación" regla y así sucesivamente.

## <a name="methods"></a>Métodos

| Método          | Tipo de valor devuelto |Descripción|
|:---------------|:--------|:--------|
|[List](../api/governancerolesetting-list.md) | colección de [governanceRoleSetting](../resources/governancerolesetting.md)|Una colección de configuración de las funciones en un recurso de la lista.|
|[Get](../api/governancerolesetting-get.md) |  [governanceRoleSetting](../resources/governancerolesetting.md) |Leer las propiedades y las relaciones de una configuración de rol.|
|[Update](../api/governancerolesetting-update.md) | [governanceRoleSetting](../resources/governancerolesetting.md)  |Actualizar un objeto de configuración de rol. |

## <a name="properties"></a>Propiedades
|Propiedad               |Tipo                                      |Descripción|
|:--------------------|:---------------------------------------|:----------|
|id                   |Cadena                                  |El identificador de la roleSetting.|
|resourceId           |Cadena                                  |Necesario. El identificador del recurso que está asociada la configuración de rol.|
|roleDefinitionId     |Cadena                                  |Necesario. El identificador de la definición de roles que está asociada la configuración de rol.|
|isDefault            |Booleano                                 |Solo lectura. Indicar si la roleSetting es un roleSetting predeterminada|
|lastUpdatedDateTime  |DateTimeOffset                          |Solo lectura. El tiempo que se actualizaron por última vez la configuración de rol. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|lastUpdatedBy        |Cadena                                  |Solo lectura. El nombre para mostrar del administrador que actualizó por última vez el roleSetting.|
|adminEligibleSettings|colección de [governanceRuleSetting](../resources/governancerulesetting.md)|La configuración de la regla que se evalúa cuando un administrador intenta agregar una asignación de rol aptos.|
|adminMemberSettings  |colección de [governanceRuleSetting](../resources/governancerulesetting.md)|La configuración de la regla que se evalúa cuando un administrador intenta agregar una asignación de rol miembro directo.|
|userEligibleSettings |colección de [governanceRuleSetting](../resources/governancerulesetting.md)|La configuración de la regla que se evalúa cuando un usuario intenta agregar una asignación de rol optan. No se admite la configuración por ahora.|
|userMemberSettings   |colección de [governanceRuleSetting](../resources/governancerulesetting.md)|La configuración de la regla que se evalúa cuando un usuario intenta activar su asignación de roles.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|resource|[governanceResource](../resources/governanceresource.md)|Solo lectura. El recurso asociado para esta configuración de rol.|
|roleDefinition|[governanceRoleDefinition](../resources/governanceroledefinition.md)|Solo lectura. La definición de roles que se aplica con esta configuración de rol. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.governanceRoleSetting"
}-->

```json
{
  "id": "String (identifier)",
  "resourceId": "String",
  "roleDefinitionId": "String",
  "isDefault": true,
  "lastUpdatedDateTime": "String (timestamp)",
  "lastUpdatedBy": "String",
  "adminEligibleSettings": [{"@odata.type": "microsoft.graph.governanceRuleSetting"}],
  "adminMemberSettings": [{"@odata.type": "microsoft.graph.governanceRuleSetting"}],
  "userEligibleSettings": [{"@odata.type": "microsoft.graph.governanceRuleSetting"}],
  "userMemberSettings": [{"@odata.type": "microsoft.graph.governanceRuleSetting"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "governanceRoleSetting",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
