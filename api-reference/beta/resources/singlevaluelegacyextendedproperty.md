---
title: Tipo de recurso singleValueLegacyExtendedProperty
description: 'Propiedad extendida que contiene un solo valor. '
localization_priority: Normal
ms.openlocfilehash: 51a42661ea3a19ea8e82ba78115bfa5290d99d15
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27857417"
---
# <a name="singlevaluelegacyextendedproperty-resource-type"></a>Tipo de recurso singleValueLegacyExtendedProperty

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Propiedad extendida que contiene un solo valor. 

Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas. 


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Post](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) | Una instancia de recursos admitidos: [mensaje](../resources/message.md), [mailFolder](../resources/mailfolder.md), [eventos](../resources/event.md), [calendario](../resources/calendar.md), [póngase en contacto con](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [tarea de Outlook](../resources/outlooktask.md), o [carpeta de tareas de Outlook](../resources/outlooktaskfolder.md), pero no grupo [registrar](../resources/post.md). | Crea una **singleValueLegacyExtendedProperty** en una instancia nueva o existente de un recurso compatible. |
|[Get](../api/singlevaluelegacyextendedproperty-get.md) |Uno o una colección de recursos admitidos instancia ([mensaje](../resources/message.md), [mailFolder](../resources/mailfolder.md), [eventos](../resources/event.md), [calendario](../resources/calendar.md), [póngase en contacto con](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [tarea de Outlook](../resources/outlooktask.md), [carpeta de tareas de Outlook](../resources/outlooktaskfolder.md)o grupo [registrar](../resources/post.md)), o bien, una instancia de este tipo expandido con un objeto [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) . |Obtiene una instancia del recurso con una propiedad extendida mediante `$expand` o `$filter`.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|string|Identificador de la propiedad. Solo lectura.|
|value|string|Valor de la propiedad.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.singleValueLegacyExtendedProperty"
}-->

```json
{
  "id": "string (identifier)",
  "value": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "singleValueLegacyExtendedProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
