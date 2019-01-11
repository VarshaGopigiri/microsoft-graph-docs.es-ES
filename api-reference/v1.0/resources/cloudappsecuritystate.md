---
title: tipo de recurso cloudAppSecurityState
description: Contiene información de estado acerca de la aplicación en la nube (destinationServiceName, destinationServiceIp).
localization_priority: Normal
ms.openlocfilehash: ff76adf1d3879c3dac3f19ae122d82c9523d5193
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876807"
---
# <a name="cloudappsecuritystate-resource-type"></a>tipo de recurso cloudAppSecurityState

Contiene información de estado acerca de la aplicación en la nube (destinationServiceName, destinationServiceIp).

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo        | Description |
|:-------------|:------------|:------------|
|destinationServiceIp|Cadena|Dirección IP de destino de la conexión a la aplicación o servicio de nube.|
|destinationServiceName|Cadena|Nombre de aplicación o servicio de nube (por ejemplo "Fuerza de ventas", "Lista desplegable", etcetera).|
|riskScore|Cadena|Puntuación de proveedor generado/calculada en el riesgo de la aplicación o servicio de nube. Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.|

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
