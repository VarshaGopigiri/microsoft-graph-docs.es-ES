---
title: Tipo de recurso inferenceClassificationOverride
description: Representa el reemplazo de un usuario para cómo los mensajes entrantes de un remitente específico siempre se debe clasificar como
localization_priority: Normal
ms.openlocfilehash: 9124f773a26c9edf1238276c3d0017dcc46e7ad8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876275"
---
# <a name="inferenceclassificationoverride-resource-type"></a>Tipo de recurso inferenceClassificationOverride

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa el reemplazo de un usuario de cómo los mensajes entrantes de un remitente específico siempre deben clasificarse como un [Dirigidos a Bandeja de entrada](manage-focused-inbox.md).


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Update](../api/inferenceclassificationoverride-update.md) | [inferenceClassificationOverride](inferenceclassificationoverride.md) |Cambie el campo **ClassifyAs** de una invalidación tal como se especifica. |
|[Delete](../api/inferenceclassificationoverride-delete.md) | None |Elimina un reemplazo especificado por su identificador. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|classifyAs|string| Especifica cómo se deben clasificar siempre los mensajes entrantes de un remitente determinado. Los valores posibles son: `focused`, `other`.|
|id|string| Identificador único del reemplazo. Solo lectura.|
|senderEmailAddress|[emailAddress](emailaddress.md)|Información de la dirección de correo del remitente para el que se creó el reemplazo.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
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
