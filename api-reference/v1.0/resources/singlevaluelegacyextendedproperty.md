---
title: Tipo de recurso singleValueLegacyExtendedProperty
description: 'Propiedad extendida que contiene un solo valor. '
ms.openlocfilehash: 82a2ca848ba22381366016617c3fa6529ce4ee54
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029629"
---
# <a name="singlevaluelegacyextendedproperty-resource-type"></a><span data-ttu-id="8b9f9-103">Tipo de recurso singleValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="8b9f9-103">singleValueLegacyExtendedProperty resource type</span></span>

<span data-ttu-id="8b9f9-104">Propiedad extendida que contiene un solo valor.</span><span class="sxs-lookup"><span data-stu-id="8b9f9-104">An extended property that contains a single value.</span></span> 

<span data-ttu-id="8b9f9-105">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="8b9f9-105">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span> 


## <a name="methods"></a><span data-ttu-id="8b9f9-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="8b9f9-106">Methods</span></span>

| <span data-ttu-id="8b9f9-107">Método</span><span class="sxs-lookup"><span data-stu-id="8b9f9-107">Method</span></span>           | <span data-ttu-id="8b9f9-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b9f9-108">Return Type</span></span>    |<span data-ttu-id="8b9f9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b9f9-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="8b9f9-110">Post</span><span class="sxs-lookup"><span data-stu-id="8b9f9-110">Post</span></span>](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) | <span data-ttu-id="8b9f9-111">Instancia de recurso admitida: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md) o [contactFolder](../resources/contactfolder.md), pero no [post](../resources/post.md) de grupo.</span><span class="sxs-lookup"><span data-stu-id="8b9f9-111">A supported resource instance: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), or [contactFolder](../resources/contactfolder.md), but not group [post](../resources/post.md).</span></span> | <span data-ttu-id="8b9f9-112">Crea una **singleValueLegacyExtendedProperty** en una instancia nueva o existente de un recurso compatible.</span><span class="sxs-lookup"><span data-stu-id="8b9f9-112">Create a **singleValueLegacyExtendedProperty** in a new or existing instance of a supported resource.</span></span> |
|[<span data-ttu-id="8b9f9-113">Get</span><span class="sxs-lookup"><span data-stu-id="8b9f9-113">Get</span></span>](../api/singlevaluelegacyextendedproperty-get.md) |<span data-ttu-id="8b9f9-114">Instancia o colección de instancias de recurso admitidas: ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md) o [post](../resources/post.md) de grupo), o una instancia de este tipo expandida con un objeto [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="8b9f9-114">One or a collection of supported resource instance ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md), or group [post](../resources/post.md)), or one such instance expanded with a [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) object.</span></span> |<span data-ttu-id="8b9f9-115">Obtiene una instancia del recurso con una propiedad extendida mediante `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="8b9f9-115">Get a resource instance with an extended property using `$expand` or `$filter`.</span></span>|

## <a name="properties"></a><span data-ttu-id="8b9f9-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8b9f9-116">Properties</span></span>
| <span data-ttu-id="8b9f9-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8b9f9-117">Property</span></span>     | <span data-ttu-id="8b9f9-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b9f9-118">Type</span></span>   |<span data-ttu-id="8b9f9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b9f9-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8b9f9-120">id</span><span class="sxs-lookup"><span data-stu-id="8b9f9-120">id</span></span>|<span data-ttu-id="8b9f9-121">string</span><span class="sxs-lookup"><span data-stu-id="8b9f9-121">string</span></span>|<span data-ttu-id="8b9f9-p101">Identificador de propiedad que se usa para identificar la propiedad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8b9f9-p101">The property ID used to identify the property. Read-only.</span></span>|
|<span data-ttu-id="8b9f9-124">value</span><span class="sxs-lookup"><span data-stu-id="8b9f9-124">value</span></span>|<span data-ttu-id="8b9f9-125">string</span><span class="sxs-lookup"><span data-stu-id="8b9f9-125">string</span></span>|<span data-ttu-id="8b9f9-126">Valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="8b9f9-126">A property value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8b9f9-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8b9f9-127">Relationships</span></span>
<span data-ttu-id="8b9f9-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8b9f9-128">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="8b9f9-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8b9f9-129">JSON representation</span></span>

<span data-ttu-id="8b9f9-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8b9f9-130">Here is a JSON representation of the resource.</span></span>

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