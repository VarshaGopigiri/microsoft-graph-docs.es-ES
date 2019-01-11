---
title: tipo de recurso mailTipsError
description: Un error que se produce durante una acción.
localization_priority: Normal
ms.openlocfilehash: 7df13bb45471d89fdf25b4a251e441bbf2dfad9e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27865627"
---
# <a name="mailtipserror-resource-type"></a><span data-ttu-id="ae9b1-103">tipo de recurso mailTipsError</span><span class="sxs-lookup"><span data-stu-id="ae9b1-103">mailTipsError resource type</span></span>

> <span data-ttu-id="ae9b1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ae9b1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ae9b1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ae9b1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ae9b1-106">Un error que se produce durante una acción.</span><span class="sxs-lookup"><span data-stu-id="ae9b1-106">An error that occurs during an action.</span></span>

## <a name="properties"></a><span data-ttu-id="ae9b1-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae9b1-107">Properties</span></span>
| <span data-ttu-id="ae9b1-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ae9b1-108">Property</span></span>     | <span data-ttu-id="ae9b1-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ae9b1-109">Type</span></span>   |<span data-ttu-id="ae9b1-110">Description</span><span class="sxs-lookup"><span data-stu-id="ae9b1-110">Description</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ae9b1-111">message</span><span class="sxs-lookup"><span data-stu-id="ae9b1-111">message</span></span> | <span data-ttu-id="ae9b1-112">String</span><span class="sxs-lookup"><span data-stu-id="ae9b1-112">String</span></span> | <span data-ttu-id="ae9b1-113">Mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="ae9b1-113">The error message.</span></span> |
| <span data-ttu-id="ae9b1-114">código</span><span class="sxs-lookup"><span data-stu-id="ae9b1-114">code</span></span> | <span data-ttu-id="ae9b1-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="ae9b1-115">String</span></span> | <span data-ttu-id="ae9b1-116">Código de error.</span><span class="sxs-lookup"><span data-stu-id="ae9b1-116">The error code.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ae9b1-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ae9b1-117">JSON representation</span></span>

<span data-ttu-id="ae9b1-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ae9b1-118">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mailTipsError"
}-->

```json
{
  "message": "string",
  "code": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailTipsError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
