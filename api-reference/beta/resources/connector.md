---
title: tipo de recurso de conector
description: Aquí tiene una representación JSON del recurso.
ms.openlocfilehash: 6d4cb7e5ca1a5384dbb6c8be92e7ce4eb107388a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089600"
---
# <a name="connector-resource-type"></a><span data-ttu-id="bbbf7-103">tipo de recurso de conector</span><span class="sxs-lookup"><span data-stu-id="bbbf7-103">connector resource type</span></span>

> <span data-ttu-id="bbbf7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bbbf7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-105">Use of these APIs in production applications is not supported.</span></span>

<!-- Not supported items
|[Create connectorGroup](../api/connector-post-memberof.md) |[connectorGroup](connectorgroup.md)| Associate a connector with a new connectorGroup by posting to the memberOf collection.|
|[Update](../api/connector-update.md) | [connector](connector.md)   | Connectors are created when they are registed with the tenant. |
|[Delete](../api/connector-delete.md) | None |Delete connector object. |

-->

## <a name="methods"></a><span data-ttu-id="bbbf7-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="bbbf7-106">Methods</span></span>

| <span data-ttu-id="bbbf7-107">Método</span><span class="sxs-lookup"><span data-stu-id="bbbf7-107">Method</span></span>           | <span data-ttu-id="bbbf7-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bbbf7-108">Return Type</span></span>    |<span data-ttu-id="bbbf7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbbf7-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="bbbf7-110">Obtener el conector</span><span class="sxs-lookup"><span data-stu-id="bbbf7-110">Get connector</span></span>](../api/connector-get.md) | [<span data-ttu-id="bbbf7-111">conector</span><span class="sxs-lookup"><span data-stu-id="bbbf7-111">connector</span></span>](connector.md) |<span data-ttu-id="bbbf7-112">Leer las propiedades y las relaciones del objeto de conector.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-112">Read properties and relationships of connector object.</span></span>|
|[<span data-ttu-id="bbbf7-113">Enumerar memberOf</span><span class="sxs-lookup"><span data-stu-id="bbbf7-113">List memberOf</span></span>](../api/connector-list-memberof.md) |<span data-ttu-id="bbbf7-114">colección de [connectorGroup](connectorgroup.md)</span><span class="sxs-lookup"><span data-stu-id="bbbf7-114">[connectorGroup](connectorgroup.md) collection</span></span>| <span data-ttu-id="bbbf7-115">Obtenga el objeto connectorGroup asociado con el conector.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-115">Get the connectorGroup object associated with the connector.</span></span>|

## <a name="properties"></a><span data-ttu-id="bbbf7-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bbbf7-116">Properties</span></span>
| <span data-ttu-id="bbbf7-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bbbf7-117">Property</span></span>     | <span data-ttu-id="bbbf7-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbbf7-118">Type</span></span>   |<span data-ttu-id="bbbf7-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbbf7-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bbbf7-120">externalIp</span><span class="sxs-lookup"><span data-stu-id="bbbf7-120">externalIp</span></span>|<span data-ttu-id="bbbf7-121">String</span><span class="sxs-lookup"><span data-stu-id="bbbf7-121">String</span></span>|<span data-ttu-id="bbbf7-122">La dirección IP externa como detectados por el servicio para la máquina de conector.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-122">The external IP address as detected by the service for the connector machine.</span></span> <span data-ttu-id="bbbf7-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbbf7-123">Read-only</span></span>|
|<span data-ttu-id="bbbf7-124">id</span><span class="sxs-lookup"><span data-stu-id="bbbf7-124">id</span></span>|<span data-ttu-id="bbbf7-125">String</span><span class="sxs-lookup"><span data-stu-id="bbbf7-125">String</span></span>| <span data-ttu-id="bbbf7-126">El identificador del objeto del conector.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-126">The object id of the connector.</span></span> <BR><span data-ttu-id="bbbf7-127">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-127">Read-only.</span></span>|
|<span data-ttu-id="bbbf7-128">nombreEquipo</span><span class="sxs-lookup"><span data-stu-id="bbbf7-128">machineName</span></span>|<span data-ttu-id="bbbf7-129">String</span><span class="sxs-lookup"><span data-stu-id="bbbf7-129">String</span></span>| <span data-ttu-id="bbbf7-130">El nombre de la máquina que se está ejecutando el conector.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-130">The name of the machine that the connector is running on.</span></span> <BR><span data-ttu-id="bbbf7-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbbf7-131">Read-only</span></span>|
|<span data-ttu-id="bbbf7-132">status</span><span class="sxs-lookup"><span data-stu-id="bbbf7-132">status</span></span>|<span data-ttu-id="bbbf7-133">string</span><span class="sxs-lookup"><span data-stu-id="bbbf7-133">string</span></span>| <span data-ttu-id="bbbf7-134">Indica el estado del conector.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-134">Indicates the status of the connector.</span></span> <span data-ttu-id="bbbf7-135">Los valores posibles son: `active` y `inactive`.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-135">Possible values are: `active`, `inactive`.</span></span> <span data-ttu-id="bbbf7-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="bbbf7-136">Read-only</span></span> |

## <a name="relationships"></a><span data-ttu-id="bbbf7-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bbbf7-137">Relationships</span></span>
| <span data-ttu-id="bbbf7-138">Relación</span><span class="sxs-lookup"><span data-stu-id="bbbf7-138">Relationship</span></span> | <span data-ttu-id="bbbf7-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="bbbf7-139">Type</span></span>   |<span data-ttu-id="bbbf7-140">Descripción</span><span class="sxs-lookup"><span data-stu-id="bbbf7-140">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bbbf7-141">memberOf</span><span class="sxs-lookup"><span data-stu-id="bbbf7-141">memberOf</span></span>|<span data-ttu-id="bbbf7-142">colección de [connectorGroup](connectorgroup.md)</span><span class="sxs-lookup"><span data-stu-id="bbbf7-142">[connectorGroup](connectorgroup.md) collection</span></span>| <span data-ttu-id="bbbf7-143">El connectorGroup que la conexión es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-143">The connectorGroup that the connect is a member of.</span></span><br><span data-ttu-id="bbbf7-144">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-144">Read-only.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="bbbf7-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bbbf7-145">JSON representation</span></span>

<span data-ttu-id="bbbf7-146">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bbbf7-146">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.connector"
}-->

```json
{
  "externalIp": "String",
  "id": "String (identifier)",
  "machineName": "String",
  "status": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "connector resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
