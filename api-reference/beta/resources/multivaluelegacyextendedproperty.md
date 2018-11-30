---
title: Tipo de recurso multiValueLegacyExtendedProperty
description: Propiedad extendida que contiene una colección de valores.
ms.openlocfilehash: efb871594028b5c2d54b1c081f901717b754c8ca
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087028"
---
# <a name="multivaluelegacyextendedproperty-resource-type"></a><span data-ttu-id="e7cec-103">Tipo de recurso multiValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="e7cec-103">multiValueLegacyExtendedProperty resource type</span></span>

> <span data-ttu-id="e7cec-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e7cec-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e7cec-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e7cec-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e7cec-106">Propiedad extendida que contiene una colección de valores.</span><span class="sxs-lookup"><span data-stu-id="e7cec-106">An extended property that contains a collection of values.</span></span>

<span data-ttu-id="e7cec-107">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="e7cec-107">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="methods"></a><span data-ttu-id="e7cec-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e7cec-108">Methods</span></span>

| <span data-ttu-id="e7cec-109">Método</span><span class="sxs-lookup"><span data-stu-id="e7cec-109">Method</span></span>           | <span data-ttu-id="e7cec-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7cec-110">Return Type</span></span>    |<span data-ttu-id="e7cec-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7cec-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e7cec-112">Post</span><span class="sxs-lookup"><span data-stu-id="e7cec-112">Post</span></span>](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | <span data-ttu-id="e7cec-113">Una instancia de recursos admitidos: [mensaje](../resources/message.md), [mailFolder](../resources/mailfolder.md), [eventos](../resources/event.md), [calendario](../resources/calendar.md), [póngase en contacto con](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [tarea de Outlook](../resources/outlooktask.md)o [carpeta de tareas de Outlook](../resources/outlooktaskfolder.md).</span><span class="sxs-lookup"><span data-stu-id="e7cec-113">A supported resource instance: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [Outlook task](../resources/outlooktask.md), or [Outlook task folder](../resources/outlooktaskfolder.md).</span></span> <span data-ttu-id="e7cec-114">Tenga en cuenta que no se admite ese grupo [registrar](../resources/post.md) .</span><span class="sxs-lookup"><span data-stu-id="e7cec-114">Note that group [post](../resources/post.md) is not supported.</span></span> | <span data-ttu-id="e7cec-115">Crea una **multiValueLegacyExtendedProperty** en una instancia nueva o existente de un recurso compatible.</span><span class="sxs-lookup"><span data-stu-id="e7cec-115">Create a **multiValueLegacyExtendedProperty** in a new or existing instance of a supported resource.</span></span> |
|[<span data-ttu-id="e7cec-116">Get</span><span class="sxs-lookup"><span data-stu-id="e7cec-116">Get</span></span>](../api/multivaluelegacyextendedproperty-get.md) |<span data-ttu-id="e7cec-117">Una instancia de recursos admitidos ([mensaje](../resources/message.md), [mailFolder](../resources/mailfolder.md), [eventos](../resources/event.md), [calendario](../resources/calendar.md), [póngase en contacto con](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [tarea de Outlook](../resources/outlooktask.md), [carpeta de tareas de Outlook](../resources/outlooktaskfolder.md)o grupo [registrar](../resources/post.md)) expandido con un [ multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) objeto.</span><span class="sxs-lookup"><span data-stu-id="e7cec-117">A supported resource instance ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [Outlook task](../resources/outlooktask.md), [Outlook task folder](../resources/outlooktaskfolder.md), or group [post](../resources/post.md)) expanded with a [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) object.</span></span> |<span data-ttu-id="e7cec-118">Obtiene una instancia del recurso con una propiedad extendida mediante `$expand`.</span><span class="sxs-lookup"><span data-stu-id="e7cec-118">Get a resource instance with an extended property using `$expand`.</span></span>|

## <a name="properties"></a><span data-ttu-id="e7cec-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e7cec-119">Properties</span></span>
| <span data-ttu-id="e7cec-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7cec-120">Property</span></span>     | <span data-ttu-id="e7cec-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="e7cec-121">Type</span></span>   |<span data-ttu-id="e7cec-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7cec-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e7cec-123">id</span><span class="sxs-lookup"><span data-stu-id="e7cec-123">id</span></span>|<span data-ttu-id="e7cec-124">string</span><span class="sxs-lookup"><span data-stu-id="e7cec-124">string</span></span>|<span data-ttu-id="e7cec-p103">Identificador de la propiedad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e7cec-p103">The property identifier. Read-only.</span></span>|
|<span data-ttu-id="e7cec-127">value</span><span class="sxs-lookup"><span data-stu-id="e7cec-127">value</span></span>|<span data-ttu-id="e7cec-128">colección string</span><span class="sxs-lookup"><span data-stu-id="e7cec-128">string collection</span></span>|<span data-ttu-id="e7cec-129">Colección de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e7cec-129">A collection of property values.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e7cec-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e7cec-130">Relationships</span></span>
<span data-ttu-id="e7cec-131">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e7cec-131">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="e7cec-132">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e7cec-132">JSON representation</span></span>

<span data-ttu-id="e7cec-133">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e7cec-133">Here is a JSON representation of the resource.</span></span>

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