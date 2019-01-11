---
title: Tipo de recurso recentNotebook
description: Bloc de notas de OneNote al que se ha accedido recientemente. Un **recentNotebook** es similar a un notebook pero tiene menos propiedades.
localization_priority: Normal
ms.openlocfilehash: f2dd1ca642203cde36bb636b9cb2eb7c79344e3e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833834"
---
# <a name="recentnotebook-resource-type"></a><span data-ttu-id="82ddd-104">Tipo de recurso recentNotebook</span><span class="sxs-lookup"><span data-stu-id="82ddd-104">recentNotebook resource type</span></span>

> <span data-ttu-id="82ddd-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="82ddd-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="82ddd-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="82ddd-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="82ddd-107">Bloc de notas de OneNote al que se ha accedido recientemente.</span><span class="sxs-lookup"><span data-stu-id="82ddd-107">A recently accessed OneNote notebook.</span></span> <span data-ttu-id="82ddd-108">Un **recentNotebook** es similar a un [notebook](notebook.md) pero tiene menos propiedades.</span><span class="sxs-lookup"><span data-stu-id="82ddd-108">A **recentNotebook** is similar to a [notebook](notebook.md) but has fewer properties.</span></span>

## <a name="properties"></a><span data-ttu-id="82ddd-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="82ddd-109">Properties</span></span>
| <span data-ttu-id="82ddd-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82ddd-110">Property</span></span>     | <span data-ttu-id="82ddd-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="82ddd-111">Type</span></span>   |<span data-ttu-id="82ddd-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="82ddd-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="82ddd-113">name</span><span class="sxs-lookup"><span data-stu-id="82ddd-113">name</span></span>|<span data-ttu-id="82ddd-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="82ddd-114">String</span></span>|<span data-ttu-id="82ddd-115">Nombre del bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="82ddd-115">The name of the notebook.</span></span>|
|<span data-ttu-id="82ddd-116">lastAccessedTime</span><span class="sxs-lookup"><span data-stu-id="82ddd-116">lastAccessedTime</span></span>|<span data-ttu-id="82ddd-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="82ddd-117">DateTimeOffset</span></span>|<span data-ttu-id="82ddd-p104">La fecha y la hora en que se modificó por última vez el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="82ddd-p104">The date and time when the notebook was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="82ddd-122">links</span><span class="sxs-lookup"><span data-stu-id="82ddd-122">links</span></span>|[<span data-ttu-id="82ddd-123">recentNotebookLinks</span><span class="sxs-lookup"><span data-stu-id="82ddd-123">recentNotebookLinks</span></span>](recentnotebooklinks.md)|<span data-ttu-id="82ddd-124">Vínculos para abrir el bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="82ddd-124">Links for opening the notebook.</span></span> <span data-ttu-id="82ddd-125">El vínculo `oneNoteClientURL` abre el bloc de notas en el cliente de OneNote si está instalado.</span><span class="sxs-lookup"><span data-stu-id="82ddd-125">The `oneNoteClientURL` link opens the notebook in the OneNote client, if it's installed.</span></span> <span data-ttu-id="82ddd-126">El vínculo `oneNoteWebURL` abre el bloc de notas en OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="82ddd-126">The `oneNoteWebURL` link opens the notebook in OneNote Online.</span></span>|
|<span data-ttu-id="82ddd-127">sourceService</span><span class="sxs-lookup"><span data-stu-id="82ddd-127">sourceService</span></span>|<span data-ttu-id="82ddd-128">String</span><span class="sxs-lookup"><span data-stu-id="82ddd-128">String</span></span>|<span data-ttu-id="82ddd-129">Almacén de back-end donde reside el Bloc de notas, `OneDriveForBusiness` o `OneDrive`.</span><span class="sxs-lookup"><span data-stu-id="82ddd-129">The backend store where the Notebook resides, either `OneDriveForBusiness` or `OneDrive`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="82ddd-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="82ddd-130">JSON representation</span></span>

<span data-ttu-id="82ddd-131">La siguiente es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="82ddd-131">The following is a JSON representation of the resource.</span></span>

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

## <a name="methods"></a><span data-ttu-id="82ddd-132">Métodos</span><span class="sxs-lookup"><span data-stu-id="82ddd-132">Methods</span></span>

| <span data-ttu-id="82ddd-133">Método</span><span class="sxs-lookup"><span data-stu-id="82ddd-133">Method</span></span>           | <span data-ttu-id="82ddd-134">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82ddd-134">Return Type</span></span>    |<span data-ttu-id="82ddd-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="82ddd-135">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="82ddd-136">getRecentNotebooks</span><span class="sxs-lookup"><span data-stu-id="82ddd-136">getRecentNotebooks</span></span>](../api/notebook-getrecentnotebooks.md) | <span data-ttu-id="82ddd-137">Colección [notebook](notebook.md)</span><span class="sxs-lookup"><span data-stu-id="82ddd-137">[notebook](notebook.md) collection</span></span> | <span data-ttu-id="82ddd-138">Obtener una colección de los blocs de notas a los que el usuario ha accedido más recientemente.</span><span class="sxs-lookup"><span data-stu-id="82ddd-138">Get a collection of the most recently accessed notebooks for the user.</span></span> |
