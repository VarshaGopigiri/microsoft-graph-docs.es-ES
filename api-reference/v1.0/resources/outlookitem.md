---
title: Tipo de recurso outlookItem
description: Aquí tiene una representación JSON del recurso
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 3bbfe6119d279a1a708b44128a7d134664d7b040
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27967052"
---
# <a name="outlookitem-resource-type"></a><span data-ttu-id="0ad1d-103">Tipo de recurso outlookItem</span><span class="sxs-lookup"><span data-stu-id="0ad1d-103">outlookItem resource type</span></span>



## <a name="json-representation"></a><span data-ttu-id="0ad1d-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0ad1d-104">JSON representation</span></span>

<span data-ttu-id="0ad1d-105">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0ad1d-105">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="0ad1d-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0ad1d-106">Properties</span></span>
| <span data-ttu-id="0ad1d-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0ad1d-107">Property</span></span>     | <span data-ttu-id="0ad1d-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ad1d-108">Type</span></span>   |<span data-ttu-id="0ad1d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ad1d-109">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0ad1d-110">categories</span><span class="sxs-lookup"><span data-stu-id="0ad1d-110">categories</span></span>|<span data-ttu-id="0ad1d-111">Colección String</span><span class="sxs-lookup"><span data-stu-id="0ad1d-111">String collection</span></span>|<span data-ttu-id="0ad1d-112">Las categorías asociadas con el elemento</span><span class="sxs-lookup"><span data-stu-id="0ad1d-112">The categories associated with the item</span></span>|
|<span data-ttu-id="0ad1d-113">changeKey</span><span class="sxs-lookup"><span data-stu-id="0ad1d-113">changeKey</span></span>|<span data-ttu-id="0ad1d-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="0ad1d-114">String</span></span>|<span data-ttu-id="0ad1d-115">Identifica la versión del elemento.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-115">Identifies the version of the item.</span></span> <span data-ttu-id="0ad1d-116">Cada vez que se cambia el elemento, changeKey cambia también.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-116">Every time the item is changed, changeKey changes as well.</span></span> <span data-ttu-id="0ad1d-117">Esto permite a Exchange aplicar los cambios a la versión correcta del objeto.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-117">This allows Exchange to apply changes to the correct version of the object.</span></span> <span data-ttu-id="0ad1d-118">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-118">Read-only.</span></span>|
|<span data-ttu-id="0ad1d-119">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0ad1d-119">createdDateTime</span></span>|<span data-ttu-id="0ad1d-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0ad1d-120">DateTimeOffset</span></span>|<span data-ttu-id="0ad1d-p102">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="0ad1d-p102">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="0ad1d-123">id</span><span class="sxs-lookup"><span data-stu-id="0ad1d-123">id</span></span>|<span data-ttu-id="0ad1d-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="0ad1d-124">String</span></span>| <span data-ttu-id="0ad1d-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ad1d-125">Read-only.</span></span>|
|<span data-ttu-id="0ad1d-126">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0ad1d-126">lastModifiedDateTime</span></span>|<span data-ttu-id="0ad1d-127">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0ad1d-127">DateTimeOffset</span></span>|<span data-ttu-id="0ad1d-p103">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="0ad1d-p103">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|

## <a name="relationships"></a><span data-ttu-id="0ad1d-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0ad1d-130">Relationships</span></span>
<span data-ttu-id="0ad1d-131">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0ad1d-131">None</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
