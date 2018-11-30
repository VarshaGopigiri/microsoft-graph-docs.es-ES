---
title: tipo de recurso meetingCapability
description: Contiene las funciones de una reunión
ms.openlocfilehash: 438193d08ab5542f07d4cbf61704520d81433e50
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086418"
---
# <a name="meetingcapability-resource-type"></a><span data-ttu-id="ee210-103">tipo de recurso meetingCapability</span><span class="sxs-lookup"><span data-stu-id="ee210-103">meetingCapability resource type</span></span>

> <span data-ttu-id="ee210-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ee210-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ee210-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ee210-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ee210-106">Contiene las funciones de una reunión</span><span class="sxs-lookup"><span data-stu-id="ee210-106">Contains the capabilities of a meeting</span></span>

## <a name="properties"></a><span data-ttu-id="ee210-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ee210-107">Properties</span></span>

| <span data-ttu-id="ee210-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ee210-108">Property</span></span>       | <span data-ttu-id="ee210-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee210-109">Type</span></span>    | <span data-ttu-id="ee210-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee210-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ee210-111">allowAnonymousUsersToDialOut</span><span class="sxs-lookup"><span data-stu-id="ee210-111">allowAnonymousUsersToDialOut</span></span> | <span data-ttu-id="ee210-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="ee210-112">Boolean</span></span> | <span data-ttu-id="ee210-113">Indica si se permiten hacer llamadas de los usuarios anónimos en una reunión.</span><span class="sxs-lookup"><span data-stu-id="ee210-113">Indicates whether anonymous users dialout is allowed in a meeting.</span></span> |
| <span data-ttu-id="ee210-114">autoAdmittedUsers</span><span class="sxs-lookup"><span data-stu-id="ee210-114">autoAdmittedUsers</span></span> | <span data-ttu-id="ee210-115">String</span><span class="sxs-lookup"><span data-stu-id="ee210-115">String</span></span> | <span data-ttu-id="ee210-116">Los valores posibles son: `everyoneInCompany` y `everyone`.</span><span class="sxs-lookup"><span data-stu-id="ee210-116">Possible values are: `everyoneInCompany`, `everyone`.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ee210-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ee210-117">JSON representation</span></span>

<span data-ttu-id="ee210-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ee210-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingCapability"
}-->
```json
{
  "allowAnonymousUsersToDialOut": true,
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
