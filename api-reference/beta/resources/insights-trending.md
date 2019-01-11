---
title: tipo de recurso de tendencias
description: Relación enriquecida conecta un usuario a los documentos que se tendencias alrededor del usuario (son relevante para el usuario). Archivos de OneDrive, y los archivos almacenados en sitios de grupo de SharePoint pueden tendencias alrededor del usuario.
author: simonhult
localization_priority: Normal
ms.openlocfilehash: dc0154d3985e5f6e1e4770bb7d10bc727a0eb0ae
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862387"
---
# <a name="trending-resource-type"></a><span data-ttu-id="3bbc3-104">tipo de recurso de tendencias</span><span class="sxs-lookup"><span data-stu-id="3bbc3-104">trending resource type</span></span>

> <span data-ttu-id="3bbc3-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3bbc3-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3bbc3-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3bbc3-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3bbc3-107">Relación enriquecida conecta un usuario a los documentos que se tendencias alrededor del usuario (son relevante para el usuario).</span><span class="sxs-lookup"><span data-stu-id="3bbc3-107">Rich relationship connecting a user to documents that are trending around the user (are relevant to the user).</span></span> <span data-ttu-id="3bbc3-108">Archivos de OneDrive, y los archivos almacenados en sitios de grupo de SharePoint pueden tendencias alrededor del usuario.</span><span class="sxs-lookup"><span data-stu-id="3bbc3-108">OneDrive files, and files stored on SharePoint team sites can trend around the user.</span></span>

## <a name="methods"></a><span data-ttu-id="3bbc3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="3bbc3-109">Methods</span></span>

| <span data-ttu-id="3bbc3-110">Método</span><span class="sxs-lookup"><span data-stu-id="3bbc3-110">Method</span></span>       | <span data-ttu-id="3bbc3-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bbc3-111">Return Type</span></span>  |<span data-ttu-id="3bbc3-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bbc3-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="3bbc3-113">Tendencias de lista</span><span class="sxs-lookup"><span data-stu-id="3bbc3-113">List trending</span></span>](../api/insights-list-trending.md) |<span data-ttu-id="3bbc3-114">colección de [insights_trending](insights-trending.md)</span><span class="sxs-lookup"><span data-stu-id="3bbc3-114">[insights_trending](insights-trending.md) collection</span></span>| <span data-ttu-id="3bbc3-115">Obtener una lista de los archivos de tendencias.</span><span class="sxs-lookup"><span data-stu-id="3bbc3-115">Get a list of trending files.</span></span>|

## <a name="properties"></a><span data-ttu-id="3bbc3-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3bbc3-116">Properties</span></span>

| <span data-ttu-id="3bbc3-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3bbc3-117">Property</span></span>      | <span data-ttu-id="3bbc3-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bbc3-118">Type</span></span>                              | <span data-ttu-id="3bbc3-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bbc3-119">Description</span></span>  |
| ------------- |---------------                    | -------------|
| <span data-ttu-id="3bbc3-120">id</span><span class="sxs-lookup"><span data-stu-id="3bbc3-120">id</span></span>                    | <span data-ttu-id="3bbc3-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="3bbc3-121">String</span></span>                    | <span data-ttu-id="3bbc3-122">Identificador único de la relación.</span><span class="sxs-lookup"><span data-stu-id="3bbc3-122">Unique identifier of the relationship.</span></span> <span data-ttu-id="3bbc3-123">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3bbc3-123">Read only.</span></span>        |
| <span data-ttu-id="3bbc3-124">weight</span><span class="sxs-lookup"><span data-stu-id="3bbc3-124">weight</span></span>                | <span data-ttu-id="3bbc3-125">Doble</span><span class="sxs-lookup"><span data-stu-id="3bbc3-125">Double</span></span>                    | <span data-ttu-id="3bbc3-126">Valor que indica cuánto el documento actualmente es tendencias.</span><span class="sxs-lookup"><span data-stu-id="3bbc3-126">Value indicating how much the document is currently trending.</span></span> <span data-ttu-id="3bbc3-127">Cuanto mayor sea el número, más el documento está actualmente tendencias alrededor del usuario (más relevante es).</span><span class="sxs-lookup"><span data-stu-id="3bbc3-127">The larger the number, the more the document is currently trending around the user (the more relevant it is).</span></span> <span data-ttu-id="3bbc3-128">Los documentos devueltos se ordenan por este valor.</span><span class="sxs-lookup"><span data-stu-id="3bbc3-128">Returned documents are sorted by this value.</span></span>  |
| <span data-ttu-id="3bbc3-129">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="3bbc3-129">resourceVisualization</span></span> | [<span data-ttu-id="3bbc3-130">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="3bbc3-130">resourceVisualization</span></span>](insights-resourcevisualization.md)    | <span data-ttu-id="3bbc3-131">Propiedades que puede usar para visualizar el documento en su experiencia.</span><span class="sxs-lookup"><span data-stu-id="3bbc3-131">Properties that you can use to visualize the document in your experience.</span></span> |
| <span data-ttu-id="3bbc3-132">resourceReference</span><span class="sxs-lookup"><span data-stu-id="3bbc3-132">resourceReference</span></span>     | [<span data-ttu-id="3bbc3-133">resourceReference</span><span class="sxs-lookup"><span data-stu-id="3bbc3-133">resourceReference</span></span>](insights-resourcereference.md)        | <span data-ttu-id="3bbc3-134">Propiedades de la referencia del documento tendencia, como la dirección url y el tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="3bbc3-134">Reference properties of the trending document, such as the url and type of the document.</span></span> |

## <a name="relationships"></a><span data-ttu-id="3bbc3-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3bbc3-135">Relationships</span></span>

| <span data-ttu-id="3bbc3-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3bbc3-136">Property</span></span>      | <span data-ttu-id="3bbc3-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="3bbc3-137">Type</span></span>          | <span data-ttu-id="3bbc3-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="3bbc3-138">Description</span></span>  |
| ------------- |---------------| -------------|
| <span data-ttu-id="3bbc3-139">resource</span><span class="sxs-lookup"><span data-stu-id="3bbc3-139">resource</span></span>      | <span data-ttu-id="3bbc3-140">Entidad</span><span class="sxs-lookup"><span data-stu-id="3bbc3-140">Entity</span></span>        | <span data-ttu-id="3bbc3-141">Se usa para navegar hasta el documento tendencia.</span><span class="sxs-lookup"><span data-stu-id="3bbc3-141">Used for navigating to the trending document.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="3bbc3-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3bbc3-142">JSON representation</span></span>

<span data-ttu-id="3bbc3-143">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3bbc3-143">Here is a JSON representation of the resource</span></span>

```json
{
  "id": "string",
  "weight": "double",
  "resourceVisualization": [{"@odata.type": "microsoft.graph.resourceVisualization"}],
  "resourceReference": [{"@odata.type": "microsoft.graph.resourceReference"}],
  
  "resource": [ { "@odata.type": "microsoft.graph.entity" } ]
}
```
