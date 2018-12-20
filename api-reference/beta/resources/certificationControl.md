---
title: " tipo de recurso certificationControl"
description: Este recurso contiene cumplimiento seguro de datos de certificación asociados con control de puntuación.
ms.openlocfilehash: 62b6627a9bb1a012d6d7e542d87abbaddb0e279a
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380948"
---
#  <a name="certificationcontrol-resource-type"></a><span data-ttu-id="4a6de-103">tipo de recurso certificationControl</span><span class="sxs-lookup"><span data-stu-id="4a6de-103">certificationControl resource type</span></span>

<span data-ttu-id="4a6de-104">Cumplimiento de normas de contiene datos de certificación asociados a garantizar el control de puntuación.</span><span class="sxs-lookup"><span data-stu-id="4a6de-104">Contains compliance certification data associated with secure score control.</span></span>

|<span data-ttu-id="4a6de-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a6de-105">Property</span></span> |<span data-ttu-id="4a6de-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a6de-106">Type</span></span> |<span data-ttu-id="4a6de-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a6de-107">Description</span></span> |
|:--|:--|:--|
|<span data-ttu-id="4a6de-108">name</span><span class="sxs-lookup"><span data-stu-id="4a6de-108">name</span></span> | <span data-ttu-id="4a6de-109">string</span><span class="sxs-lookup"><span data-stu-id="4a6de-109">string</span></span> | <span data-ttu-id="4a6de-110">Nombre del control de certificación</span><span class="sxs-lookup"><span data-stu-id="4a6de-110">Certification control name</span></span> |
|<span data-ttu-id="4a6de-111">url</span><span class="sxs-lookup"><span data-stu-id="4a6de-111">url</span></span> | <span data-ttu-id="4a6de-112">string</span><span class="sxs-lookup"><span data-stu-id="4a6de-112">string</span></span> | <span data-ttu-id="4a6de-113">Portal de confianza de la dirección URL del servicio de Microsoft</span><span class="sxs-lookup"><span data-stu-id="4a6de-113">URL for the Microsoft Service Trust Portal</span></span> |

## <a name="json-representation"></a><span data-ttu-id="4a6de-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4a6de-114">JSON representation</span></span>

<span data-ttu-id="4a6de-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4a6de-115">The following is a JSON representation of the resource.</span></span>

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
