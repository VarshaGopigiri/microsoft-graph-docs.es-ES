---
title: tipo de recurso de conector
description: Aquí tiene una representación JSON del recurso.
localization_priority: Normal
ms.openlocfilehash: 98fa998a37b01ad64e556b229912932f4d1cfc75
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884626"
---
# <a name="connector-resource-type"></a><span data-ttu-id="5c341-103">tipo de recurso de conector</span><span class="sxs-lookup"><span data-stu-id="5c341-103">connector resource type</span></span>

> <span data-ttu-id="5c341-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5c341-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5c341-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5c341-105">Use of these APIs in production applications is not supported.</span></span>

<!-- Not supported items
|[Create connectorGroup](../api/connector-post-memberof.md) |[connectorGroup](connectorgroup.md)| Associate a connector with a new connectorGroup by posting to the memberOf collection.|
|[Update](../api/connector-update.md) | [connector](connector.md)   | Connectors are created when they are registed with the tenant. |
|[Delete](../api/connector-delete.md) | None |Delete connector object. |

-->

## <a name="methods"></a><span data-ttu-id="5c341-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="5c341-106">Methods</span></span>

| <span data-ttu-id="5c341-107">Método</span><span class="sxs-lookup"><span data-stu-id="5c341-107">Method</span></span>           | <span data-ttu-id="5c341-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c341-108">Return Type</span></span>    |<span data-ttu-id="5c341-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c341-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="5c341-110">Obtener el conector</span><span class="sxs-lookup"><span data-stu-id="5c341-110">Get connector</span></span>](../api/connector-get.md) | [<span data-ttu-id="5c341-111">conector</span><span class="sxs-lookup"><span data-stu-id="5c341-111">connector</span></span>](connector.md) |<span data-ttu-id="5c341-112">Leer las propiedades y las relaciones del objeto de conector.</span><span class="sxs-lookup"><span data-stu-id="5c341-112">Read properties and relationships of connector object.</span></span>|
|[<span data-ttu-id="5c341-113">Enumerar memberOf</span><span class="sxs-lookup"><span data-stu-id="5c341-113">List memberOf</span></span>](../api/connector-list-memberof.md) |<span data-ttu-id="5c341-114">colección de [connectorGroup](connectorgroup.md)</span><span class="sxs-lookup"><span data-stu-id="5c341-114">[connectorGroup](connectorgroup.md) collection</span></span>| <span data-ttu-id="5c341-115">Obtenga el objeto connectorGroup asociado con el conector.</span><span class="sxs-lookup"><span data-stu-id="5c341-115">Get the connectorGroup object associated with the connector.</span></span>|

## <a name="properties"></a><span data-ttu-id="5c341-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c341-116">Properties</span></span>
| <span data-ttu-id="5c341-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5c341-117">Property</span></span>     | <span data-ttu-id="5c341-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c341-118">Type</span></span>   |<span data-ttu-id="5c341-119">Description</span><span class="sxs-lookup"><span data-stu-id="5c341-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5c341-120">externalIp</span><span class="sxs-lookup"><span data-stu-id="5c341-120">externalIp</span></span>|<span data-ttu-id="5c341-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c341-121">String</span></span>|<span data-ttu-id="5c341-122">La dirección IP externa como detectados por el servicio para la máquina de conector.</span><span class="sxs-lookup"><span data-stu-id="5c341-122">The external IP address as detected by the service for the connector machine.</span></span> <span data-ttu-id="5c341-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c341-123">Read-only</span></span>|
|<span data-ttu-id="5c341-124">id</span><span class="sxs-lookup"><span data-stu-id="5c341-124">id</span></span>|<span data-ttu-id="5c341-125">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c341-125">String</span></span>| <span data-ttu-id="5c341-126">El identificador del objeto del conector.</span><span class="sxs-lookup"><span data-stu-id="5c341-126">The object id of the connector.</span></span> <BR><span data-ttu-id="5c341-127">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c341-127">Read-only.</span></span>|
|<span data-ttu-id="5c341-128">nombreEquipo</span><span class="sxs-lookup"><span data-stu-id="5c341-128">machineName</span></span>|<span data-ttu-id="5c341-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="5c341-129">String</span></span>| <span data-ttu-id="5c341-130">El nombre de la máquina que se está ejecutando el conector.</span><span class="sxs-lookup"><span data-stu-id="5c341-130">The name of the machine that the connector is running on.</span></span> <BR><span data-ttu-id="5c341-131">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c341-131">Read-only</span></span>|
|<span data-ttu-id="5c341-132">status</span><span class="sxs-lookup"><span data-stu-id="5c341-132">status</span></span>|<span data-ttu-id="5c341-133">string</span><span class="sxs-lookup"><span data-stu-id="5c341-133">string</span></span>| <span data-ttu-id="5c341-134">Indica el estado del conector.</span><span class="sxs-lookup"><span data-stu-id="5c341-134">Indicates the status of the connector.</span></span> <span data-ttu-id="5c341-135">Los valores posibles son: `active` y `inactive`.</span><span class="sxs-lookup"><span data-stu-id="5c341-135">Possible values are: `active`, `inactive`.</span></span> <span data-ttu-id="5c341-136">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c341-136">Read-only</span></span> |

## <a name="relationships"></a><span data-ttu-id="5c341-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5c341-137">Relationships</span></span>
| <span data-ttu-id="5c341-138">Relación</span><span class="sxs-lookup"><span data-stu-id="5c341-138">Relationship</span></span> | <span data-ttu-id="5c341-139">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c341-139">Type</span></span>   |<span data-ttu-id="5c341-140">Description</span><span class="sxs-lookup"><span data-stu-id="5c341-140">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5c341-141">memberOf</span><span class="sxs-lookup"><span data-stu-id="5c341-141">memberOf</span></span>|<span data-ttu-id="5c341-142">colección de [connectorGroup](connectorgroup.md)</span><span class="sxs-lookup"><span data-stu-id="5c341-142">[connectorGroup](connectorgroup.md) collection</span></span>| <span data-ttu-id="5c341-143">El connectorGroup que la conexión es un miembro de.</span><span class="sxs-lookup"><span data-stu-id="5c341-143">The connectorGroup that the connect is a member of.</span></span><br><span data-ttu-id="5c341-144">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5c341-144">Read-only.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="5c341-145">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5c341-145">JSON representation</span></span>

<span data-ttu-id="5c341-146">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5c341-146">Here is a JSON representation of the resource.</span></span>

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
