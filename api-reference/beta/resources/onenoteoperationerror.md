---
title: Tipo de recurso onenoteOperationError
description: Error de una operación de OneNote que no se pudo completar.
ms.openlocfilehash: 0dab8b405c99f2931d2cc02cc915df5f805322d8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089737"
---
# <a name="onenoteoperationerror-resource-type"></a><span data-ttu-id="9473f-103">Tipo de recurso onenoteOperationError</span><span class="sxs-lookup"><span data-stu-id="9473f-103">onenoteOperationError resource type</span></span>

> <span data-ttu-id="9473f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9473f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9473f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9473f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9473f-106">Error de una operación de OneNote que no se pudo completar.</span><span class="sxs-lookup"><span data-stu-id="9473f-106">An error from a failed OneNote operation.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9473f-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9473f-107">JSON representation</span></span>

<span data-ttu-id="9473f-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9473f-108">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="9473f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9473f-109">Properties</span></span>
| <span data-ttu-id="9473f-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9473f-110">Property</span></span>     | <span data-ttu-id="9473f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="9473f-111">Type</span></span>   |<span data-ttu-id="9473f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9473f-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9473f-113">código</span><span class="sxs-lookup"><span data-stu-id="9473f-113">code</span></span>|<span data-ttu-id="9473f-114">string</span><span class="sxs-lookup"><span data-stu-id="9473f-114">string</span></span>|<span data-ttu-id="9473f-115">Código de error.</span><span class="sxs-lookup"><span data-stu-id="9473f-115">The error code.</span></span>|
|<span data-ttu-id="9473f-116">message</span><span class="sxs-lookup"><span data-stu-id="9473f-116">message</span></span>|<span data-ttu-id="9473f-117">string</span><span class="sxs-lookup"><span data-stu-id="9473f-117">string</span></span>|<span data-ttu-id="9473f-118">Mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="9473f-118">The error message.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteOperationError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
