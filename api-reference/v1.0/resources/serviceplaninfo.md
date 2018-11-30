---
title: Tipo de recurso servicePlanInfo
description: Contiene información sobre un plan de servicio asociado a una SKU suscrita. La propiedad **servicePlans** de la entidad subscribedSku es una colección de **servicePlanInfo**.
ms.openlocfilehash: 70d49eb22542e9bc22ee28df5bc77b3bf6146b6d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030478"
---
# <a name="serviceplaninfo-resource-type"></a>Tipo de recurso servicePlanInfo

Contiene información sobre un plan de servicio asociado a una SKU suscrita. La propiedad **servicePlans** de la entidad [subscribedSku](subscribedsku.md) es una colección de **servicePlanInfo**.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|servicePlanId|Guid|Identificador único del plan de servicio.|
|servicePlanName|String|Nombre del plan de servicio.|
|provisioningStatus|String|El estado de aprovisionamiento del plan de servicio. Valores posibles:<br/>“Success”: el servicio está completamente aprovisionado.<br/>“Disabled”: se deshabilitó el servicio.<br/>“PendingInput”: aún no se aprovisionó el servicio; esperando la confirmación del servicio.<br/>“PendingActivation”: el servicio está aprovisionado, pero necesita una activación explícita por el administrador (por ejemplo, plan de servicio de Intune_O365).<br/>“PendingProvisioning”: Microsoft agregó un nuevo servicio al SKU del producto y aún no se activó en el inquilino.|
|appliesTo|String|El objeto al que se puede asignar el plan de servicio. Valores posibles:<br/>“User”: el plan de servicio se puede asignar a usuarios individuales.<br/>“Company”: el plan de servicio se puede asignar a todo el inquilino.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.servicePlanInfo"
}-->

```json
{
  "appliesTo": "string",
  "provisioningStatus": "string",
  "servicePlanId": "guid",
  "servicePlanName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "servicePlanInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
