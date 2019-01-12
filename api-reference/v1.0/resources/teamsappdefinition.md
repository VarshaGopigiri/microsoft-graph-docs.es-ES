---
title: tipo de recurso teamsAppDefinition
description: Los detalles de una versión de un teamsApp.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 3aed533ecca3bff48071b04adadcea6b52169f89
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27951932"
---
# <a name="teamsappdefinition-resource-type"></a><span data-ttu-id="ce30f-103">tipo de recurso teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="ce30f-103">teamsAppDefinition resource type</span></span>



<span data-ttu-id="ce30f-104">Los detalles de una versión de un [teamsApp](teamsapp.md).</span><span class="sxs-lookup"><span data-stu-id="ce30f-104">The details of one version of a [teamsApp](teamsapp.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ce30f-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ce30f-105">Properties</span></span>

| <span data-ttu-id="ce30f-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce30f-106">Property</span></span>            | <span data-ttu-id="ce30f-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce30f-107">Type</span></span>     | <span data-ttu-id="ce30f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce30f-108">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="ce30f-109">id</span><span class="sxs-lookup"><span data-stu-id="ce30f-109">id</span></span>                  | <span data-ttu-id="ce30f-110">string</span><span class="sxs-lookup"><span data-stu-id="ce30f-110">string</span></span>   | <span data-ttu-id="ce30f-111">Un identificador único (no el identificador de aplicación de los equipos).</span><span class="sxs-lookup"><span data-stu-id="ce30f-111">A unique id (not the teams appid).</span></span> |
| <span data-ttu-id="ce30f-112">teamsAppId</span><span class="sxs-lookup"><span data-stu-id="ce30f-112">teamsAppId</span></span>          | <span data-ttu-id="ce30f-113">string</span><span class="sxs-lookup"><span data-stu-id="ce30f-113">string</span></span>   | <span data-ttu-id="ce30f-114">El identificador de manifiesto de la aplicación de los equipos.</span><span class="sxs-lookup"><span data-stu-id="ce30f-114">The id from the Teams App manifest.</span></span> |
| <span data-ttu-id="ce30f-115">displayName</span><span class="sxs-lookup"><span data-stu-id="ce30f-115">displayName</span></span>         | <span data-ttu-id="ce30f-116">string</span><span class="sxs-lookup"><span data-stu-id="ce30f-116">string</span></span>   | <span data-ttu-id="ce30f-117">El nombre de la aplicación proporcionada por el desarrollador de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ce30f-117">The name of the app provided by the app developer.</span></span> |
| <span data-ttu-id="ce30f-118">version</span><span class="sxs-lookup"><span data-stu-id="ce30f-118">version</span></span>             | <span data-ttu-id="ce30f-119">string</span><span class="sxs-lookup"><span data-stu-id="ce30f-119">string</span></span>   | <span data-ttu-id="ce30f-120">El número de versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ce30f-120">The version number of the application.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ce30f-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ce30f-121">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamsAppDefinition",
  "baseType": "microsoft.graph.entity"
}-->

```json
{
  "id": "string",
  "teamsAppId": "string",
  "displayName": "Test App",
  "version": "1.0.0",
}
```

# <a name="see-also"></a><span data-ttu-id="ce30f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce30f-122">See also</span></span>

- [<span data-ttu-id="ce30f-123">teamsApp</span><span class="sxs-lookup"><span data-stu-id="ce30f-123">teamsApp</span></span>](teamsapp.md)
- [<span data-ttu-id="ce30f-124">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="ce30f-124">teamsAppInstallation</span></span>](teamsappinstallation.md)
- [<span data-ttu-id="ce30f-125">teamsTab</span><span class="sxs-lookup"><span data-stu-id="ce30f-125">teamsTab</span></span>](../resources/teamstab.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

