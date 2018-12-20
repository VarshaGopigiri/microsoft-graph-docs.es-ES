---
title: tipo de recurso meetingCapability
description: Contiene las funciones de una reunión
author: VinodRavichandran
ms.openlocfilehash: 1a6f172922c0efbc9ad93e32141e364e2d0fc711
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380250"
---
# <a name="meetingcapability-resource-type"></a><span data-ttu-id="4159e-103">tipo de recurso meetingCapability</span><span class="sxs-lookup"><span data-stu-id="4159e-103">meetingCapability resource type</span></span>

> <span data-ttu-id="4159e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4159e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4159e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4159e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4159e-106">Contiene las funciones de una reunión</span><span class="sxs-lookup"><span data-stu-id="4159e-106">Contains the capabilities of a meeting</span></span>

## <a name="properties"></a><span data-ttu-id="4159e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4159e-107">Properties</span></span>

| <span data-ttu-id="4159e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4159e-108">Property</span></span>                          | <span data-ttu-id="4159e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4159e-109">Type</span></span>    | <span data-ttu-id="4159e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4159e-110">Description</span></span>                                                        |
|:----------------------------------|:--------|:-------------------------------------------------------------------|
| <span data-ttu-id="4159e-111">allowAnonymousUsersToDialOut</span><span class="sxs-lookup"><span data-stu-id="4159e-111">allowAnonymousUsersToDialOut</span></span>      | <span data-ttu-id="4159e-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="4159e-112">Boolean</span></span> | <span data-ttu-id="4159e-113">Indica si se permiten hacer llamadas de los usuarios anónimos en una reunión.</span><span class="sxs-lookup"><span data-stu-id="4159e-113">Indicates whether anonymous users dialout is allowed in a meeting.</span></span> |
| <span data-ttu-id="4159e-114">allowAnonymousUsersToStartMeeting</span><span class="sxs-lookup"><span data-stu-id="4159e-114">allowAnonymousUsersToStartMeeting</span></span> | <span data-ttu-id="4159e-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="4159e-115">Boolean</span></span> | <span data-ttu-id="4159e-116">Indica si se permiten a los usuarios anónimos para iniciar una reunión.</span><span class="sxs-lookup"><span data-stu-id="4159e-116">Indicates whether anonymous users are allowed to start a meeting.</span></span>  |
| <span data-ttu-id="4159e-117">autoAdmittedUsers</span><span class="sxs-lookup"><span data-stu-id="4159e-117">autoAdmittedUsers</span></span>                 | <span data-ttu-id="4159e-118">String</span><span class="sxs-lookup"><span data-stu-id="4159e-118">String</span></span>  | <span data-ttu-id="4159e-119">Los valores posibles son: `everyoneInCompany` y `everyone`.</span><span class="sxs-lookup"><span data-stu-id="4159e-119">Possible values are: `everyoneInCompany`, `everyone`.</span></span>              |

## <a name="json-representation"></a><span data-ttu-id="4159e-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4159e-120">JSON representation</span></span>

<span data-ttu-id="4159e-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4159e-121">The following is a JSON representation of the resource.</span></span>

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
