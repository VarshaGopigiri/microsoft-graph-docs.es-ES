---
title: " tipo de recurso certificationControl"
description: Este recurso contiene cumplimiento seguro de datos de certificación asociados con control de puntuación.
localization_priority: Normal
ms.openlocfilehash: 6f8269a85a8d3cb032f3e58457df95f4dd432c11
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810391"
---
#  <a name="certificationcontrol-resource-type"></a><span data-ttu-id="f3e1d-103">tipo de recurso certificationControl</span><span class="sxs-lookup"><span data-stu-id="f3e1d-103">certificationControl resource type</span></span>

<span data-ttu-id="f3e1d-104">Cumplimiento de normas de contiene datos de certificación asociados a garantizar el control de puntuación.</span><span class="sxs-lookup"><span data-stu-id="f3e1d-104">Contains compliance certification data associated with secure score control.</span></span>

|<span data-ttu-id="f3e1d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f3e1d-105">Property</span></span> |<span data-ttu-id="f3e1d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3e1d-106">Type</span></span> |<span data-ttu-id="f3e1d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3e1d-107">Description</span></span> |
|:--|:--|:--|
|<span data-ttu-id="f3e1d-108">name</span><span class="sxs-lookup"><span data-stu-id="f3e1d-108">name</span></span> | <span data-ttu-id="f3e1d-109">string</span><span class="sxs-lookup"><span data-stu-id="f3e1d-109">string</span></span> | <span data-ttu-id="f3e1d-110">Nombre del control de certificación</span><span class="sxs-lookup"><span data-stu-id="f3e1d-110">Certification control name</span></span> |
|<span data-ttu-id="f3e1d-111">url</span><span class="sxs-lookup"><span data-stu-id="f3e1d-111">url</span></span> | <span data-ttu-id="f3e1d-112">string</span><span class="sxs-lookup"><span data-stu-id="f3e1d-112">string</span></span> | <span data-ttu-id="f3e1d-113">Portal de confianza de la dirección URL del servicio de Microsoft</span><span class="sxs-lookup"><span data-stu-id="f3e1d-113">URL for the Microsoft Service Trust Portal</span></span> |

## <a name="json-representation"></a><span data-ttu-id="f3e1d-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f3e1d-114">JSON representation</span></span>

<span data-ttu-id="f3e1d-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f3e1d-115">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.certificationControl"
}-->

```json
{
  "name": "String",
  "url": "Collection(microsoft.graph.certificationControl)"
}

```


<!-- {
  "type": "#page.annotation",
  "description": "certificationControl resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
