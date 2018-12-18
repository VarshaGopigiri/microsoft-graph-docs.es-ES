---
title: tipo de recurso compartido
description: 'Una idea que representa los archivos compartidos con o por un usuario específico. Se admiten los siguientes archivos compartidos:'
author: simonhult
ms.openlocfilehash: fc48fe3c591d981bd6229c26aaccb85552f4836f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315809"
---
# <a name="shared-resource-type"></a><span data-ttu-id="11123-104">tipo de recurso compartido</span><span class="sxs-lookup"><span data-stu-id="11123-104">shared resource type</span></span>

> <span data-ttu-id="11123-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="11123-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="11123-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="11123-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="11123-107">Una idea que representa los archivos compartidos con o por un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="11123-107">An insight representing files shared with or by a specific user.</span></span> <span data-ttu-id="11123-108">Se admiten los siguientes archivos compartidos:</span><span class="sxs-lookup"><span data-stu-id="11123-108">The following shared files are supported:</span></span>

- <span data-ttu-id="11123-109">Invitar archivos adjuntos directamente en un correo electrónico o una reunión.</span><span class="sxs-lookup"><span data-stu-id="11123-109">Files attached directly in an email or a meeting invite.</span></span>
- <span data-ttu-id="11123-110">OneDrive para Bussiness y SharePoint moderno datos adjuntos - archivos almacenados en OneDrive para profesionales y SharePoint que los usuarios compartir como vínculos en un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="11123-110">OneDrive for Bussiness and SharePoint modern attachments - files stored in OneDrive for Business and SharePoint that users share as a links in an email.</span></span>

<span data-ttu-id="11123-111">**Nota**: actualmente estamos trabajando en rellenar los resultados de la API compartidos con datos.</span><span class="sxs-lookup"><span data-stu-id="11123-111">**Note**: We are currently working on populating the results of the Shared API with data.</span></span> <span data-ttu-id="11123-112">Puede haber algunos datos que faltan en las primeras semanas después del lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="11123-112">There may be some data missing in the first weeks after release.</span></span>

## <a name="methods"></a><span data-ttu-id="11123-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="11123-113">Methods</span></span>

| <span data-ttu-id="11123-114">Método</span><span class="sxs-lookup"><span data-stu-id="11123-114">Method</span></span>       | <span data-ttu-id="11123-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11123-115">Return Type</span></span>  |<span data-ttu-id="11123-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="11123-116">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="11123-117">Lista compartida</span><span class="sxs-lookup"><span data-stu-id="11123-117">List shared</span></span>](../api/insights-list-shared.md) |<span data-ttu-id="11123-118">colección de [insights_shared](insights-shared.md)</span><span class="sxs-lookup"><span data-stu-id="11123-118">[insights_shared](insights-shared.md) collection</span></span>| <span data-ttu-id="11123-119">Obtener una lista de los archivos compartidos.</span><span class="sxs-lookup"><span data-stu-id="11123-119">Get a list of shared files.</span></span>|

## <a name="properties"></a><span data-ttu-id="11123-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="11123-120">Properties</span></span>

| <span data-ttu-id="11123-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11123-121">Property</span></span>              | <span data-ttu-id="11123-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="11123-122">Type</span></span>                      | <span data-ttu-id="11123-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="11123-123">Description</span></span>  |
| -------------         |---------------            | -------------|
| <span data-ttu-id="11123-124">id</span><span class="sxs-lookup"><span data-stu-id="11123-124">id</span></span>                    | <span data-ttu-id="11123-125">String</span><span class="sxs-lookup"><span data-stu-id="11123-125">String</span></span>                    | <span data-ttu-id="11123-126">Identificador único de la relación.</span><span class="sxs-lookup"><span data-stu-id="11123-126">Unique identifier of the relationship.</span></span> <span data-ttu-id="11123-127">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="11123-127">Read only.</span></span>        |
| <span data-ttu-id="11123-128">lastShared</span><span class="sxs-lookup"><span data-stu-id="11123-128">lastShared</span></span>            | [<span data-ttu-id="11123-129">sharingDetail</span><span class="sxs-lookup"><span data-stu-id="11123-129">sharingDetail</span></span>](insights-sharingdetail.md)                | <span data-ttu-id="11123-130">Obtener información detallada sobre el elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="11123-130">Details about the shared item.</span></span> <span data-ttu-id="11123-131">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="11123-131">Read only.</span></span>        |
| <span data-ttu-id="11123-132">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="11123-132">resourceVisualization</span></span> | [<span data-ttu-id="11123-133">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="11123-133">resourceVisualization</span></span>](insights-resourcevisualization.md)                | <span data-ttu-id="11123-134">Propiedades que puede usar para visualizar el documento en su experiencia.</span><span class="sxs-lookup"><span data-stu-id="11123-134">Properties that you can use to visualize the document in your experience.</span></span> <span data-ttu-id="11123-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="11123-135">Read-only</span></span>      |
| <span data-ttu-id="11123-136">resourceReference</span><span class="sxs-lookup"><span data-stu-id="11123-136">resourceReference</span></span>     | [<span data-ttu-id="11123-137">resourceReference</span><span class="sxs-lookup"><span data-stu-id="11123-137">resourceReference</span></span>](insights-resourcereference.md)                      | <span data-ttu-id="11123-138">Propiedades de la referencia del documento compartido, como la dirección url y el tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="11123-138">Reference properties of the shared document, such as the url and type of the document.</span></span> <span data-ttu-id="11123-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="11123-139">Read-only</span></span>       |

## <a name="relationships"></a><span data-ttu-id="11123-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="11123-140">Relationships</span></span>

| <span data-ttu-id="11123-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="11123-141">Property</span></span>      | <span data-ttu-id="11123-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="11123-142">Type</span></span>          | <span data-ttu-id="11123-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="11123-143">Description</span></span>  |
| ------------- |---------------| -------------|
| <span data-ttu-id="11123-144">resource</span><span class="sxs-lookup"><span data-stu-id="11123-144">resource</span></span>      | <span data-ttu-id="11123-145">Entidad</span><span class="sxs-lookup"><span data-stu-id="11123-145">Entity</span></span>        | <span data-ttu-id="11123-146">Se usa para navegar hasta el elemento que se ha compartido.</span><span class="sxs-lookup"><span data-stu-id="11123-146">Used for navigating to the item that was shared.</span></span> <span data-ttu-id="11123-147">Los datos adjuntos de archivo, el tipo es *fileAttachment*.</span><span class="sxs-lookup"><span data-stu-id="11123-147">For file attachments, the type is *fileAttachment*.</span></span> <span data-ttu-id="11123-148">Los datos adjuntos vinculados, el tipo es *driveItem*.</span><span class="sxs-lookup"><span data-stu-id="11123-148">For linked attachments, the type is *driveItem*.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="11123-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="11123-149">JSON representation</span></span>
<span data-ttu-id="11123-150">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="11123-150">Here is a JSON representation of the resource</span></span>

```json
{
  "id": "string",
  "lastShared": "sharingDetail",
  "resourceVisualization": "resourceVisualization",
  "resourceReference": "resourceReference",
  
  "resource": [ { "@odata.type": "microsoft.graph.entity" } ]
}
```