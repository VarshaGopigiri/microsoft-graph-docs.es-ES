---
title: Tipo de recurso timeZoneBase
description: Representación básica de una zona horaria.
ms.openlocfilehash: 18df657ab561163b64bcf224f8902f2ba7e0039c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030691"
---
# <a name="timezonebase-resource-type"></a><span data-ttu-id="7c0cc-103">Tipo de recurso timeZoneBase</span><span class="sxs-lookup"><span data-stu-id="7c0cc-103">timeZoneBase resource type</span></span>

<span data-ttu-id="7c0cc-104">Representación básica de una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="7c0cc-104">The basic representation of a time zone.</span></span>


## <a name="properties"></a><span data-ttu-id="7c0cc-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c0cc-105">Properties</span></span>
| <span data-ttu-id="7c0cc-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7c0cc-106">Property</span></span>     | <span data-ttu-id="7c0cc-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c0cc-107">Type</span></span>   |<span data-ttu-id="7c0cc-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c0cc-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7c0cc-109">name</span><span class="sxs-lookup"><span data-stu-id="7c0cc-109">name</span></span> | <span data-ttu-id="7c0cc-110">string</span><span class="sxs-lookup"><span data-stu-id="7c0cc-110">string</span></span> | <span data-ttu-id="7c0cc-111">Nombre de una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="7c0cc-111">The name of a time zone.</span></span> <span data-ttu-id="7c0cc-112">Puede ser un nombre de zona de hora estándar como "hora estándar de Hawái-Aleutianas" o "zona horaria personalizada" para una zona horaria personalizada.</span><span class="sxs-lookup"><span data-stu-id="7c0cc-112">It can be a standard time zone name such as "Hawaii-Aleutian Standard Time", or "Customized Time Zone" for a custom time zone.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="7c0cc-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7c0cc-113">JSON representation</span></span>

<span data-ttu-id="7c0cc-114">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7c0cc-114">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeZoneBase"
}-->

```json
{
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeZoneBase resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->