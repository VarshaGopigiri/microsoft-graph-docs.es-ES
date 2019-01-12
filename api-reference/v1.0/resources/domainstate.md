---
title: Tipo de recurso domainState
description: Representa el estado de las operaciones asincrónicas programadas en un dominio.
author: lleonard-msft
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 6a7741448b9c91be32f67f89cbafa5a579320083
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938296"
---
# <a name="domainstate-resource-type"></a><span data-ttu-id="36fef-103">Tipo de recurso domainState</span><span class="sxs-lookup"><span data-stu-id="36fef-103">domainState resource type</span></span>

<span data-ttu-id="36fef-104">Representa el estado de las operaciones asincrónicas programadas en un dominio.</span><span class="sxs-lookup"><span data-stu-id="36fef-104">Represents the status of asynchronous operations scheduled on a domain.</span></span>

## <a name="properties"></a><span data-ttu-id="36fef-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36fef-105">Properties</span></span>

| <span data-ttu-id="36fef-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="36fef-106">Property</span></span>   | <span data-ttu-id="36fef-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="36fef-107">Type</span></span> | <span data-ttu-id="36fef-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="36fef-108">Description</span></span> |
|:---------------|:--------|:----------|
| <span data-ttu-id="36fef-109">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="36fef-109">lastActionDateTime</span></span> | <span data-ttu-id="36fef-110">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="36fef-110">DateTimeOffset</span></span> | <span data-ttu-id="36fef-p101">Marca de tiempo de la última actividad. El valor se actualiza cuando se programa una operación, se inicia la tarea asincrónica y cuando termina la operación.</span><span class="sxs-lookup"><span data-stu-id="36fef-p101">Timestamp for when the last activity occurred. The value is updated when an operation is scheduled, the asynchronous task starts, and when the operation completes.</span></span> |
| <span data-ttu-id="36fef-113">operación</span><span class="sxs-lookup"><span data-stu-id="36fef-113">operation</span></span> | <span data-ttu-id="36fef-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="36fef-114">String</span></span> | <span data-ttu-id="36fef-p102">Tipo de operación asincrónica. Los valores pueden ser *ForceDelete* o *Verification*</span><span class="sxs-lookup"><span data-stu-id="36fef-p102">Type of asynchronous operation. The values can be *ForceDelete* or *Verification*</span></span> |
| <span data-ttu-id="36fef-117">status</span><span class="sxs-lookup"><span data-stu-id="36fef-117">status</span></span> | <span data-ttu-id="36fef-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="36fef-118">String</span></span> | <span data-ttu-id="36fef-119">Estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="36fef-119">Current status of the operation.</span></span> <br> <span data-ttu-id="36fef-120">*Programada*: La operación se ha programado, pero no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="36fef-120">*Scheduled* - Operation has been scheduled but has not started.</span></span> <br> <span data-ttu-id="36fef-121">*En curso*: La tarea se ha iniciado y está en curso.</span><span class="sxs-lookup"><span data-stu-id="36fef-121">*InProgress* - Task has started and is in progress.</span></span> <br> <span data-ttu-id="36fef-122">*Error*: Se ha producido un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="36fef-122">*Failed* - Operation has failed.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="36fef-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="36fef-123">JSON representation</span></span>
<span data-ttu-id="36fef-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="36fef-124">Here is a JSON representation of the resource.</span></span>

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
