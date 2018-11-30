---
title: tipo de recurso signInLocation
description: Proporciona la ciudad, estado y país o región desde donde ha ocurrido en el inicio de sesión.
ms.openlocfilehash: a3d4f6ca5ec18e70960f45a3da1bb06d51ee1e65
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087242"
---
# <a name="signinlocation-resource-type"></a><span data-ttu-id="b310e-103">tipo de recurso signInLocation</span><span class="sxs-lookup"><span data-stu-id="b310e-103">signInLocation resource type</span></span>
<span data-ttu-id="b310e-104">Proporciona la ciudad, estado y país o región desde donde ha ocurrido en el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b310e-104">Provides the city, state and country/region from where the sign-in happened.</span></span>



## <a name="properties"></a><span data-ttu-id="b310e-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b310e-105">Properties</span></span>
| <span data-ttu-id="b310e-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b310e-106">Property</span></span>     | <span data-ttu-id="b310e-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b310e-107">Type</span></span>   |<span data-ttu-id="b310e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b310e-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b310e-109">city</span><span class="sxs-lookup"><span data-stu-id="b310e-109">city</span></span>|<span data-ttu-id="b310e-110">String</span><span class="sxs-lookup"><span data-stu-id="b310e-110">String</span></span>|<span data-ttu-id="b310e-111">Proporciona la ciudad donde se originó en el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b310e-111">Provides the city where the sign-in originated.</span></span> <span data-ttu-id="b310e-112">Esto se calcula utilizando la información de latitud y longitud de la actividad de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b310e-112">This is calculated using latitude/longitude information from the sign-in activity.</span></span>|
|<span data-ttu-id="b310e-113">countryOrRegion</span><span class="sxs-lookup"><span data-stu-id="b310e-113">countryOrRegion</span></span>|<span data-ttu-id="b310e-114">String</span><span class="sxs-lookup"><span data-stu-id="b310e-114">String</span></span>|<span data-ttu-id="b310e-115">Proporciona la información de código de país (código de 2 letras) donde se originó en el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b310e-115">Provides the country code info (2 letter code) where the sign-in originated.</span></span>  <span data-ttu-id="b310e-116">Esto se calcula utilizando la información de latitud y longitud de la actividad de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b310e-116">This is calculated using latitude/longitude information from the sign-in activity.</span></span>|
|<span data-ttu-id="b310e-117">coordenadas geográficas</span><span class="sxs-lookup"><span data-stu-id="b310e-117">geoCoordinates</span></span>|[<span data-ttu-id="b310e-118">geoCoordinates</span><span class="sxs-lookup"><span data-stu-id="b310e-118">geoCoordinates</span></span>](geocoordinates.md)|<span data-ttu-id="b310e-119">Proporciona la latitud, longitud y altitud donde se originó en el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b310e-119">Provides the latitude, longitude and altitude where the sign-in originated.</span></span>|
|<span data-ttu-id="b310e-120">estado</span><span class="sxs-lookup"><span data-stu-id="b310e-120">state</span></span>|<span data-ttu-id="b310e-121">String</span><span class="sxs-lookup"><span data-stu-id="b310e-121">String</span></span>|<span data-ttu-id="b310e-122">Proporciona el estado donde se originó en el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b310e-122">Provides the State where the sign-in originated.</span></span> <span data-ttu-id="b310e-123">Esto se calcula utilizando la información de latitud y longitud de la actividad de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b310e-123">This is calculated using latitude/longitude information from the sign-in activity.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b310e-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b310e-124">JSON representation</span></span>

<span data-ttu-id="b310e-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b310e-125">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.signInLocation"
}-->

```json
{
  "city": "String",
  "countryOrRegion": "String",
  "geoCoordinates": {"@odata.type": "microsoft.graph.geoCoordinates"},
  "state": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "signInLocation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->