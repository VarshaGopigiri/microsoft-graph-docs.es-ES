---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Compartidos
ms.openlocfilehash: 1d828310a226edd0443ff3b5f60156df1e7c98cb
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="shared-resource-type"></a><span data-ttu-id="e54ed-102">Tipo de recurso Shared</span><span class="sxs-lookup"><span data-stu-id="e54ed-102">Shared resource type</span></span>

<span data-ttu-id="e54ed-103">El recurso **Shared** indica que se ha compartido un objeto DriveItem con otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="e54ed-103">The **Shared** resource indicates a DriveItem has been shared with others. The resource includes information about how the item is shared.</span></span>
<span data-ttu-id="e54ed-104">El recurso incluye información sobre cómo se comparte el elemento.</span><span class="sxs-lookup"><span data-stu-id="e54ed-104">The Shared resource indicates a DriveItem has been shared with others. The resource includes information about how the item is shared.</span></span>

<span data-ttu-id="e54ed-105">Si un objeto [**DriveItem**](driveitem.md) tiene una faceta **shared** que no es null, el elemento se ha compartido.</span><span class="sxs-lookup"><span data-stu-id="e54ed-105">If a [**Driveitem**](driveitem.md) has a non-null **shared** facet, the item has been shared.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e54ed-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e54ed-106">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="e54ed-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e54ed-107">Properties</span></span>

| <span data-ttu-id="e54ed-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e54ed-108">Property</span></span>       | <span data-ttu-id="e54ed-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e54ed-109">Type</span></span>                          | <span data-ttu-id="e54ed-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e54ed-110">Description</span></span>
| :------------- |:------------------------------|:----------------------------
| <span data-ttu-id="e54ed-111">owner</span><span class="sxs-lookup"><span data-stu-id="e54ed-111">owner</span></span>          | [<span data-ttu-id="e54ed-112">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="e54ed-112">IdentitySet</span></span>](identityset.md) | <span data-ttu-id="e54ed-p102">La identidad del propietario del elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e54ed-p102">The identity of the owner of the shared item. Read-only.</span></span>
| <span data-ttu-id="e54ed-115">scope</span><span class="sxs-lookup"><span data-stu-id="e54ed-115">scope</span></span>          | <span data-ttu-id="e54ed-116">String</span><span class="sxs-lookup"><span data-stu-id="e54ed-116">String</span></span>                        | <span data-ttu-id="e54ed-117">Indica el ámbito sobre cómo se comparte el elemento: `anonymous`, `organization` o `users`.</span><span class="sxs-lookup"><span data-stu-id="e54ed-117">Indicates the scope of how the item is shared: `anonymous`, `organization`, or `users`.</span></span> <span data-ttu-id="e54ed-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e54ed-118">Read-only.</span></span>
| <span data-ttu-id="e54ed-119">sharedBy</span><span class="sxs-lookup"><span data-stu-id="e54ed-119">sharedBy</span></span>       | [<span data-ttu-id="e54ed-120">identitySet</span><span class="sxs-lookup"><span data-stu-id="e54ed-120">identitySet</span></span>](identityset.md) | <span data-ttu-id="e54ed-p104">La identidad del usuario que ha compartido el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e54ed-p104">The identity of the user who shared the item. Read-only.</span></span>
| <span data-ttu-id="e54ed-123">sharedDateTime</span><span class="sxs-lookup"><span data-stu-id="e54ed-123">sharedDateTime</span></span> | <span data-ttu-id="e54ed-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e54ed-124">DateTimeOffset</span></span>                | <span data-ttu-id="e54ed-p105">Fecha y hora UTC de la última vez que se compartió el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e54ed-p105">The UTC date and time when the item was shared. Read-only.</span></span>

## <a name="scope-values"></a><span data-ttu-id="e54ed-127">Valores del ámbito</span><span class="sxs-lookup"><span data-stu-id="e54ed-127">Scope values</span></span>

| <span data-ttu-id="e54ed-128">Valor</span><span class="sxs-lookup"><span data-stu-id="e54ed-128">Value</span></span>          | <span data-ttu-id="e54ed-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="e54ed-129">Description</span></span>                                                                           |
|:---------------|:--------------------------------------------------------------------------------------|
| `anonymous`    | <span data-ttu-id="e54ed-130">El elemento se comparte mediante un vínculo que le funciona a cualquier usuario con el vínculo.</span><span class="sxs-lookup"><span data-stu-id="e54ed-130">The item is shared by using a link that works for anyone with the link.</span></span>               |
| `organization` | <span data-ttu-id="e54ed-131">El elemento se comparte mediante un vínculo que le funciona a cualquier usuario de la organización del propietario.</span><span class="sxs-lookup"><span data-stu-id="e54ed-131">The item is shared by using a link that works for anyone in the owner's organization.</span></span> |
| `users`        | <span data-ttu-id="e54ed-132">El elemento se comparte solo con usuarios específicos.</span><span class="sxs-lookup"><span data-stu-id="e54ed-132">The item is shared with specific users only.</span></span>                                          |

## <a name="remarks"></a><span data-ttu-id="e54ed-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e54ed-133">Remarks</span></span>

<span data-ttu-id="e54ed-134">Para obtener más información sobre las facetas de **driveItem**, consulte [**driveItem**](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="e54ed-134">For more information about the facets on a **driveItem**, see [**driveItem**](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The shared facet provides info about shared items.",
  "keywords": "shared,share,item,facet,onedrive",
  "section": "documentation",
  "tocPath": "Facets/Shared"
} -->
