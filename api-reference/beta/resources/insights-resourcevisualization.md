---
title: tipo de recurso resourceVisualization
description: Tipo complejo que contiene las propiedades de conocimientos.
ms.openlocfilehash: 3ed61a8547e072938fc073d90f2592baf4c08fba
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088207"
---
# <a name="resourcevisualization-resource-type"></a><span data-ttu-id="52941-103">tipo de recurso resourceVisualization</span><span class="sxs-lookup"><span data-stu-id="52941-103">resourceVisualization resource type</span></span>

> <span data-ttu-id="52941-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="52941-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="52941-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="52941-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="52941-106">Tipo complejo que contiene las propiedades de [conocimientos](insights.md).</span><span class="sxs-lookup"><span data-stu-id="52941-106">Complex type containing properties of [Insights](insights.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="52941-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="52941-107">JSON representation</span></span>

<span data-ttu-id="52941-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="52941-108">Here is a JSON representation of the resource</span></span>

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

## <a name="properties"></a><span data-ttu-id="52941-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="52941-109">Properties</span></span>

| <span data-ttu-id="52941-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="52941-110">Property</span></span>              | <span data-ttu-id="52941-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="52941-111">Type</span></span>          | <span data-ttu-id="52941-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="52941-112">Description</span></span>  |
| -------------         |---------------| -------------|
| <span data-ttu-id="52941-113">title</span><span class="sxs-lookup"><span data-stu-id="52941-113">title</span></span>                 | <span data-ttu-id="52941-114">String</span><span class="sxs-lookup"><span data-stu-id="52941-114">String</span></span>        | <span data-ttu-id="52941-115">Texto del título del elemento.</span><span class="sxs-lookup"><span data-stu-id="52941-115">The item's title text.</span></span>               |
| <span data-ttu-id="52941-116">type</span><span class="sxs-lookup"><span data-stu-id="52941-116">type</span></span>              | <span data-ttu-id="52941-117">String</span><span class="sxs-lookup"><span data-stu-id="52941-117">String</span></span>        | <span data-ttu-id="52941-118">El tipo del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="52941-118">The item's media type.</span></span> <span data-ttu-id="52941-119">Se puede usar para el filtrado para un archivo específico en función de un tipo específico.</span><span class="sxs-lookup"><span data-stu-id="52941-119">Can be used for filtering for a specific file based on a specific type.</span></span> <span data-ttu-id="52941-120">Vea más adelante para tipos compatibles.</span><span class="sxs-lookup"><span data-stu-id="52941-120">See below for supported types.</span></span> |
| <span data-ttu-id="52941-121">mediaType</span><span class="sxs-lookup"><span data-stu-id="52941-121">mediaType</span></span>             | <span data-ttu-id="52941-122">String</span><span class="sxs-lookup"><span data-stu-id="52941-122">String</span></span>        | <span data-ttu-id="52941-123">El tipo del elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="52941-123">The item's media type.</span></span> <span data-ttu-id="52941-124">Se puede usar para el filtrado de un tipo específico de archivo basado en tipos de Mime de medios IANA compatibles.</span><span class="sxs-lookup"><span data-stu-id="52941-124">Can be used for for filtering for a specific type of file based on supported IANA Media Mime Types.</span></span> <span data-ttu-id="52941-125">Tenga en cuenta que no todos los tipos Mime de medios son compatibles.</span><span class="sxs-lookup"><span data-stu-id="52941-125">Note that not all Media Mime Types are supported.</span></span> |
| <span data-ttu-id="52941-126">previewImageUrl</span><span class="sxs-lookup"><span data-stu-id="52941-126">previewImageUrl</span></span>       | <span data-ttu-id="52941-127">String</span><span class="sxs-lookup"><span data-stu-id="52941-127">String</span></span>        | <span data-ttu-id="52941-128">Una dirección URL conduce a la imagen de vista previa para el elemento.</span><span class="sxs-lookup"><span data-stu-id="52941-128">A URL leading to the preview image for the item.</span></span> |
| <span data-ttu-id="52941-129">previewText</span><span class="sxs-lookup"><span data-stu-id="52941-129">previewText</span></span>           | <span data-ttu-id="52941-130">String</span><span class="sxs-lookup"><span data-stu-id="52941-130">String</span></span>        | <span data-ttu-id="52941-131">Una vista previa de texto para el elemento.</span><span class="sxs-lookup"><span data-stu-id="52941-131">A preview text for the item.</span></span> |
| <span data-ttu-id="52941-132">containerWebUrl</span><span class="sxs-lookup"><span data-stu-id="52941-132">containerWebUrl</span></span>       | <span data-ttu-id="52941-133">String</span><span class="sxs-lookup"><span data-stu-id="52941-133">String</span></span>        | <span data-ttu-id="52941-134">Una ruta de acceso que conduce a la carpeta en la que está almacenado el artículo.</span><span class="sxs-lookup"><span data-stu-id="52941-134">A path leading to the folder in which the item is stored.</span></span> |
| <span data-ttu-id="52941-135">containerDisplayName</span><span class="sxs-lookup"><span data-stu-id="52941-135">containerDisplayName</span></span>  | <span data-ttu-id="52941-136">String</span><span class="sxs-lookup"><span data-stu-id="52941-136">String</span></span>        | <span data-ttu-id="52941-137">Una cadena que describe donde está almacenado el artículo.</span><span class="sxs-lookup"><span data-stu-id="52941-137">A string describing where the item is stored.</span></span> <span data-ttu-id="52941-138">Por ejemplo, el nombre de un sitio de SharePoint o el nombre de usuario que identifica el propietario de la OneDrive para almacenar el elemento.</span><span class="sxs-lookup"><span data-stu-id="52941-138">For example, the name of a SharePoint site or the user name identifying the owner of the OneDrive storing the item.</span></span>  |
| <span data-ttu-id="52941-139">containerType</span><span class="sxs-lookup"><span data-stu-id="52941-139">containerType</span></span>         | <span data-ttu-id="52941-140">String</span><span class="sxs-lookup"><span data-stu-id="52941-140">String</span></span> | <span data-ttu-id="52941-141">Se puede usar para filtrar por el tipo de contenedor en el que se almacena el archivo.</span><span class="sxs-lookup"><span data-stu-id="52941-141">Can be used for filtering by the type of container in which the file is stored.</span></span> <span data-ttu-id="52941-142">Por ejemplo, sitio o OneDriveBusiness.</span><span class="sxs-lookup"><span data-stu-id="52941-142">Such as Site or OneDriveBusiness.</span></span>       |

## <a name="type-property-values"></a><span data-ttu-id="52941-143">Valores de propiedad de tipo</span><span class="sxs-lookup"><span data-stu-id="52941-143">Type property values</span></span>
-   <span data-ttu-id="52941-144">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="52941-144">PowerPoint</span></span>
-   <span data-ttu-id="52941-145">Word</span><span class="sxs-lookup"><span data-stu-id="52941-145">Word</span></span>
-   <span data-ttu-id="52941-146">Excel</span><span class="sxs-lookup"><span data-stu-id="52941-146">Excel</span></span>
-   <span data-ttu-id="52941-147">Pdf</span><span class="sxs-lookup"><span data-stu-id="52941-147">Pdf</span></span>
-   <span data-ttu-id="52941-148">OneNote</span><span class="sxs-lookup"><span data-stu-id="52941-148">OneNote</span></span>
-   <span data-ttu-id="52941-149">OneNotePage</span><span class="sxs-lookup"><span data-stu-id="52941-149">OneNotePage</span></span>
-   <span data-ttu-id="52941-150">InfoPath</span><span class="sxs-lookup"><span data-stu-id="52941-150">InfoPath</span></span>
-   <span data-ttu-id="52941-151">Visio</span><span class="sxs-lookup"><span data-stu-id="52941-151">Visio</span></span>
-   <span data-ttu-id="52941-152">Publisher</span><span class="sxs-lookup"><span data-stu-id="52941-152">Publisher</span></span>
-   <span data-ttu-id="52941-153">Proyecto</span><span class="sxs-lookup"><span data-stu-id="52941-153">Project</span></span>
-   <span data-ttu-id="52941-154">Access</span><span class="sxs-lookup"><span data-stu-id="52941-154">Access</span></span>
-   <span data-ttu-id="52941-155">Correo</span><span class="sxs-lookup"><span data-stu-id="52941-155">Mail</span></span>
-   <span data-ttu-id="52941-156">CSV</span><span class="sxs-lookup"><span data-stu-id="52941-156">Csv</span></span>
-   <span data-ttu-id="52941-157">Archivo</span><span class="sxs-lookup"><span data-stu-id="52941-157">Archive</span></span>
-   <span data-ttu-id="52941-158">Xps</span><span class="sxs-lookup"><span data-stu-id="52941-158">Xps</span></span>
-   <span data-ttu-id="52941-159">Audio</span><span class="sxs-lookup"><span data-stu-id="52941-159">Audio</span></span>
-   <span data-ttu-id="52941-160">Vídeo</span><span class="sxs-lookup"><span data-stu-id="52941-160">Video</span></span>
-   <span data-ttu-id="52941-161">Image (Imagen)</span><span class="sxs-lookup"><span data-stu-id="52941-161">Image</span></span>
-   <span data-ttu-id="52941-162">Web</span><span class="sxs-lookup"><span data-stu-id="52941-162">Web</span></span>
-   <span data-ttu-id="52941-163">Texto</span><span class="sxs-lookup"><span data-stu-id="52941-163">Text</span></span>
-   <span data-ttu-id="52941-164">Xml</span><span class="sxs-lookup"><span data-stu-id="52941-164">Xml</span></span>
-   <span data-ttu-id="52941-165">Story</span><span class="sxs-lookup"><span data-stu-id="52941-165">Story</span></span>
-   <span data-ttu-id="52941-166">ExternalContent</span><span class="sxs-lookup"><span data-stu-id="52941-166">ExternalContent</span></span>
-   <span data-ttu-id="52941-167">Carpeta</span><span class="sxs-lookup"><span data-stu-id="52941-167">Folder</span></span>
-   <span data-ttu-id="52941-168">Otro</span><span class="sxs-lookup"><span data-stu-id="52941-168">Other</span></span>

<span data-ttu-id="52941-169">Consulta de ejemplo:`https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/Type eq 'PowerPoint'`</span><span class="sxs-lookup"><span data-stu-id="52941-169">Example query: `https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/Type eq 'PowerPoint'`</span></span>

## <a name="containertype-property-values"></a><span data-ttu-id="52941-170">valores de la propiedad containerType</span><span class="sxs-lookup"><span data-stu-id="52941-170">containerType property values</span></span>
<span data-ttu-id="52941-171">Los tipos admitidos pueden variar en función de en los contenedores desde la que el [entendimiento](insights.md) devuelve los archivos.</span><span class="sxs-lookup"><span data-stu-id="52941-171">The supported types can differ based on containers from which the [Insight](insights.md) returns files.</span></span> <span data-ttu-id="52941-172">Por ejemplo, solo los conocimientos [compartidos](insights-shared.md) devuelve los archivos de 'Lista desplegable', 'Cuadro' y 'GDrive'.</span><span class="sxs-lookup"><span data-stu-id="52941-172">For example, only the [Shared](insights-shared.md) insight returns files from 'DropBox', 'Box', and 'GDrive'.</span></span>

-   <span data-ttu-id="52941-173">OneDriveBusiness</span><span class="sxs-lookup"><span data-stu-id="52941-173">OneDriveBusiness</span></span>
-   <span data-ttu-id="52941-174">Sitio</span><span class="sxs-lookup"><span data-stu-id="52941-174">Site</span></span>
-   <span data-ttu-id="52941-175">Correo</span><span class="sxs-lookup"><span data-stu-id="52941-175">Mail</span></span>
-   <span data-ttu-id="52941-176">Lista desplegable</span><span class="sxs-lookup"><span data-stu-id="52941-176">DropBox</span></span>
-   <span data-ttu-id="52941-177">Cuadro</span><span class="sxs-lookup"><span data-stu-id="52941-177">Box</span></span>
-   <span data-ttu-id="52941-178">GDrive</span><span class="sxs-lookup"><span data-stu-id="52941-178">GDrive</span></span>

<span data-ttu-id="52941-179">Consulta de ejemplo:`https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/containerType eq 'OneDriveBusiness'`</span><span class="sxs-lookup"><span data-stu-id="52941-179">Example query: `https://graph.microsoft.com/beta/me/insights/trending?$filter=ResourceVisualization/containerType eq 'OneDriveBusiness'`</span></span>