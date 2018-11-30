---
title: Tipo de recurso timeZoneInformation
description: Representa una zona horaria. El formato compatible es Windows, y la autoridad de números asignados de Internet (IANA) hora zona (también conocida como zona horaria de Olson)
ms.openlocfilehash: 5508f20812b8327a068364df7eb33c5072c3512e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086673"
---
# <a name="timezoneinformation-resource-type"></a><span data-ttu-id="70691-104">Tipo de recurso timeZoneInformation</span><span class="sxs-lookup"><span data-stu-id="70691-104">timeZoneInformation resource type</span></span>

> <span data-ttu-id="70691-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="70691-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="70691-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="70691-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="70691-107">Representa una zona horaria.</span><span class="sxs-lookup"><span data-stu-id="70691-107">Represents a time zone.</span></span> <span data-ttu-id="70691-108">El formato admitido es Windows y, cuando se corrija el problema conocido actual, también se admitirá el formato de [zona horaria Internet Assigned Numbers Authority (IANA)](https://www.iana.org/time-zones) (también conocida como "zona horaria Olson").</span><span class="sxs-lookup"><span data-stu-id="70691-108">The supported format is Windows, and [Internet Assigned Numbers Authority (IANA) time zone](https://www.iana.org/time-zones) (also known as Olson time zone) format as well when the current known problem is fixed.</span></span>

## <a name="properties"></a><span data-ttu-id="70691-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="70691-109">Properties</span></span>
| <span data-ttu-id="70691-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="70691-110">Property</span></span>     | <span data-ttu-id="70691-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="70691-111">Type</span></span>   |<span data-ttu-id="70691-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="70691-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="70691-113">alias</span><span class="sxs-lookup"><span data-stu-id="70691-113">alias</span></span>|<span data-ttu-id="70691-114">string</span><span class="sxs-lookup"><span data-stu-id="70691-114">string</span></span>|<span data-ttu-id="70691-115">Identificador de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="70691-115">An identifier for the time zone.</span></span>|
|<span data-ttu-id="70691-116">displayName</span><span class="sxs-lookup"><span data-stu-id="70691-116">displayName</span></span>|<span data-ttu-id="70691-117">string</span><span class="sxs-lookup"><span data-stu-id="70691-117">string</span></span>|<span data-ttu-id="70691-118">Cadena de visualización que representa la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="70691-118">A display string that represents the time zone.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="70691-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="70691-119">JSON representation</span></span>

<span data-ttu-id="70691-120">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="70691-120">Here is a JSON representation of the resource.</span></span>

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