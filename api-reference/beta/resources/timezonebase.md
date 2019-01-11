---
title: Tipo de recurso timeZoneBase
description: Representación básica de una zona horaria.
localization_priority: Normal
ms.openlocfilehash: 95d3409c40b3cc151f7b2f4b69580b9c1bbbe1ed
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882456"
---
# <a name="timezonebase-resource-type"></a><span data-ttu-id="45a43-103">Tipo de recurso timeZoneBase</span><span class="sxs-lookup"><span data-stu-id="45a43-103">timeZoneBase resource type</span></span>

> <span data-ttu-id="45a43-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="45a43-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="45a43-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="45a43-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="45a43-106">Representación básica de una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="45a43-106">The basic representation of a time zone.</span></span>


## <a name="properties"></a><span data-ttu-id="45a43-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="45a43-107">Properties</span></span>
| <span data-ttu-id="45a43-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="45a43-108">Property</span></span>     | <span data-ttu-id="45a43-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="45a43-109">Type</span></span>   |<span data-ttu-id="45a43-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="45a43-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="45a43-111">name</span><span class="sxs-lookup"><span data-stu-id="45a43-111">name</span></span> | <span data-ttu-id="45a43-112">string</span><span class="sxs-lookup"><span data-stu-id="45a43-112">string</span></span> | <span data-ttu-id="45a43-113">Nombre de una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="45a43-113">The name of a time zone.</span></span> <span data-ttu-id="45a43-114">Puede ser un nombre de zona de hora estándar como "hora estándar de Hawái-Aleutianas" o "zona horaria personalizada" para una zona horaria personalizada.</span><span class="sxs-lookup"><span data-stu-id="45a43-114">It can be a standard time zone name such as "Hawaii-Aleutian Standard Time", or "Customized Time Zone" for a custom time zone.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="45a43-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="45a43-115">JSON representation</span></span>

<span data-ttu-id="45a43-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="45a43-116">Here is a JSON representation of the resource.</span></span>

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
