---
title: tipo de recurso mentionsPreview
description: Representa información acerca de los objetos de mención en una instancia de recursos.
ms.openlocfilehash: cf6bed3cdfb2d3f541438da0c06fcf8f4873c17e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089766"
---
# <a name="mentionspreview-resource-type"></a><span data-ttu-id="ca93a-103">tipo de recurso mentionsPreview</span><span class="sxs-lookup"><span data-stu-id="ca93a-103">mentionsPreview resource type</span></span>

> <span data-ttu-id="ca93a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ca93a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ca93a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ca93a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ca93a-106">Representa información sobre los objetos [mencione](../resources/mention.md) en una instancia de recursos.</span><span class="sxs-lookup"><span data-stu-id="ca93a-106">Represents information about [mention](../resources/mention.md) objects in a resource instance.</span></span>

## <a name="properties"></a><span data-ttu-id="ca93a-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca93a-107">Properties</span></span>
| <span data-ttu-id="ca93a-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ca93a-108">Property</span></span>     | <span data-ttu-id="ca93a-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca93a-109">Type</span></span>   |<span data-ttu-id="ca93a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca93a-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ca93a-111">isMentioned</span><span class="sxs-lookup"><span data-stu-id="ca93a-111">isMentioned</span></span> | <span data-ttu-id="ca93a-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="ca93a-112">Boolean</span></span> | <span data-ttu-id="ca93a-113">Es True si el usuario ha iniciado sesión se menciona en la instancia de recurso primario.</span><span class="sxs-lookup"><span data-stu-id="ca93a-113">True if the signed-in user is mentioned in the parent resource instance.</span></span> <span data-ttu-id="ca93a-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ca93a-114">Read-only.</span></span> <span data-ttu-id="ca93a-115">Filtro de admite.</span><span class="sxs-lookup"><span data-stu-id="ca93a-115">Supports filter.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ca93a-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ca93a-116">JSON representation</span></span>

<span data-ttu-id="ca93a-117">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ca93a-117">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mentionsPreview"
}-->

```json
{
  "isMentioned": "Boolean"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mentionsPreview resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->