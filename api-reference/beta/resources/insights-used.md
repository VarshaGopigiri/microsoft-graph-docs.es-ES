---
title: utiliza el tipo de recurso
description: Una idea que representa documentos usados por un usuario específico. Los conocimientos devuelve los documentos más importantes que se pueden ve ni tener acceso a un usuario.
author: simonhult
ms.openlocfilehash: 89eac33ad954905c77a26df669bb15a2cf471edd
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27323488"
---
# <a name="used-resource-type"></a><span data-ttu-id="27b68-104">utiliza el tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="27b68-104">used resource type</span></span>

> <span data-ttu-id="27b68-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="27b68-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="27b68-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="27b68-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="27b68-107">Una idea que representa documentos usados por un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="27b68-107">An insight representing documents used by a specific user.</span></span> <span data-ttu-id="27b68-108">Los conocimientos devuelve los documentos más importantes que se pueden ve ni tener acceso a un usuario.</span><span class="sxs-lookup"><span data-stu-id="27b68-108">The insights returns the most relevant documents that a user viewed or accessed.</span></span> <span data-ttu-id="27b68-109">Esto incluye documentos en:</span><span class="sxs-lookup"><span data-stu-id="27b68-109">This includes documents in:</span></span>

- <span data-ttu-id="27b68-110">OneDrive para la Empresa</span><span class="sxs-lookup"><span data-stu-id="27b68-110">OneDrive for Business</span></span>
- <span data-ttu-id="27b68-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="27b68-111">SharePoint</span></span>

## <a name="methods"></a><span data-ttu-id="27b68-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="27b68-112">Methods</span></span>

| <span data-ttu-id="27b68-113">Método</span><span class="sxs-lookup"><span data-stu-id="27b68-113">Method</span></span>       | <span data-ttu-id="27b68-114">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="27b68-114">Return Type</span></span>  |<span data-ttu-id="27b68-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="27b68-115">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="27b68-116">Lista usada</span><span class="sxs-lookup"><span data-stu-id="27b68-116">List used</span></span>](../api/insights-list-used.md) |<span data-ttu-id="27b68-117">colección de [insights_used](insights-used.md)</span><span class="sxs-lookup"><span data-stu-id="27b68-117">[insights_used](insights-used.md) collection</span></span>| <span data-ttu-id="27b68-118">Obtener una lista de archivos usados.</span><span class="sxs-lookup"><span data-stu-id="27b68-118">Get a list of used files.</span></span>|

## <a name="properties"></a><span data-ttu-id="27b68-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27b68-119">Properties</span></span>

| <span data-ttu-id="27b68-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27b68-120">Property</span></span>              | <span data-ttu-id="27b68-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="27b68-121">Type</span></span>                      | <span data-ttu-id="27b68-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="27b68-122">Description</span></span>  |
| -------------         |---------------            | -------------|
| <span data-ttu-id="27b68-123">id</span><span class="sxs-lookup"><span data-stu-id="27b68-123">id</span></span>                    | <span data-ttu-id="27b68-124">String</span><span class="sxs-lookup"><span data-stu-id="27b68-124">String</span></span>                    | <span data-ttu-id="27b68-125">Identificador único de la relación.</span><span class="sxs-lookup"><span data-stu-id="27b68-125">Unique identifier of the relationship.</span></span> <span data-ttu-id="27b68-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27b68-126">Read only.</span></span>        |
| <span data-ttu-id="27b68-127">lastUsed</span><span class="sxs-lookup"><span data-stu-id="27b68-127">lastUsed</span></span>              | [<span data-ttu-id="27b68-128">usageDetails</span><span class="sxs-lookup"><span data-stu-id="27b68-128">usageDetails</span></span>](insights-usagedetails.md)              | <span data-ttu-id="27b68-129">Obtener información acerca de cuándo por última vez el elemento de ve y modifica el usuario.</span><span class="sxs-lookup"><span data-stu-id="27b68-129">Information about when the item was last viewed and modified by the user.</span></span> <span data-ttu-id="27b68-130">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="27b68-130">Read only.</span></span>     |
| <span data-ttu-id="27b68-131">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="27b68-131">resourceVisualization</span></span> | [<span data-ttu-id="27b68-132">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="27b68-132">resourceVisualization</span></span>](insights-resourcevisualization.md)                | <span data-ttu-id="27b68-133">Propiedades que puede usar para visualizar el documento en su experiencia.</span><span class="sxs-lookup"><span data-stu-id="27b68-133">Properties that you can use to visualize the document in your experience.</span></span> <span data-ttu-id="27b68-134">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b68-134">Read-only</span></span>      |
| <span data-ttu-id="27b68-135">resourceReference</span><span class="sxs-lookup"><span data-stu-id="27b68-135">resourceReference</span></span>     | [<span data-ttu-id="27b68-136">resourceReference</span><span class="sxs-lookup"><span data-stu-id="27b68-136">resourceReference</span></span>](insights-resourcereference.md)                      | <span data-ttu-id="27b68-137">Propiedades de la referencia del documento usado, por ejemplo, la dirección url y el tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="27b68-137">Reference properties of the used document, such as the url and type of the document.</span></span> <span data-ttu-id="27b68-138">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="27b68-138">Read-only</span></span>     |

## <a name="relationships"></a><span data-ttu-id="27b68-139">Relaciones</span><span class="sxs-lookup"><span data-stu-id="27b68-139">Relationships</span></span>

| <span data-ttu-id="27b68-140">Propiedad</span><span class="sxs-lookup"><span data-stu-id="27b68-140">Property</span></span>      | <span data-ttu-id="27b68-141">Tipo</span><span class="sxs-lookup"><span data-stu-id="27b68-141">Type</span></span>          | <span data-ttu-id="27b68-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="27b68-142">Description</span></span>  |
| ------------- |---------------| -------------|
| <span data-ttu-id="27b68-143">resource</span><span class="sxs-lookup"><span data-stu-id="27b68-143">resource</span></span>      | <span data-ttu-id="27b68-144">Entidad</span><span class="sxs-lookup"><span data-stu-id="27b68-144">Entity</span></span>        | <span data-ttu-id="27b68-145">Se usa para navegar hasta el elemento que se usó.</span><span class="sxs-lookup"><span data-stu-id="27b68-145">Used for navigating to the item that was used.</span></span> <span data-ttu-id="27b68-146">Los datos adjuntos de archivo, el tipo es *fileAttachment*.</span><span class="sxs-lookup"><span data-stu-id="27b68-146">For file attachments, the type is *fileAttachment*.</span></span> <span data-ttu-id="27b68-147">Los datos adjuntos vinculados, el tipo es *driveItem*.</span><span class="sxs-lookup"><span data-stu-id="27b68-147">For linked attachments, the type is *driveItem*.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="27b68-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="27b68-148">JSON representation</span></span>
<span data-ttu-id="27b68-149">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="27b68-149">Here is a JSON representation of the resource</span></span>

```json
{
  "id": "string",
  "lastUsed": "usageDetails",
  "resourceVisualization": "resourceVisualization",
  "resourceReference": "resourceReference",
  
  "resource": [ { "@odata.type": "microsoft.graph.entity" } ]
}
```