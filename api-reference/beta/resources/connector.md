---
title: tipo de recurso de conector
description: Aquí tiene una representación JSON del recurso.
ms.openlocfilehash: 6d4cb7e5ca1a5384dbb6c8be92e7ce4eb107388a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089600"
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
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|externalIp|String|La dirección IP externa como detectados por el servicio para la máquina de conector. Solo lectura|
|id|String| El identificador del objeto del conector. <BR>Solo lectura.|
|nombreEquipo|String| El nombre de la máquina que se está ejecutando el conector. <BR>Solo lectura|
|status|string| Indica el estado del conector. Los valores posibles son: `active` y `inactive`. Solo lectura |

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
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
