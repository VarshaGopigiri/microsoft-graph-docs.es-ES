---
title: tipo de recurso de marca de tiempo
description: Información de fecha y hora de un punto en el tiempo.
localization_priority: Normal
ms.openlocfilehash: b3e6e7384c9efdcb0e606f91d7357272f27ceaa1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830229"
---
# <a name="timestamp-resource-type"></a><span data-ttu-id="91cd0-103">tipo de recurso de marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="91cd0-103">timeStamp resource type</span></span>

> <span data-ttu-id="91cd0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="91cd0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="91cd0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="91cd0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="91cd0-106">Información de fecha y hora de un punto en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="91cd0-106">Date and time information for a point in time.</span></span>

## <a name="json-representation"></a><span data-ttu-id="91cd0-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="91cd0-107">JSON representation</span></span>

<span data-ttu-id="91cd0-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="91cd0-108">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="91cd0-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="91cd0-109">Properties</span></span>
| <span data-ttu-id="91cd0-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="91cd0-110">Property</span></span>     | <span data-ttu-id="91cd0-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="91cd0-111">Type</span></span>   |<span data-ttu-id="91cd0-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="91cd0-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="91cd0-113">date</span><span class="sxs-lookup"><span data-stu-id="91cd0-113">date</span></span>|<span data-ttu-id="91cd0-114">Fecha</span><span class="sxs-lookup"><span data-stu-id="91cd0-114">Date</span></span>|<span data-ttu-id="91cd0-115">La parte de fecha de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="91cd0-115">The date portion of the timestamp.</span></span>|
|<span data-ttu-id="91cd0-116">time</span><span class="sxs-lookup"><span data-stu-id="91cd0-116">time</span></span>|<span data-ttu-id="91cd0-117">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="91cd0-117">TimeOfDay</span></span>|<span data-ttu-id="91cd0-118">La parte de tiempo de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="91cd0-118">The time portion of the timestamp.</span></span>|
|<span data-ttu-id="91cd0-119">timeZone</span><span class="sxs-lookup"><span data-stu-id="91cd0-119">timeZone</span></span>|<span data-ttu-id="91cd0-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="91cd0-120">String</span></span>|<span data-ttu-id="91cd0-121">La parte de la zona horaria de la marca de tiempo, que es una de las áreas longitudinales 24 en el mundo.</span><span class="sxs-lookup"><span data-stu-id="91cd0-121">The timezone portion of the timestamp, which is one of the 24 longitudinal areas in the world.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeStamp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
