---
title: Tipo de recurso inferenceClassificationOverride
description: Representa el reemplazo de un usuario sobre cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado.
ms.openlocfilehash: 3f3f07e870a4ba549062197a380633ab591c54fe
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030409"
---
# <a name="inferenceclassificationoverride-resource-type"></a>Tipo de recurso inferenceClassificationOverride

Representa el reemplazo de un usuario sobre cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Update](../api/inferenceclassificationoverride-update.md) | [inferenceClassificationOverride](inferenceclassificationoverride.md) |Cambie el campo **ClassifyAs** de una invalidación tal como se especifica. |
|[Delete](../api/inferenceclassificationoverride-delete.md) | None |Elimina un reemplazo especificado por su identificador. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|classifyAs|inferenceClassificationType| Especifica cómo los mensajes entrantes de una determinada siempre debe clasificarse como remitente. Los valores posibles son: `focused`, `other`.|
|id|string| Identificador único del reemplazo. Solo lectura.|
|senderEmailAddress|[emailAddress](emailaddress.md)|Información de la dirección de correo del remitente para el que se creó el reemplazo.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.inferenceClassificationOverride"
}-->

```json
{
  "classifyAs": "string",
  "id": "string (identifier)",
  "senderEmailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "inferenceClassificationOverride resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->