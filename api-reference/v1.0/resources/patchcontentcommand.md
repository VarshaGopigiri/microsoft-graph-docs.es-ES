---
title: Tipo de recurso patchContentCommand
description: Cambios que se deben realizar en una solicitud de revisión de una página de OneNote.
localization_priority: Normal
ms.openlocfilehash: fb0900490b3fe05e6fb90dc4ab8252620bf43983
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27804539"
---
# <a name="patchcontentcommand-resource-type"></a><span data-ttu-id="26c7a-103">Tipo de recurso patchContentCommand</span><span class="sxs-lookup"><span data-stu-id="26c7a-103">patchContentCommand resource type</span></span>

<span data-ttu-id="26c7a-104">Cambios que se deben realizar en una solicitud de revisión de una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="26c7a-104">The changes to make to a OneNote page in a PATCH request.</span></span>

## <a name="json-representation"></a><span data-ttu-id="26c7a-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="26c7a-105">JSON representation</span></span>

<span data-ttu-id="26c7a-106">Aquí se muestra una representación JSON del recurso, que se envía en el cuerpo de la solicitud [PATCH pages/{id}\`](../api/page-update.md).</span><span class="sxs-lookup"><span data-stu-id="26c7a-106">Here is a JSON representation of the resource, which is sent in the body of the [PATCH pages/{id}\`](../api/page-update.md) request.</span></span> 

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

## <a name="properties"></a><span data-ttu-id="26c7a-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26c7a-107">Properties</span></span>
| <span data-ttu-id="26c7a-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26c7a-108">Property</span></span>     | <span data-ttu-id="26c7a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="26c7a-109">Type</span></span>   |<span data-ttu-id="26c7a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="26c7a-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="26c7a-111">action</span><span class="sxs-lookup"><span data-stu-id="26c7a-111">action</span></span>|<span data-ttu-id="26c7a-112">onenotePatchActionType</span><span class="sxs-lookup"><span data-stu-id="26c7a-112">onenotePatchActionType</span></span>|<span data-ttu-id="26c7a-113">Acción que se debe efectuar en el elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="26c7a-113">The action to perform on the target element.</span></span> <span data-ttu-id="26c7a-114">Los valores posibles son: `replace`, `append`, `delete`, `insert`, o `prepend`.</span><span class="sxs-lookup"><span data-stu-id="26c7a-114">The possible values are: `replace`, `append`, `delete`, `insert`, or `prepend`.</span></span>|
|<span data-ttu-id="26c7a-115">content</span><span class="sxs-lookup"><span data-stu-id="26c7a-115">content</span></span>|<span data-ttu-id="26c7a-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="26c7a-116">String</span></span>|<span data-ttu-id="26c7a-p102">Cadena de HTML sintácticamente correcto para agregar a la página y datos binarios de cualquier imagen o archivo. Si el contenido incluye datos binarios, la solicitud se debe enviar mediante el tipo de contenido `multipart/form-data` con una parte "Comandos".</span><span class="sxs-lookup"><span data-stu-id="26c7a-p102">A string of well-formed HTML to add to the page, and any image or file binary data. If the content contains binary data, the request must be sent using the `multipart/form-data` content type with a "Commands" part.</span></span> |
|<span data-ttu-id="26c7a-119">position</span><span class="sxs-lookup"><span data-stu-id="26c7a-119">position</span></span>|<span data-ttu-id="26c7a-120">onenotePatchInsertPosition</span><span class="sxs-lookup"><span data-stu-id="26c7a-120">onenotePatchInsertPosition</span></span>|<span data-ttu-id="26c7a-121">Ubicación donde se debe agregar el contenido provisto, en relación con el elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="26c7a-121">The location to add the supplied content, relative to the target element.</span></span> <span data-ttu-id="26c7a-122">Los valores posibles son: `after` (valor predeterminado) o `before`.</span><span class="sxs-lookup"><span data-stu-id="26c7a-122">The possible values are: `after` (default) or `before`.</span></span>|
|<span data-ttu-id="26c7a-123">target</span><span class="sxs-lookup"><span data-stu-id="26c7a-123">target</span></span>|<span data-ttu-id="26c7a-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="26c7a-124">String</span></span>|<span data-ttu-id="26c7a-p104">Elemento que se va a actualizar. Debe ser el `#<data-id>` o el `<id>` generado del elemento, o bien la palabra clave `body` o `title`.</span><span class="sxs-lookup"><span data-stu-id="26c7a-p104">The element to update. Must be the `#<data-id>` or the generated `<id>` of the element, or the `body` or `title` keyword.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "patchContentCommand resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
