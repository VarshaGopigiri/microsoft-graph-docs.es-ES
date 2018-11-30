---
title: Tipo de recurso singleValueLegacyExtendedProperty
description: 'Propiedad extendida que contiene un solo valor. '
ms.openlocfilehash: 1b9eeaa05ee15aab30c1761cd35f70f586dffb24
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089991"
---
# <a name="singlevaluelegacyextendedproperty-resource-type"></a><span data-ttu-id="bb9d4-103">Tipo de recurso singleValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="bb9d4-103">singleValueLegacyExtendedProperty resource type</span></span>

> <span data-ttu-id="bb9d4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bb9d4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bb9d4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bb9d4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bb9d4-106">Propiedad extendida que contiene un solo valor.</span><span class="sxs-lookup"><span data-stu-id="bb9d4-106">An extended property that contains a single value.</span></span> 

<span data-ttu-id="bb9d4-107">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="bb9d4-107">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span> 


## <a name="methods"></a><span data-ttu-id="bb9d4-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="bb9d4-108">Methods</span></span>

| <span data-ttu-id="bb9d4-109">Método</span><span class="sxs-lookup"><span data-stu-id="bb9d4-109">Method</span></span>           | <span data-ttu-id="bb9d4-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb9d4-110">Return Type</span></span>    |<span data-ttu-id="bb9d4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb9d4-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="bb9d4-112">Post</span><span class="sxs-lookup"><span data-stu-id="bb9d4-112">Post</span></span>](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) | <span data-ttu-id="bb9d4-113">Una instancia de recursos admitidos: [mensaje](../resources/message.md), [mailFolder](../resources/mailfolder.md), [eventos](../resources/event.md), [calendario](../resources/calendar.md), [póngase en contacto con](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [tarea de Outlook](../resources/outlooktask.md), o [carpeta de tareas de Outlook](../resources/outlooktaskfolder.md), pero no grupo [registrar](../resources/post.md).</span><span class="sxs-lookup"><span data-stu-id="bb9d4-113">A supported resource instance: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [Outlook task](../resources/outlooktask.md), or [Outlook task folder](../resources/outlooktaskfolder.md), but not group [post](../resources/post.md).</span></span> | <span data-ttu-id="bb9d4-114">Crea una **singleValueLegacyExtendedProperty** en una instancia nueva o existente de un recurso compatible.</span><span class="sxs-lookup"><span data-stu-id="bb9d4-114">Create a **singleValueLegacyExtendedProperty** in a new or existing instance of a supported resource.</span></span> |
|[<span data-ttu-id="bb9d4-115">Get</span><span class="sxs-lookup"><span data-stu-id="bb9d4-115">Get</span></span>](../api/singlevaluelegacyextendedproperty-get.md) |<span data-ttu-id="bb9d4-116">Uno o una colección de recursos admitidos instancia ([mensaje](../resources/message.md), [mailFolder](../resources/mailfolder.md), [eventos](../resources/event.md), [calendario](../resources/calendar.md), [póngase en contacto con](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [tarea de Outlook](../resources/outlooktask.md), [carpeta de tareas de Outlook](../resources/outlooktaskfolder.md)o grupo [registrar](../resources/post.md)), o bien, una instancia de este tipo expandido con un objeto [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="bb9d4-116">One or a collection of supported resource instance ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md), [Outlook task](../resources/outlooktask.md), [Outlook task folder](../resources/outlooktaskfolder.md), or group [post](../resources/post.md)), or one such instance expanded with a [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) object.</span></span> |<span data-ttu-id="bb9d4-117">Obtiene una instancia del recurso con una propiedad extendida mediante `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="bb9d4-117">Get a resource instance with an extended property using `$expand` or `$filter`.</span></span>|

## <a name="properties"></a><span data-ttu-id="bb9d4-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bb9d4-118">Properties</span></span>
| <span data-ttu-id="bb9d4-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bb9d4-119">Property</span></span>     | <span data-ttu-id="bb9d4-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="bb9d4-120">Type</span></span>   |<span data-ttu-id="bb9d4-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="bb9d4-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bb9d4-122">id</span><span class="sxs-lookup"><span data-stu-id="bb9d4-122">id</span></span>|<span data-ttu-id="bb9d4-123">string</span><span class="sxs-lookup"><span data-stu-id="bb9d4-123">string</span></span>|<span data-ttu-id="bb9d4-p102">Identificador de la propiedad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bb9d4-p102">The property identifier. Read-only.</span></span>|
|<span data-ttu-id="bb9d4-126">value</span><span class="sxs-lookup"><span data-stu-id="bb9d4-126">value</span></span>|<span data-ttu-id="bb9d4-127">string</span><span class="sxs-lookup"><span data-stu-id="bb9d4-127">string</span></span>|<span data-ttu-id="bb9d4-128">Valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="bb9d4-128">A property value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bb9d4-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bb9d4-129">Relationships</span></span>
<span data-ttu-id="bb9d4-130">Ninguno</span><span class="sxs-lookup"><span data-stu-id="bb9d4-130">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="bb9d4-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bb9d4-131">JSON representation</span></span>

<span data-ttu-id="bb9d4-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bb9d4-132">Here is a JSON representation of the resource.</span></span>

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