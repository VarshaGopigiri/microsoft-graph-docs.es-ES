---
title: Tipo de recurso subscribedSku
description: Contiene información acerca de una SKU de servicio a la que la empresa está suscrita.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: e9e61fba199d6d3e509700fe61e75bde240c7f16
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27937442"
---
# <a name="subscribedsku-resource-type"></a><span data-ttu-id="b3f6c-103">Tipo de recurso subscribedSku</span><span class="sxs-lookup"><span data-stu-id="b3f6c-103">subscribedSku resource type</span></span>

<span data-ttu-id="b3f6c-104">Contiene información acerca de una SKU de servicio a la que la empresa está suscrita.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-104">Contains information about a service SKU that a company is subscribed to.</span></span>

<span data-ttu-id="b3f6c-p101">Solo se admite la operación de lectura con las SKU suscritas; no se admiten las operaciones de creación, actualización y eliminación. No se admiten expresiones de filtro de consulta. Se hereda de [DirectoryObject](directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="b3f6c-p101">Only the read operation is supported on subscribed SKUs; create, update, and delete are not supported. Query filter expressions are not supported. Inherits from [directoryObject](directoryobject.md).</span></span>

## <a name="methods"></a><span data-ttu-id="b3f6c-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="b3f6c-108">Methods</span></span>
| <span data-ttu-id="b3f6c-109">Método</span><span class="sxs-lookup"><span data-stu-id="b3f6c-109">Method</span></span>           | <span data-ttu-id="b3f6c-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3f6c-110">Return Type</span></span>    |<span data-ttu-id="b3f6c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3f6c-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="b3f6c-112">Get subscribedSku</span><span class="sxs-lookup"><span data-stu-id="b3f6c-112">Get subscribedSku</span></span>](../api/subscribedsku-get.md) | [<span data-ttu-id="b3f6c-113">subscribedSku</span><span class="sxs-lookup"><span data-stu-id="b3f6c-113">subscribedSku</span></span>](subscribedsku.md) |<span data-ttu-id="b3f6c-114">Lea las propiedades y relaciones del objeto subscribedSku.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-114">Read properties and relationships of subscribedSku object.</span></span>|
|[<span data-ttu-id="b3f6c-115">Lista subscribedsku</span><span class="sxs-lookup"><span data-stu-id="b3f6c-115">List subscribedsku</span></span>](../api/subscribedsku-list.md) | <span data-ttu-id="b3f6c-116">Colección [subscribedSku](subscribedsku.md)</span><span class="sxs-lookup"><span data-stu-id="b3f6c-116">[subscribedSku](subscribedsku.md) collection</span></span> |<span data-ttu-id="b3f6c-117">Recupere la lista de suscripciones comerciales que ha adquirido una organización.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-117">Retrieve the list of commercial subscriptions that an organization has acquired.</span></span>|

## <a name="properties"></a><span data-ttu-id="b3f6c-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b3f6c-118">Properties</span></span>
| <span data-ttu-id="b3f6c-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b3f6c-119">Property</span></span>     | <span data-ttu-id="b3f6c-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3f6c-120">Type</span></span>   |<span data-ttu-id="b3f6c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3f6c-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b3f6c-122">appliesTo</span><span class="sxs-lookup"><span data-stu-id="b3f6c-122">appliesTo</span></span>|<span data-ttu-id="b3f6c-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="b3f6c-123">String</span></span>| <span data-ttu-id="b3f6c-124">Por ejemplo, "usuario" o "empresa".</span><span class="sxs-lookup"><span data-stu-id="b3f6c-124">For example, "User" or "Company".</span></span> |
|<span data-ttu-id="b3f6c-125">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="b3f6c-125">capabilityStatus</span></span>|<span data-ttu-id="b3f6c-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="b3f6c-126">String</span></span>| <span data-ttu-id="b3f6c-127">Por ejemplo, "habilitado".</span><span class="sxs-lookup"><span data-stu-id="b3f6c-127">For example, "Enabled".</span></span> |
|<span data-ttu-id="b3f6c-128">consumedUnits</span><span class="sxs-lookup"><span data-stu-id="b3f6c-128">consumedUnits</span></span>|<span data-ttu-id="b3f6c-129">Int32</span><span class="sxs-lookup"><span data-stu-id="b3f6c-129">Int32</span></span>| <span data-ttu-id="b3f6c-130">El número de licencias asignadas.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-130">The number of licenses that have been assigned.</span></span> |
|<span data-ttu-id="b3f6c-131">id</span><span class="sxs-lookup"><span data-stu-id="b3f6c-131">id</span></span>|<span data-ttu-id="b3f6c-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="b3f6c-132">String</span></span>| <span data-ttu-id="b3f6c-p102">El identificador único del recurso del objeto sku suscrito. Clave, no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-p102">The unique identifier for the subscribed sku object. Key, not nullable.</span></span> |
|<span data-ttu-id="b3f6c-135">prepaidUnits</span><span class="sxs-lookup"><span data-stu-id="b3f6c-135">prepaidUnits</span></span>|[<span data-ttu-id="b3f6c-136">licenseUnitsDetail</span><span class="sxs-lookup"><span data-stu-id="b3f6c-136">licenseUnitsDetail</span></span>](licenseunitsdetail.md)| <span data-ttu-id="b3f6c-137">Información sobre el número y el estado de las licencias prepagadas.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-137">Information about the number and status of prepaid licenses.</span></span> |
|<span data-ttu-id="b3f6c-138">servicePlans</span><span class="sxs-lookup"><span data-stu-id="b3f6c-138">servicePlans</span></span>|<span data-ttu-id="b3f6c-139">Colección [servicePlanInfo](serviceplaninfo.md)</span><span class="sxs-lookup"><span data-stu-id="b3f6c-139">[servicePlanInfo](serviceplaninfo.md) collection</span></span>| <span data-ttu-id="b3f6c-p103">Información acerca de los planes de servicio que están disponibles con el SKU. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="b3f6c-p103">Information about the service plans that are available with the SKU. Not nullable</span></span> |
|<span data-ttu-id="b3f6c-142">skuId</span><span class="sxs-lookup"><span data-stu-id="b3f6c-142">skuId</span></span>|<span data-ttu-id="b3f6c-143">Guid</span><span class="sxs-lookup"><span data-stu-id="b3f6c-143">Guid</span></span>| <span data-ttu-id="b3f6c-144">El identificador único (GUID) para el SKU de servicio.</span><span class="sxs-lookup"><span data-stu-id="b3f6c-144">The unique identifier (GUID) for the service SKU.</span></span> |
|<span data-ttu-id="b3f6c-145">skuPartNumber</span><span class="sxs-lookup"><span data-stu-id="b3f6c-145">skuPartNumber</span></span>|<span data-ttu-id="b3f6c-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="b3f6c-146">String</span></span>| <span data-ttu-id="b3f6c-147">La parte numérica del SKU, por ejemplo: "AAD_PREMIUM" o "RMSBASIC".</span><span class="sxs-lookup"><span data-stu-id="b3f6c-147">The SKU part number; for example: "AAD_PREMIUM" or "RMSBASIC".</span></span> |

## <a name="relationships"></a><span data-ttu-id="b3f6c-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b3f6c-148">Relationships</span></span>
<span data-ttu-id="b3f6c-149">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b3f6c-149">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="b3f6c-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b3f6c-150">JSON representation</span></span>

<span data-ttu-id="b3f6c-151">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b3f6c-151">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.subscribedSku",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "toppable": false,
        "countable": false,
        "expandable": false,
        "filterable": false,
        "referenceable": false,
        "selectable": false
      }
    }
  ]
}-->

```json
{
  "appliesTo": "string",
  "capabilityStatus": "string",
  "consumedUnits": 1024,
  "id": "string (identifier)",
  "prepaidUnits": {"@odata.type": "microsoft.graph.licenseUnitsDetail"},
  "servicePlans": [{"@odata.type": "microsoft.graph.servicePlanInfo"}],
  "skuId": "guid",
  "skuPartNumber": "string"
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscribedSku resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
