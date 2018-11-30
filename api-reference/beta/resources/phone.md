---
title: Tipo de recurso phone
description: Representa un número de teléfono.
ms.openlocfilehash: d47f2c36f9913eb75868077bdd5bb2d599055c59
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083046"
---
# <a name="phone-resource-type"></a><span data-ttu-id="af405-103">Tipo de recurso phone</span><span class="sxs-lookup"><span data-stu-id="af405-103">phone resource type</span></span>

> <span data-ttu-id="af405-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="af405-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="af405-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="af405-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="af405-106">Representa un número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="af405-106">Represents a phone number.</span></span>


## <a name="properties"></a><span data-ttu-id="af405-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af405-107">Properties</span></span>
| <span data-ttu-id="af405-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="af405-108">Property</span></span>     | <span data-ttu-id="af405-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="af405-109">Type</span></span>   |<span data-ttu-id="af405-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="af405-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="af405-111">number</span><span class="sxs-lookup"><span data-stu-id="af405-111">number</span></span>|<span data-ttu-id="af405-112">string</span><span class="sxs-lookup"><span data-stu-id="af405-112">string</span></span>|<span data-ttu-id="af405-113">El número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="af405-113">The phone number.</span></span>|
|<span data-ttu-id="af405-114">type</span><span class="sxs-lookup"><span data-stu-id="af405-114">type</span></span>|<span data-ttu-id="af405-115">String</span><span class="sxs-lookup"><span data-stu-id="af405-115">String</span></span>|<span data-ttu-id="af405-p102">El tipo de número de teléfono. Valores posibles: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span><span class="sxs-lookup"><span data-stu-id="af405-p102">The type of phone number. Possible values are: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="af405-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="af405-118">JSON representation</span></span>

<span data-ttu-id="af405-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="af405-119">Here is a JSON representation of the resource.</span></span>

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