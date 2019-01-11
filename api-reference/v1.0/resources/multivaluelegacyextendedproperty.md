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
# <a name="multivaluelegacyextendedproperty-resource-type"></a><span data-ttu-id="3670e-103">Tipo de recurso multiValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="3670e-103">multiValueLegacyExtendedProperty resource type</span></span>

<span data-ttu-id="3670e-104">Propiedad extendida que contiene una colección de valores.</span><span class="sxs-lookup"><span data-stu-id="3670e-104">An extended property that contains a collection of values.</span></span>

<span data-ttu-id="3670e-105">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="3670e-105">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="methods"></a><span data-ttu-id="3670e-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="3670e-106">Methods</span></span>

| <span data-ttu-id="3670e-107">Método</span><span class="sxs-lookup"><span data-stu-id="3670e-107">Method</span></span>           | <span data-ttu-id="3670e-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3670e-108">Return Type</span></span>    |<span data-ttu-id="3670e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3670e-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="3670e-110">Post</span><span class="sxs-lookup"><span data-stu-id="3670e-110">Post</span></span>](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | <span data-ttu-id="3670e-p101">Instancia de recurso admitida: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md) o [contactFolder](../resources/contactfolder.md). Tenga en cuenta que no se admite [post](../resources/post.md) de grupo.</span><span class="sxs-lookup"><span data-stu-id="3670e-p101">A supported resource instance: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), or [contactFolder](../resources/contactfolder.md). Note that group [post](../resources/post.md) is not supported.</span></span> | <span data-ttu-id="3670e-113">Crea una **multiValueLegacyExtendedProperty** en una instancia nueva o existente de un recurso compatible.</span><span class="sxs-lookup"><span data-stu-id="3670e-113">Create a **multiValueLegacyExtendedProperty** in a new or existing instance of a supported resource.</span></span> |
|[<span data-ttu-id="3670e-114">Get</span><span class="sxs-lookup"><span data-stu-id="3670e-114">Get</span></span>](../api/multivaluelegacyextendedproperty-get.md) |<span data-ttu-id="3670e-115">Instancia de recurso admitida ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md) o [post](../resources/post.md) de grupo) expandida con un objeto [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="3670e-115">A supported resource instance ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md), or group [post](../resources/post.md)) expanded with a [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) object.</span></span> |<span data-ttu-id="3670e-116">Obtiene una instancia del recurso con una propiedad extendida mediante `$expand`.</span><span class="sxs-lookup"><span data-stu-id="3670e-116">Get a resource instance with an extended property using `$expand`.</span></span>|

## <a name="properties"></a><span data-ttu-id="3670e-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3670e-117">Properties</span></span>
| <span data-ttu-id="3670e-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3670e-118">Property</span></span>     | <span data-ttu-id="3670e-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="3670e-119">Type</span></span>   |<span data-ttu-id="3670e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="3670e-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3670e-121">id</span><span class="sxs-lookup"><span data-stu-id="3670e-121">id</span></span>|<span data-ttu-id="3670e-122">string</span><span class="sxs-lookup"><span data-stu-id="3670e-122">string</span></span>|<span data-ttu-id="3670e-p102">Identificador de la propiedad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3670e-p102">The property identifier. Read-only.</span></span>|
|<span data-ttu-id="3670e-125">value</span><span class="sxs-lookup"><span data-stu-id="3670e-125">value</span></span>|<span data-ttu-id="3670e-126">colección string</span><span class="sxs-lookup"><span data-stu-id="3670e-126">string collection</span></span>|<span data-ttu-id="3670e-127">Colección de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="3670e-127">A collection of property values.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3670e-128">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3670e-128">Relationships</span></span>
<span data-ttu-id="3670e-129">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3670e-129">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="3670e-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3670e-130">JSON representation</span></span>

<span data-ttu-id="3670e-131">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3670e-131">Here is a JSON representation of the resource.</span></span>

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
