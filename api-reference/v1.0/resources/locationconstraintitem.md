---
title: Tipo de recurso locationConstraintItem
description: Las condiciones establecidas por un cliente para la ubicación de una reunión.
localization_priority: Normal
ms.openlocfilehash: d9124377172c7598d45b0be9b9f3f9799bd3e1f5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874322"
---
# <a name="locationconstraintitem-resource-type"></a><span data-ttu-id="989b0-103">Tipo de recurso locationConstraintItem</span><span class="sxs-lookup"><span data-stu-id="989b0-103">locationConstraintItem resource type</span></span>

<span data-ttu-id="989b0-104">Las condiciones establecidas por un cliente para la ubicación de una reunión.</span><span class="sxs-lookup"><span data-stu-id="989b0-104">The conditions stated by a client for the location of a meeting.</span></span>

<span data-ttu-id="989b0-105">Derivado de [ubicación](location.md).</span><span class="sxs-lookup"><span data-stu-id="989b0-105">Derived from [location](location.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="989b0-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="989b0-106">JSON representation</span></span>

<span data-ttu-id="989b0-107">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="989b0-107">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.location",
  "@odata.type": "microsoft.graph.locationConstraintItem"
}-->

```json
{
  "resolveAvailability": true,
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "displayName": "string",
  "locationEmailAddress": "string"
}

```
## <a name="properties"></a><span data-ttu-id="989b0-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="989b0-108">Properties</span></span>
| <span data-ttu-id="989b0-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="989b0-109">Property</span></span>     | <span data-ttu-id="989b0-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="989b0-110">Type</span></span>   |<span data-ttu-id="989b0-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="989b0-111">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="989b0-112">address</span><span class="sxs-lookup"><span data-stu-id="989b0-112">address</span></span> | [<span data-ttu-id="989b0-113">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="989b0-113">physicalAddress</span></span>](physicaladdress.md) |<span data-ttu-id="989b0-114">Dirección postal de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="989b0-114">The street address of the location.</span></span> |
| <span data-ttu-id="989b0-115">displayName</span><span class="sxs-lookup"><span data-stu-id="989b0-115">displayName</span></span>  | <span data-ttu-id="989b0-116">String</span><span class="sxs-lookup"><span data-stu-id="989b0-116">String</span></span> | <span data-ttu-id="989b0-117">Nombre asociado a la ubicación.</span><span class="sxs-lookup"><span data-stu-id="989b0-117">The name associated with the location.</span></span>                       |
| <span data-ttu-id="989b0-118">locationEmailAddress</span><span class="sxs-lookup"><span data-stu-id="989b0-118">locationEmailAddress</span></span> | <span data-ttu-id="989b0-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="989b0-119">String</span></span> | <span data-ttu-id="989b0-120">Dirección de correo electrónico opcional en la ubicación</span><span class="sxs-lookup"><span data-stu-id="989b0-120">Optional email address of the location.</span></span> |
| <span data-ttu-id="989b0-121">resolveAvailability</span><span class="sxs-lookup"><span data-stu-id="989b0-121">resolveAvailability</span></span> | <span data-ttu-id="989b0-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="989b0-122">Boolean</span></span> | <span data-ttu-id="989b0-p101">Si se establece en verdadero y el recurso especificado está ocupado [findMeetingTimes](../api/user-findmeetingtimes.md) buscará otro recurso que esté libre. Si se establece en falso y el recurso especificado está ocupado, **findMeetingTimes** devolverá el recurso mejor puntuado en la caché del usuario sin comprobar que esté libre o no. El valor predeterminado es "true".</span><span class="sxs-lookup"><span data-stu-id="989b0-p101">If set to true and the specified resource is busy, [findMeetingTimes](../api/user-findmeetingtimes.md) looks for another resource that is free. If set to false and the specified resource is busy, **findMeetingTimes** returns the resource best ranked in the user's cache without checking if it's free. Default is true.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "locationConstraintItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
