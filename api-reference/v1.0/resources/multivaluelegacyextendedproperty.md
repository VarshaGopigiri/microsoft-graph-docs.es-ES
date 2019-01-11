---
title: Tipo de recurso multiValueLegacyExtendedProperty
description: Propiedad extendida que contiene una colección de valores.
localization_priority: Normal
ms.openlocfilehash: 87823559bad3e149ef3c4d4d6f21f43cf66c41fa
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27827037"
---
# <a name="multivaluelegacyextendedproperty-resource-type"></a>Tipo de recurso multiValueLegacyExtendedProperty

Propiedad extendida que contiene una colección de valores.

Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Post](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | Instancia de recurso admitida: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md) o [contactFolder](../resources/contactfolder.md). Tenga en cuenta que no se admite [post](../resources/post.md) de grupo. | Crea una **multiValueLegacyExtendedProperty** en una instancia nueva o existente de un recurso compatible. |
|[Get](../api/multivaluelegacyextendedproperty-get.md) |Instancia de recurso admitida ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md) o [post](../resources/post.md) de grupo) expandida con un objeto [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md). |Obtiene una instancia del recurso con una propiedad extendida mediante `$expand`.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|string|Identificador de la propiedad. Solo lectura.|
|value|colección string|Colección de valores de propiedad.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty"
}-->

```json
{
  "id": "string (identifier)",
  "value": ["string"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "multiValueLegacyExtendedProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
