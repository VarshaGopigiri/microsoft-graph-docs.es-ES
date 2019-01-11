---
title: Tipo de recurso recentNotebook
description: Bloc de notas de OneNote al que se ha accedido recientemente. Un **recentNotebook** es similar a un notebook pero tiene menos propiedades.
localization_priority: Normal
ms.openlocfilehash: 67c707043e5b6ca65cd72ddc323b5a484f0f2959
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889228"
---
# <a name="recentnotebook-resource-type"></a><span data-ttu-id="759b4-104">Tipo de recurso recentNotebook</span><span class="sxs-lookup"><span data-stu-id="759b4-104">recentNotebook resource type</span></span>

<span data-ttu-id="759b4-105">Bloc de notas de OneNote al que se ha accedido recientemente.</span><span class="sxs-lookup"><span data-stu-id="759b4-105">A recently accessed OneNote notebook.</span></span> <span data-ttu-id="759b4-106">Un **recentNotebook** es similar a un [notebook](notebook.md) pero tiene menos propiedades.</span><span class="sxs-lookup"><span data-stu-id="759b4-106">A **recentNotebook** is similar to a [notebook](notebook.md) but has fewer properties.</span></span>

## <a name="properties"></a><span data-ttu-id="759b4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="759b4-107">Properties</span></span>
| <span data-ttu-id="759b4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="759b4-108">Property</span></span>     | <span data-ttu-id="759b4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="759b4-109">Type</span></span>   |<span data-ttu-id="759b4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="759b4-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="759b4-111">displayName</span><span class="sxs-lookup"><span data-stu-id="759b4-111">displayName</span></span>|<span data-ttu-id="759b4-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="759b4-112">String</span></span>|<span data-ttu-id="759b4-113">Nombre del bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="759b4-113">The name of the notebook.</span></span>|
|<span data-ttu-id="759b4-114">lastAccessedTime</span><span class="sxs-lookup"><span data-stu-id="759b4-114">lastAccessedTime</span></span>|<span data-ttu-id="759b4-115">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="759b4-115">DateTimeOffset</span></span>|<span data-ttu-id="759b4-p103">La fecha y la hora en que se modificó por última vez el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="759b4-p103">The date and time when the notebook was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="759b4-120">links</span><span class="sxs-lookup"><span data-stu-id="759b4-120">links</span></span>|[<span data-ttu-id="759b4-121">recentNotebookLinks</span><span class="sxs-lookup"><span data-stu-id="759b4-121">recentNotebookLinks</span></span>](recentnotebooklinks.md)|<span data-ttu-id="759b4-122">Vínculos para abrir el bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="759b4-122">Links for opening the notebook.</span></span> <span data-ttu-id="759b4-123">El vínculo `oneNoteClientURL` abre el bloc de notas en el cliente de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="759b4-123">The `oneNoteClientURL` link opens the notebook in the OneNote client, if it's installed.</span></span> <span data-ttu-id="759b4-124">El vínculo `oneNoteWebURL` abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="759b4-124">The `oneNoteWebURL` link opens the notebook in OneNote Online.</span></span>|
|<span data-ttu-id="759b4-125">sourceService</span><span class="sxs-lookup"><span data-stu-id="759b4-125">sourceService</span></span>|<span data-ttu-id="759b4-126">onenoteSourceService</span><span class="sxs-lookup"><span data-stu-id="759b4-126">onenoteSourceService</span></span>|<span data-ttu-id="759b4-127">Almacén de back-end donde reside el Bloc de notas, `OneDriveForBusiness` o `OneDrive`.</span><span class="sxs-lookup"><span data-stu-id="759b4-127">The backend store where the Notebook resides, either `OneDriveForBusiness` or `OneDrive`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="759b4-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="759b4-128">JSON representation</span></span>

<span data-ttu-id="759b4-129">La siguiente es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="759b4-129">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recentNotebook"
}-->

```json
{
  "displayName": "String",
  "lastAccessedTime": "String (timestamp)",
  "links": {"@odata.type": "microsoft.graph.recentNotebookLinks"},
  "sourceService": "String"
}
```

## <a name="methods"></a><span data-ttu-id="759b4-130">Métodos</span><span class="sxs-lookup"><span data-stu-id="759b4-130">Methods</span></span>

| <span data-ttu-id="759b4-131">Método</span><span class="sxs-lookup"><span data-stu-id="759b4-131">Method</span></span>           | <span data-ttu-id="759b4-132">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="759b4-132">Return Type</span></span>    |<span data-ttu-id="759b4-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="759b4-133">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="759b4-134">getRecentNotebooks</span><span class="sxs-lookup"><span data-stu-id="759b4-134">getRecentNotebooks</span></span>](../api/notebook-getrecentnotebooks.md) | <span data-ttu-id="759b4-135">Colección [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="759b4-135">[notebook](notebook.md) collection</span></span> | <span data-ttu-id="759b4-136">Obtener una colección de los blocs de notas a los que el usuario ha accedido más recientemente.</span><span class="sxs-lookup"><span data-stu-id="759b4-136">Get a collection of the most recently accessed notebooks for the user.</span></span> |
