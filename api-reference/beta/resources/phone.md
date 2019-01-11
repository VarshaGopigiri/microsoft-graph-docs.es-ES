---
title: Tipo de recurso phone
description: Representa un número de teléfono.
localization_priority: Normal
ms.openlocfilehash: 7397349e1fee1164d3bcde8ebc785edd9402fe75
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874182"
---
# <a name="phone-resource-type"></a><span data-ttu-id="f885f-103">Tipo de recurso phone</span><span class="sxs-lookup"><span data-stu-id="f885f-103">phone resource type</span></span>

> <span data-ttu-id="f885f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f885f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f885f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f885f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f885f-106">Representa un número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="f885f-106">Represents a phone number.</span></span>


## <a name="properties"></a><span data-ttu-id="f885f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f885f-107">Properties</span></span>
| <span data-ttu-id="f885f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f885f-108">Property</span></span>     | <span data-ttu-id="f885f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f885f-109">Type</span></span>   |<span data-ttu-id="f885f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f885f-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f885f-111">number</span><span class="sxs-lookup"><span data-stu-id="f885f-111">number</span></span>|<span data-ttu-id="f885f-112">string</span><span class="sxs-lookup"><span data-stu-id="f885f-112">string</span></span>|<span data-ttu-id="f885f-113">El número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="f885f-113">The phone number.</span></span>|
|<span data-ttu-id="f885f-114">type</span><span class="sxs-lookup"><span data-stu-id="f885f-114">type</span></span>|<span data-ttu-id="f885f-115">String</span><span class="sxs-lookup"><span data-stu-id="f885f-115">String</span></span>|<span data-ttu-id="f885f-p102">El tipo de número de teléfono. Valores posibles: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span><span class="sxs-lookup"><span data-stu-id="f885f-p102">The type of phone number. Possible values are: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f885f-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f885f-118">JSON representation</span></span>

<span data-ttu-id="f885f-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f885f-119">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.phone"
}-->

```json
{
  "number": "string",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "phone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
