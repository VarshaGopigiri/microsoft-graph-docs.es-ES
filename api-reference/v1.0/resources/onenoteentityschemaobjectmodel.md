---
title: recursos de onenoteEntitySchemaObjectModel
description: Éste es un tipo base para las entidades de OneNote.
author: Jewan-microsoft
ms.openlocfilehash: a44d05a512b8e4ed2615296faae3f35bd7bd554f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27319449"
---
# <a name="onenoteentityschemaobjectmodel-resource"></a><span data-ttu-id="e51cf-103">recursos de onenoteEntitySchemaObjectModel</span><span class="sxs-lookup"><span data-stu-id="e51cf-103">onenoteEntitySchemaObjectModel resource</span></span>

<span data-ttu-id="e51cf-104">Éste es un tipo base para las entidades de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e51cf-104">This is a base type for OneNote entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e51cf-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e51cf-105">JSON representation</span></span>

<span data-ttu-id="e51cf-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e51cf-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.onenoteEntityBaseModel",
  "optionalProperties": [
    "self"
  ],
  "@odata.type": "microsoft.graph.onenoteEntitySchemaObjectModel"
}-->

```json
{
  "createdDateTime": "String (timestamp)"
}

```
## <a name="properties"></a><span data-ttu-id="e51cf-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e51cf-107">Properties</span></span>
| <span data-ttu-id="e51cf-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e51cf-108">Property</span></span>     | <span data-ttu-id="e51cf-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e51cf-109">Type</span></span>   |<span data-ttu-id="e51cf-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e51cf-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e51cf-111">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e51cf-111">createdDateTime</span></span>|<span data-ttu-id="e51cf-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e51cf-112">DateTimeOffset</span></span>|<span data-ttu-id="e51cf-p101">La fecha y la hora en que se creó la página. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e51cf-p101">The date and time when the page was created. The timestamp represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`. Read-only.</span></span>|

<!-- uuid: bfb567de-2a2a-4b81-bf47-a55626a0c166
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->