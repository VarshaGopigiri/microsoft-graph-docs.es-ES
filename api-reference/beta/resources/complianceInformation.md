---
title: " tipo de recurso complianceInformation"
description: Este recurso contiene cumplimiento seguro de los datos asociados con el control de puntuación.
localization_priority: Normal
ms.openlocfilehash: 7a3968e6e043d2019100870061c5e34b03b1b8bd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820604"
---
#  <a name="complianceinformation-resource-type"></a><span data-ttu-id="4c2ac-103">tipo de recurso complianceInformation</span><span class="sxs-lookup"><span data-stu-id="4c2ac-103">complianceInformation resource type</span></span>

<span data-ttu-id="4c2ac-104">Contiene el cumplimiento seguro de los datos asociados con el control de puntuación.</span><span class="sxs-lookup"><span data-stu-id="4c2ac-104">Contains compliance data associated with secure score control.</span></span>

|<span data-ttu-id="4c2ac-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4c2ac-105">Property</span></span> |<span data-ttu-id="4c2ac-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c2ac-106">Type</span></span> |<span data-ttu-id="4c2ac-107">Description</span><span class="sxs-lookup"><span data-stu-id="4c2ac-107">Description</span></span> |
|:--|:--|:--|
|<span data-ttu-id="4c2ac-108">certificationName</span><span class="sxs-lookup"><span data-stu-id="4c2ac-108">certificationName</span></span> | <span data-ttu-id="4c2ac-109">string</span><span class="sxs-lookup"><span data-stu-id="4c2ac-109">string</span></span> | <span data-ttu-id="4c2ac-110">Nombre de certificación de cumplimiento de normas (por ejemplo, ISO 27018:2014, GDPR, FedRAMP, NIST 800-171)</span><span class="sxs-lookup"><span data-stu-id="4c2ac-110">Compliance certification name (for example, ISO 27018:2014, GDPR, FedRAMP, NIST 800-171)</span></span> |
|<span data-ttu-id="4c2ac-111">certificationControls</span><span class="sxs-lookup"><span data-stu-id="4c2ac-111">certificationControls</span></span> | <span data-ttu-id="4c2ac-112">colección de [certificationControl](certificationcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="4c2ac-112">[certificationControl](certificationcontrol.md) collection</span></span> | <span data-ttu-id="4c2ac-113">Colección de los controles de certificación asociados con la certificación</span><span class="sxs-lookup"><span data-stu-id="4c2ac-113">Collection of the certification controls associated with certification</span></span> |

## <a name="json-representation"></a><span data-ttu-id="4c2ac-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4c2ac-114">JSON representation</span></span>

<span data-ttu-id="4c2ac-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4c2ac-115">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.complianceInformation"
}-->

```json
{
  "certificationName": "String",
  "certificationControls": "Collection(microsoft.graph.complianceInformation)"
}

```


<!-- {
  "type": "#page.annotation",
  "description": "complianceInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
