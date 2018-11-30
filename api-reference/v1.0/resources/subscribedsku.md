---
title: Tipo de recurso subscribedSku
description: Contiene información acerca de una SKU de servicio a la que la empresa está suscrita.
ms.openlocfilehash: 5a3c3515d4d902810db32acf10b4cee6a889bfc9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031422"
---
# <a name="subscribedsku-resource-type"></a><span data-ttu-id="79b9a-103">Tipo de recurso subscribedSku</span><span class="sxs-lookup"><span data-stu-id="79b9a-103">subscribedSku resource type</span></span>

<span data-ttu-id="79b9a-104">Contiene información acerca de una SKU de servicio a la que la empresa está suscrita.</span><span class="sxs-lookup"><span data-stu-id="79b9a-104">Contains information about a service SKU that a company is subscribed to.</span></span>

<span data-ttu-id="79b9a-p101">Solo se admite la operación de lectura con las SKU suscritas; no se admiten las operaciones de creación, actualización y eliminación. No se admiten expresiones de filtro de consulta. Se hereda de [DirectoryObject](directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="79b9a-p101">Only the read operation is supported on subscribed SKUs; create, update, and delete are not supported. Query filter expressions are not supported. Inherits from [directoryObject](directoryobject.md).</span></span>

## <a name="methods"></a><span data-ttu-id="79b9a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="79b9a-108">Methods</span></span>
| <span data-ttu-id="79b9a-109">Método</span><span class="sxs-lookup"><span data-stu-id="79b9a-109">Method</span></span>           | <span data-ttu-id="79b9a-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79b9a-110">Return Type</span></span>    |<span data-ttu-id="79b9a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="79b9a-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="79b9a-112">Get subscribedSku</span><span class="sxs-lookup"><span data-stu-id="79b9a-112">Get subscribedSku</span></span>](../api/subscribedsku-get.md) | [<span data-ttu-id="79b9a-113">subscribedSku</span><span class="sxs-lookup"><span data-stu-id="79b9a-113">subscribedSku</span></span>](subscribedsku.md) |<span data-ttu-id="79b9a-114">Lea las propiedades y relaciones del objeto subscribedSku.</span><span class="sxs-lookup"><span data-stu-id="79b9a-114">Read properties and relationships of subscribedSku object.</span></span>|
|[<span data-ttu-id="79b9a-115">Lista subscribedsku</span><span class="sxs-lookup"><span data-stu-id="79b9a-115">List subscribedsku</span></span>](../api/subscribedsku-list.md) | <span data-ttu-id="79b9a-116">Colección [subscribedSku](subscribedsku.md)</span><span class="sxs-lookup"><span data-stu-id="79b9a-116">[subscribedSku](subscribedsku.md) collection</span></span> |<span data-ttu-id="79b9a-117">Recupere la lista de suscripciones comerciales que ha adquirido una organización.</span><span class="sxs-lookup"><span data-stu-id="79b9a-117">Retrieve the list of commercial subscriptions that an organization has acquired.</span></span>|

