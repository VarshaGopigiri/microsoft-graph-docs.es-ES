---
title: Tipo de recurso onenoteOperationError
description: Error de una operación de OneNote que no se pudo completar.
author: Jewan-microsoft
ms.openlocfilehash: 4cba6de22f08e2e41f281863e3494fbb589e6e41
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27354785"
---
# <a name="onenoteoperationerror-resource-type"></a><span data-ttu-id="7c098-103">Tipo de recurso onenoteOperationError</span><span class="sxs-lookup"><span data-stu-id="7c098-103">onenoteOperationError resource type</span></span>

> <span data-ttu-id="7c098-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7c098-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7c098-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7c098-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="7c098-106">Error de una operación de OneNote que no se pudo completar.</span><span class="sxs-lookup"><span data-stu-id="7c098-106">An error from a failed OneNote operation.</span></span>

## <a name="json-representation"></a><span data-ttu-id="7c098-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7c098-107">JSON representation</span></span>

<span data-ttu-id="7c098-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7c098-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenoteOperationError"
}-->

```json
{
  "code": "string",
  "message": "string"
}

```
## <a name="properties"></a><span data-ttu-id="7c098-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7c098-109">Properties</span></span>
| <span data-ttu-id="7c098-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7c098-110">Property</span></span>     | <span data-ttu-id="7c098-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="7c098-111">Type</span></span>   |<span data-ttu-id="7c098-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c098-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="7c098-113">código</span><span class="sxs-lookup"><span data-stu-id="7c098-113">code</span></span>|<span data-ttu-id="7c098-114">string</span><span class="sxs-lookup"><span data-stu-id="7c098-114">string</span></span>|<span data-ttu-id="7c098-115">Código de error.</span><span class="sxs-lookup"><span data-stu-id="7c098-115">The error code.</span></span>|
|<span data-ttu-id="7c098-116">message</span><span class="sxs-lookup"><span data-stu-id="7c098-116">message</span></span>|<span data-ttu-id="7c098-117">string</span><span class="sxs-lookup"><span data-stu-id="7c098-117">string</span></span>|<span data-ttu-id="7c098-118">Mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="7c098-118">The error message.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteOperationError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
