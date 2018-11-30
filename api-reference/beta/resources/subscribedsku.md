---
title: Tipo de recurso subscribedSku
description: " crear, update y delete no son compatibles. No se admiten expresiones de filtro de consulta. Se hereda de directoryObject."
ms.openlocfilehash: ab9b64d8de67379aa002ffeec78edd327b15b222
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089769"
---
# <a name="subscribedsku-resource-type"></a>Tipo de recurso subscribedSku

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Solo se admite la operación de lectura con las SKU suscritas; no se admiten las operaciones de creación, actualización y eliminación. No se admiten expresiones de filtro de consulta. Se hereda de [DirectoryObject](directoryobject.md).


## <a name="methods"></a>Métodos
| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Get subscribedSku](../api/subscribedsku-get.md) | [subscribedSku](subscribedsku.md) |Lea las propiedades y relaciones del objeto subscribedSku.|
|[Lista subscribedsku](../api/subscribedsku-list.md) | Colección [subscribedSku](subscribedsku.md) |Recupere la lista de suscripciones comerciales que ha adquirido una organización.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|appliesTo|String| Por ejemplo, "usuario" o "empresa". |
|capabilityStatus|String| Por ejemplo, "habilitado". |
|consumedUnits|Int32| El número de licencias asignadas. |
|id|String| El identificador único del recurso del objeto sku suscrito. Clave, no admite valores NULL. |
|prepaidUnits|[licenseUnitsDetail](licenseunitsdetail.md)| Información sobre el número y el estado de las licencias prepagadas. |
|servicePlans|Colección [servicePlanInfo](serviceplaninfo.md)| Información acerca de los planes de servicio que están disponibles con el SKU. No admite valores NULL |
|skuId|Guid| El identificador único (GUID) para el SKU de servicio. |
|skuPartNumber|String| La parte numérica del SKU, por ejemplo: "AAD_PREMIUM" o "RMSBASIC". |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.subscribedSku"
}-->

```json
{
  "appliesTo": "string",
  "capabilityStatus": "string",
  "consumedUnits": 1024,
  "id": "string (identifier)",
  "prepaidUnits": {"@odata.type": "microsoft.graph.licenseUnitsDetail"},
  "servicePlans": [{"@odata.type": "microsoft.graph.servicePlanInfo"}],
  "skuId": "guid",
  "skuPartNumber": "string"
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscribedSku resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
