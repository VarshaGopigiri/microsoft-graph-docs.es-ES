---
title: tipo de recurso commsOperation
description: El estado de determinadas operaciones de larga duración.
author: VinodRavichandran
ms.openlocfilehash: 09d3f81e8f6307850d94cfab43f98426dae47a5f
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380355"
---
# <a name="commsoperation-resource-type"></a><span data-ttu-id="d1052-103">tipo de recurso commsOperation</span><span class="sxs-lookup"><span data-stu-id="d1052-103">commsOperation resource type</span></span>

> <span data-ttu-id="d1052-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d1052-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d1052-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d1052-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d1052-106">El estado de determinadas operaciones de larga duración.</span><span class="sxs-lookup"><span data-stu-id="d1052-106">The status of certain long-running operations.</span></span>

## <a name="methods"></a><span data-ttu-id="d1052-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1052-107">Methods</span></span>
<span data-ttu-id="d1052-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d1052-108">None</span></span>

## <a name="properties"></a><span data-ttu-id="d1052-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1052-109">Properties</span></span>

| <span data-ttu-id="d1052-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d1052-110">Property</span></span>           | <span data-ttu-id="d1052-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1052-111">Type</span></span>                        | <span data-ttu-id="d1052-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1052-112">Description</span></span>                                                                     |
| :----------------- | :-------------------------- | :-------------------------------------------------------------------------------|
| <span data-ttu-id="d1052-113">clientContext</span><span class="sxs-lookup"><span data-stu-id="d1052-113">clientContext</span></span>      | <span data-ttu-id="d1052-114">String</span><span class="sxs-lookup"><span data-stu-id="d1052-114">String</span></span>                      | <span data-ttu-id="d1052-115">El contexto de cliente.</span><span class="sxs-lookup"><span data-stu-id="d1052-115">The client context.</span></span>                                                             |
| <span data-ttu-id="d1052-116">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d1052-116">createdDateTime</span></span>    | <span data-ttu-id="d1052-117">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d1052-117">DateTimeOffset</span></span>              | <span data-ttu-id="d1052-118">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="d1052-118">The start time of the operation.</span></span>                                                |
| <span data-ttu-id="d1052-119">id</span><span class="sxs-lookup"><span data-stu-id="d1052-119">id</span></span>                 | <span data-ttu-id="d1052-120">String</span><span class="sxs-lookup"><span data-stu-id="d1052-120">String</span></span>                      | <span data-ttu-id="d1052-121">Id. de operación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d1052-121">The operation id. Read-only.</span></span> <span data-ttu-id="d1052-122">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="d1052-122">Server generated.</span></span>                                  |
| <span data-ttu-id="d1052-123">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="d1052-123">lastActionDateTime</span></span> | <span data-ttu-id="d1052-124">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d1052-124">DateTimeOffset</span></span>              | <span data-ttu-id="d1052-125">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="d1052-125">The time of the last action of the operation.</span></span>                                   |
| <span data-ttu-id="d1052-126">resultInfo</span><span class="sxs-lookup"><span data-stu-id="d1052-126">resultInfo</span></span>         | [<span data-ttu-id="d1052-127">resultInfo</span><span class="sxs-lookup"><span data-stu-id="d1052-127">resultInfo</span></span>](resultinfo.md) | <span data-ttu-id="d1052-128">La información del resultado.</span><span class="sxs-lookup"><span data-stu-id="d1052-128">The result information.</span></span> <span data-ttu-id="d1052-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d1052-129">Read-only.</span></span> <span data-ttu-id="d1052-130">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="d1052-130">Server generated.</span></span>                            |
| <span data-ttu-id="d1052-131">status</span><span class="sxs-lookup"><span data-stu-id="d1052-131">status</span></span>             | <span data-ttu-id="d1052-132">String</span><span class="sxs-lookup"><span data-stu-id="d1052-132">String</span></span>                      | <span data-ttu-id="d1052-133">Los valores posibles son: `notStarted`, `running`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="d1052-133">Possible values are: `notStarted`, `running`, `completed`, `failed`.</span></span> <span data-ttu-id="d1052-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d1052-134">Read-only.</span></span> |

## <a name="relationships"></a><span data-ttu-id="d1052-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d1052-135">Relationships</span></span>
<span data-ttu-id="d1052-136">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d1052-136">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="d1052-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d1052-137">JSON representation</span></span>

<span data-ttu-id="d1052-138">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d1052-138">The following is a JSON representation of the resource.</span></span>

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

## <a name="example"></a><span data-ttu-id="d1052-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d1052-139">Example</span></span>

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
