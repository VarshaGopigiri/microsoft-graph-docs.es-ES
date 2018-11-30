---
title: tipo de recurso de marca de tiempo
description: Información de fecha y hora de un punto en el tiempo.
ms.openlocfilehash: 4f392e880bb165841fd8a9a31b6ed00bf2ba36fb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029326"
---
# <a name="timestamp-resource-type"></a><span data-ttu-id="738d8-103">tipo de recurso de marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="738d8-103">timeStamp resource type</span></span>

<span data-ttu-id="738d8-104">Información de fecha y hora de un punto en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="738d8-104">Date and time information for a point in time.</span></span>

## <a name="json-representation"></a><span data-ttu-id="738d8-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="738d8-105">JSON representation</span></span>

<span data-ttu-id="738d8-106">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="738d8-106">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeStamp"
}-->

```json
{
  "date": "String (timestamp)",
  "time": "String (timestamp)",
  "timeZone": "string"
}

```
## <a name="properties"></a><span data-ttu-id="738d8-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="738d8-107">Properties</span></span>
| <span data-ttu-id="738d8-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="738d8-108">Property</span></span>       | <span data-ttu-id="738d8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="738d8-109">Type</span></span>    |<span data-ttu-id="738d8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="738d8-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="738d8-111">date</span><span class="sxs-lookup"><span data-stu-id="738d8-111">date</span></span>|<span data-ttu-id="738d8-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="738d8-112">Date</span></span>|<span data-ttu-id="738d8-113">La parte de fecha de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="738d8-113">The date portion of the timestamp.</span></span>|
|<span data-ttu-id="738d8-114">time</span><span class="sxs-lookup"><span data-stu-id="738d8-114">time</span></span>|<span data-ttu-id="738d8-115">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="738d8-115">TimeOfDay</span></span>|<span data-ttu-id="738d8-116">La parte de tiempo de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="738d8-116">The time portion of the timestamp.</span></span>|
|<span data-ttu-id="738d8-117">timeZone</span><span class="sxs-lookup"><span data-stu-id="738d8-117">timeZone</span></span>|<span data-ttu-id="738d8-118">String</span><span class="sxs-lookup"><span data-stu-id="738d8-118">String</span></span>|<span data-ttu-id="738d8-119">La parte de la zona horaria de la marca de tiempo, que es una de las áreas longitudinales 24 en el mundo.</span><span class="sxs-lookup"><span data-stu-id="738d8-119">The timezone portion of the timestamp, which is one of the 24 longitudinal areas in the world.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeStamp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->