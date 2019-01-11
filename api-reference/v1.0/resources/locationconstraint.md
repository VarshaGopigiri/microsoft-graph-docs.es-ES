---
title: Tipo de recurso locationConstraint
description: Las condiciones establecidas por un cliente para la ubicación de una reunión.
localization_priority: Normal
ms.openlocfilehash: 2f6d4951eb8654f2100b17ef35d150023dafbc93
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887923"
---
# <a name="locationconstraint-resource-type"></a><span data-ttu-id="8b2fc-103">Tipo de recurso locationConstraint</span><span class="sxs-lookup"><span data-stu-id="8b2fc-103">locationConstraint resource type</span></span>

<span data-ttu-id="8b2fc-104">Las condiciones establecidas por un cliente para la ubicación de una reunión.</span><span class="sxs-lookup"><span data-stu-id="8b2fc-104">The conditions stated by a client for the location of a meeting.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8b2fc-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8b2fc-105">JSON representation</span></span>

<span data-ttu-id="8b2fc-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8b2fc-106">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.locationConstraint"
}-->

```json
{
  "isRequired": true,
  "locations": [{"@odata.type": "microsoft.graph.locationConstraintItem"}],
  "suggestLocation": true
}

```
## <a name="properties"></a><span data-ttu-id="8b2fc-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8b2fc-107">Properties</span></span>
| <span data-ttu-id="8b2fc-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8b2fc-108">Property</span></span>     | <span data-ttu-id="8b2fc-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8b2fc-109">Type</span></span>   |<span data-ttu-id="8b2fc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8b2fc-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8b2fc-111">isRequired</span><span class="sxs-lookup"><span data-stu-id="8b2fc-111">isRequired</span></span>|<span data-ttu-id="8b2fc-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="8b2fc-112">Boolean</span></span>|<span data-ttu-id="8b2fc-p101">El cliente solicita que el servicio incluya en la respuesta una ubicación para la reunión. Si esto es verdadero y todos los recursos están ocupados, [findMeetingTimes](../api/user-findmeetingtimes.md) no devolverá ninguna sugerencia de fecha de reunión. Si esto es falso y todos los recursos están ocupados, **findMeetingTimes** buscará igual fechas de reunión sin ubicación.</span><span class="sxs-lookup"><span data-stu-id="8b2fc-p101">The client requests the service to include in the response a meeting location for the meeting. If this is true and all the resources are busy, [findMeetingTimes](../api/user-findmeetingtimes.md) will not return any meeting time suggestions. If this is false and all the resources are busy, **findMeetingTimes** would still look for meeting times without locations.</span></span> |
|<span data-ttu-id="8b2fc-116">locations</span><span class="sxs-lookup"><span data-stu-id="8b2fc-116">locations</span></span>|<span data-ttu-id="8b2fc-117">Colección [locationConstraintItem](locationconstraintitem.md)</span><span class="sxs-lookup"><span data-stu-id="8b2fc-117">[locationConstraintItem](locationconstraintitem.md) collection</span></span>|<span data-ttu-id="8b2fc-118">Información de restricciones para una o más ubicaciones que el cliente solicita para la reunión.</span><span class="sxs-lookup"><span data-stu-id="8b2fc-118">Constraint information for one or more locations that the client requests for the meeting.</span></span>|
|<span data-ttu-id="8b2fc-119">suggestLocation</span><span class="sxs-lookup"><span data-stu-id="8b2fc-119">suggestLocation</span></span>|<span data-ttu-id="8b2fc-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="8b2fc-120">Boolean</span></span>|<span data-ttu-id="8b2fc-121">El cliente solicita al servicio que sugiera una o más ubicaciones de reunión.</span><span class="sxs-lookup"><span data-stu-id="8b2fc-121">The client requests the service to suggest one or more meeting locations.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "locationConstraint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
