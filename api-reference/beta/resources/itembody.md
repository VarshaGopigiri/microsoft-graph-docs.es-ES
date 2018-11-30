---
title: Tipo de recurso itemBody
description: Representa las propiedades del cuerpo de un elemento, como un mensaje, un evento o una publicación de grupo.
ms.openlocfilehash: 4ceada2ffe8106c270aa262d32ff85e349a8e657
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083218"
---
# <a name="itembody-resource-type"></a><span data-ttu-id="d81ff-103">Tipo de recurso itemBody</span><span class="sxs-lookup"><span data-stu-id="d81ff-103">itemBody resource type</span></span>

> <span data-ttu-id="d81ff-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d81ff-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d81ff-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d81ff-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d81ff-106">Representa las propiedades del cuerpo de un elemento, como un mensaje, un evento o una publicación de grupo.</span><span class="sxs-lookup"><span data-stu-id="d81ff-106">Represents properties of the body of an item, such as a message, event or group post.</span></span>

## <a name="properties"></a><span data-ttu-id="d81ff-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d81ff-107">Properties</span></span>
| <span data-ttu-id="d81ff-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d81ff-108">Property</span></span>     | <span data-ttu-id="d81ff-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d81ff-109">Type</span></span>   |<span data-ttu-id="d81ff-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d81ff-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d81ff-111">content</span><span class="sxs-lookup"><span data-stu-id="d81ff-111">content</span></span>|<span data-ttu-id="d81ff-112">String</span><span class="sxs-lookup"><span data-stu-id="d81ff-112">String</span></span>|<span data-ttu-id="d81ff-113">Contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="d81ff-113">The content of the item.</span></span>|
|<span data-ttu-id="d81ff-114">contentType</span><span class="sxs-lookup"><span data-stu-id="d81ff-114">contentType</span></span>|<span data-ttu-id="d81ff-115">String</span><span class="sxs-lookup"><span data-stu-id="d81ff-115">String</span></span>|<span data-ttu-id="d81ff-p102">Tipo de contenido. Valores posibles: `Text` y `HTML`.</span><span class="sxs-lookup"><span data-stu-id="d81ff-p102">The type of the content. Possible values are `Text` and `HTML`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d81ff-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d81ff-118">JSON representation</span></span>

<span data-ttu-id="d81ff-119">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d81ff-119">Here is a JSON representation of the resource</span></span>

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
