---
title: Tipo de recurso page
description: Una página de un bloc de notas de OneNote.
localization_priority: Normal
ms.openlocfilehash: 5928f430fcbfe9f41c6aa83e99d7dfe737e8e1c7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850137"
---
# <a name="page-resource-type"></a><span data-ttu-id="01778-103">Tipo de recurso page</span><span class="sxs-lookup"><span data-stu-id="01778-103">page resource type</span></span>

> <span data-ttu-id="01778-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="01778-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="01778-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="01778-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="01778-106">Una página de un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="01778-106">A page in a OneNote notebook.</span></span>

## <a name="json-representation"></a><span data-ttu-id="01778-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="01778-107">JSON representation</span></span>

<span data-ttu-id="01778-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="01778-108">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="01778-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01778-109">Properties</span></span>
| <span data-ttu-id="01778-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="01778-110">Property</span></span>     | <span data-ttu-id="01778-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="01778-111">Type</span></span>   |<span data-ttu-id="01778-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="01778-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="01778-113">content</span><span class="sxs-lookup"><span data-stu-id="01778-113">content</span></span>|<span data-ttu-id="01778-114">Secuencia</span><span class="sxs-lookup"><span data-stu-id="01778-114">Stream</span></span>|<span data-ttu-id="01778-115">Contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="01778-115">The page's HTML content.</span></span>|
|<span data-ttu-id="01778-116">contentUrl</span><span class="sxs-lookup"><span data-stu-id="01778-116">contentUrl</span></span>|<span data-ttu-id="01778-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="01778-117">String</span></span>|<span data-ttu-id="01778-p102">Dirección URL del contenido HTML de la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01778-p102">The URL for the page's HTML content.  Read-only.</span></span>|
|<span data-ttu-id="01778-120">createdByAppId</span><span class="sxs-lookup"><span data-stu-id="01778-120">createdByAppId</span></span>|<span data-ttu-id="01778-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="01778-121">String</span></span>|<span data-ttu-id="01778-p103">Identificador único de la aplicación que creó la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01778-p103">The unique identifier of the application that created the page. Read-only.</span></span>|
|<span data-ttu-id="01778-124">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="01778-124">createdDateTime</span></span>|<span data-ttu-id="01778-125">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="01778-125">DateTimeOffset</span></span>|<span data-ttu-id="01778-p104">La fecha y la hora en que se creó la página. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01778-p104">The date and time when the page was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="01778-130">id</span><span class="sxs-lookup"><span data-stu-id="01778-130">id</span></span>|<span data-ttu-id="01778-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="01778-131">String</span></span>|<span data-ttu-id="01778-p105">Identificador único de la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01778-p105">The unique identifier of the page.  Read-only.</span></span>|
|<span data-ttu-id="01778-134">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="01778-134">lastModifiedDateTime</span></span>|<span data-ttu-id="01778-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="01778-135">DateTimeOffset</span></span>|<span data-ttu-id="01778-p106">La fecha y la hora en que se modificó la página por última vez. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01778-p106">The date and time when the page was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="01778-140">nivel</span><span class="sxs-lookup"><span data-stu-id="01778-140">level</span></span>|<span data-ttu-id="01778-141">Int32</span><span class="sxs-lookup"><span data-stu-id="01778-141">Int32</span></span>|<span data-ttu-id="01778-p107">Nivel de sangría de la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01778-p107">The indentation level of the page. Read-only.</span></span>|
|<span data-ttu-id="01778-144">vínculos</span><span class="sxs-lookup"><span data-stu-id="01778-144">links</span></span>|[<span data-ttu-id="01778-145">PageLinks</span><span class="sxs-lookup"><span data-stu-id="01778-145">PageLinks</span></span>](pagelinks.md)|<span data-ttu-id="01778-p108">Vínculos para abrir la página. El vínculo `oneNoteClientURL` abre la página en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebUrl` abre la página en OneNote Online. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01778-p108">Links for opening the page. The `oneNoteClientURL` link opens the page in the OneNote native client if it 's installed. The `oneNoteWebUrl` link opens the page in OneNote Online. Read-only.</span></span>|
|<span data-ttu-id="01778-150">order</span><span class="sxs-lookup"><span data-stu-id="01778-150">order</span></span>|<span data-ttu-id="01778-151">Int32</span><span class="sxs-lookup"><span data-stu-id="01778-151">Int32</span></span>|<span data-ttu-id="01778-p109">El orden de la página dentro de su sección primaria. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01778-p109">The order of the page within its parent section. Read-only.</span></span>|
|<span data-ttu-id="01778-154">self</span><span class="sxs-lookup"><span data-stu-id="01778-154">self</span></span>|<span data-ttu-id="01778-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="01778-155">String</span></span>|<span data-ttu-id="01778-p110">El punto de conexión donde puede obtener información detallada sobre la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01778-p110">The endpoint where you can get details about the page. Read-only.</span></span>|
|<span data-ttu-id="01778-158">title</span><span class="sxs-lookup"><span data-stu-id="01778-158">title</span></span>|<span data-ttu-id="01778-159">Cadena</span><span class="sxs-lookup"><span data-stu-id="01778-159">String</span></span>|<span data-ttu-id="01778-160">Título de la página.</span><span class="sxs-lookup"><span data-stu-id="01778-160">The title of the page.</span></span> |

## <a name="relationships"></a><span data-ttu-id="01778-161">Relaciones</span><span class="sxs-lookup"><span data-stu-id="01778-161">Relationships</span></span>
| <span data-ttu-id="01778-162">Relación</span><span class="sxs-lookup"><span data-stu-id="01778-162">Relationship</span></span> | <span data-ttu-id="01778-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="01778-163">Type</span></span>   |<span data-ttu-id="01778-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="01778-164">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="01778-165">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="01778-165">parentNotebook</span></span>|[<span data-ttu-id="01778-166">Notebook</span><span class="sxs-lookup"><span data-stu-id="01778-166">Notebook</span></span>](notebook.md)|<span data-ttu-id="01778-p111">Bloc de notas que contiene la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01778-p111">The notebook that contains the page.  Read-only.</span></span>|
|<span data-ttu-id="01778-169">parentSection</span><span class="sxs-lookup"><span data-stu-id="01778-169">parentSection</span></span>|[<span data-ttu-id="01778-170">Section</span><span class="sxs-lookup"><span data-stu-id="01778-170">Section</span></span>](section.md)|<span data-ttu-id="01778-p112">Sección que contiene la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="01778-p112">The section that contains the page. Read-only.</span></span>|

## <a name="methods"></a><span data-ttu-id="01778-173">Métodos</span><span class="sxs-lookup"><span data-stu-id="01778-173">Methods</span></span>

| <span data-ttu-id="01778-174">Método</span><span class="sxs-lookup"><span data-stu-id="01778-174">Method</span></span>           | <span data-ttu-id="01778-175">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="01778-175">Return Type</span></span>    |<span data-ttu-id="01778-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="01778-176">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="01778-177">Obtener página</span><span class="sxs-lookup"><span data-stu-id="01778-177">Get page</span></span>](../api/page-get.md) | [<span data-ttu-id="01778-178">Page</span><span class="sxs-lookup"><span data-stu-id="01778-178">Page</span></span>](page.md) |<span data-ttu-id="01778-179">Leer las propiedades y las relaciones de la página.</span><span class="sxs-lookup"><span data-stu-id="01778-179">Read the properties and relationships of the page.</span></span>|
|[<span data-ttu-id="01778-180">Actualizar contenido de la página</span><span class="sxs-lookup"><span data-stu-id="01778-180">Update page content</span></span>](../api/page-update.md) | <span data-ttu-id="01778-181">Ninguno</span><span class="sxs-lookup"><span data-stu-id="01778-181">None</span></span> |<span data-ttu-id="01778-182">Actualizar el contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="01778-182">Update the HTML content of the page.</span></span> |
|[<span data-ttu-id="01778-183">Eliminar página</span><span class="sxs-lookup"><span data-stu-id="01778-183">Delete page</span></span>](../api/page-delete.md) | <span data-ttu-id="01778-184">Ninguno</span><span class="sxs-lookup"><span data-stu-id="01778-184">None</span></span> |<span data-ttu-id="01778-185">Eliminar la página.</span><span class="sxs-lookup"><span data-stu-id="01778-185">Delete the page.</span></span> |
|[<span data-ttu-id="01778-186">copyToSection</span><span class="sxs-lookup"><span data-stu-id="01778-186">copyToSection</span></span>](../api/page-copytosection.md)| <span data-ttu-id="01778-187">Ninguno</span><span class="sxs-lookup"><span data-stu-id="01778-187">None</span></span> |<span data-ttu-id="01778-188">Copia la página en una sección específica.</span><span class="sxs-lookup"><span data-stu-id="01778-188">Copies the page to a specific section.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
