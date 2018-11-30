---
title: tipo de recurso compartido
description: 'Una idea que representa los archivos compartidos con o por un usuario específico. Se admiten los siguientes archivos compartidos:'
ms.openlocfilehash: 786e3cc94a3c108b30cca880491dab5725014570
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088115"
---
# <a name="shared-resource-type"></a><span data-ttu-id="cbf95-104">tipo de recurso compartido</span><span class="sxs-lookup"><span data-stu-id="cbf95-104">shared resource type</span></span>

> <span data-ttu-id="cbf95-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cbf95-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cbf95-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cbf95-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cbf95-107">Una idea que representa los archivos compartidos con o por un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="cbf95-107">An insight representing files shared with or by a specific user.</span></span> <span data-ttu-id="cbf95-108">Se admiten los siguientes archivos compartidos:</span><span class="sxs-lookup"><span data-stu-id="cbf95-108">The following shared files are supported:</span></span>

- <span data-ttu-id="cbf95-109">Invitar archivos adjuntos directamente en un correo electrónico o una reunión.</span><span class="sxs-lookup"><span data-stu-id="cbf95-109">Files attached directly in an email or a meeting invite.</span></span>
- <span data-ttu-id="cbf95-110">OneDrive para Bussiness y SharePoint moderno datos adjuntos - archivos almacenados en OneDrive para profesionales y SharePoint que los usuarios compartir como vínculos en un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="cbf95-110">OneDrive for Bussiness and SharePoint modern attachments - files stored in OneDrive for Business and SharePoint that users share as a links in an email.</span></span>

<span data-ttu-id="cbf95-111">**Nota**: actualmente estamos trabajando en rellenar los resultados de la API compartidos con datos.</span><span class="sxs-lookup"><span data-stu-id="cbf95-111">**Note**: We are currently working on populating the results of the Shared API with data.</span></span> <span data-ttu-id="cbf95-112">Puede haber algunos datos que faltan en las primeras semanas después del lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="cbf95-112">There may be some data missing in the first weeks after release.</span></span>

## <a name="methods"></a><span data-ttu-id="cbf95-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="cbf95-113">Methods</span></span>

| <span data-ttu-id="cbf95-114">Método</span><span class="sxs-lookup"><span data-stu-id="cbf95-114">Method</span></span>       | <span data-ttu-id="cbf95-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbf95-115">Return Type</span></span>  |<span data-ttu-id="cbf95-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbf95-116">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="cbf95-117">Lista compartida</span><span class="sxs-lookup"><span data-stu-id="cbf95-117">List shared</span></span>](../api/insights-list-shared.md) |<span data-ttu-id="cbf95-118">colección de [insights_shared](insights-shared.md)</span><span class="sxs-lookup"><span data-stu-id="cbf95-118">[insights_shared](insights-shared.md) collection</span></span>| <span data-ttu-id="cbf95-119">Obtener una lista de los archivos compartidos.</span><span class="sxs-lookup"><span data-stu-id="cbf95-119">Get a list of shared files.</span></span>|

## <a name="properties"></a><span data-ttu-id="cbf95-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cbf95-120">Properties</span></span>

| <span data-ttu-id="cbf95-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cbf95-121">Property</span></span>              | <span data-ttu-id="cbf95-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbf95-122">Type</span></span>                      | <span data-ttu-id="cbf95-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbf95-123">Description</span></span>  |
| -------------         |---------------            | -------------|
| <span data-ttu-id="cbf95-124">id</span><span class="sxs-lookup"><span data-stu-id="cbf95-124">id</span></span>                    | <span data-ttu-id="cbf95-125">String</span><span class="sxs-lookup"><span data-stu-id="cbf95-125">String</span></span>                    | <span data-ttu-id="cbf95-126">Identificador único de la relación.</span><span class="sxs-lookup"><span data-stu-id="cbf95-126">Unique identifier of the relationship.</span></span> <span data-ttu-id="cbf95-127">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cbf95-127">Read only.</span></span>        |
| <span data-ttu-id="cbf95-128">lastShared</span><span class="sxs-lookup"><span data-stu-id="cbf95-128">lastShared</span></span>            | [<span data-ttu-id="cbf95-129">sharingDetail</span><span class="sxs-lookup"><span data-stu-id="cbf95-129">sharingDetail</span></span>](insights-sharingdetail.md)                | <span data-ttu-id="cbf95-130">Obtener información detallada sobre el elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="cbf95-130">Details about the shared item.</span></span> <span data-ttu-id="cbf95-131">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cbf95-131">Read only.</span></span>        |
| <span data-ttu-id="cbf95-132">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="cbf95-132">resourceVisualization</span></span> | [<span data-ttu-id="cbf95-133">resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="cbf95-133">resourceVisualization</span></span>](insights-resourcevisualization.md)                | <span data-ttu-id="cbf95-134">Propiedades que puede usar para visualizar el documento en su experiencia.</span><span class="sxs-lookup"><span data-stu-id="cbf95-134">Properties that you can use to visualize the document in your experience.</span></span> <span data-ttu-id="cbf95-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="cbf95-135">Read-only</span></span>      |
| <span data-ttu-id="cbf95-136">resourceReference</span><span class="sxs-lookup"><span data-stu-id="cbf95-136">resourceReference</span></span>     | [<span data-ttu-id="cbf95-137">resourceReference</span><span class="sxs-lookup"><span data-stu-id="cbf95-137">resourceReference</span></span>](insights-resourcereference.md)                      | <span data-ttu-id="cbf95-138">Propiedades de la referencia del documento compartido, como la dirección url y el tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="cbf95-138">Reference properties of the shared document, such as the url and type of the document.</span></span> <span data-ttu-id="cbf95-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="cbf95-139">Read-only</span></span>       |

## <a name="relationships"></a><span data-ttu-id="cbf95-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cbf95-140">Relationships</span></span>

| <span data-ttu-id="cbf95-141">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cbf95-141">Property</span></span>      | <span data-ttu-id="cbf95-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbf95-142">Type</span></span>          | <span data-ttu-id="cbf95-143">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbf95-143">Description</span></span>  |
| ------------- |---------------| -------------|
| <span data-ttu-id="cbf95-144">resource</span><span class="sxs-lookup"><span data-stu-id="cbf95-144">resource</span></span>      | <span data-ttu-id="cbf95-145">Entidad</span><span class="sxs-lookup"><span data-stu-id="cbf95-145">Entity</span></span>        | <span data-ttu-id="cbf95-146">Se usa para navegar hasta el elemento que se ha compartido.</span><span class="sxs-lookup"><span data-stu-id="cbf95-146">Used for navigating to the item that was shared.</span></span> <span data-ttu-id="cbf95-147">Los datos adjuntos de archivo, el tipo es *fileAttachment*.</span><span class="sxs-lookup"><span data-stu-id="cbf95-147">For file attachments, the type is *fileAttachment*.</span></span> <span data-ttu-id="cbf95-148">Los datos adjuntos vinculados, el tipo es *driveItem*.</span><span class="sxs-lookup"><span data-stu-id="cbf95-148">For linked attachments, the type is *driveItem*.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="cbf95-149">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cbf95-149">JSON representation</span></span>
<span data-ttu-id="cbf95-150">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="cbf95-150">Here is a JSON representation of the resource</span></span>

```json
{
  "id": "string",
  "lastShared": "sharingDetail",
  "resourceVisualization": "resourceVisualization",
  "resourceReference": "resourceReference",
  
  "resource": [ { "@odata.type": "microsoft.graph.entity" } ]
}
```