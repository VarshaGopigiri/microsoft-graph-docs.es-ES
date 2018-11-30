---
title: Tipo de recurso outlookItem
description: Aquí tiene una representación JSON del recurso
ms.openlocfilehash: 6de0b5f9f79f8c3f813cbd876fa22f6b43f71a53
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089750"
---
# <a name="outlookitem-resource-type"></a><span data-ttu-id="b8f87-103">Tipo de recurso outlookItem</span><span class="sxs-lookup"><span data-stu-id="b8f87-103">outlookItem resource type</span></span>

> <span data-ttu-id="b8f87-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b8f87-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b8f87-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b8f87-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b8f87-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b8f87-106">JSON representation</span></span>

<span data-ttu-id="b8f87-107">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b8f87-107">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="b8f87-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b8f87-108">Properties</span></span>
| <span data-ttu-id="b8f87-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b8f87-109">Property</span></span>     | <span data-ttu-id="b8f87-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8f87-110">Type</span></span>   |<span data-ttu-id="b8f87-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8f87-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b8f87-112">categories</span><span class="sxs-lookup"><span data-stu-id="b8f87-112">categories</span></span>|<span data-ttu-id="b8f87-113">String collection</span><span class="sxs-lookup"><span data-stu-id="b8f87-113">String collection</span></span>||
|<span data-ttu-id="b8f87-114">changeKey</span><span class="sxs-lookup"><span data-stu-id="b8f87-114">changeKey</span></span>|<span data-ttu-id="b8f87-115">String</span><span class="sxs-lookup"><span data-stu-id="b8f87-115">String</span></span>||
|<span data-ttu-id="b8f87-116">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="b8f87-116">createdDateTime</span></span>|<span data-ttu-id="b8f87-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b8f87-117">DateTimeOffset</span></span>|<span data-ttu-id="b8f87-p102">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="b8f87-p102">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="b8f87-120">id</span><span class="sxs-lookup"><span data-stu-id="b8f87-120">id</span></span>|<span data-ttu-id="b8f87-121">String</span><span class="sxs-lookup"><span data-stu-id="b8f87-121">String</span></span>| <span data-ttu-id="b8f87-122">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b8f87-122">Read-only.</span></span>|
|<span data-ttu-id="b8f87-123">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="b8f87-123">lastModifiedDateTime</span></span>|<span data-ttu-id="b8f87-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b8f87-124">DateTimeOffset</span></span>|<span data-ttu-id="b8f87-p103">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="b8f87-p103">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|

## <a name="relationships"></a><span data-ttu-id="b8f87-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b8f87-127">Relationships</span></span>
<span data-ttu-id="b8f87-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b8f87-128">None</span></span>


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->