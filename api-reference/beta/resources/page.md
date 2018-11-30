---
title: Tipo de recurso page
description: Una página de un bloc de notas de OneNote.
ms.openlocfilehash: 82b9ca00cb4488c33e73daa94844b11f8de301cd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088654"
---
# <a name="page-resource-type"></a><span data-ttu-id="ceb6a-103">Tipo de recurso page</span><span class="sxs-lookup"><span data-stu-id="ceb6a-103">page resource type</span></span>

> <span data-ttu-id="ceb6a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ceb6a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ceb6a-106">Una página de un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-106">A page in a OneNote notebook.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ceb6a-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ceb6a-107">JSON representation</span></span>

<span data-ttu-id="ceb6a-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "parentNotebook",
    "parentSection"
  ],
  "@odata.type": "microsoft.graph.onenotePage"
}-->

```json
{
  "content": "stream",
  "contentUrl": "string",
  "createdByAppId": "string",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "level": 1024,
  "links": {"@odata.type": "microsoft.graph.pageLinks"},
  "order": 1024,
  "self": "string",
  "title": "string"
}

```
## <a name="properties"></a><span data-ttu-id="ceb6a-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ceb6a-109">Properties</span></span>
| <span data-ttu-id="ceb6a-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ceb6a-110">Property</span></span>     | <span data-ttu-id="ceb6a-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ceb6a-111">Type</span></span>   |<span data-ttu-id="ceb6a-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceb6a-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ceb6a-113">content</span><span class="sxs-lookup"><span data-stu-id="ceb6a-113">content</span></span>|<span data-ttu-id="ceb6a-114">Secuencia</span><span class="sxs-lookup"><span data-stu-id="ceb6a-114">Stream</span></span>|<span data-ttu-id="ceb6a-115">Contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-115">The page's HTML content.</span></span>|
|<span data-ttu-id="ceb6a-116">contentUrl</span><span class="sxs-lookup"><span data-stu-id="ceb6a-116">contentUrl</span></span>|<span data-ttu-id="ceb6a-117">String</span><span class="sxs-lookup"><span data-stu-id="ceb6a-117">String</span></span>|<span data-ttu-id="ceb6a-p102">Dirección URL del contenido HTML de la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-p102">The URL for the page's HTML content.  Read-only.</span></span>|
|<span data-ttu-id="ceb6a-120">createdByAppId</span><span class="sxs-lookup"><span data-stu-id="ceb6a-120">createdByAppId</span></span>|<span data-ttu-id="ceb6a-121">String</span><span class="sxs-lookup"><span data-stu-id="ceb6a-121">String</span></span>|<span data-ttu-id="ceb6a-p103">Identificador único de la aplicación que creó la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-p103">The unique identifier of the application that created the page. Read-only.</span></span>|
|<span data-ttu-id="ceb6a-124">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ceb6a-124">createdDateTime</span></span>|<span data-ttu-id="ceb6a-125">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ceb6a-125">DateTimeOffset</span></span>|<span data-ttu-id="ceb6a-p104">La fecha y la hora en que se creó la página. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-p104">The date and time when the page was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="ceb6a-130">id</span><span class="sxs-lookup"><span data-stu-id="ceb6a-130">id</span></span>|<span data-ttu-id="ceb6a-131">String</span><span class="sxs-lookup"><span data-stu-id="ceb6a-131">String</span></span>|<span data-ttu-id="ceb6a-p105">Identificador único de la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-p105">The unique identifier of the page.  Read-only.</span></span>|
|<span data-ttu-id="ceb6a-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ceb6a-134">lastModifiedDateTime</span></span>|<span data-ttu-id="ceb6a-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ceb6a-135">DateTimeOffset</span></span>|<span data-ttu-id="ceb6a-p106">La fecha y la hora en que se modificó la página por última vez. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-p106">The date and time when the page was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="ceb6a-140">nivel</span><span class="sxs-lookup"><span data-stu-id="ceb6a-140">level</span></span>|<span data-ttu-id="ceb6a-141">Int32</span><span class="sxs-lookup"><span data-stu-id="ceb6a-141">Int32</span></span>|<span data-ttu-id="ceb6a-p107">Nivel de sangría de la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-p107">The indentation level of the page. Read-only.</span></span>|
|<span data-ttu-id="ceb6a-144">vínculos</span><span class="sxs-lookup"><span data-stu-id="ceb6a-144">links</span></span>|[<span data-ttu-id="ceb6a-145">PageLinks</span><span class="sxs-lookup"><span data-stu-id="ceb6a-145">PageLinks</span></span>](pagelinks.md)|<span data-ttu-id="ceb6a-p108">Vínculos para abrir la página. El vínculo `oneNoteClientURL` abre la página en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebUrl` abre la página en OneNote Online. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-p108">Links for opening the page. The `oneNoteClientURL` link opens the page in the OneNote native client if it 's installed. The `oneNoteWebUrl` link opens the page in OneNote Online. Read-only.</span></span>|
|<span data-ttu-id="ceb6a-150">order</span><span class="sxs-lookup"><span data-stu-id="ceb6a-150">order</span></span>|<span data-ttu-id="ceb6a-151">Int32</span><span class="sxs-lookup"><span data-stu-id="ceb6a-151">Int32</span></span>|<span data-ttu-id="ceb6a-p109">El orden de la página dentro de su sección primaria. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-p109">The order of the page within its parent section. Read-only.</span></span>|
|<span data-ttu-id="ceb6a-154">self</span><span class="sxs-lookup"><span data-stu-id="ceb6a-154">self</span></span>|<span data-ttu-id="ceb6a-155">String</span><span class="sxs-lookup"><span data-stu-id="ceb6a-155">String</span></span>|<span data-ttu-id="ceb6a-p110">El punto de conexión donde puede obtener información detallada sobre la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-p110">The endpoint where you can get details about the page. Read-only.</span></span>|
|<span data-ttu-id="ceb6a-158">title</span><span class="sxs-lookup"><span data-stu-id="ceb6a-158">title</span></span>|<span data-ttu-id="ceb6a-159">String</span><span class="sxs-lookup"><span data-stu-id="ceb6a-159">String</span></span>|<span data-ttu-id="ceb6a-160">Título de la página.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-160">The title of the page.</span></span> |

## <a name="relationships"></a><span data-ttu-id="ceb6a-161">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ceb6a-161">Relationships</span></span>
| <span data-ttu-id="ceb6a-162">Relación</span><span class="sxs-lookup"><span data-stu-id="ceb6a-162">Relationship</span></span> | <span data-ttu-id="ceb6a-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="ceb6a-163">Type</span></span>   |<span data-ttu-id="ceb6a-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceb6a-164">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ceb6a-165">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="ceb6a-165">parentNotebook</span></span>|[<span data-ttu-id="ceb6a-166">Notebook</span><span class="sxs-lookup"><span data-stu-id="ceb6a-166">Notebook</span></span>](notebook.md)|<span data-ttu-id="ceb6a-p111">Bloc de notas que contiene la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-p111">The notebook that contains the page.  Read-only.</span></span>|
|<span data-ttu-id="ceb6a-169">parentSection</span><span class="sxs-lookup"><span data-stu-id="ceb6a-169">parentSection</span></span>|[<span data-ttu-id="ceb6a-170">Section</span><span class="sxs-lookup"><span data-stu-id="ceb6a-170">Section</span></span>](section.md)|<span data-ttu-id="ceb6a-p112">Sección que contiene la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-p112">The section that contains the page. Read-only.</span></span>|

## <a name="methods"></a><span data-ttu-id="ceb6a-173">Métodos</span><span class="sxs-lookup"><span data-stu-id="ceb6a-173">Methods</span></span>

| <span data-ttu-id="ceb6a-174">Método</span><span class="sxs-lookup"><span data-stu-id="ceb6a-174">Method</span></span>           | <span data-ttu-id="ceb6a-175">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ceb6a-175">Return Type</span></span>    |<span data-ttu-id="ceb6a-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="ceb6a-176">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="ceb6a-177">Obtener página</span><span class="sxs-lookup"><span data-stu-id="ceb6a-177">Get page</span></span>](../api/page-get.md) | [<span data-ttu-id="ceb6a-178">Page</span><span class="sxs-lookup"><span data-stu-id="ceb6a-178">Page</span></span>](page.md) |<span data-ttu-id="ceb6a-179">Leer las propiedades y las relaciones de la página.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-179">Read the properties and relationships of the page.</span></span>|
|[<span data-ttu-id="ceb6a-180">Actualizar contenido de la página</span><span class="sxs-lookup"><span data-stu-id="ceb6a-180">Update page content</span></span>](../api/page-update.md) | <span data-ttu-id="ceb6a-181">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ceb6a-181">None</span></span> |<span data-ttu-id="ceb6a-182">Actualizar el contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-182">Update the HTML content of the page.</span></span> |
|[<span data-ttu-id="ceb6a-183">Eliminar página</span><span class="sxs-lookup"><span data-stu-id="ceb6a-183">Delete page</span></span>](../api/page-delete.md) | <span data-ttu-id="ceb6a-184">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ceb6a-184">None</span></span> |<span data-ttu-id="ceb6a-185">Eliminar la página.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-185">Delete the page.</span></span> |
|[<span data-ttu-id="ceb6a-186">copyToSection</span><span class="sxs-lookup"><span data-stu-id="ceb6a-186">copyToSection</span></span>](../api/page-copytosection.md)| <span data-ttu-id="ceb6a-187">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ceb6a-187">None</span></span> |<span data-ttu-id="ceb6a-188">Copia la página en una sección específica.</span><span class="sxs-lookup"><span data-stu-id="ceb6a-188">Copies the page to a specific section.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->