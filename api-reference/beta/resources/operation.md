---
title: tipo de recurso de la operación
description: El estado de una operación de larga duración.
ms.openlocfilehash: 71e6a1c47e1f3b18f1481700320779714d716bec
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085836"
---
# <a name="operation-resource-type"></a><span data-ttu-id="ac12f-103">tipo de recurso de la operación</span><span class="sxs-lookup"><span data-stu-id="ac12f-103">operation resource type</span></span>

> <span data-ttu-id="ac12f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ac12f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ac12f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ac12f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ac12f-106">El estado de una operación de larga duración.</span><span class="sxs-lookup"><span data-stu-id="ac12f-106">The status of a long-running operation.</span></span>

## <a name="methods"></a><span data-ttu-id="ac12f-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="ac12f-107">Methods</span></span>

<span data-ttu-id="ac12f-108">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ac12f-108">None</span></span>

## <a name="properties"></a><span data-ttu-id="ac12f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ac12f-109">Properties</span></span>

| <span data-ttu-id="ac12f-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac12f-110">Property</span></span>           | <span data-ttu-id="ac12f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ac12f-111">Type</span></span>            | <span data-ttu-id="ac12f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac12f-112">Description</span></span>                                                                     |
| :----------------- | :-------------- | :-------------------------------------------------------------------------------|
| <span data-ttu-id="ac12f-113">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ac12f-113">createdDateTime</span></span>    | <span data-ttu-id="ac12f-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ac12f-114">DateTimeOffset</span></span>  | <span data-ttu-id="ac12f-115">La hora de inicio de la operación.</span><span class="sxs-lookup"><span data-stu-id="ac12f-115">The start time of the operation.</span></span>                                                |
| <span data-ttu-id="ac12f-116">id</span><span class="sxs-lookup"><span data-stu-id="ac12f-116">id</span></span>                 | <span data-ttu-id="ac12f-117">String</span><span class="sxs-lookup"><span data-stu-id="ac12f-117">String</span></span>          | <span data-ttu-id="ac12f-118">Id. de operación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ac12f-118">The operation id. Read-only.</span></span> <span data-ttu-id="ac12f-119">Servidor que se generó.</span><span class="sxs-lookup"><span data-stu-id="ac12f-119">Server generated.</span></span>                                  |
| <span data-ttu-id="ac12f-120">lastActionDateTime</span><span class="sxs-lookup"><span data-stu-id="ac12f-120">lastActionDateTime</span></span> | <span data-ttu-id="ac12f-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ac12f-121">DateTimeOffset</span></span>  | <span data-ttu-id="ac12f-122">Hora de la última acción de la operación.</span><span class="sxs-lookup"><span data-stu-id="ac12f-122">The time of the last action of the operation.</span></span>                                   |
| <span data-ttu-id="ac12f-123">status</span><span class="sxs-lookup"><span data-stu-id="ac12f-123">status</span></span>             | <span data-ttu-id="ac12f-124">String</span><span class="sxs-lookup"><span data-stu-id="ac12f-124">String</span></span>          | <span data-ttu-id="ac12f-125">Los valores posibles son: `notStarted`, `running`, `completed` y `failed`.</span><span class="sxs-lookup"><span data-stu-id="ac12f-125">Possible values are: `notStarted`, `running`, `completed`, `failed`.</span></span> <span data-ttu-id="ac12f-126">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ac12f-126">Read-only.</span></span> |

## <a name="relationships"></a><span data-ttu-id="ac12f-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ac12f-127">Relationships</span></span>

<span data-ttu-id="ac12f-128">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ac12f-128">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="ac12f-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ac12f-129">JSON representation</span></span>

<span data-ttu-id="ac12f-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ac12f-130">The following is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.operation"
}-->
```json
{
  "createdDateTime": "String (timestamp)",
  "id": "String (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "status": "notStarted | running | completed | failed"
}
```

## <a name="example"></a><span data-ttu-id="ac12f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac12f-131">Example</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.operation"
}-->
```json
{
  "createdDateTime": "2018-09-06T15:58:41Z",
  "id": "ABB33D04-3A2C-4D78-996F-9EEEF55EF119",
  "lastActionDateTime": "2018-09-06T15:58:41Z",
  "status": "completed"
}
```

<!-- uuid: 13fa92b1-3b41-498b-aab1-f943464a124f
2018-03-30 10:29:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "operation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->