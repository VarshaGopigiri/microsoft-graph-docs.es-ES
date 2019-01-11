---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Compartidos
localization_priority: Normal
ms.openlocfilehash: 3478a8911a402bf86a04f196d87409e7cddb246e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868078"
---
# <a name="shared-resource-type"></a><span data-ttu-id="436e7-102">Tipo de recurso Shared</span><span class="sxs-lookup"><span data-stu-id="436e7-102">Shared resource type</span></span>

<span data-ttu-id="436e7-p101">El recurso **Shared** indica que se ha compartido un objeto DriveItem con otros usuarios. El recurso incluye información sobre cómo se comparte el elemento.</span><span class="sxs-lookup"><span data-stu-id="436e7-p101">The **Shared** resource indicates a DriveItem has been shared with others. The resource includes information about how the item is shared.</span></span>

<span data-ttu-id="436e7-105">Si un objeto [**DriveItem**](driveitem.md) tiene una faceta **shared** que no es null, el elemento se ha compartido.</span><span class="sxs-lookup"><span data-stu-id="436e7-105">If a [**Driveitem**](driveitem.md) has a non-null **shared** facet, the item has been shared.</span></span>

## <a name="json-representation"></a><span data-ttu-id="436e7-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="436e7-106">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="436e7-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="436e7-107">Properties</span></span>

| <span data-ttu-id="436e7-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="436e7-108">Property</span></span>       | <span data-ttu-id="436e7-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="436e7-109">Type</span></span>                          | <span data-ttu-id="436e7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="436e7-110">Description</span></span>
| :------------- |:------------------------------|:----------------------------
| <span data-ttu-id="436e7-111">owner</span><span class="sxs-lookup"><span data-stu-id="436e7-111">owner</span></span>          | [<span data-ttu-id="436e7-112">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="436e7-112">IdentitySet</span></span>](identityset.md) | <span data-ttu-id="436e7-p102">La identidad del propietario del elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="436e7-p102">The identity of the owner of the shared item. Read-only.</span></span>
| <span data-ttu-id="436e7-115">scope</span><span class="sxs-lookup"><span data-stu-id="436e7-115">scope</span></span>          | <span data-ttu-id="436e7-116">String</span><span class="sxs-lookup"><span data-stu-id="436e7-116">String</span></span>                        | <span data-ttu-id="436e7-p103">Indica el ámbito sobre cómo se comparte el elemento: `anonymous`, `organization` o `users`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="436e7-p103">Indicates the scope of how the item is shared: `anonymous`, `organization`, or `users`. Read-only.</span></span>
| <span data-ttu-id="436e7-119">sharedBy</span><span class="sxs-lookup"><span data-stu-id="436e7-119">sharedBy</span></span>       | [<span data-ttu-id="436e7-120">identitySet</span><span class="sxs-lookup"><span data-stu-id="436e7-120">identitySet</span></span>](identityset.md) | <span data-ttu-id="436e7-p104">La identidad del usuario que ha compartido el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="436e7-p104">The identity of the user who shared the item. Read-only.</span></span>
| <span data-ttu-id="436e7-123">sharedDateTime</span><span class="sxs-lookup"><span data-stu-id="436e7-123">sharedDateTime</span></span> | <span data-ttu-id="436e7-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="436e7-124">DateTimeOffset</span></span>                | <span data-ttu-id="436e7-p105">Fecha y hora UTC de la última vez que se compartió el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="436e7-p105">The UTC date and time when the item was shared. Read-only.</span></span>

## <a name="scope-options"></a><span data-ttu-id="436e7-127">Opciones de ámbito</span><span class="sxs-lookup"><span data-stu-id="436e7-127">Scope options</span></span>

| <span data-ttu-id="436e7-128">Valor</span><span class="sxs-lookup"><span data-stu-id="436e7-128">Value</span></span>          | <span data-ttu-id="436e7-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="436e7-129">Description</span></span>                                                                           |
|:---------------|:--------------------------------------------------------------------------------------|
| `anonymous`    | <span data-ttu-id="436e7-130">El elemento se comparte mediante un vínculo que le funciona a cualquier usuario con el vínculo.</span><span class="sxs-lookup"><span data-stu-id="436e7-130">The item is shared by using a link that works for anyone with the link.</span></span>               |
| `organization` | <span data-ttu-id="436e7-131">El elemento se comparte mediante un vínculo que le funciona a cualquier usuario de la organización del propietario.</span><span class="sxs-lookup"><span data-stu-id="436e7-131">The item is shared by using a link that works for anyone in the owner's organization.</span></span> |
| `users`        | <span data-ttu-id="436e7-132">El elemento se comparte solo con usuarios específicos.</span><span class="sxs-lookup"><span data-stu-id="436e7-132">The item is shared with specific users only.</span></span>                                          |

## <a name="remarks"></a><span data-ttu-id="436e7-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="436e7-133">Remarks</span></span>

<span data-ttu-id="436e7-134">Para obtener más información sobre las facetas de **driveItem**, consulte [**driveItem**](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="436e7-134">For more information about the facets on a **driveItem**, see [**driveItem**](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The shared facet provides info about shared items.",
  "keywords": "shared,share,item,facet,onedrive",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/shared.md:
      Found potential enums in resource example that weren't defined in a table:(anonymous,organization,users) are in resource, but () are in table"
  ],
  "tocPath": "Facets/Shared"
} -->
