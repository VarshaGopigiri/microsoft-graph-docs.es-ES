---
title: Tipo de recurso inferenceClassification
description: 'Clasificación de mensajes de un usuario que permite poner el foco en los que son más relevantes o importantes para el usuario. '
ms.openlocfilehash: c1536ff2b88b1830c2f2a2bc5a7bed519782df4e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083033"
---
# <a name="inferenceclassification-resource-type"></a><span data-ttu-id="11149-103">Tipo de recurso inferenceClassification</span><span class="sxs-lookup"><span data-stu-id="11149-103">inferenceClassification resource type</span></span>

> <span data-ttu-id="11149-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="11149-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="11149-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="11149-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="11149-106">Clasificación de mensajes de un usuario que permite poner el foco en los que son más relevantes o importantes para el usuario.</span><span class="sxs-lookup"><span data-stu-id="11149-106">Classification of a user's messages to enable focus on those that are more relevant or important to the user.</span></span> 

<span data-ttu-id="11149-107">Para obtener más información, consulte [Administrar Bandeja de entrada Prioritarios](manage-focused-inbox.md).</span><span class="sxs-lookup"><span data-stu-id="11149-107">For more information, see [Manage Focused Inbox](manage-focused-inbox.md).</span></span>


## <a name="methods"></a><span data-ttu-id="11149-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="11149-108">Methods</span></span>

| <span data-ttu-id="11149-109">Método</span><span class="sxs-lookup"><span data-stu-id="11149-109">Method</span></span>           | <span data-ttu-id="11149-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11149-110">Return Type</span></span>    |<span data-ttu-id="11149-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="11149-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="11149-112">Create inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="11149-112">Create inferenceClassificationOverride</span></span>](../api/inferenceclassification-post-overrides.md) |[<span data-ttu-id="11149-113">inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="11149-113">inferenceClassificationOverride</span></span>](inferenceclassificationoverride.md)| <span data-ttu-id="11149-p102">Cree una invalidación para un remitente que se ha identificado mediante una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasificarán sistemáticamente como se especifica en la invalidación.</span><span class="sxs-lookup"><span data-stu-id="11149-p102">Create an override for a sender identified by an SMTP address. Future messages from that SMTP address will be consistently classified as specified in the override.</span></span>|
|[<span data-ttu-id="11149-116">List overrides</span><span class="sxs-lookup"><span data-stu-id="11149-116">List overrides</span></span>](../api/inferenceclassification-list-overrides.md) |<span data-ttu-id="11149-117">Colección [inferenceClassificationOverride](inferenceclassificationoverride.md)</span><span class="sxs-lookup"><span data-stu-id="11149-117">[inferenceClassificationOverride](inferenceclassificationoverride.md) collection</span></span>| <span data-ttu-id="11149-118">Obtiene los reemplazos que un usuario ha configurado para clasificar siempre los mensajes de determinados remitentes de forma específica.</span><span class="sxs-lookup"><span data-stu-id="11149-118">Get the overrides that a user has set up to always classify messages from certain senders in specific ways.</span></span>|

## <a name="properties"></a><span data-ttu-id="11149-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11149-119">Properties</span></span>
| <span data-ttu-id="11149-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11149-120">Property</span></span>     | <span data-ttu-id="11149-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="11149-121">Type</span></span>   |<span data-ttu-id="11149-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="11149-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="11149-123">id</span><span class="sxs-lookup"><span data-stu-id="11149-123">id</span></span>|<span data-ttu-id="11149-124">string</span><span class="sxs-lookup"><span data-stu-id="11149-124">string</span></span>| <span data-ttu-id="11149-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="11149-125">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="11149-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="11149-126">Relationships</span></span>
| <span data-ttu-id="11149-127">Relación</span><span class="sxs-lookup"><span data-stu-id="11149-127">Relationship</span></span> | <span data-ttu-id="11149-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="11149-128">Type</span></span>   |<span data-ttu-id="11149-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="11149-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="11149-130">overrides</span><span class="sxs-lookup"><span data-stu-id="11149-130">overrides</span></span>|<span data-ttu-id="11149-131">Colección [inferenceClassificationOverride](inferenceclassificationoverride.md)</span><span class="sxs-lookup"><span data-stu-id="11149-131">[inferenceClassificationOverride](inferenceclassificationoverride.md) collection</span></span>| <span data-ttu-id="11149-p103">Conjunto de valores de reemplazo de un usuario para clasificar siempre los mensajes de remitentes concretos de determinada manera: `focused`, o `other`. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="11149-p103">A set of overrides for a user to always classify messages from specific senders in certain ways: `focused`, or `other`. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="11149-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="11149-135">JSON representation</span></span>

<span data-ttu-id="11149-136">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="11149-136">Here is a JSON representation of the resource.</span></span>

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