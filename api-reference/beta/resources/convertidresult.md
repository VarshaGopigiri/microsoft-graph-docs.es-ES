---
title: tipo de recurso convertIdResult
description: El resultado de una conversión de formato de identificador realizado por la función translateExchangeIds.
localization_priority: Normal
ms.openlocfilehash: 7e1878de3d3b7ddee36d799c928d6a130b578200
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821458"
---
# <a name="convertidresult-resource-type"></a><span data-ttu-id="9d46e-103">tipo de recurso convertIdResult</span><span class="sxs-lookup"><span data-stu-id="9d46e-103">convertIdResult resource type</span></span>

> <span data-ttu-id="9d46e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9d46e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9d46e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9d46e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9d46e-106">El resultado de una conversión de formato de identificador realizado por la función [translateExchangeIds](../api/user-translateexchangeids.md) .</span><span class="sxs-lookup"><span data-stu-id="9d46e-106">The result of an ID format conversion performed by the [translateExchangeIds](../api/user-translateexchangeids.md) function.</span></span>

## <a name="properties"></a><span data-ttu-id="9d46e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9d46e-107">Properties</span></span>

| <span data-ttu-id="9d46e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9d46e-108">Property</span></span> | <span data-ttu-id="9d46e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d46e-109">Type</span></span> | <span data-ttu-id="9d46e-110">Description</span><span class="sxs-lookup"><span data-stu-id="9d46e-110">Description</span></span> |
|:---------|:-----|:------------|
| <span data-ttu-id="9d46e-111">sourceId</span><span class="sxs-lookup"><span data-stu-id="9d46e-111">sourceId</span></span> | <span data-ttu-id="9d46e-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="9d46e-112">String</span></span> | <span data-ttu-id="9d46e-113">El identificador que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="9d46e-113">The identifier that was converted.</span></span> <span data-ttu-id="9d46e-114">Este valor es el identificador original, reactivar convertido.</span><span class="sxs-lookup"><span data-stu-id="9d46e-114">This value is the original, un-converted identifier.</span></span> |
| <span data-ttu-id="9d46e-115">targetId</span><span class="sxs-lookup"><span data-stu-id="9d46e-115">targetId</span></span> | <span data-ttu-id="9d46e-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="9d46e-116">String</span></span> | <span data-ttu-id="9d46e-117">El identificador convertido.</span><span class="sxs-lookup"><span data-stu-id="9d46e-117">The converted identifier.</span></span> <span data-ttu-id="9d46e-118">Este valor no está presente si la conversión produjo un error.</span><span class="sxs-lookup"><span data-stu-id="9d46e-118">This value is not present if the conversion failed.</span></span> |
| <span data-ttu-id="9d46e-119">errorDetails</span><span class="sxs-lookup"><span data-stu-id="9d46e-119">errorDetails</span></span> | [<span data-ttu-id="9d46e-120">Error genérico</span><span class="sxs-lookup"><span data-stu-id="9d46e-120">genericError</span></span>](genericerror.md) | <span data-ttu-id="9d46e-121">Un objeto de error que indica el motivo del error de conversión.</span><span class="sxs-lookup"><span data-stu-id="9d46e-121">An error object indicating the reason for the conversion failure.</span></span> <span data-ttu-id="9d46e-122">Este valor no está presente si la conversión se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9d46e-122">This value is not present if the conversion succeeded.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="9d46e-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9d46e-123">JSON representation</span></span>

<span data-ttu-id="9d46e-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9d46e-124">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "targetId",
    "errorDetails"
  ],
  "@odata.type": "microsoft.graph.convertIdResult"
}-->

```json
{
  "sourceId": "String",
  "targetId": "String",
  "errorDetails": {
    "@odata.type": "microsoft.graph.genericError"
  }
}
```
