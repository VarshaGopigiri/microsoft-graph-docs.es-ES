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
# <a name="inferenceclassification-resource-type"></a><span data-ttu-id="22415-103">Tipo de recurso inferenceClassification</span><span class="sxs-lookup"><span data-stu-id="22415-103">inferenceClassification resource type</span></span>

<span data-ttu-id="22415-104">Clasificación de mensajes de un usuario que permite poner el foco en los que son más relevantes o importantes para el usuario.</span><span class="sxs-lookup"><span data-stu-id="22415-104">Classification of a user's messages to enable focus on those that are more relevant or important to the user.</span></span> 

<span data-ttu-id="22415-105">Para obtener más información, consulte [Administrar Bandeja de entrada Prioritarios](manage-focused-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="22415-105">For more information, see [Manage Focused Inbox](manage-focused-inbox.md).</span></span>


## <a name="methods"></a><span data-ttu-id="22415-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="22415-106">Methods</span></span>

| <span data-ttu-id="22415-107">Método</span><span class="sxs-lookup"><span data-stu-id="22415-107">Method</span></span>           | <span data-ttu-id="22415-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22415-108">Return Type</span></span>    |<span data-ttu-id="22415-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="22415-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="22415-110">Create inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="22415-110">Create inferenceClassificationOverride</span></span>](../api/inferenceclassification-post-overrides.md) |[<span data-ttu-id="22415-111">inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="22415-111">inferenceClassificationOverride</span></span>](inferenceclassificationoverride.md)| <span data-ttu-id="22415-p101">Cree una invalidación para un remitente que se ha identificado mediante una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasificarán sistemáticamente como se especifica en la invalidación.</span><span class="sxs-lookup"><span data-stu-id="22415-p101">Create an override for a sender identified by an SMTP address. Future messages from that SMTP address will be consistently classified as specified in the override.</span></span>|
|[<span data-ttu-id="22415-114">List overrides</span><span class="sxs-lookup"><span data-stu-id="22415-114">List overrides</span></span>](../api/inferenceclassification-list-overrides.md) |<span data-ttu-id="22415-115">Colección [inferenceClassificationOverride](inferenceclassificationoverride.md)</span><span class="sxs-lookup"><span data-stu-id="22415-115">[inferenceClassificationOverride](inferenceclassificationoverride.md) collection</span></span>| <span data-ttu-id="22415-116">Obtiene los reemplazos que un usuario ha configurado para clasificar siempre los mensajes de determinados remitentes de forma específica.</span><span class="sxs-lookup"><span data-stu-id="22415-116">Get the overrides that a user has set up to always classify messages from certain senders in specific ways.</span></span>|

## <a name="properties"></a><span data-ttu-id="22415-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22415-117">Properties</span></span>
| <span data-ttu-id="22415-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="22415-118">Property</span></span>     | <span data-ttu-id="22415-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="22415-119">Type</span></span>   |<span data-ttu-id="22415-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="22415-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="22415-121">id</span><span class="sxs-lookup"><span data-stu-id="22415-121">id</span></span>|<span data-ttu-id="22415-122">string</span><span class="sxs-lookup"><span data-stu-id="22415-122">string</span></span>| <span data-ttu-id="22415-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="22415-123">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="22415-124">Relaciones</span><span class="sxs-lookup"><span data-stu-id="22415-124">Relationships</span></span>
| <span data-ttu-id="22415-125">Relación</span><span class="sxs-lookup"><span data-stu-id="22415-125">Relationship</span></span> | <span data-ttu-id="22415-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="22415-126">Type</span></span>   |<span data-ttu-id="22415-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="22415-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="22415-128">overrides</span><span class="sxs-lookup"><span data-stu-id="22415-128">overrides</span></span>|<span data-ttu-id="22415-129">Colección [inferenceClassificationOverride](inferenceclassificationoverride.md)</span><span class="sxs-lookup"><span data-stu-id="22415-129">[inferenceClassificationOverride](inferenceclassificationoverride.md) collection</span></span>| <span data-ttu-id="22415-p102">Conjunto de valores de reemplazo de un usuario para clasificar siempre los mensajes de remitentes concretos de determinada manera: `focused`, o `other`. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="22415-p102">A set of overrides for a user to always classify messages from specific senders in certain ways: `focused`, or `other`. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="22415-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="22415-133">JSON representation</span></span>

<span data-ttu-id="22415-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="22415-134">Here is a JSON representation of the resource.</span></span>

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