---
title: " tipo de recurso complianceInformation"
description: Este recurso contiene cumplimiento seguro de los datos asociados con el control de puntuación.
ms.openlocfilehash: a32670c6d11d391834358b769ae938a67b3d8aad
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380962"
---
#  <a name="complianceinformation-resource-type"></a><span data-ttu-id="e3192-103">tipo de recurso complianceInformation</span><span class="sxs-lookup"><span data-stu-id="e3192-103">complianceInformation resource type</span></span>

<span data-ttu-id="e3192-104">Contiene el cumplimiento seguro de los datos asociados con el control de puntuación.</span><span class="sxs-lookup"><span data-stu-id="e3192-104">Contains compliance data associated with secure score control.</span></span>

|<span data-ttu-id="e3192-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3192-105">Property</span></span> |<span data-ttu-id="e3192-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3192-106">Type</span></span> |<span data-ttu-id="e3192-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3192-107">Description</span></span> |
|:--|:--|:--|
|<span data-ttu-id="e3192-108">certificationName</span><span class="sxs-lookup"><span data-stu-id="e3192-108">certificationName</span></span> | <span data-ttu-id="e3192-109">string</span><span class="sxs-lookup"><span data-stu-id="e3192-109">string</span></span> | <span data-ttu-id="e3192-110">Nombre de certificación de cumplimiento de normas (por ejemplo, ISO 27018:2014, GDPR, FedRAMP, NIST 800-171)</span><span class="sxs-lookup"><span data-stu-id="e3192-110">Compliance certification name (for example, ISO 27018:2014, GDPR, FedRAMP, NIST 800-171)</span></span> |
|<span data-ttu-id="e3192-111">certificationControls</span><span class="sxs-lookup"><span data-stu-id="e3192-111">certificationControls</span></span> | <span data-ttu-id="e3192-112">colección de [certificationControl](certificationcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="e3192-112">[certificationControl](certificationcontrol.md) collection</span></span> | <span data-ttu-id="e3192-113">Colección de los controles de certificación asociados con la certificación</span><span class="sxs-lookup"><span data-stu-id="e3192-113">Collection of the certification controls associated with certification</span></span> |

## <a name="json-representation"></a><span data-ttu-id="e3192-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e3192-114">JSON representation</span></span>

<span data-ttu-id="e3192-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e3192-115">The following is a JSON representation of the resource.</span></span>

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
