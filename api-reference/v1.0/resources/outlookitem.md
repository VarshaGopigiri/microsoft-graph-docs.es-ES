---
title: Tipo de recurso outlookItem
description: Aquí tiene una representación JSON del recurso
author: angelgolfer-ms
ms.openlocfilehash: 750239156e6f4e2874783ae160a7018fb58e259d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332518"
---
# <a name="outlookitem-resource-type"></a><span data-ttu-id="0d9eb-103">Tipo de recurso outlookItem</span><span class="sxs-lookup"><span data-stu-id="0d9eb-103">outlookItem resource type</span></span>



## <a name="json-representation"></a><span data-ttu-id="0d9eb-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0d9eb-104">JSON representation</span></span>

<span data-ttu-id="0d9eb-105">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0d9eb-105">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "abstract": true,
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.outlookItem"
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
## <a name="properties"></a><span data-ttu-id="0d9eb-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0d9eb-106">Properties</span></span>
| <span data-ttu-id="0d9eb-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0d9eb-107">Property</span></span>     | <span data-ttu-id="0d9eb-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d9eb-108">Type</span></span>   |<span data-ttu-id="0d9eb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0d9eb-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0d9eb-110">categories</span><span class="sxs-lookup"><span data-stu-id="0d9eb-110">categories</span></span>|<span data-ttu-id="0d9eb-111">Colección String</span><span class="sxs-lookup"><span data-stu-id="0d9eb-111">String collection</span></span>|<span data-ttu-id="0d9eb-112">Las categorías asociadas con el elemento</span><span class="sxs-lookup"><span data-stu-id="0d9eb-112">The categories associated with the item</span></span>|
|<span data-ttu-id="0d9eb-113">changeKey</span><span class="sxs-lookup"><span data-stu-id="0d9eb-113">changeKey</span></span>|<span data-ttu-id="0d9eb-114">String</span><span class="sxs-lookup"><span data-stu-id="0d9eb-114">String</span></span>|<span data-ttu-id="0d9eb-115">Identifica la versión del elemento.</span><span class="sxs-lookup"><span data-stu-id="0d9eb-115">Identifies the version of the item.</span></span> <span data-ttu-id="0d9eb-116">Cada vez que se cambia el elemento, changeKey cambia también.</span><span class="sxs-lookup"><span data-stu-id="0d9eb-116">Every time the item is changed, changeKey changes as well.</span></span> <span data-ttu-id="0d9eb-117">Esto permite a Exchange aplicar los cambios a la versión correcta del objeto.</span><span class="sxs-lookup"><span data-stu-id="0d9eb-117">This allows Exchange to apply changes to the correct version of the object.</span></span> <span data-ttu-id="0d9eb-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0d9eb-118">Read-only.</span></span>|
|<span data-ttu-id="0d9eb-119">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0d9eb-119">createdDateTime</span></span>|<span data-ttu-id="0d9eb-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0d9eb-120">DateTimeOffset</span></span>|<span data-ttu-id="0d9eb-p102">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="0d9eb-p102">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="0d9eb-123">id</span><span class="sxs-lookup"><span data-stu-id="0d9eb-123">id</span></span>|<span data-ttu-id="0d9eb-124">String</span><span class="sxs-lookup"><span data-stu-id="0d9eb-124">String</span></span>| <span data-ttu-id="0d9eb-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0d9eb-125">Read-only.</span></span>|
|<span data-ttu-id="0d9eb-126">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0d9eb-126">lastModifiedDateTime</span></span>|<span data-ttu-id="0d9eb-127">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0d9eb-127">DateTimeOffset</span></span>|<span data-ttu-id="0d9eb-p103">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="0d9eb-p103">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|

## <a name="relationships"></a><span data-ttu-id="0d9eb-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0d9eb-130">Relationships</span></span>
<span data-ttu-id="0d9eb-131">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0d9eb-131">None</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
