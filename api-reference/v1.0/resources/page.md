---
title: Tipo de recurso page
description: Una página de un bloc de notas de OneNote.
ms.openlocfilehash: 19380f06ad4706f623397681a020054e65eba029
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031917"
---
# <a name="page-resource-type"></a><span data-ttu-id="9d8b9-103">Tipo de recurso page</span><span class="sxs-lookup"><span data-stu-id="9d8b9-103">page resource type</span></span>

<span data-ttu-id="9d8b9-104">Una página de un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-104">A page in a OneNote notebook.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9d8b9-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9d8b9-105">JSON representation</span></span>

<span data-ttu-id="9d8b9-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-106">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.onenoteEntitySchemaObjectModel",
  "optionalProperties": [
    "parentNotebook",
    "parentSection"
  ],
  "isMediaEntity": true,
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
## <a name="properties"></a><span data-ttu-id="9d8b9-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9d8b9-107">Properties</span></span>
| <span data-ttu-id="9d8b9-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9d8b9-108">Property</span></span>     | <span data-ttu-id="9d8b9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d8b9-109">Type</span></span>   |<span data-ttu-id="9d8b9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d8b9-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9d8b9-111">content</span><span class="sxs-lookup"><span data-stu-id="9d8b9-111">content</span></span>|<span data-ttu-id="9d8b9-112">Secuencia</span><span class="sxs-lookup"><span data-stu-id="9d8b9-112">Stream</span></span>|<span data-ttu-id="9d8b9-113">Contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-113">The page's HTML content.</span></span>|
|<span data-ttu-id="9d8b9-114">contentUrl</span><span class="sxs-lookup"><span data-stu-id="9d8b9-114">contentUrl</span></span>|<span data-ttu-id="9d8b9-115">String</span><span class="sxs-lookup"><span data-stu-id="9d8b9-115">String</span></span>|<span data-ttu-id="9d8b9-p101">Dirección URL del contenido HTML de la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-p101">The URL for the page's HTML content.  Read-only.</span></span>|
|<span data-ttu-id="9d8b9-118">createdByAppId</span><span class="sxs-lookup"><span data-stu-id="9d8b9-118">createdByAppId</span></span>|<span data-ttu-id="9d8b9-119">String</span><span class="sxs-lookup"><span data-stu-id="9d8b9-119">String</span></span>|<span data-ttu-id="9d8b9-p102">Identificador único de la aplicación que creó la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-p102">The unique identifier of the application that created the page. Read-only.</span></span>|
|<span data-ttu-id="9d8b9-122">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9d8b9-122">createdDateTime</span></span>|<span data-ttu-id="9d8b9-123">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9d8b9-123">DateTimeOffset</span></span>|<span data-ttu-id="9d8b9-p103">La fecha y la hora en que se creó la página. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-p103">The date and time when the page was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="9d8b9-128">id</span><span class="sxs-lookup"><span data-stu-id="9d8b9-128">id</span></span>|<span data-ttu-id="9d8b9-129">String</span><span class="sxs-lookup"><span data-stu-id="9d8b9-129">String</span></span>|<span data-ttu-id="9d8b9-p104">Identificador único de la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-p104">The unique identifier of the page.  Read-only.</span></span>|
|<span data-ttu-id="9d8b9-132">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9d8b9-132">lastModifiedDateTime</span></span>|<span data-ttu-id="9d8b9-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9d8b9-133">DateTimeOffset</span></span>|<span data-ttu-id="9d8b9-p105">La fecha y la hora en que se modificó la página por última vez. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-p105">The date and time when the page was last modified. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|
|<span data-ttu-id="9d8b9-138">nivel</span><span class="sxs-lookup"><span data-stu-id="9d8b9-138">level</span></span>|<span data-ttu-id="9d8b9-139">Int32</span><span class="sxs-lookup"><span data-stu-id="9d8b9-139">Int32</span></span>|<span data-ttu-id="9d8b9-p106">Nivel de sangría de la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-p106">The indentation level of the page. Read-only.</span></span>|
|<span data-ttu-id="9d8b9-142">vínculos</span><span class="sxs-lookup"><span data-stu-id="9d8b9-142">links</span></span>|[<span data-ttu-id="9d8b9-143">PageLinks</span><span class="sxs-lookup"><span data-stu-id="9d8b9-143">PageLinks</span></span>](pagelinks.md)|<span data-ttu-id="9d8b9-p107">Vínculos para abrir la página. El vínculo `oneNoteClientURL` abre la página en el cliente nativo de OneNote si está instalado. El vínculo `oneNoteWebUrl` abre la página en OneNote Online. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-p107">Links for opening the page. The `oneNoteClientURL` link opens the page in the OneNote native client if it 's installed. The `oneNoteWebUrl` link opens the page in OneNote Online. Read-only.</span></span>|
|<span data-ttu-id="9d8b9-148">order</span><span class="sxs-lookup"><span data-stu-id="9d8b9-148">order</span></span>|<span data-ttu-id="9d8b9-149">Int32</span><span class="sxs-lookup"><span data-stu-id="9d8b9-149">Int32</span></span>|<span data-ttu-id="9d8b9-p108">El orden de la página dentro de su sección primaria. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-p108">The order of the page within its parent section. Read-only.</span></span>|
|<span data-ttu-id="9d8b9-152">self</span><span class="sxs-lookup"><span data-stu-id="9d8b9-152">self</span></span>|<span data-ttu-id="9d8b9-153">String</span><span class="sxs-lookup"><span data-stu-id="9d8b9-153">String</span></span>|<span data-ttu-id="9d8b9-p109">El punto de conexión donde puede obtener información detallada sobre la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-p109">The endpoint where you can get details about the page. Read-only.</span></span>|
|<span data-ttu-id="9d8b9-156">title</span><span class="sxs-lookup"><span data-stu-id="9d8b9-156">title</span></span>|<span data-ttu-id="9d8b9-157">String</span><span class="sxs-lookup"><span data-stu-id="9d8b9-157">String</span></span>|<span data-ttu-id="9d8b9-158">Título de la página.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-158">The title of the page.</span></span> |

