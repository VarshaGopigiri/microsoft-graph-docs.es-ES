---
title: Tipo de recurso inferenceClassification
description: 'Clasificación de mensajes de un usuario que permite poner el foco en los que son más relevantes o importantes para el usuario. '
localization_priority: Normal
ms.openlocfilehash: 82d16e24e21231b8ec168eda793257ef780c2219
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877794"
---
# <a name="inferenceclassification-resource-type"></a>Tipo de recurso inferenceClassification

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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
  "@odata.type": "microsoft.graph.inferenceClassification"
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
