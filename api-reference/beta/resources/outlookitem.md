---
title: Tipo de recurso outlookItem
description: Aquí tiene una representación JSON del recurso
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 7095be63657dacab2927abc3adb77854374c3674
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27941943"
---
# <a name="outlookitem-resource-type"></a><span data-ttu-id="3baad-103">Tipo de recurso outlookItem</span><span class="sxs-lookup"><span data-stu-id="3baad-103">outlookItem resource type</span></span>

> <span data-ttu-id="3baad-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3baad-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3baad-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3baad-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3baad-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3baad-106">JSON representation</span></span>

<span data-ttu-id="3baad-107">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3baad-107">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.outlookitem"
}-->

```json
{
  "categories": ["string"],
  "changeKey": "string",
  "createdDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "lastModifiedDateTime": "String (timestamp)"
}

```
## <a name="properties"></a><span data-ttu-id="3baad-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3baad-108">Properties</span></span>
| <span data-ttu-id="3baad-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3baad-109">Property</span></span>     | <span data-ttu-id="3baad-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="3baad-110">Type</span></span>   |<span data-ttu-id="3baad-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="3baad-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3baad-112">categories</span><span class="sxs-lookup"><span data-stu-id="3baad-112">categories</span></span>|<span data-ttu-id="3baad-113">String collection</span><span class="sxs-lookup"><span data-stu-id="3baad-113">String collection</span></span>||
|<span data-ttu-id="3baad-114">changeKey</span><span class="sxs-lookup"><span data-stu-id="3baad-114">changeKey</span></span>|<span data-ttu-id="3baad-115">String</span><span class="sxs-lookup"><span data-stu-id="3baad-115">String</span></span>||
|<span data-ttu-id="3baad-116">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="3baad-116">createdDateTime</span></span>|<span data-ttu-id="3baad-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3baad-117">DateTimeOffset</span></span>|<span data-ttu-id="3baad-p102">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="3baad-p102">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="3baad-120">id</span><span class="sxs-lookup"><span data-stu-id="3baad-120">id</span></span>|<span data-ttu-id="3baad-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="3baad-121">String</span></span>| <span data-ttu-id="3baad-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3baad-122">Read-only.</span></span>|
|<span data-ttu-id="3baad-123">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="3baad-123">lastModifiedDateTime</span></span>|<span data-ttu-id="3baad-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3baad-124">DateTimeOffset</span></span>|<span data-ttu-id="3baad-p103">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="3baad-p103">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|

## <a name="relationships"></a><span data-ttu-id="3baad-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3baad-127">Relationships</span></span>
<span data-ttu-id="3baad-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="3baad-128">None</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
