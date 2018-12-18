---
title: Tipo de recurso domainState
description: Representa el estado de las operaciones asincrónicas programadas en un dominio.
author: lleonard-msft
ms.openlocfilehash: 683390998254cbf3f7146d1fe89a0a2f109be320
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27355891"
---
# <a name="domainstate-resource-type"></a><span data-ttu-id="ea768-103">Tipo de recurso domainState</span><span class="sxs-lookup"><span data-stu-id="ea768-103">domainState resource type</span></span>

> <span data-ttu-id="ea768-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ea768-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ea768-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ea768-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ea768-106">Representa el estado de las operaciones asincrónicas programadas en un dominio.</span><span class="sxs-lookup"><span data-stu-id="ea768-106">Represents the status of asynchronous operations scheduled on a domain.</span></span>

## <a name="properties"></a><span data-ttu-id="ea768-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ea768-107">Properties</span></span>

| <span data-ttu-id="ea768-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea768-108">Property</span></span>   | <span data-ttu-id="ea768-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea768-109">Type</span></span> | <span data-ttu-id="ea768-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea768-110">Description</span></span> |
|:---------------|:--------|:----------|
| <span data-ttu-id="ea768-111">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="ea768-111">lastActionDateTime</span></span> | <span data-ttu-id="ea768-112">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea768-112">DateTimeOffset</span></span> | <span data-ttu-id="ea768-p102">Marca de tiempo de la última actividad. El valor se actualiza cuando se programa una operación, se inicia la tarea asincrónica y cuando termina la operación.</span><span class="sxs-lookup"><span data-stu-id="ea768-p102">Timestamp for when the last activity occurred. The value is updated when an operation is scheduled, the asynchronous task starts, and when the operation completes.</span></span> |
| <span data-ttu-id="ea768-115">operación</span><span class="sxs-lookup"><span data-stu-id="ea768-115">operation</span></span> | <span data-ttu-id="ea768-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea768-116">String</span></span> | <span data-ttu-id="ea768-p103">Tipo de operación asincrónica. Los valores pueden ser *ForceDelete* o *Verification*</span><span class="sxs-lookup"><span data-stu-id="ea768-p103">Type of asynchronous operation. The values can be *ForceDelete* or *Verification*</span></span> |
| <span data-ttu-id="ea768-119">status</span><span class="sxs-lookup"><span data-stu-id="ea768-119">status</span></span> | <span data-ttu-id="ea768-120">String</span><span class="sxs-lookup"><span data-stu-id="ea768-120">String</span></span> | <span data-ttu-id="ea768-121">Estado actual de la operación.</span><span class="sxs-lookup"><span data-stu-id="ea768-121">Current status of the operation.</span></span> <br> <span data-ttu-id="ea768-122">*Programada*: La operación se ha programado, pero no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="ea768-122">*Scheduled* - Operation has been scheduled but has not started.</span></span> <br> <span data-ttu-id="ea768-123">*En curso*: La tarea se ha iniciado y está en curso.</span><span class="sxs-lookup"><span data-stu-id="ea768-123">*InProgress* - Task has started and is in progress.</span></span> <br> <span data-ttu-id="ea768-124">*Error*: Se ha producido un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="ea768-124">*Failed* - Operation has failed.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ea768-125">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ea768-125">JSON representation</span></span>
<span data-ttu-id="ea768-126">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ea768-126">Here is a JSON representation of the resource.</span></span>

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