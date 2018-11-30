---
title: Tipo de recurso locationConstraintItem
description: Las condiciones establecidas por un cliente para la ubicación de una reunión.
ms.openlocfilehash: f29ff1283d876e726e27473485a183956137f981
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083456"
---
# <a name="locationconstraintitem-resource-type"></a><span data-ttu-id="e454a-103">Tipo de recurso locationConstraintItem</span><span class="sxs-lookup"><span data-stu-id="e454a-103">locationConstraintItem resource type</span></span>

> <span data-ttu-id="e454a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e454a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e454a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e454a-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e454a-106">Las condiciones establecidas por un cliente para la ubicación de una reunión.</span><span class="sxs-lookup"><span data-stu-id="e454a-106">The conditions stated by a client for the location of a meeting.</span></span>

<span data-ttu-id="e454a-107">Derivado de [ubicación](location.md).</span><span class="sxs-lookup"><span data-stu-id="e454a-107">Derived from [location](location.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="e454a-108">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e454a-108">JSON representation</span></span>

<span data-ttu-id="e454a-109">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e454a-109">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  
  ],
  "@odata.type": "microsoft.graph.locationConstraintItem"
}-->

```json
{
  "resolveAvailability": true,
  "address": {"@odata.type": "microsoft.graph.physicalAddress"},
  "coordinates": {"@odata.type": "microsoft.graph.outlookGeoCoordinates"},
  "displayName": "string",
  "locationEmailAddress": "string",
  "locationUri": "string"
}

```
## <a name="properties"></a><span data-ttu-id="e454a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e454a-110">Properties</span></span>
| <span data-ttu-id="e454a-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e454a-111">Property</span></span>     | <span data-ttu-id="e454a-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="e454a-112">Type</span></span>   |<span data-ttu-id="e454a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e454a-113">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e454a-114">address</span><span class="sxs-lookup"><span data-stu-id="e454a-114">address</span></span> | [<span data-ttu-id="e454a-115">physicalAddress</span><span class="sxs-lookup"><span data-stu-id="e454a-115">physicalAddress</span></span>](physicaladdress.md) |<span data-ttu-id="e454a-116">Dirección postal de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="e454a-116">The street address of the location.</span></span> |
| <span data-ttu-id="e454a-117">coordinates</span><span class="sxs-lookup"><span data-stu-id="e454a-117">coordinates</span></span> | [<span data-ttu-id="e454a-118">outlookGeoCoordinates</span><span class="sxs-lookup"><span data-stu-id="e454a-118">outlookGeoCoordinates</span></span>](outlookgeocoordinates.md) | <span data-ttu-id="e454a-119">Coordenadas geográficas y elevación de la ubicación.</span><span class="sxs-lookup"><span data-stu-id="e454a-119">The geographic coordinates and elevation of the location.</span></span> |
| <span data-ttu-id="e454a-120">displayName</span><span class="sxs-lookup"><span data-stu-id="e454a-120">displayName</span></span>  | <span data-ttu-id="e454a-121">String</span><span class="sxs-lookup"><span data-stu-id="e454a-121">String</span></span> | <span data-ttu-id="e454a-122">Nombre asociado a la ubicación.</span><span class="sxs-lookup"><span data-stu-id="e454a-122">The name associated with the location.</span></span>                       |
| <span data-ttu-id="e454a-123">locationEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e454a-123">locationEmailAddress</span></span> | <span data-ttu-id="e454a-124">String</span><span class="sxs-lookup"><span data-stu-id="e454a-124">String</span></span> | <span data-ttu-id="e454a-125">Dirección de correo electrónico opcional de la ubicación</span><span class="sxs-lookup"><span data-stu-id="e454a-125">Optional email address of the location.</span></span> |
| <span data-ttu-id="e454a-126">locationUri</span><span class="sxs-lookup"><span data-stu-id="e454a-126">locationUri</span></span> | <span data-ttu-id="e454a-127">String</span><span class="sxs-lookup"><span data-stu-id="e454a-127">String</span></span> | <span data-ttu-id="e454a-128">URI opcional que representa la ubicación.</span><span class="sxs-lookup"><span data-stu-id="e454a-128">Optional URI representing the location.</span></span> |
| <span data-ttu-id="e454a-129">resolveAvailability</span><span class="sxs-lookup"><span data-stu-id="e454a-129">resolveAvailability</span></span> | <span data-ttu-id="e454a-130">Booleano</span><span class="sxs-lookup"><span data-stu-id="e454a-130">Boolean</span></span> | <span data-ttu-id="e454a-p102">Si se establece en verdadero y el recurso especificado está ocupado [findMeetingTimes](../api/user-findmeetingtimes.md) buscará otro recurso que esté libre. Si se establece en falso y el recurso especificado está ocupado, **findMeetingTimes** devolverá el recurso mejor puntuado en la caché del usuario sin comprobar que esté libre o no. El valor predeterminado es "true".</span><span class="sxs-lookup"><span data-stu-id="e454a-p102">If set to true and the specified resource is busy, [findMeetingTimes](../api/user-findmeetingtimes.md) looks for another resource that is free. If set to false and the specified resource is busy, **findMeetingTimes** returns the resource best ranked in the user's cache without checking if it's free. Default is true.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "locationConstraintItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->