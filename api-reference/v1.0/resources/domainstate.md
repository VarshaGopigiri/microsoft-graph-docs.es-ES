---
title: Tipo de recurso domainState
description: Representa el estado de las operaciones asincrónicas programadas en un dominio.
author: lleonard-msft
localization_priority: Normal
ms.openlocfilehash: f24a5a9c493dc1cea16cb9038b85dc0a793bdfee
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27880650"
---
# <a name="domainstate-resource-type"></a><span data-ttu-id="1c62c-103">Tipo de recurso domainState</span><span class="sxs-lookup"><span data-stu-id="1c62c-103">domainState resource type</span></span>

<span data-ttu-id="1c62c-104">Representa el estado de las operaciones asincrónicas programadas en un dominio.</span><span class="sxs-lookup"><span data-stu-id="1c62c-104">Represents the status of asynchronous operations scheduled on a domain.</span></span>

## <a name="properties"></a><span data-ttu-id="1c62c-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1c62c-105">Properties</span></span>

| <span data-ttu-id="1c62c-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1c62c-106">Property</span></span>   | <span data-ttu-id="1c62c-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c62c-107">Type</span></span> | <span data-ttu-id="1c62c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c62c-108">Description</span></span> |
|:---------------|:--------|:----------|
| <span data-ttu-id="1c62c-109">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="1c62c-109">lastActionDateTime</span></span> | <span data-ttu-id="1c62c-110">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1c62c-110">DateTimeOffset</span></span> | <span data-ttu-id="1c62c-p101">Marca de tiempo de la última actividad. El valor se actualiza cuando se programa una operación, se inicia la tarea asincrónica y cuando termina la operación.</span><span class="sxs-lookup"><span data-stu-id="1c62c-p101">Timestamp for when the last activity occurred. The value is updated when an operation is scheduled, the asynchronous task starts, and when the operation completes.</span></span> |
| <span data-ttu-id="1c62c-113">operación</span><span class="sxs-lookup"><span data-stu-id="1c62c-113">operation</span></span> | <span data-ttu-id="1c62c-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="1c62c-114">String</span></span> | <span data-ttu-id="1c62c-p102">Tipo de operación asincrónica. Los valores pueden ser *ForceDelete* o *Verification*</span><span class="sxs-lookup"><span data-stu-id="1c62c-p102">Type of asynchronous operation. The values can be *ForceDelete* or *Verification*</span></span> |
| <span data-ttu-id="1c62c-117">status</span><span class="sxs-lookup"><span data-stu-id="1c62c-117">status</span></span> | <span data-ttu-id="1c62c-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="1c62c-118">String</span></span> | <span data-ttu-id="1c62c-119">Estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="1c62c-119">Current status of the operation.</span></span> <br> <span data-ttu-id="1c62c-120">*Programada*: La operación se ha programado, pero no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="1c62c-120">*Scheduled* - Operation has been scheduled but has not started.</span></span> <br> <span data-ttu-id="1c62c-121">*En curso*: La tarea se ha iniciado y está en curso.</span><span class="sxs-lookup"><span data-stu-id="1c62c-121">*InProgress* - Task has started and is in progress.</span></span> <br> <span data-ttu-id="1c62c-122">*Error*: Se ha producido un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="1c62c-122">*Failed* - Operation has failed.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="1c62c-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1c62c-123">JSON representation</span></span>
<span data-ttu-id="1c62c-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1c62c-124">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.domainState"
}-->

```json
{
  "lastActionDateTime": "String (timestamp)",
  "operation": "String",
  "status": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "domainState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
