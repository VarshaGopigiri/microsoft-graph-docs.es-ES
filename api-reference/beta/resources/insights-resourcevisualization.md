---
title: tipo de recurso resourceVisualization
description: Tipo complejo que contiene las propiedades de conocimientos.
author: simonhult
ms.openlocfilehash: d0c54895468fc9a01017e448df57c09c654616e9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27333540"
---
# <a name="resourcevisualization-resource-type"></a><span data-ttu-id="947e1-103">tipo de recurso resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="947e1-103">resourceVisualization resource type</span></span>

> <span data-ttu-id="947e1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="947e1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="947e1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="947e1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="947e1-106">Tipo complejo que contiene las propiedades de [conocimientos](insights.md).</span><span class="sxs-lookup"><span data-stu-id="947e1-106">Complex type containing properties of [Insights](insights.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="947e1-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="947e1-107">JSON representation</span></span>

<span data-ttu-id="947e1-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="947e1-108">Here is a JSON representation of the resource</span></span>

```json
{
  "title": "string",
  "type"  : "string",
  "mediaType": "string",
  "previewImageUrl": "string",
  "previewText": "string",
  "containerWebUrl": "string",
  "containerDisplayName": "string",
  "containerType": "string"
}
```

## <a name="properties"></a><span data-ttu-id="947e1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="947e1-109">Properties</span></span>

| <span data-ttu-id="947e1-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="947e1-110">Property</span></span>              | <span data-ttu-id="947e1-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="947e1-111">Type</span></span>          | <span data-ttu-id="947e1-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="947e1-112">Description</span></span>  |
| -------------         |---------------| -------------|
| <span data-ttu-id="947e1-113">title</span><span class="sxs-lookup"><span data-stu-id="947e1-113">title</span></span>                 | <span data-ttu-id="947e1-114">String</span><span class="sxs-lookup"><span data-stu-id="947e1-114">String</span></span>        | <span data-ttu-id="947e1-115">Texto del título del elemento.</span><span class="sxs-lookup"><span data-stu-id="947e1-115">The item's title text.</span></span>               |
| <span data-ttu-id="947e1-116">type</span><span class="sxs-lookup"><span data-stu-id="947e1-116">type</span></span>              | <span data-ttu-id="947e1-117">String</span><span class="sxs-lookup"><span data-stu-id="947e1-117">String</span></span>        | <span data-ttu-id="947e1-118">El tipo del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="947e1-118">The item's media type.</span></span> <span data-ttu-id="947e1-119">Se puede usar para el filtrado para un archivo específico en función de un tipo específico.</span><span class="sxs-lookup"><span data-stu-id="947e1-119">Can be used for filtering for a specific file based on a specific type.</span></span> <span data-ttu-id="947e1-120">Vea más adelante para tipos compatibles.</span><span class="sxs-lookup"><span data-stu-id="947e1-120">See below for supported types.</span></span> |
| <span data-ttu-id="947e1-121">mediaType</span><span class="sxs-lookup"><span data-stu-id="947e1-121">mediaType</span></span>             | <span data-ttu-id="947e1-122">String</span><span class="sxs-lookup"><span data-stu-id="947e1-122">String</span></span>        | <span data-ttu-id="947e1-123">El tipo del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="947e1-123">The item's media type.</span></span> <span data-ttu-id="947e1-124">Se puede usar para el filtrado de un tipo específico de archivo basado en tipos de Mime de medios IANA compatibles.</span><span class="sxs-lookup"><span data-stu-id="947e1-124">Can be used for for filtering for a specific type of file based on supported IANA Media Mime Types.</span></span> <span data-ttu-id="947e1-125">Tenga en cuenta que no todos los tipos Mime de medios son compatibles.</span><span class="sxs-lookup"><span data-stu-id="947e1-125">Note that not all Media Mime Types are supported.</span></span> |
| <span data-ttu-id="947e1-126">previewImageUrl</span><span class="sxs-lookup"><span data-stu-id="947e1-126">previewImageUrl</span></span>       | <span data-ttu-id="947e1-127">String</span><span class="sxs-lookup"><span data-stu-id="947e1-127">String</span></span>        | <span data-ttu-id="947e1-128">Una dirección URL conduce a la imagen de vista previa para el elemento.</span><span class="sxs-lookup"><span data-stu-id="947e1-128">A URL leading to the preview image for the item.</span></span> |
| <span data-ttu-id="947e1-129">previewText</span><span class="sxs-lookup"><span data-stu-id="947e1-129">previewText</span></span>           | <span data-ttu-id="947e1-130">String</span><span class="sxs-lookup"><span data-stu-id="947e1-130">String</span></span>        | <span data-ttu-id="947e1-131">Una vista previa de texto para el elemento.</span><span class="sxs-lookup"><span data-stu-id="947e1-131">A preview text for the item.</span></span> |
| <span data-ttu-id="947e1-132">containerWebUrl</span><span class="sxs-lookup"><span data-stu-id="947e1-132">containerWebUrl</span></span>       | <span data-ttu-id="947e1-133">String</span><span class="sxs-lookup"><span data-stu-id="947e1-133">String</span></span>        | <span data-ttu-id="947e1-134">Una ruta de acceso que conduce a la carpeta en la que está almacenado el artículo.</span><span class="sxs-lookup"><span data-stu-id="947e1-134">A path leading to the folder in which the item is stored.</span></span> |
| <span data-ttu-id="947e1-135">containerDisplayName</span><span class="sxs-lookup"><span data-stu-id="947e1-135">containerDisplayName</span></span>  | <span data-ttu-id="947e1-136">String</span><span class="sxs-lookup"><span data-stu-id="947e1-136">String</span></span>        | <span data-ttu-id="947e1-137">Una cadena que describe donde está almacenado el artículo.</span><span class="sxs-lookup"><span data-stu-id="947e1-137">A string describing where the item is stored.</span></span> <span data-ttu-id="947e1-138">Por ejemplo, el nombre de un sitio de SharePoint o el nombre de usuario que identifica el propietario de la OneDrive para almacenar el elemento.</span><span class="sxs-lookup"><span data-stu-id="947e1-138">For example, the name of a SharePoint site or the user name identifying the owner of the OneDrive storing the item.</span></span>  |
| <span data-ttu-id="947e1-139">containerType</span><span class="sxs-lookup"><span data-stu-id="947e1-139">containerType</span></span>         | <span data-ttu-id="947e1-140">String</span><span class="sxs-lookup"><span data-stu-id="947e1-140">String</span></span> | <span data-ttu-id="947e1-141">Se puede usar para filtrar por el tipo de contenedor en el que se almacena el archivo.</span><span class="sxs-lookup"><span data-stu-id="947e1-141">Can be used for filtering by the type of container in which the file is stored.</span></span> <span data-ttu-id="947e1-142">Por ejemplo, sitio o OneDriveBusiness.</span><span class="sxs-lookup"><span data-stu-id="947e1-142">Such as Site or OneDriveBusiness.</span></span>       |

## <a name="type-property-values"></a><span data-ttu-id="947e1-143">Valores de propiedad de tipo</span><span class="sxs-lookup"><span data-stu-id="947e1-143">Type property values</span></span>
-   <span data-ttu-id="947e1-144">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="947e1-144">PowerPoint</span></span>
-   <span data-ttu-id="947e1-145">Word</span><span class="sxs-lookup"><span data-stu-id="947e1-145">Word</span></span>
-   <span data-ttu-id="947e1-146">Excel</span><span class="sxs-lookup"><span data-stu-id="947e1-146">Excel</span></span>
-   <span data-ttu-id="947e1-147">PDF</span><span class="sxs-lookup"><span data-stu-id="947e1-147">Pdf</span></span>
-   <span data-ttu-id="947e1-148">OneNote</span><span class="sxs-lookup"><span data-stu-id="947e1-148">OneNote</span></span>
-   <span data-ttu-id="947e1-149">OneNotePage</span><span class="sxs-lookup"><span data-stu-id="947e1-149">OneNotePage</span></span>
-   <span data-ttu-id="947e1-150">InfoPath</span><span class="sxs-lookup"><span data-stu-id="947e1-150">InfoPath</span></span>
-   <span data-ttu-id="947e1-151">Visio</span><span class="sxs-lookup"><span data-stu-id="947e1-151">Visio</span></span>
-   <span data-ttu-id="947e1-152">Publisher</span><span class="sxs-lookup"><span data-stu-id="947e1-152">Publisher</span></span>
-   <span data-ttu-id="947e1-153">Project</span><span class="sxs-lookup"><span data-stu-id="947e1-153">Project</span></span>
-   <span data-ttu-id="947e1-154">Access</span><span class="sxs-lookup"><span data-stu-id="947e1-154">Access</span></span>
-   <span data-ttu-id="947e1-155">Correo</span><span class="sxs-lookup"><span data-stu-id="947e1-155">Mail</span></span>
-   <span data-ttu-id="947e1-156">CSV</span><span class="sxs-lookup"><span data-stu-id="947e1-156">Csv</span></span>
-   <span data-ttu-id="947e1-157">Archivo</span><span class="sxs-lookup"><span data-stu-id="947e1-157">Archive</span></span>
-   <span data-ttu-id="947e1-158">Xps</span><span class="sxs-lookup"><span data-stu-id="947e1-158">Xps</span></span>
-   <span data-ttu-id="947e1-159">Audio</span><span class="sxs-lookup"><span data-stu-id="947e1-159">Audio</span></span>
-   <span data-ttu-id="947e1-160">Vídeo</span><span class="sxs-lookup"><span data-stu-id="947e1-160">Video</span></span>
-   <span data-ttu-id="947e1-161">Image (Imagen)</span><span class="sxs-lookup"><span data-stu-id="947e1-161">Image</span></span>
-   <span data-ttu-id="947e1-162">Web</span><span class="sxs-lookup"><span data-stu-id="947e1-162">Web</span></span>
-   <span data-ttu-id="947e1-163">Texto</span><span class="sxs-lookup"><span data-stu-id="947e1-163">Text</span></span>
-   <span data-ttu-id="947e1-164">Xml</span><span class="sxs-lookup"><span data-stu-id="947e1-164">Xml</span></span>
-   <span data-ttu-id="947e1-165">Story</span><span class="sxs-lookup"><span data-stu-id="947e1-165">Story</span></span>
-   <span data-ttu-id="947e1-166">ExternalContent</span><span class="sxs-lookup"><span data-stu-id="947e1-166">ExternalContent</span></span>
-   <span data-ttu-id="947e1-167">Folder</span><span class="sxs-lookup"><span data-stu-id="947e1-167">Folder</span></span>
-   <span data-ttu-id="947e1-168">Otros</span><span class="sxs-lookup"><span data-stu-id="947e1-168">Other</span></span>

<span data-ttu-id="947e1-169">Consulta de ejemplo:`https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/Type eq 'PowerPoint'`</span><span class="sxs-lookup"><span data-stu-id="947e1-169">Example query: `https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/Type eq 'PowerPoint'`</span></span>

## <a name="containertype-property-values"></a><span data-ttu-id="947e1-170">valores de la propiedad containerType</span><span class="sxs-lookup"><span data-stu-id="947e1-170">containerType property values</span></span>
<span data-ttu-id="947e1-171">Los tipos admitidos pueden variar en función de en los contenedores desde la que el [entendimiento](insights.md) devuelve los archivos.</span><span class="sxs-lookup"><span data-stu-id="947e1-171">The supported types can differ based on containers from which the [Insight](insights.md) returns files.</span></span> <span data-ttu-id="947e1-172">Por ejemplo, solo los conocimientos [compartidos](insights-shared.md) devuelve los archivos de 'Lista desplegable', 'Cuadro' y 'GDrive'.</span><span class="sxs-lookup"><span data-stu-id="947e1-172">For example, only the [Shared](insights-shared.md) insight returns files from 'DropBox', 'Box', and 'GDrive'.</span></span>

-   <span data-ttu-id="947e1-173">OneDriveBusiness</span><span class="sxs-lookup"><span data-stu-id="947e1-173">OneDriveBusiness</span></span>
-   <span data-ttu-id="947e1-174">Site</span><span class="sxs-lookup"><span data-stu-id="947e1-174">Site</span></span>
-   <span data-ttu-id="947e1-175">Correo</span><span class="sxs-lookup"><span data-stu-id="947e1-175">Mail</span></span>
-   <span data-ttu-id="947e1-176">Lista desplegable</span><span class="sxs-lookup"><span data-stu-id="947e1-176">DropBox</span></span>
-   <span data-ttu-id="947e1-177">Cuadro</span><span class="sxs-lookup"><span data-stu-id="947e1-177">Box</span></span>
-   <span data-ttu-id="947e1-178">GDrive</span><span class="sxs-lookup"><span data-stu-id="947e1-178">GDrive</span></span>

<span data-ttu-id="947e1-179">Consulta de ejemplo:`https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/containerType eq 'OneDriveBusiness'`</span><span class="sxs-lookup"><span data-stu-id="947e1-179">Example query: `https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/containerType eq 'OneDriveBusiness'`</span></span>