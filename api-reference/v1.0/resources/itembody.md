---
title: Tipo de recurso itemBody
description: Representa las propiedades del cuerpo de un elemento, como un mensaje, un evento o una publicación de grupo.
ms.openlocfilehash: ebcc2797052ac3a5a73547332e37c5e9c1bd3a41
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031246"
---
# <a name="itembody-resource-type"></a><span data-ttu-id="25317-103">Tipo de recurso itemBody</span><span class="sxs-lookup"><span data-stu-id="25317-103">itemBody resource type</span></span>

<span data-ttu-id="25317-104">Representa las propiedades del cuerpo de un elemento, como un mensaje, un evento o una publicación de grupo.</span><span class="sxs-lookup"><span data-stu-id="25317-104">Represents properties of the body of an item, such as a message, event or group post.</span></span>

## <a name="properties"></a><span data-ttu-id="25317-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="25317-105">Properties</span></span>
| <span data-ttu-id="25317-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25317-106">Property</span></span>     | <span data-ttu-id="25317-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="25317-107">Type</span></span>   |<span data-ttu-id="25317-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="25317-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="25317-109">content</span><span class="sxs-lookup"><span data-stu-id="25317-109">content</span></span>|<span data-ttu-id="25317-110">String</span><span class="sxs-lookup"><span data-stu-id="25317-110">String</span></span>|<span data-ttu-id="25317-111">Contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="25317-111">The content of the item.</span></span>|
|<span data-ttu-id="25317-112">contentType</span><span class="sxs-lookup"><span data-stu-id="25317-112">contentType</span></span>|<span data-ttu-id="25317-113">bodyType</span><span class="sxs-lookup"><span data-stu-id="25317-113">bodyType</span></span>|<span data-ttu-id="25317-p101">Tipo de contenido. Valores posibles: `Text` y `HTML`.</span><span class="sxs-lookup"><span data-stu-id="25317-p101">The type of the content. Possible values are `Text` and `HTML`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="25317-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="25317-116">JSON representation</span></span>

<span data-ttu-id="25317-117">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="25317-117">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.itemBody"
}-->

```json
{
  "content": "string",
  "contentType": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "itemBody resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
