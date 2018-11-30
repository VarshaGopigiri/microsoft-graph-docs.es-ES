---
title: Tipo de recurso timeZoneInformation
description: Representa una zona horaria. El formato compatible es Windows, y la autoridad de números asignados de Internet (IANA) hora zona (también conocida como zona horaria de Olson)
ms.openlocfilehash: de80ed293af834d299be5f9543c5c3bedde7a540
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028690"
---
# <a name="timezoneinformation-resource-type"></a><span data-ttu-id="3587d-104">Tipo de recurso timeZoneInformation</span><span class="sxs-lookup"><span data-stu-id="3587d-104">timeZoneInformation resource type</span></span>


<span data-ttu-id="3587d-105">Representa una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="3587d-105">Represents a time zone.</span></span> <span data-ttu-id="3587d-106">El formato admitido es Windows y, cuando se corrija el problema conocido actual, también se admitirá el formato de [zona horaria Internet Assigned Numbers Authority (IANA)](https://www.iana.org/time-zones) (también conocida como "zona horaria Olson").</span><span class="sxs-lookup"><span data-stu-id="3587d-106">The supported format is Windows, and [Internet Assigned Numbers Authority (IANA) time zone](https://www.iana.org/time-zones) (also known as Olson time zone) format as well when the current known problem is fixed.</span></span>

## <a name="properties"></a><span data-ttu-id="3587d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3587d-107">Properties</span></span>
| <span data-ttu-id="3587d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3587d-108">Property</span></span>     | <span data-ttu-id="3587d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3587d-109">Type</span></span>   |<span data-ttu-id="3587d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3587d-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3587d-111">alias</span><span class="sxs-lookup"><span data-stu-id="3587d-111">alias</span></span>|<span data-ttu-id="3587d-112">string</span><span class="sxs-lookup"><span data-stu-id="3587d-112">string</span></span>|<span data-ttu-id="3587d-113">Identificador de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="3587d-113">An identifier for the time zone.</span></span>|
|<span data-ttu-id="3587d-114">displayName</span><span class="sxs-lookup"><span data-stu-id="3587d-114">displayName</span></span>|<span data-ttu-id="3587d-115">string</span><span class="sxs-lookup"><span data-stu-id="3587d-115">string</span></span>|<span data-ttu-id="3587d-116">Cadena de visualización que representa la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="3587d-116">A display string that represents the time zone.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3587d-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3587d-117">JSON representation</span></span>

<span data-ttu-id="3587d-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3587d-118">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeZoneInformation"
}-->

```json
{
  "alias": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeZoneInformation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->