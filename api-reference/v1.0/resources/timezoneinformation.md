---
title: Tipo de recurso timeZoneInformation
description: Representa una zona horaria. El formato compatible es Windows, y la autoridad de números asignados de Internet (IANA) hora zona (también conocida como zona horaria de Olson)
localization_priority: Normal
ms.openlocfilehash: ced18a28a5c086416fa7247e1531d772fd63b977
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830201"
---
# <a name="timezoneinformation-resource-type"></a><span data-ttu-id="858b8-104">Tipo de recurso timeZoneInformation</span><span class="sxs-lookup"><span data-stu-id="858b8-104">timeZoneInformation resource type</span></span>


<span data-ttu-id="858b8-105">Representa una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="858b8-105">Represents a time zone.</span></span> <span data-ttu-id="858b8-106">El formato admitido es Windows y, cuando se corrija el problema conocido actual, también se admitirá el formato de [zona horaria Internet Assigned Numbers Authority (IANA)](https://www.iana.org/time-zones) (también conocida como "zona horaria Olson").</span><span class="sxs-lookup"><span data-stu-id="858b8-106">The supported format is Windows, and [Internet Assigned Numbers Authority (IANA) time zone](https://www.iana.org/time-zones) (also known as Olson time zone) format as well when the current known problem is fixed.</span></span>

## <a name="properties"></a><span data-ttu-id="858b8-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="858b8-107">Properties</span></span>
| <span data-ttu-id="858b8-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="858b8-108">Property</span></span>     | <span data-ttu-id="858b8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="858b8-109">Type</span></span>   |<span data-ttu-id="858b8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="858b8-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="858b8-111">alias</span><span class="sxs-lookup"><span data-stu-id="858b8-111">alias</span></span>|<span data-ttu-id="858b8-112">string</span><span class="sxs-lookup"><span data-stu-id="858b8-112">string</span></span>|<span data-ttu-id="858b8-113">Identificador de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="858b8-113">An identifier for the time zone.</span></span>|
|<span data-ttu-id="858b8-114">displayName</span><span class="sxs-lookup"><span data-stu-id="858b8-114">displayName</span></span>|<span data-ttu-id="858b8-115">string</span><span class="sxs-lookup"><span data-stu-id="858b8-115">string</span></span>|<span data-ttu-id="858b8-116">Cadena de visualización que representa la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="858b8-116">A display string that represents the time zone.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="858b8-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="858b8-117">JSON representation</span></span>

<span data-ttu-id="858b8-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="858b8-118">Here is a JSON representation of the resource.</span></span>

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
