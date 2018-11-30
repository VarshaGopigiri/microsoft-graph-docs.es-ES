---
title: tipo de recurso commsOperation
description: El estado de determinadas operaciones de larga duración.
ms.openlocfilehash: d9adf240bff566dc0af5e369da24c7f8658a6c1c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087855"
---
# <a name="commsoperation-resource-type"></a><span data-ttu-id="e2a37-103">tipo de recurso commsOperation</span><span class="sxs-lookup"><span data-stu-id="e2a37-103">commsOperation resource type</span></span>

> <span data-ttu-id="e2a37-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e2a37-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e2a37-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e2a37-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e2a37-106">El estado de determinadas operaciones de larga duración.</span><span class="sxs-lookup"><span data-stu-id="e2a37-106">The status of certain long-running operations.</span></span>

## <a name="methods"></a><span data-ttu-id="e2a37-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="e2a37-107">Methods</span></span>
<span data-ttu-id="e2a37-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e2a37-108">None</span></span>

## <a name="properties"></a><span data-ttu-id="e2a37-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2a37-109">Properties</span></span>

| <span data-ttu-id="e2a37-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e2a37-110">Property</span></span>           | <span data-ttu-id="e2a37-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="e2a37-111">Type</span></span>                        | <span data-ttu-id="e2a37-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2a37-112">Description</span></span>                                                                     |
| :----------------- | :-------------------------- | :-------------------------------------------------------------------------------|
| <span data-ttu-id="e2a37-113">clientContext</span><span class="sxs-lookup"><span data-stu-id="e2a37-113">clientContext</span></span>      | <span data-ttu-id="e2a37-114">String</span><span class="sxs-lookup"><span data-stu-id="e2a37-114">String</span></span>                      | <span data-ttu-id="e2a37-115">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="e2a37-115">The client context.</span></span>                                                             |
| <span data-ttu-id="e2a37-116">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e2a37-116">createdDateTime</span></span>    | <span data-ttu-id="e2a37-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e2a37-117">DateTimeOffset</span></span>              | <span data-ttu-id="e2a37-118">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="e2a37-118">The start time of the operation.</span></span>                                                |
| <span data-ttu-id="e2a37-119">id</span><span class="sxs-lookup"><span data-stu-id="e2a37-119">id</span></span>                 | <span data-ttu-id="e2a37-120">String</span><span class="sxs-lookup"><span data-stu-id="e2a37-120">String</span></span>                      | <span data-ttu-id="e2a37-121">Id. de operación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e2a37-121">The operation id. Read-only.</span></span> <span data-ttu-id="e2a37-122">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="e2a37-122">Server generated.</span></span>                                  |
| <span data-ttu-id="e2a37-123">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="e2a37-123">lastActionDateTime</span></span> | <span data-ttu-id="e2a37-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e2a37-124">DateTimeOffset</span></span>              | <span data-ttu-id="e2a37-125">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="e2a37-125">The time of the last action of the operation.</span></span>                                   |
| <span data-ttu-id="e2a37-126">resultInfo</span><span class="sxs-lookup"><span data-stu-id="e2a37-126">resultInfo</span></span>         | [<span data-ttu-id="e2a37-127">resultInfo</span><span class="sxs-lookup"><span data-stu-id="e2a37-127">resultInfo</span></span>](resultinfo.md) | <span data-ttu-id="e2a37-128">La información del resultado.</span><span class="sxs-lookup"><span data-stu-id="e2a37-128">The result information.</span></span> <span data-ttu-id="e2a37-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e2a37-129">Read-only.</span></span> <span data-ttu-id="e2a37-130">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="e2a37-130">Server generated.</span></span>                            |
| <span data-ttu-id="e2a37-131">status</span><span class="sxs-lookup"><span data-stu-id="e2a37-131">status</span></span>             | <span data-ttu-id="e2a37-132">String</span><span class="sxs-lookup"><span data-stu-id="e2a37-132">String</span></span>                      | <span data-ttu-id="e2a37-133">Los valores posibles son: `notStarted`, `running`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="e2a37-133">Possible values are: `notStarted`, `running`, `completed`, `failed`.</span></span> <span data-ttu-id="e2a37-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e2a37-134">Read-only.</span></span> |

## <a name="relationships"></a><span data-ttu-id="e2a37-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e2a37-135">Relationships</span></span>
<span data-ttu-id="e2a37-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e2a37-136">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="e2a37-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e2a37-137">JSON representation</span></span>

<span data-ttu-id="e2a37-138">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e2a37-138">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.commsOperation"
}-->
```json
{
  "clientContext": "String",
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "resultInfo": { "@odata.type": "#microsoft.graph.resultInfo" },
  "status": "notStarted | running | completed | failed"
}
```

## <a name="example"></a><span data-ttu-id="e2a37-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2a37-139">Example</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsOperation"
}-->
```json
{
  "clientContext": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "createdDateTime": "2018-09-06T15:58:41Z",
  "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "lastActionDateTime": "2018-09-06T15:58:41Z",
  "resultInfo": {
    "@odata.type": "#microsoft.graph.resultInfo",
    "code": "200"
  },
  "status": "completed"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "commsOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
