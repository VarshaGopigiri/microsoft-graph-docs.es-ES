---
title: tipo de recurso de conector
description: Aquí tiene una representación JSON del recurso.
localization_priority: Normal
ms.openlocfilehash: 98fa998a37b01ad64e556b229912932f4d1cfc75
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884626"
---
# <a name="connector-resource-type"></a>tipo de recurso de conector

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

<!-- Not supported items
|[Create connectorGroup](../api/connector-post-memberof.md) |[connectorGroup](connectorgroup.md)| Associate a connector with a new connectorGroup by posting to the memberOf collection.|
|[Update](../api/connector-update.md) | [connector](connector.md)   | Connectors are created when they are registed with the tenant. |
|[Delete](../api/connector-delete.md) | None |Delete connector object. |

-->

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener el conector](../api/connector-get.md) | [conector](connector.md) |Leer las propiedades y las relaciones del objeto de conector.|
|[Enumerar memberOf](../api/connector-list-memberof.md) |colección de [connectorGroup](connectorgroup.md)| Obtenga el objeto connectorGroup asociado con el conector.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|externalIp|Cadena|La dirección IP externa como detectados por el servicio para la máquina de conector. Solo lectura|
|id|Cadena| El identificador del objeto del conector. <BR>Solo lectura.|
|nombreEquipo|Cadena| El nombre de la máquina que se está ejecutando el conector. <BR>Solo lectura|
|status|string| Indica el estado del conector. Los valores posibles son: `active` y `inactive`. Solo lectura |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Description|
|:---------------|:--------|:----------|
|memberOf|colección de [connectorGroup](connectorgroup.md)| El connectorGroup que la conexión es un miembro de.<br>Solo lectura. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.connector"
}-->

```json
{
  "externalIp": "String",
  "id": "String (identifier)",
  "machineName": "String",
  "status": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "connector resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
