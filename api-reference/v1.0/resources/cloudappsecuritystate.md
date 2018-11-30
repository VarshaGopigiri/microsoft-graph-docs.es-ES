---
title: tipo de recurso cloudAppSecurityState
description: Contiene información de estado acerca de la aplicación en la nube (destinationServiceName, destinationServiceIp).
ms.openlocfilehash: 915044c3084e3d9a9435d602ecc7ec809d2168f2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032365"
---
# <a name="cloudappsecuritystate-resource-type"></a>tipo de recurso cloudAppSecurityState

Contiene información de estado acerca de la aplicación en la nube (destinationServiceName, destinationServiceIp).

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo        | Descripción |
|:-------------|:------------|:------------|
|destinationServiceIp|String|Dirección IP de destino de la conexión a la aplicación o servicio de nube.|
|destinationServiceName|String|Nombre de aplicación o servicio de nube (por ejemplo "Fuerza de ventas", "Lista desplegable", etcetera).|
|riskScore|String|Puntuación de proveedor generado/calculada en el riesgo de la aplicación o servicio de nube. Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.cloudAppSecurityState"
}-->

```json
{
  "destinationServiceIp": "String",
  "destinationServiceName": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "cloudAppSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->