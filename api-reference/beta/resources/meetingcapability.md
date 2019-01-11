---
title: tipo de recurso meetingCapability
description: Contiene las funciones de una reunión
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 3a7f291c81522d33bffbcce6e97a407f09234db5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825812"
---
# <a name="meetingcapability-resource-type"></a><span data-ttu-id="7c371-103">tipo de recurso meetingCapability</span><span class="sxs-lookup"><span data-stu-id="7c371-103">meetingCapability resource type</span></span>

> <span data-ttu-id="7c371-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c371-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c371-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c371-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7c371-106">Contiene las funciones de una reunión</span><span class="sxs-lookup"><span data-stu-id="7c371-106">Contains the capabilities of a meeting</span></span>

## <a name="properties"></a><span data-ttu-id="7c371-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c371-107">Properties</span></span>

| <span data-ttu-id="7c371-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7c371-108">Property</span></span>                          | <span data-ttu-id="7c371-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c371-109">Type</span></span>    | <span data-ttu-id="7c371-110">Description</span><span class="sxs-lookup"><span data-stu-id="7c371-110">Description</span></span>                                                        |
|:----------------------------------|:--------|:-------------------------------------------------------------------|
| <span data-ttu-id="7c371-111">allowAnonymousUsersToDialOut</span><span class="sxs-lookup"><span data-stu-id="7c371-111">allowAnonymousUsersToDialOut</span></span>      | <span data-ttu-id="7c371-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="7c371-112">Boolean</span></span> | <span data-ttu-id="7c371-113">Indica si se permiten hacer llamadas de los usuarios anónimos en una reunión.</span><span class="sxs-lookup"><span data-stu-id="7c371-113">Indicates whether anonymous users dialout is allowed in a meeting.</span></span> |
| <span data-ttu-id="7c371-114">allowAnonymousUsersToStartMeeting</span><span class="sxs-lookup"><span data-stu-id="7c371-114">allowAnonymousUsersToStartMeeting</span></span> | <span data-ttu-id="7c371-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="7c371-115">Boolean</span></span> | <span data-ttu-id="7c371-116">Indica si se permiten a los usuarios anónimos para iniciar una reunión.</span><span class="sxs-lookup"><span data-stu-id="7c371-116">Indicates whether anonymous users are allowed to start a meeting.</span></span>  |
| <span data-ttu-id="7c371-117">autoAdmittedUsers</span><span class="sxs-lookup"><span data-stu-id="7c371-117">autoAdmittedUsers</span></span>                 | <span data-ttu-id="7c371-118">String</span><span class="sxs-lookup"><span data-stu-id="7c371-118">String</span></span>  | <span data-ttu-id="7c371-119">Los valores posibles son: `everyoneInCompany` y `everyone`.</span><span class="sxs-lookup"><span data-stu-id="7c371-119">Possible values are: `everyoneInCompany`, `everyone`.</span></span>              |

## <a name="json-representation"></a><span data-ttu-id="7c371-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7c371-120">JSON representation</span></span>

<span data-ttu-id="7c371-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="7c371-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingCapability"
}-->
```json
{
  "allowAnonymousUsersToDialOut": true,
  "allowAnonymousUsersToStartMeeting": true,
  "autoAdmittedUsers": "everyoneInCompany | everyone"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "meetingCapability resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