## <a name="relationships"></a><span data-ttu-id="9d8b9-159">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9d8b9-159">Relationships</span></span>
| <span data-ttu-id="9d8b9-160">Relación</span><span class="sxs-lookup"><span data-stu-id="9d8b9-160">Relationship</span></span> | <span data-ttu-id="9d8b9-161">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d8b9-161">Type</span></span>   |<span data-ttu-id="9d8b9-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d8b9-162">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9d8b9-163">parentNotebook</span><span class="sxs-lookup"><span data-stu-id="9d8b9-163">parentNotebook</span></span>|[<span data-ttu-id="9d8b9-164">Notebook</span><span class="sxs-lookup"><span data-stu-id="9d8b9-164">Notebook</span></span>](notebook.md)|<span data-ttu-id="9d8b9-p110">Bloc de notas que contiene la página.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-p110">The notebook that contains the page.  Read-only.</span></span>|
|<span data-ttu-id="9d8b9-167">parentSection</span><span class="sxs-lookup"><span data-stu-id="9d8b9-167">parentSection</span></span>|[<span data-ttu-id="9d8b9-168">OnenoteSection</span><span class="sxs-lookup"><span data-stu-id="9d8b9-168">OnenoteSection</span></span>](section.md)|<span data-ttu-id="9d8b9-p111">Sección que contiene la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-p111">The section that contains the page. Read-only.</span></span>|

## <a name="methods"></a><span data-ttu-id="9d8b9-171">Métodos</span><span class="sxs-lookup"><span data-stu-id="9d8b9-171">Methods</span></span>

| <span data-ttu-id="9d8b9-172">Método</span><span class="sxs-lookup"><span data-stu-id="9d8b9-172">Method</span></span>           | <span data-ttu-id="9d8b9-173">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d8b9-173">Return Type</span></span>    |<span data-ttu-id="9d8b9-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d8b9-174">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9d8b9-175">Obtener página</span><span class="sxs-lookup"><span data-stu-id="9d8b9-175">Get page</span></span>](../api/page-get.md) | [<span data-ttu-id="9d8b9-176">Page</span><span class="sxs-lookup"><span data-stu-id="9d8b9-176">Page</span></span>](page.md) |<span data-ttu-id="9d8b9-177">Leer las propiedades y las relaciones de la página.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-177">Read the properties and relationships of the page.</span></span>|
|[<span data-ttu-id="9d8b9-178">Actualizar contenido de la página</span><span class="sxs-lookup"><span data-stu-id="9d8b9-178">Update page content</span></span>](../api/page-update.md) | <span data-ttu-id="9d8b9-179">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9d8b9-179">None</span></span> |<span data-ttu-id="9d8b9-180">Actualizar el contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-180">Update the HTML content of the page.</span></span> |
|[<span data-ttu-id="9d8b9-181">Eliminar página</span><span class="sxs-lookup"><span data-stu-id="9d8b9-181">Delete page</span></span>](../api/page-delete.md) | <span data-ttu-id="9d8b9-182">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9d8b9-182">None</span></span> |<span data-ttu-id="9d8b9-183">Eliminar la página.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-183">Delete the page.</span></span> |
|[<span data-ttu-id="9d8b9-184">copyToSection</span><span class="sxs-lookup"><span data-stu-id="9d8b9-184">copyToSection</span></span>](../api/page-copytosection.md)| <span data-ttu-id="9d8b9-185">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9d8b9-185">None</span></span> |<span data-ttu-id="9d8b9-186">Copia la página en una sección específica.</span><span class="sxs-lookup"><span data-stu-id="9d8b9-186">Copies the page to a specific section.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->