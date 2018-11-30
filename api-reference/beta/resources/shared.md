---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Compartidos
ms.openlocfilehash: 38bc8604ba2528a24e2193a2fb521428b2b5c2d3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088890"
---
# <a name="shared-resource-type"></a><span data-ttu-id="4b234-102">Tipo de recurso Shared</span><span class="sxs-lookup"><span data-stu-id="4b234-102">Shared resource type</span></span>

> <span data-ttu-id="4b234-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4b234-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4b234-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4b234-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4b234-p102">El recurso **Shared** indica que se ha compartido un objeto DriveItem con otros usuarios. El recurso incluye información sobre cómo se comparte el elemento.</span><span class="sxs-lookup"><span data-stu-id="4b234-p102">The **Shared** resource indicates a DriveItem has been shared with others. The resource includes information about how the item is shared.</span></span>

<span data-ttu-id="4b234-107">Si un objeto [**DriveItem**](driveitem.md) tiene una faceta **shared** que no es null, el elemento se ha compartido.</span><span class="sxs-lookup"><span data-stu-id="4b234-107">If a [**Driveitem**](driveitem.md) has a non-null **shared** facet, the item has been shared.</span></span>

## <a name="json-representation"></a><span data-ttu-id="4b234-108">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4b234-108">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.shared",
  "optionalProperties": [ "sharedBy", "sharedDateTime" ]
}-->

```json
{
  "owner": { "@odata.type": "microsoft.graph.identitySet" },
  "scope": "anonymous | organization | users",
  "sharedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "sharedDateTime": "datetime"
}
```

## <a name="properties"></a><span data-ttu-id="4b234-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4b234-109">Properties</span></span>

| <span data-ttu-id="4b234-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4b234-110">Property</span></span>       | <span data-ttu-id="4b234-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="4b234-111">Type</span></span>                          | <span data-ttu-id="4b234-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b234-112">Description</span></span>
| :------------- |:------------------------------|:----------------------------
| <span data-ttu-id="4b234-113">owner</span><span class="sxs-lookup"><span data-stu-id="4b234-113">owner</span></span>          | [<span data-ttu-id="4b234-114">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="4b234-114">IdentitySet</span></span>](identityset.md) | <span data-ttu-id="4b234-p103">La identidad del propietario del elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4b234-p103">The identity of the owner of the shared item. Read-only.</span></span>
| <span data-ttu-id="4b234-117">scope</span><span class="sxs-lookup"><span data-stu-id="4b234-117">scope</span></span>          | <span data-ttu-id="4b234-118">String</span><span class="sxs-lookup"><span data-stu-id="4b234-118">String</span></span>                        | <span data-ttu-id="4b234-p104">Indica el ámbito sobre cómo se comparte el elemento: `anonymous`, `organization` o `users`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4b234-p104">Indicates the scope of how the item is shared: `anonymous`, `organization`, or `users`. Read-only.</span></span>
| <span data-ttu-id="4b234-121">sharedBy</span><span class="sxs-lookup"><span data-stu-id="4b234-121">sharedBy</span></span>       | [<span data-ttu-id="4b234-122">identitySet</span><span class="sxs-lookup"><span data-stu-id="4b234-122">identitySet</span></span>](identityset.md) | <span data-ttu-id="4b234-p105">La identidad del usuario que ha compartido el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4b234-p105">The identity of the user who shared the item. Read-only.</span></span>
| <span data-ttu-id="4b234-125">sharedDateTime</span><span class="sxs-lookup"><span data-stu-id="4b234-125">sharedDateTime</span></span> | <span data-ttu-id="4b234-126">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4b234-126">DateTimeOffset</span></span>                | <span data-ttu-id="4b234-p106">Fecha y hora UTC de la última vez que se compartió el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4b234-p106">The UTC date and time when the item was shared. Read-only.</span></span>

## <a name="scope-values"></a><span data-ttu-id="4b234-129">Valores del ámbito</span><span class="sxs-lookup"><span data-stu-id="4b234-129">Scope values</span></span>

| <span data-ttu-id="4b234-130">Valor</span><span class="sxs-lookup"><span data-stu-id="4b234-130">Value</span></span>          | <span data-ttu-id="4b234-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="4b234-131">Description</span></span>                                                                           |
|:---------------|:--------------------------------------------------------------------------------------|
| `anonymous`    | <span data-ttu-id="4b234-132">El elemento se comparte mediante un vínculo que le funciona a cualquier usuario con el vínculo.</span><span class="sxs-lookup"><span data-stu-id="4b234-132">The item is shared by using a link that works for anyone with the link.</span></span>               |
| `organization` | <span data-ttu-id="4b234-133">El elemento se comparte mediante un vínculo que le funciona a cualquier usuario de la organización del propietario.</span><span class="sxs-lookup"><span data-stu-id="4b234-133">The item is shared by using a link that works for anyone in the owner's organization.</span></span> |
| `users`        | <span data-ttu-id="4b234-134">El elemento se comparte solo con usuarios específicos.</span><span class="sxs-lookup"><span data-stu-id="4b234-134">The item is shared with specific users only.</span></span>                                          |

## <a name="remarks"></a><span data-ttu-id="4b234-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4b234-135">Remarks</span></span>

<span data-ttu-id="4b234-136">Para obtener más información sobre las facetas de **driveItem**, consulte [**driveItem**](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="4b234-136">For more information about the facets on a **driveItem**, see [**driveItem**](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The shared facet provides info about shared items.",
  "keywords": "shared,share,item,facet,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Shared"
} -->
