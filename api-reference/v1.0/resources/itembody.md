---
title: Tipo de recurso itemBody
description: Representa las propiedades del cuerpo de un elemento, como un mensaje, un evento o una publicación de grupo.
localization_priority: Normal
ms.openlocfilehash: 2eaf3b5e13833665c452eeecd74169915f5ac2fd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805232"
---
# <a name="itembody-resource-type"></a><span data-ttu-id="d6931-103">Tipo de recurso itemBody</span><span class="sxs-lookup"><span data-stu-id="d6931-103">itemBody resource type</span></span>

<span data-ttu-id="d6931-104">Representa las propiedades del cuerpo de un elemento, como un mensaje, un evento o una publicación de grupo.</span><span class="sxs-lookup"><span data-stu-id="d6931-104">Represents properties of the body of an item, such as a message, event or group post.</span></span>

## <a name="properties"></a><span data-ttu-id="d6931-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6931-105">Properties</span></span>
| <span data-ttu-id="d6931-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d6931-106">Property</span></span>     | <span data-ttu-id="d6931-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6931-107">Type</span></span>   |<span data-ttu-id="d6931-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6931-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d6931-109">content</span><span class="sxs-lookup"><span data-stu-id="d6931-109">content</span></span>|<span data-ttu-id="d6931-110">String</span><span class="sxs-lookup"><span data-stu-id="d6931-110">String</span></span>|<span data-ttu-id="d6931-111">Contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="d6931-111">The content of the item.</span></span>|
|<span data-ttu-id="d6931-112">contentType</span><span class="sxs-lookup"><span data-stu-id="d6931-112">contentType</span></span>|<span data-ttu-id="d6931-113">bodyType</span><span class="sxs-lookup"><span data-stu-id="d6931-113">bodyType</span></span>|<span data-ttu-id="d6931-p101">Tipo de contenido. Valores posibles: `Text` y `HTML`.</span><span class="sxs-lookup"><span data-stu-id="d6931-p101">The type of the content. Possible values are `Text` and `HTML`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d6931-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d6931-116">JSON representation</span></span>

<span data-ttu-id="d6931-117">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d6931-117">Here is a JSON representation of the resource</span></span>

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
