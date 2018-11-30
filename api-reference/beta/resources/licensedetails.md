---
title: Tipo de recurso licenseDetails
description: Contiene información sobre una licencia asignada a un usuario.
ms.openlocfilehash: dd56026d2c1d230fe6bb25b78ff8ababa01f577b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090729"
---
# <a name="licensedetails-resource-type"></a>Tipo de recurso licenseDetails

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Contiene información sobre una licencia asignada a un usuario.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Enumerar licenseDetails](../api/user-list-licensedetails.md) | Colección licenseDetails |Recupere una lista de objetos licenseDetails para un usuario.|

<!--|[Get licenseDetails](../api/licensedetails-get.md) | licenseDetails |Read properties and relationships of a licenseDetails object.|-->

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|String| Identificador único del objeto licenseDetails. Solo lectura, no admite valores NULL. |
|servicePlans|Colección [servicePlanInfo](serviceplaninfo.md)| Información sobre los planes de servicio asignados a la licencia. Solo lectura, no admite valores NULL. |
|skuId|Guid| Identificador único (GUID) del SKU de servicio. Es igual a la propiedad skuId en el objeto [SubscribedSku](subscribedsku.md) relacionado. Solo lectura |
|skuPartNumber|Cadena| Nombre para mostrar de SKU único. Es igual al skuPartNumber en el objeto [SubscribedSku](subscribedsku.md) relacionado; por ejemplo: "AAD_Premium". Solo lectura |

## <a name="relationships"></a>Relaciones
Ninguno

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.licenseDetails"
}-->

```json
{
  "id": "String (identifier)",
  "servicePlans": [{"@odata.type": "microsoft.graph.servicePlanInfo"}],
  "skuId": "Guid",
  "skuPartNumber": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "licenseDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->