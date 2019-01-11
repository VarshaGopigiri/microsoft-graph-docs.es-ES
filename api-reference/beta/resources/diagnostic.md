---
title: tipo de recurso de diagnóstico
description: Información acerca de un error o una advertencia para una operación de OneNote.
localization_priority: Normal
ms.openlocfilehash: 28cdd1c07bab0494a69cfb7ce6a5284238e1ff19
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845993"
---
# <a name="diagnostic-resource-type"></a><span data-ttu-id="9742c-103">tipo de recurso de diagnóstico</span><span class="sxs-lookup"><span data-stu-id="9742c-103">diagnostic resource type</span></span>

> <span data-ttu-id="9742c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9742c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9742c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9742c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9742c-106">Información acerca de un error o una advertencia para una operación de OneNote.</span><span class="sxs-lookup"><span data-stu-id="9742c-106">Information about an error or warning for a OneNote operation.</span></span>

## <a name="json-representation"></a><span data-ttu-id="9742c-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9742c-107">JSON representation</span></span>

<span data-ttu-id="9742c-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9742c-108">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.diagnostic"
}-->

```json
{
  "message": "string",
  "url": "string"
}

```
## <a name="properties"></a><span data-ttu-id="9742c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9742c-109">Properties</span></span>
| <span data-ttu-id="9742c-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9742c-110">Property</span></span>     | <span data-ttu-id="9742c-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="9742c-111">Type</span></span>   |<span data-ttu-id="9742c-112">Description</span><span class="sxs-lookup"><span data-stu-id="9742c-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9742c-113">message</span><span class="sxs-lookup"><span data-stu-id="9742c-113">message</span></span>|<span data-ttu-id="9742c-114">String</span><span class="sxs-lookup"><span data-stu-id="9742c-114">String</span></span>|<span data-ttu-id="9742c-115">El mensaje que describe la condición que desencadenó el error o la advertencia.</span><span class="sxs-lookup"><span data-stu-id="9742c-115">The message describing the condition that triggered the error or warning.</span></span>|
|<span data-ttu-id="9742c-116">url</span><span class="sxs-lookup"><span data-stu-id="9742c-116">url</span></span>|<span data-ttu-id="9742c-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="9742c-117">String</span></span>|<span data-ttu-id="9742c-118">El vínculo a la documentación para este problema.</span><span class="sxs-lookup"><span data-stu-id="9742c-118">The link to the documentation for this issue.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "diagnostic resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
