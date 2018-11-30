---
title: Tipo de recurso patchContentCommand
description: Cambios que se deben realizar en una solicitud de revisión de una página de OneNote.
ms.openlocfilehash: fb559a96aa5eef94dd07280b888da0df989b2363
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089941"
---
# <a name="patchcontentcommand-resource-type"></a><span data-ttu-id="ab4a5-103">Tipo de recurso patchContentCommand</span><span class="sxs-lookup"><span data-stu-id="ab4a5-103">patchContentCommand resource type</span></span>

> <span data-ttu-id="ab4a5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ab4a5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ab4a5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ab4a5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ab4a5-106">Cambios que se deben realizar en una solicitud de revisión de una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="ab4a5-106">The changes to make to a OneNote page in a PATCH request.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ab4a5-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ab4a5-107">JSON representation</span></span>

<span data-ttu-id="ab4a5-108">Aquí se muestra una representación JSON del recurso, que se envía en el cuerpo de la solicitud [PATCH pages/{id}\`](../api/page-update.md).</span><span class="sxs-lookup"><span data-stu-id="ab4a5-108">Here is a JSON representation of the resource, which is sent in the body of the [PATCH pages/{id}\`](../api/page-update.md) request.</span></span> 

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenotePatchContentCommand"
}-->

```json
{
  "action": "String",
  "content": "string",
  "position": "String",
  "target": "string"
}

```

## <a name="properties"></a><span data-ttu-id="ab4a5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ab4a5-109">Properties</span></span>
| <span data-ttu-id="ab4a5-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ab4a5-110">Property</span></span>     | <span data-ttu-id="ab4a5-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab4a5-111">Type</span></span>   |<span data-ttu-id="ab4a5-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab4a5-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ab4a5-113">action</span><span class="sxs-lookup"><span data-stu-id="ab4a5-113">action</span></span>|<span data-ttu-id="ab4a5-114">String</span><span class="sxs-lookup"><span data-stu-id="ab4a5-114">String</span></span>|<span data-ttu-id="ab4a5-p102">La acción que se debe efectuar en el elemento de destino. Los valores posibles son `replace`, `append`, `delete`, `insert` o `prepend`.</span><span class="sxs-lookup"><span data-stu-id="ab4a5-p102">The action to perform on the target element. Possible values are: `replace`, `append`, `delete`, `insert`, or `prepend`.</span></span>|
|<span data-ttu-id="ab4a5-117">content</span><span class="sxs-lookup"><span data-stu-id="ab4a5-117">content</span></span>|<span data-ttu-id="ab4a5-118">String</span><span class="sxs-lookup"><span data-stu-id="ab4a5-118">String</span></span>|<span data-ttu-id="ab4a5-p103">Cadena de HTML sintácticamente correcto para agregar a la página y datos binarios de cualquier imagen o archivo. Si el contenido incluye datos binarios, la solicitud se debe enviar mediante el tipo de contenido `multipart/form-data` con una parte "Comandos".</span><span class="sxs-lookup"><span data-stu-id="ab4a5-p103">A string of well-formed HTML to add to the page, and any image or file binary data. If the content contains binary data, the request must be sent using the `multipart/form-data` content type with a "Commands" part.</span></span> |
|<span data-ttu-id="ab4a5-121">position</span><span class="sxs-lookup"><span data-stu-id="ab4a5-121">position</span></span>|<span data-ttu-id="ab4a5-122">String</span><span class="sxs-lookup"><span data-stu-id="ab4a5-122">String</span></span>|<span data-ttu-id="ab4a5-p104">Ubicación donde se debe agregar el contenido provisto, en relación con el elemento de destino. Los valores posibles son `after` (predeterminado) y `before`.</span><span class="sxs-lookup"><span data-stu-id="ab4a5-p104">The location to add the supplied content, relative to the target element. Possible values are: `after` (default) or `before`.</span></span>|
|<span data-ttu-id="ab4a5-125">target</span><span class="sxs-lookup"><span data-stu-id="ab4a5-125">target</span></span>|<span data-ttu-id="ab4a5-126">String</span><span class="sxs-lookup"><span data-stu-id="ab4a5-126">String</span></span>|<span data-ttu-id="ab4a5-p105">Elemento que se va a actualizar. Debe ser el `#<data-id>` o el `<id>` generado del elemento, o bien la palabra clave `body` o `title`.</span><span class="sxs-lookup"><span data-stu-id="ab4a5-p105">The element to update. Must be the `#<data-id>` or the generated `<id>` of the element, or the `body` or `title` keyword.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "patchContentCommand resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->