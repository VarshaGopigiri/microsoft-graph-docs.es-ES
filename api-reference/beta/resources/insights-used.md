---
title: utiliza el tipo de recurso
description: 'Una idea que representa documentos usados por un usuario específico. Los conocimientos devuelve los documentos más importantes que se pueden ve ni tener acceso a un usuario. Esto incluye documentos en:'
ms.openlocfilehash: 3c82d268a67ef52d0ddfdad9193558080048ad6b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088995"
---
# <a name="used-resource-type"></a><span data-ttu-id="423d9-105">utiliza el tipo de recurso</span><span class="sxs-lookup"><span data-stu-id="423d9-105">used resource type</span></span>

> <span data-ttu-id="423d9-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="423d9-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="423d9-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="423d9-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="423d9-108">Una idea que representa documentos usados por un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="423d9-108">An insight representing documents used by a specific user.</span></span> <span data-ttu-id="423d9-109">Los conocimientos devuelve los documentos más importantes que se pueden ve ni tener acceso a un usuario.</span><span class="sxs-lookup"><span data-stu-id="423d9-109">The insights returns the most relevant documents that a user viewed or accessed.</span></span> <span data-ttu-id="423d9-110">Esto incluye documentos en:</span><span class="sxs-lookup"><span data-stu-id="423d9-110">This includes documents in:</span></span>

- <span data-ttu-id="423d9-111">OneDrive para la Empresa</span><span class="sxs-lookup"><span data-stu-id="423d9-111">OneDrive for Business</span></span>
- <span data-ttu-id="423d9-112">SharePoint</span><span class="sxs-lookup"><span data-stu-id="423d9-112">SharePoint</span></span>

## <a name="methods"></a><span data-ttu-id="423d9-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="423d9-113">Methods</span></span>

| <span data-ttu-id="423d9-114">Método</span><span class="sxs-lookup"><span data-stu-id="423d9-114">Method</span></span>       | <span data-ttu-id="423d9-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="423d9-115">Return Type</span></span>  |<span data-ttu-id="423d9-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="423d9-116">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="423d9-117">Lista usada</span><span class="sxs-lookup"><span data-stu-id="423d9-117">List used</span></span>](../api/insights-list-used.md) |<span data-ttu-id="423d9-118">colección de [insights_used](insights-used.md)</span><span class="sxs-lookup"><span data-stu-id="423d9-118">[insights_used](insights-used.md) collection</span></span>| <span data-ttu-id="423d9-119">Obtener una lista de archivos usados.</span><span class="sxs-lookup"><span data-stu-id="423d9-119">Get a list of used files.</span></span>|

## <a name="properties"></a><span data-ttu-id="423d9-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="423d9-120">Properties</span></span>

| <span data-ttu-id="423d9-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="423d9-121">Property</span></span>              | <span data-ttu-id="423d9-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="423d9-122">Type</span></span>                      | <span data-ttu-id="423d9-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="423d9-123">Description</span></span>  |
| -------------         |---------------            | -------------|
| <span data-ttu-id="423d9-124">id</span><span class="sxs-lookup"><span data-stu-id="423d9-124">id</span></span>                    | <span data-ttu-id="423d9-125">String</span><span class="sxs-lookup"><span data-stu-id="423d9-125">String</span></span>                    | <span data-ttu-id="423d9-126">Identificador único de la relación.</span><span class="sxs-lookup"><span data-stu-id="423d9-126">Unique identifier of the relationship.</span></span> <span data-ttu-id="423d9-127">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="423d9-127">Read only.</span></span>        |
| <span data-ttu-id="423d9-128">lastUsed</span><span class="sxs-lookup"><span data-stu-id="423d9-128">lastUsed</span></span>              | [<span data-ttu-id="423d9-129">usageDetails</span><span class="sxs-lookup"><span data-stu-id="423d9-129">usageDetails</span></span>](insights-usagedetails.md)              | <span data-ttu-id="423d9-130">Obtener información acerca de cuándo por última vez el elemento de ve y modifica el usuario.</span><span class="sxs-lookup"><span data-stu-id="423d9-130">Information about when the item was last viewed and modified by the user.</span></span> <span data-ttu-id="423d9-131">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="423d9-131">Read only.</span></span>     |
| <span data-ttu-id="423d9-132">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="423d9-132">resourceVisualization</span></span> | [<span data-ttu-id="423d9-133">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="423d9-133">resourceVisualization</span></span>](insights-resourcevisualization.md)                | <span data-ttu-id="423d9-134">Propiedades que puede usar para visualizar el documento en su experiencia.</span><span class="sxs-lookup"><span data-stu-id="423d9-134">Properties that you can use to visualize the document in your experience.</span></span> <span data-ttu-id="423d9-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="423d9-135">Read-only</span></span>      |
| <span data-ttu-id="423d9-136">resourceReference</span><span class="sxs-lookup"><span data-stu-id="423d9-136">resourceReference</span></span>     | [<span data-ttu-id="423d9-137">resourceReference</span><span class="sxs-lookup"><span data-stu-id="423d9-137">resourceReference</span></span>](insights-resourcereference.md)                      | <span data-ttu-id="423d9-138">Propiedades de la referencia del documento usado, por ejemplo, la dirección url y el tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="423d9-138">Reference properties of the used document, such as the url and type of the document.</span></span> <span data-ttu-id="423d9-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="423d9-139">Read-only</span></span>     |

## <a name="relationships"></a><span data-ttu-id="423d9-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="423d9-140">Relationships</span></span>

| <span data-ttu-id="423d9-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="423d9-141">Property</span></span>      | <span data-ttu-id="423d9-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="423d9-142">Type</span></span>          | <span data-ttu-id="423d9-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="423d9-143">Description</span></span>  |
| ------------- |---------------| -------------|
| <span data-ttu-id="423d9-144">resource</span><span class="sxs-lookup"><span data-stu-id="423d9-144">resource</span></span>      | <span data-ttu-id="423d9-145">Entidad</span><span class="sxs-lookup"><span data-stu-id="423d9-145">Entity</span></span>        | <span data-ttu-id="423d9-146">Se usa para navegar hasta el elemento que se usó.</span><span class="sxs-lookup"><span data-stu-id="423d9-146">Used for navigating to the item that was used.</span></span> <span data-ttu-id="423d9-147">Los datos adjuntos de archivo, el tipo es *fileAttachment*.</span><span class="sxs-lookup"><span data-stu-id="423d9-147">For file attachments, the type is *fileAttachment*.</span></span> <span data-ttu-id="423d9-148">Los datos adjuntos vinculados, el tipo es *driveItem*.</span><span class="sxs-lookup"><span data-stu-id="423d9-148">For linked attachments, the type is *driveItem*.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="423d9-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="423d9-149">JSON representation</span></span>
<span data-ttu-id="423d9-150">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="423d9-150">Here is a JSON representation of the resource</span></span>

```json
{
  "id": "string",
  "lastUsed": "usageDetails",
  "resourceVisualization": "resourceVisualization",
  "resourceReference": "resourceReference",
  
  "resource": [ { "@odata.type": "microsoft.graph.entity" } ]
}
```