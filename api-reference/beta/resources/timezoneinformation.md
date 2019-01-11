---
title: Tipo de recurso timeZoneInformation
description: Representa una zona horaria. El formato compatible es Windows, y la autoridad de números asignados de Internet (IANA) hora zona (también conocida como zona horaria de Olson)
localization_priority: Normal
ms.openlocfilehash: dc53cca34ef9c6a53a39394cbba8be4e1baca662
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27839742"
---
# <a name="timezoneinformation-resource-type"></a><span data-ttu-id="ad101-104">Tipo de recurso timeZoneInformation</span><span class="sxs-lookup"><span data-stu-id="ad101-104">timeZoneInformation resource type</span></span>

> <span data-ttu-id="ad101-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ad101-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ad101-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ad101-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ad101-107">Representa una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="ad101-107">Represents a time zone.</span></span> <span data-ttu-id="ad101-108">El formato admitido es Windows y, cuando se corrija el problema conocido actual, también se admitirá el formato de [zona horaria Internet Assigned Numbers Authority (IANA)](https://www.iana.org/time-zones) (también conocida como "zona horaria Olson").</span><span class="sxs-lookup"><span data-stu-id="ad101-108">The supported format is Windows, and [Internet Assigned Numbers Authority (IANA) time zone](https://www.iana.org/time-zones) (also known as Olson time zone) format as well when the current known problem is fixed.</span></span>

## <a name="properties"></a><span data-ttu-id="ad101-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ad101-109">Properties</span></span>
| <span data-ttu-id="ad101-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ad101-110">Property</span></span>     | <span data-ttu-id="ad101-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad101-111">Type</span></span>   |<span data-ttu-id="ad101-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad101-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ad101-113">alias</span><span class="sxs-lookup"><span data-stu-id="ad101-113">alias</span></span>|<span data-ttu-id="ad101-114">string</span><span class="sxs-lookup"><span data-stu-id="ad101-114">string</span></span>|<span data-ttu-id="ad101-115">Identificador de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="ad101-115">An identifier for the time zone.</span></span>|
|<span data-ttu-id="ad101-116">displayName</span><span class="sxs-lookup"><span data-stu-id="ad101-116">displayName</span></span>|<span data-ttu-id="ad101-117">string</span><span class="sxs-lookup"><span data-stu-id="ad101-117">string</span></span>|<span data-ttu-id="ad101-118">Cadena de visualización que representa la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="ad101-118">A display string that represents the time zone.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ad101-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ad101-119">JSON representation</span></span>

<span data-ttu-id="ad101-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ad101-120">Here is a JSON representation of the resource.</span></span>

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
