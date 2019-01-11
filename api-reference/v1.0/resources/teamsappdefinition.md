---
title: tipo de recurso teamsAppDefinition
description: Los detalles de una versión de un teamsApp.
author: nkramer
localization_priority: Normal
ms.openlocfilehash: 8fafb266b2bfc2c7ea6e0951ac2906f133817246
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860980"
---
# <a name="teamsappdefinition-resource-type"></a><span data-ttu-id="9c684-103">tipo de recurso teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="9c684-103">teamsAppDefinition resource type</span></span>



<span data-ttu-id="9c684-104">Los detalles de una versión de un [teamsApp](teamsapp.md).</span><span class="sxs-lookup"><span data-stu-id="9c684-104">The details of one version of a [teamsApp](teamsapp.md).</span></span>

## <a name="properties"></a><span data-ttu-id="9c684-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c684-105">Properties</span></span>

| <span data-ttu-id="9c684-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9c684-106">Property</span></span>            | <span data-ttu-id="9c684-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="9c684-107">Type</span></span>     | <span data-ttu-id="9c684-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c684-108">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="9c684-109">id</span><span class="sxs-lookup"><span data-stu-id="9c684-109">id</span></span>                  | <span data-ttu-id="9c684-110">string</span><span class="sxs-lookup"><span data-stu-id="9c684-110">string</span></span>   | <span data-ttu-id="9c684-111">Un identificador único (no el identificador de aplicación de los equipos).</span><span class="sxs-lookup"><span data-stu-id="9c684-111">A unique id (not the teams appid).</span></span> |
| <span data-ttu-id="9c684-112">teamsAppId</span><span class="sxs-lookup"><span data-stu-id="9c684-112">teamsAppId</span></span>          | <span data-ttu-id="9c684-113">string</span><span class="sxs-lookup"><span data-stu-id="9c684-113">string</span></span>   | <span data-ttu-id="9c684-114">El identificador de manifiesto de la aplicación de los equipos.</span><span class="sxs-lookup"><span data-stu-id="9c684-114">The id from the Teams App manifest.</span></span> |
| <span data-ttu-id="9c684-115">displayName</span><span class="sxs-lookup"><span data-stu-id="9c684-115">displayName</span></span>         | <span data-ttu-id="9c684-116">string</span><span class="sxs-lookup"><span data-stu-id="9c684-116">string</span></span>   | <span data-ttu-id="9c684-117">El nombre de la aplicación proporcionada por el desarrollador de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9c684-117">The name of the app provided by the app developer.</span></span> |
| <span data-ttu-id="9c684-118">version</span><span class="sxs-lookup"><span data-stu-id="9c684-118">version</span></span>             | <span data-ttu-id="9c684-119">string</span><span class="sxs-lookup"><span data-stu-id="9c684-119">string</span></span>   | <span data-ttu-id="9c684-120">El número de versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9c684-120">The version number of the application.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="9c684-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9c684-121">JSON representation</span></span>

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

# <a name="see-also"></a><span data-ttu-id="9c684-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c684-122">See also</span></span>

- [<span data-ttu-id="9c684-123">teamsApp</span><span class="sxs-lookup"><span data-stu-id="9c684-123">teamsApp</span></span>](teamsapp.md)
- [<span data-ttu-id="9c684-124">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="9c684-124">teamsAppInstallation</span></span>](teamsappinstallation.md)
- [<span data-ttu-id="9c684-125">teamsTab</span><span class="sxs-lookup"><span data-stu-id="9c684-125">teamsTab</span></span>](../resources/teamstab.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

