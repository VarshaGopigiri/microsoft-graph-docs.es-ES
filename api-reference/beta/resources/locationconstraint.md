---
title: Tipo de recurso locationConstraint
description: Las condiciones establecidas por un cliente para la ubicación de una reunión.
localization_priority: Normal
ms.openlocfilehash: b1ff078efd5608fa388587003cf904c2b995f12e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851530"
---
# <a name="locationconstraint-resource-type"></a><span data-ttu-id="c9136-103">Tipo de recurso locationConstraint</span><span class="sxs-lookup"><span data-stu-id="c9136-103">locationConstraint resource type</span></span>

> <span data-ttu-id="c9136-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c9136-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c9136-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c9136-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c9136-106">Las condiciones establecidas por un cliente para la ubicación de una reunión.</span><span class="sxs-lookup"><span data-stu-id="c9136-106">The conditions stated by a client for the location of a meeting.</span></span>

## <a name="json-representation"></a><span data-ttu-id="c9136-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c9136-107">JSON representation</span></span>

<span data-ttu-id="c9136-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="c9136-108">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.locationconstraint"
}-->

```json
{
  "isRequired": true,
  "locations": [{"@odata.type": "microsoft.graph.locationConstraintItem"}],
  "suggestLocation": true
}

```
## <a name="properties"></a><span data-ttu-id="c9136-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c9136-109">Properties</span></span>
| <span data-ttu-id="c9136-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c9136-110">Property</span></span>     | <span data-ttu-id="c9136-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="c9136-111">Type</span></span>   |<span data-ttu-id="c9136-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c9136-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c9136-113">isRequired</span><span class="sxs-lookup"><span data-stu-id="c9136-113">isRequired</span></span>|<span data-ttu-id="c9136-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="c9136-114">Boolean</span></span>|<span data-ttu-id="c9136-p102">El cliente solicita que el servicio incluya en la respuesta una ubicación para la reunión. Si esto es verdadero y todos los recursos están ocupados, [findMeetingTimes](../api/user-findmeetingtimes.md) no devolverá ninguna sugerencia de fecha de reunión. Si esto es falso y todos los recursos están ocupados, **findMeetingTimes** buscará igual fechas de reunión sin ubicación.</span><span class="sxs-lookup"><span data-stu-id="c9136-p102">The client requests the service to include in the response a meeting location for the meeting. If this is true and all the resources are busy, [findMeetingTimes](../api/user-findmeetingtimes.md) will not return any meeting time suggestions. If this is false and all the resources are busy, **findMeetingTimes** would still look for meeting times without locations.</span></span> |
|<span data-ttu-id="c9136-118">locations</span><span class="sxs-lookup"><span data-stu-id="c9136-118">locations</span></span>|<span data-ttu-id="c9136-119">Colección [locationConstraintItem](locationconstraintitem.md)</span><span class="sxs-lookup"><span data-stu-id="c9136-119">[locationConstraintItem](locationconstraintitem.md) collection</span></span>|<span data-ttu-id="c9136-120">Información de restricciones para una o más ubicaciones que el cliente solicita para la reunión.</span><span class="sxs-lookup"><span data-stu-id="c9136-120">Constraint information for one or more locations that the client requests for the meeting.</span></span>|
|<span data-ttu-id="c9136-121">suggestLocation</span><span class="sxs-lookup"><span data-stu-id="c9136-121">suggestLocation</span></span>|<span data-ttu-id="c9136-122">Booleano</span><span class="sxs-lookup"><span data-stu-id="c9136-122">Boolean</span></span>|<span data-ttu-id="c9136-123">El cliente solicita al servicio que sugiera una o más ubicaciones de reunión.</span><span class="sxs-lookup"><span data-stu-id="c9136-123">The client requests the service to suggest one or more meeting locations.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "locationConstraint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
