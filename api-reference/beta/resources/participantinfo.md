---
title: tipo de recurso participantInfo
description: Contiene propiedades adicionales acerca de la identidad del participante
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 7860c80da8e0f56ca425cffe8876d6003fba1d0d
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991415"
---
# <a name="participantinfo-resource-type"></a><span data-ttu-id="9fe8c-103">tipo de recurso participantInfo</span><span class="sxs-lookup"><span data-stu-id="9fe8c-103">participantInfo resource type</span></span>

> <span data-ttu-id="9fe8c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9fe8c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9fe8c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9fe8c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9fe8c-106">Contiene propiedades adicionales acerca de la identidad del participante</span><span class="sxs-lookup"><span data-stu-id="9fe8c-106">Contains additional properties about the participant identity</span></span>

## <a name="properties"></a><span data-ttu-id="9fe8c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9fe8c-107">Properties</span></span>

| <span data-ttu-id="9fe8c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9fe8c-108">Property</span></span>       | <span data-ttu-id="9fe8c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fe8c-109">Type</span></span>                          | <span data-ttu-id="9fe8c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fe8c-110">Description</span></span>  |
|:---------------|:------------------------------|:-------------|
| <span data-ttu-id="9fe8c-111">identity</span><span class="sxs-lookup"><span data-stu-id="9fe8c-111">identity</span></span>       | [<span data-ttu-id="9fe8c-112">identitySet</span><span class="sxs-lookup"><span data-stu-id="9fe8c-112">identitySet</span></span>](identityset.md) | <span data-ttu-id="9fe8c-113">El [identitySet](identityset.md) asociado a este participante.</span><span class="sxs-lookup"><span data-stu-id="9fe8c-113">The [identitySet](identityset.md) associated with this participant.</span></span> |
| <span data-ttu-id="9fe8c-114">languageId</span><span class="sxs-lookup"><span data-stu-id="9fe8c-114">languageId</span></span>     | <span data-ttu-id="9fe8c-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="9fe8c-115">String</span></span>                        | <span data-ttu-id="9fe8c-116">La cadena de referencia cultural del idioma.</span><span class="sxs-lookup"><span data-stu-id="9fe8c-116">The language culture string.</span></span> |
| <span data-ttu-id="9fe8c-117">región</span><span class="sxs-lookup"><span data-stu-id="9fe8c-117">region</span></span>         | <span data-ttu-id="9fe8c-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="9fe8c-118">String</span></span>                        | <span data-ttu-id="9fe8c-119">Región del participante.</span><span class="sxs-lookup"><span data-stu-id="9fe8c-119">Region of the participant.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="9fe8c-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9fe8c-120">JSON representation</span></span>

<span data-ttu-id="9fe8c-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9fe8c-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "languageId", "region"
  ],
  "@odata.type": "microsoft.graph.participantInfo"
}-->
```json
{
  "identity": { "@odata.type": "#microsoft.graph.identitySet" },
  "languageId": "String",
  "region": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "participantInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
