---
title: tipo de recurso teamsAppDefinition
description: Los detalles de una versión de un teamsApp.
author: nkramer
ms.openlocfilehash: 71a1783131661aed120f375f7cc58d55fb0ca0d2
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27336837"
---
# <a name="teamsappdefinition-resource-type"></a><span data-ttu-id="a9c81-103">tipo de recurso teamsAppDefinition</span><span class="sxs-lookup"><span data-stu-id="a9c81-103">teamsAppDefinition resource type</span></span>

> <span data-ttu-id="a9c81-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a9c81-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a9c81-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a9c81-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a9c81-106">Los detalles de una versión de un [teamsApp](teamsapp.md).</span><span class="sxs-lookup"><span data-stu-id="a9c81-106">The details of one version of a [teamsApp](teamsapp.md).</span></span>

## <a name="properties"></a><span data-ttu-id="a9c81-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9c81-107">Properties</span></span>

| <span data-ttu-id="a9c81-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a9c81-108">Property</span></span>            | <span data-ttu-id="a9c81-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9c81-109">Type</span></span>     | <span data-ttu-id="a9c81-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9c81-110">Description</span></span> |
|:------------------- |:-------- |:----------- |
| <span data-ttu-id="a9c81-111">id</span><span class="sxs-lookup"><span data-stu-id="a9c81-111">id</span></span>                  | <span data-ttu-id="a9c81-112">string</span><span class="sxs-lookup"><span data-stu-id="a9c81-112">string</span></span>   | <span data-ttu-id="a9c81-113">Un identificador único (no el identificador de aplicación de los equipos).</span><span class="sxs-lookup"><span data-stu-id="a9c81-113">A unique id (not the teams appid).</span></span> |
| <span data-ttu-id="a9c81-114">teamsAppId</span><span class="sxs-lookup"><span data-stu-id="a9c81-114">teamsAppId</span></span>          | <span data-ttu-id="a9c81-115">string</span><span class="sxs-lookup"><span data-stu-id="a9c81-115">string</span></span>   | <span data-ttu-id="a9c81-116">El identificador de manifiesto de la aplicación de los equipos.</span><span class="sxs-lookup"><span data-stu-id="a9c81-116">The id from the Teams App manifest.</span></span> |
| <span data-ttu-id="a9c81-117">displayName</span><span class="sxs-lookup"><span data-stu-id="a9c81-117">displayName</span></span>         | <span data-ttu-id="a9c81-118">string</span><span class="sxs-lookup"><span data-stu-id="a9c81-118">string</span></span>   | <span data-ttu-id="a9c81-119">El nombre de la aplicación proporcionada por el desarrollador de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="a9c81-119">The name of the app provided by the app developer.</span></span> |
| <span data-ttu-id="a9c81-120">version</span><span class="sxs-lookup"><span data-stu-id="a9c81-120">version</span></span>             | <span data-ttu-id="a9c81-121">string</span><span class="sxs-lookup"><span data-stu-id="a9c81-121">string</span></span>   | <span data-ttu-id="a9c81-122">El número de versión de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a9c81-122">The version number of the application.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="a9c81-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a9c81-123">JSON representation</span></span>

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

# <a name="see-also"></a><span data-ttu-id="a9c81-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9c81-124">See also</span></span>

- [<span data-ttu-id="a9c81-125">teamsApp</span><span class="sxs-lookup"><span data-stu-id="a9c81-125">teamsApp</span></span>](teamsapp.md)
- [<span data-ttu-id="a9c81-126">teamsAppInstallation</span><span class="sxs-lookup"><span data-stu-id="a9c81-126">teamsAppInstallation</span></span>](teamsappinstallation.md)
- [<span data-ttu-id="a9c81-127">teamsTab</span><span class="sxs-lookup"><span data-stu-id="a9c81-127">teamsTab</span></span>](../resources/teamstab.md)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "teamsApp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

