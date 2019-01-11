---
title: Tipo de recurso onenoteOperationError
description: Error de una operación de OneNote que no se pudo completar.
author: Jewan-microsoft
localization_priority: Normal
ms.openlocfilehash: cfe859bea40f15311a631e8b1d2b3c3a3c179d0c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891535"
---
# <a name="onenoteoperationerror-resource-type"></a><span data-ttu-id="39067-103">Tipo de recurso onenoteOperationError</span><span class="sxs-lookup"><span data-stu-id="39067-103">onenoteOperationError resource type</span></span>

> <span data-ttu-id="39067-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="39067-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="39067-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="39067-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="39067-106">Error de una operación de OneNote que no se pudo completar.</span><span class="sxs-lookup"><span data-stu-id="39067-106">An error from a failed OneNote operation.</span></span>

## <a name="json-representation"></a><span data-ttu-id="39067-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="39067-107">JSON representation</span></span>

<span data-ttu-id="39067-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="39067-108">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="39067-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39067-109">Properties</span></span>
| <span data-ttu-id="39067-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="39067-110">Property</span></span>     | <span data-ttu-id="39067-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="39067-111">Type</span></span>   |<span data-ttu-id="39067-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="39067-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="39067-113">código</span><span class="sxs-lookup"><span data-stu-id="39067-113">code</span></span>|<span data-ttu-id="39067-114">string</span><span class="sxs-lookup"><span data-stu-id="39067-114">string</span></span>|<span data-ttu-id="39067-115">Código de error.</span><span class="sxs-lookup"><span data-stu-id="39067-115">The error code.</span></span>|
|<span data-ttu-id="39067-116">message</span><span class="sxs-lookup"><span data-stu-id="39067-116">message</span></span>|<span data-ttu-id="39067-117">string</span><span class="sxs-lookup"><span data-stu-id="39067-117">string</span></span>|<span data-ttu-id="39067-118">Mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="39067-118">The error message.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteOperationError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
