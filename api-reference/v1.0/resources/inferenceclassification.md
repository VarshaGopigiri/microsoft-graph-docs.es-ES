---
title: Tipo de recurso inferenceClassification
description: 'Clasificación de mensajes de un usuario que permite poner el foco en los que son más relevantes o importantes para el usuario. '
ms.openlocfilehash: 0fb1e01ad9710a0ff5f2de7f63808a6f3e988c13
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029456"
---
# <a name="inferenceclassification-resource-type"></a>Tipo de recurso inferenceClassification

Clasificación de mensajes de un usuario que permite poner el foco en los que son más relevantes o importantes para el usuario. 

Para obtener más información, consulte [Administrar Bandeja de entrada Prioritarios](manage-focused-inbox.md).


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Create inferenceClassificationOverride](../api/inferenceclassification-post-overrides.md) |[inferenceClassificationOverride](inferenceclassificationoverride.md)| Cree una invalidación para un remitente que se ha identificado mediante una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasificarán sistemáticamente como se especifica en la invalidación.|
|[List overrides](../api/inferenceclassification-list-overrides.md) |Colección [inferenceClassificationOverride](inferenceclassificationoverride.md)| Obtiene los reemplazos que un usuario ha configurado para clasificar siempre los mensajes de determinados remitentes de forma específica.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|string| Solo lectura.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|overrides|Colección [inferenceClassificationOverride](inferenceclassificationoverride.md)| Conjunto de valores de reemplazo de un usuario para clasificar siempre los mensajes de remitentes concretos de determinada manera: `focused`, o `other`. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.inferenceClassification",
  "@odata.annotations": [
    {
      "property": "overrides",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false
      }
    }
  ]
}-->

```json
{
  "id": "string (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "inferenceClassification resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->