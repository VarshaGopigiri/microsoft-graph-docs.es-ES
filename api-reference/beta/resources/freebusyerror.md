---
title: tipo de recurso freeBusyError
description: " > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción."
localization_priority: Normal
ms.openlocfilehash: 63cfc4b14ba6176d582155df57b7f7f787e63cf4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889771"
---
# <a name="freebusyerror-resource-type"></a><span data-ttu-id="5329a-104">tipo de recurso freeBusyError</span><span class="sxs-lookup"><span data-stu-id="5329a-104">freeBusyError resource type</span></span>

 > <span data-ttu-id="5329a-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5329a-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5329a-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5329a-106">Use of these APIs in production applications is not supported.</span></span>
 
<span data-ttu-id="5329a-107">Representa información de error al intentar obtener la disponibilidad de un usuario, una lista de distribución o un recurso.</span><span class="sxs-lookup"><span data-stu-id="5329a-107">Represents error information from attempting to get the availability of a user, distribution list, or resource.</span></span>

## <a name="properties"></a><span data-ttu-id="5329a-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5329a-108">Properties</span></span>
| <span data-ttu-id="5329a-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5329a-109">Property</span></span>     | <span data-ttu-id="5329a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5329a-110">Type</span></span>   |<span data-ttu-id="5329a-111">Description</span><span class="sxs-lookup"><span data-stu-id="5329a-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5329a-112">message</span><span class="sxs-lookup"><span data-stu-id="5329a-112">message</span></span> |<span data-ttu-id="5329a-113">String</span><span class="sxs-lookup"><span data-stu-id="5329a-113">String</span></span> |<span data-ttu-id="5329a-114">Describe el error.</span><span class="sxs-lookup"><span data-stu-id="5329a-114">Describes the error.</span></span> |
|<span data-ttu-id="5329a-115">responseCode</span><span class="sxs-lookup"><span data-stu-id="5329a-115">responseCode</span></span> |<span data-ttu-id="5329a-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="5329a-116">String</span></span> |<span data-ttu-id="5329a-117">El código de respuesta de consulta de la disponibilidad del usuario, la lista de distribución o el recurso.</span><span class="sxs-lookup"><span data-stu-id="5329a-117">The response code from querying for the availability of the user, distribution list, or resource.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="5329a-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5329a-118">JSON representation</span></span>

<span data-ttu-id="5329a-119">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5329a-119">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.freeBusyError"
}-->

```json
{
  "message": "String",
  "responseCode": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "freeBusyError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
