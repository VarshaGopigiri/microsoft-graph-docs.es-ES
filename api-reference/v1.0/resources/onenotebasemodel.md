---
title: recursos de onenoteEntityBaseModel
description: Éste es el tipo base para las entidades de OneNote.
author: Jewan-microsoft
ms.openlocfilehash: 25e2da6732fd831c6bbec5ae86bddeae7b702aa5
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27310468"
---
# <a name="onenoteentitybasemodel-resource"></a><span data-ttu-id="cd88e-103">recursos de onenoteEntityBaseModel</span><span class="sxs-lookup"><span data-stu-id="cd88e-103">onenoteEntityBaseModel resource</span></span>

<span data-ttu-id="cd88e-104">Éste es el tipo base para las entidades de OneNote.</span><span class="sxs-lookup"><span data-stu-id="cd88e-104">This is the base type for OneNote entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="cd88e-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cd88e-105">JSON representation</span></span>

<span data-ttu-id="cd88e-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cd88e-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [
    "self"
  ],
  "@odata.type": "microsoft.graph.onenoteEntityBaseModel"
}-->

```json
{
  "self": "string"
}

```
## <a name="properties"></a><span data-ttu-id="cd88e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd88e-107">Properties</span></span>
| <span data-ttu-id="cd88e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd88e-108">Property</span></span>     | <span data-ttu-id="cd88e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd88e-109">Type</span></span>   |<span data-ttu-id="cd88e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd88e-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="cd88e-111">self</span><span class="sxs-lookup"><span data-stu-id="cd88e-111">self</span></span>|<span data-ttu-id="cd88e-112">String</span><span class="sxs-lookup"><span data-stu-id="cd88e-112">String</span></span>|<span data-ttu-id="cd88e-p101">El punto de conexión donde puede obtener información detallada sobre la página. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cd88e-p101">The endpoint where you can get details about the page. Read-only.</span></span>|

<!-- uuid: bfb567de-2a2a-4b81-bf47-a55626a0c166
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "page resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->