## <a name="properties"></a><span data-ttu-id="79b9a-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79b9a-118">Properties</span></span>
| <span data-ttu-id="79b9a-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="79b9a-119">Property</span></span>     | <span data-ttu-id="79b9a-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="79b9a-120">Type</span></span>   |<span data-ttu-id="79b9a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="79b9a-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="79b9a-122">appliesTo</span><span class="sxs-lookup"><span data-stu-id="79b9a-122">appliesTo</span></span>|<span data-ttu-id="79b9a-123">String</span><span class="sxs-lookup"><span data-stu-id="79b9a-123">String</span></span>| <span data-ttu-id="79b9a-124">Por ejemplo, "usuario" o "empresa".</span><span class="sxs-lookup"><span data-stu-id="79b9a-124">For example, "User" or "Company".</span></span> |
|<span data-ttu-id="79b9a-125">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="79b9a-125">capabilityStatus</span></span>|<span data-ttu-id="79b9a-126">String</span><span class="sxs-lookup"><span data-stu-id="79b9a-126">String</span></span>| <span data-ttu-id="79b9a-127">Por ejemplo, "habilitado".</span><span class="sxs-lookup"><span data-stu-id="79b9a-127">For example, "Enabled".</span></span> |
|<span data-ttu-id="79b9a-128">consumedUnits</span><span class="sxs-lookup"><span data-stu-id="79b9a-128">consumedUnits</span></span>|<span data-ttu-id="79b9a-129">Int32</span><span class="sxs-lookup"><span data-stu-id="79b9a-129">Int32</span></span>| <span data-ttu-id="79b9a-130">El número de licencias asignadas.</span><span class="sxs-lookup"><span data-stu-id="79b9a-130">The number of licenses that have been assigned.</span></span> |
|<span data-ttu-id="79b9a-131">id</span><span class="sxs-lookup"><span data-stu-id="79b9a-131">id</span></span>|<span data-ttu-id="79b9a-132">String</span><span class="sxs-lookup"><span data-stu-id="79b9a-132">String</span></span>| <span data-ttu-id="79b9a-p102">El identificador único del recurso del objeto sku suscrito. Clave, no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="79b9a-p102">The unique identifier for the subscribed sku object. Key, not nullable.</span></span> |
|<span data-ttu-id="79b9a-135">prepaidUnits</span><span class="sxs-lookup"><span data-stu-id="79b9a-135">prepaidUnits</span></span>|[<span data-ttu-id="79b9a-136">licenseUnitsDetail</span><span class="sxs-lookup"><span data-stu-id="79b9a-136">licenseUnitsDetail</span></span>](licenseunitsdetail.md)| <span data-ttu-id="79b9a-137">Información sobre el número y el estado de las licencias prepagadas.</span><span class="sxs-lookup"><span data-stu-id="79b9a-137">Information about the number and status of prepaid licenses.</span></span> |
|<span data-ttu-id="79b9a-138">servicePlans</span><span class="sxs-lookup"><span data-stu-id="79b9a-138">servicePlans</span></span>|<span data-ttu-id="79b9a-139">Colección [servicePlanInfo](serviceplaninfo.md)</span><span class="sxs-lookup"><span data-stu-id="79b9a-139">[servicePlanInfo](serviceplaninfo.md) collection</span></span>| <span data-ttu-id="79b9a-p103">Información acerca de los planes de servicio que están disponibles con el SKU. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="79b9a-p103">Information about the service plans that are available with the SKU. Not nullable</span></span> |
|<span data-ttu-id="79b9a-142">skuId</span><span class="sxs-lookup"><span data-stu-id="79b9a-142">skuId</span></span>|<span data-ttu-id="79b9a-143">Guid</span><span class="sxs-lookup"><span data-stu-id="79b9a-143">Guid</span></span>| <span data-ttu-id="79b9a-144">El identificador único (GUID) para el SKU de servicio.</span><span class="sxs-lookup"><span data-stu-id="79b9a-144">The unique identifier (GUID) for the service SKU.</span></span> |
|<span data-ttu-id="79b9a-145">skuPartNumber</span><span class="sxs-lookup"><span data-stu-id="79b9a-145">skuPartNumber</span></span>|<span data-ttu-id="79b9a-146">String</span><span class="sxs-lookup"><span data-stu-id="79b9a-146">String</span></span>| <span data-ttu-id="79b9a-147">La parte numérica del SKU, por ejemplo: "AAD_PREMIUM" o "RMSBASIC".</span><span class="sxs-lookup"><span data-stu-id="79b9a-147">The SKU part number; for example: "AAD_PREMIUM" or "RMSBASIC".</span></span> |

## <a name="relationships"></a><span data-ttu-id="79b9a-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="79b9a-148">Relationships</span></span>
<span data-ttu-id="79b9a-149">Ninguno</span><span class="sxs-lookup"><span data-stu-id="79b9a-149">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="79b9a-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="79b9a-150">JSON representation</span></span>

<span data-ttu-id="79b9a-151">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="79b9a-151">Here is a JSON representation of the resource</span></span>

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
