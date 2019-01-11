---
title: utiliza el tipo de recurso
description: Una idea que representa documentos usados por un usuario específico. Los conocimientos devuelve los documentos más importantes que se pueden ve ni tener acceso a un usuario.
author: simonhult
localization_priority: Normal
ms.openlocfilehash: cb41fcb7cef5c9e39f9100ebd1d8c2640f06e2d0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885536"
---
# <a name="used-resource-type"></a><span data-ttu-id="96b84-104">utiliza el tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="96b84-104">used resource type</span></span>

> <span data-ttu-id="96b84-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="96b84-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="96b84-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="96b84-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="96b84-107">Una idea que representa documentos usados por un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="96b84-107">An insight representing documents used by a specific user.</span></span> <span data-ttu-id="96b84-108">Los conocimientos devuelve los documentos más importantes que se pueden ve ni tener acceso a un usuario.</span><span class="sxs-lookup"><span data-stu-id="96b84-108">The insights returns the most relevant documents that a user viewed or accessed.</span></span> <span data-ttu-id="96b84-109">Esto incluye documentos en:</span><span class="sxs-lookup"><span data-stu-id="96b84-109">This includes documents in:</span></span>

- <span data-ttu-id="96b84-110">OneDrive para la Empresa</span><span class="sxs-lookup"><span data-stu-id="96b84-110">OneDrive for Business</span></span>
- <span data-ttu-id="96b84-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="96b84-111">SharePoint</span></span>

## <a name="methods"></a><span data-ttu-id="96b84-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="96b84-112">Methods</span></span>

| <span data-ttu-id="96b84-113">Método</span><span class="sxs-lookup"><span data-stu-id="96b84-113">Method</span></span>       | <span data-ttu-id="96b84-114">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96b84-114">Return Type</span></span>  |<span data-ttu-id="96b84-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="96b84-115">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="96b84-116">Lista usada</span><span class="sxs-lookup"><span data-stu-id="96b84-116">List used</span></span>](../api/insights-list-used.md) |<span data-ttu-id="96b84-117">colección de [insights_used](insights-used.md)</span><span class="sxs-lookup"><span data-stu-id="96b84-117">[insights_used](insights-used.md) collection</span></span>| <span data-ttu-id="96b84-118">Obtener una lista de archivos usados.</span><span class="sxs-lookup"><span data-stu-id="96b84-118">Get a list of used files.</span></span>|

## <a name="properties"></a><span data-ttu-id="96b84-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96b84-119">Properties</span></span>

| <span data-ttu-id="96b84-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96b84-120">Property</span></span>              | <span data-ttu-id="96b84-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="96b84-121">Type</span></span>                      | <span data-ttu-id="96b84-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="96b84-122">Description</span></span>  |
| -------------         |---------------            | -------------|
| <span data-ttu-id="96b84-123">id</span><span class="sxs-lookup"><span data-stu-id="96b84-123">id</span></span>                    | <span data-ttu-id="96b84-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="96b84-124">String</span></span>                    | <span data-ttu-id="96b84-125">Identificador único de la relación.</span><span class="sxs-lookup"><span data-stu-id="96b84-125">Unique identifier of the relationship.</span></span> <span data-ttu-id="96b84-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="96b84-126">Read only.</span></span>        |
| <span data-ttu-id="96b84-127">lastUsed</span><span class="sxs-lookup"><span data-stu-id="96b84-127">lastUsed</span></span>              | [<span data-ttu-id="96b84-128">usageDetails</span><span class="sxs-lookup"><span data-stu-id="96b84-128">usageDetails</span></span>](insights-usagedetails.md)              | <span data-ttu-id="96b84-129">Obtener información acerca de cuándo por última vez el elemento de ve y modifica el usuario.</span><span class="sxs-lookup"><span data-stu-id="96b84-129">Information about when the item was last viewed and modified by the user.</span></span> <span data-ttu-id="96b84-130">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="96b84-130">Read only.</span></span>     |
| <span data-ttu-id="96b84-131">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="96b84-131">resourceVisualization</span></span> | [<span data-ttu-id="96b84-132">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="96b84-132">resourceVisualization</span></span>](insights-resourcevisualization.md)                | <span data-ttu-id="96b84-133">Propiedades que puede usar para visualizar el documento en su experiencia.</span><span class="sxs-lookup"><span data-stu-id="96b84-133">Properties that you can use to visualize the document in your experience.</span></span> <span data-ttu-id="96b84-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96b84-134">Read-only</span></span>      |
| <span data-ttu-id="96b84-135">resourceReference</span><span class="sxs-lookup"><span data-stu-id="96b84-135">resourceReference</span></span>     | [<span data-ttu-id="96b84-136">resourceReference</span><span class="sxs-lookup"><span data-stu-id="96b84-136">resourceReference</span></span>](insights-resourcereference.md)                      | <span data-ttu-id="96b84-137">Propiedades de la referencia del documento usado, por ejemplo, la dirección url y el tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="96b84-137">Reference properties of the used document, such as the url and type of the document.</span></span> <span data-ttu-id="96b84-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96b84-138">Read-only</span></span>     |

## <a name="relationships"></a><span data-ttu-id="96b84-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="96b84-139">Relationships</span></span>

| <span data-ttu-id="96b84-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96b84-140">Property</span></span>      | <span data-ttu-id="96b84-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="96b84-141">Type</span></span>          | <span data-ttu-id="96b84-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="96b84-142">Description</span></span>  |
| ------------- |---------------| -------------|
| <span data-ttu-id="96b84-143">resource</span><span class="sxs-lookup"><span data-stu-id="96b84-143">resource</span></span>      | <span data-ttu-id="96b84-144">Entidad</span><span class="sxs-lookup"><span data-stu-id="96b84-144">Entity</span></span>        | <span data-ttu-id="96b84-145">Se usa para navegar hasta el elemento que se usó.</span><span class="sxs-lookup"><span data-stu-id="96b84-145">Used for navigating to the item that was used.</span></span> <span data-ttu-id="96b84-146">Los datos adjuntos de archivo, el tipo es *fileAttachment*.</span><span class="sxs-lookup"><span data-stu-id="96b84-146">For file attachments, the type is *fileAttachment*.</span></span> <span data-ttu-id="96b84-147">Los datos adjuntos vinculados, el tipo es *driveItem*.</span><span class="sxs-lookup"><span data-stu-id="96b84-147">For linked attachments, the type is *driveItem*.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="96b84-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="96b84-148">JSON representation</span></span>
<span data-ttu-id="96b84-149">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="96b84-149">Here is a JSON representation of the resource</span></span>

```json
{
  "id": "string",
  "lastUsed": "usageDetails",
  "resourceVisualization": "resourceVisualization",
  "resourceReference": "resourceReference",
  
  "resource": [ { "@odata.type": "microsoft.graph.entity" } ]
}
```
