---
title: Tipo de recurso multiValueLegacyExtendedProperty
description: Propiedad extendida que contiene una colección de valores.
localization_priority: Normal
ms.openlocfilehash: e98963eea5e1e996170f6330b9b4b333a72ad159
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839455"
---
# <a name="multivaluelegacyextendedproperty-resource-type"></a>Tipo de recurso multiValueLegacyExtendedProperty

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Propiedad extendida que contiene una colección de valores.

Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Post](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | Una instancia de recursos admitidos: [mensaje](../resources/message.md), [mailFolder](../resources/mailfolder.md), [eventos](../resources/event.md), [calendario](../resources/calendar.md), [póngase en contacto con](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [tarea de Outlook](../resources/outlooktask.md)o [carpeta de tareas de Outlook](../resources/outlooktaskfolder.md). Tenga en cuenta que no se admite ese grupo [registrar](../resources/post.md) . | Crea una **multiValueLegacyExtendedProperty** en una instancia nueva o existente de un recurso compatible. |
|[Get](../api/multivaluelegacyextendedproperty-get.md) |Una instancia de recursos admitidos ([mensaje](../resources/message.md), [mailFolder](../resources/mailfolder.md), [eventos](../resources/event.md), [calendario](../resources/calendar.md), [póngase en contacto con](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [tarea de Outlook](../resources/outlooktask.md), [carpeta de tareas de Outlook](../resources/outlooktaskfolder.md)o grupo [registrar](../resources/post.md)) expandido con un [ multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) objeto. |Obtiene una instancia del recurso con una propiedad extendida mediante `$expand`.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|string|Identificador de la propiedad. Solo lectura.|
|value|colección string|Colección de valores de propiedad.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.multivaluelegacyextendedproperty"
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
