---
title: Tipo de recurso singleValueLegacyExtendedProperty
description: 'Propiedad extendida que contiene un solo valor. '
localization_priority: Normal
ms.openlocfilehash: f865da1a8a4211ac99a70881b2851b38b8e72727
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894232"
---
# <a name="singlevaluelegacyextendedproperty-resource-type"></a><span data-ttu-id="802c7-103">Tipo de recurso singleValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="802c7-103">singleValueLegacyExtendedProperty resource type</span></span>

<span data-ttu-id="802c7-104">Propiedad extendida que contiene un solo valor.</span><span class="sxs-lookup"><span data-stu-id="802c7-104">An extended property that contains a single value.</span></span> 

<span data-ttu-id="802c7-105">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="802c7-105">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span> 


## <a name="methods"></a><span data-ttu-id="802c7-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="802c7-106">Methods</span></span>

| <span data-ttu-id="802c7-107">Método</span><span class="sxs-lookup"><span data-stu-id="802c7-107">Method</span></span>           | <span data-ttu-id="802c7-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="802c7-108">Return Type</span></span>    |<span data-ttu-id="802c7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="802c7-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="802c7-110">Post</span><span class="sxs-lookup"><span data-stu-id="802c7-110">Post</span></span>](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) | <span data-ttu-id="802c7-111">Instancia de recurso admitida: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md) o [contactFolder](../resources/contactfolder.md), pero no [post](../resources/post.md) de grupo.</span><span class="sxs-lookup"><span data-stu-id="802c7-111">A supported resource instance: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), or [contactFolder](../resources/contactfolder.md), but not group [post](../resources/post.md).</span></span> | <span data-ttu-id="802c7-112">Crea una **singleValueLegacyExtendedProperty** en una instancia nueva o existente de un recurso compatible.</span><span class="sxs-lookup"><span data-stu-id="802c7-112">Create a **singleValueLegacyExtendedProperty** in a new or existing instance of a supported resource.</span></span> |
|[<span data-ttu-id="802c7-113">Get</span><span class="sxs-lookup"><span data-stu-id="802c7-113">Get</span></span>](../api/singlevaluelegacyextendedproperty-get.md) |<span data-ttu-id="802c7-114">Instancia o colección de instancias de recurso admitidas: ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md) o [post](../resources/post.md) de grupo), o una instancia de este tipo expandida con un objeto [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="802c7-114">One or a collection of supported resource instance ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md), or group [post](../resources/post.md)), or one such instance expanded with a [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) object.</span></span> |<span data-ttu-id="802c7-115">Obtiene una instancia del recurso con una propiedad extendida mediante `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="802c7-115">Get a resource instance with an extended property using `$expand` or `$filter`.</span></span>|

## <a name="properties"></a><span data-ttu-id="802c7-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="802c7-116">Properties</span></span>
| <span data-ttu-id="802c7-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="802c7-117">Property</span></span>     | <span data-ttu-id="802c7-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="802c7-118">Type</span></span>   |<span data-ttu-id="802c7-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="802c7-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="802c7-120">id</span><span class="sxs-lookup"><span data-stu-id="802c7-120">id</span></span>|<span data-ttu-id="802c7-121">string</span><span class="sxs-lookup"><span data-stu-id="802c7-121">string</span></span>|<span data-ttu-id="802c7-p101">Identificador de propiedad que se usa para identificar la propiedad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="802c7-p101">The property ID used to identify the property. Read-only.</span></span>|
|<span data-ttu-id="802c7-124">value</span><span class="sxs-lookup"><span data-stu-id="802c7-124">value</span></span>|<span data-ttu-id="802c7-125">string</span><span class="sxs-lookup"><span data-stu-id="802c7-125">string</span></span>|<span data-ttu-id="802c7-126">Valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="802c7-126">A property value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="802c7-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="802c7-127">Relationships</span></span>
<span data-ttu-id="802c7-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="802c7-128">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="802c7-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="802c7-129">JSON representation</span></span>

<span data-ttu-id="802c7-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="802c7-130">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
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
