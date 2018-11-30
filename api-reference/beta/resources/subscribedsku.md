---
title: Tipo de recurso subscribedSku
description: " crear, update y delete no son compatibles. No se admiten expresiones de filtro de consulta. Se hereda de directoryObject."
ms.openlocfilehash: ab9b64d8de67379aa002ffeec78edd327b15b222
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089769"
---
# <a name="subscribedsku-resource-type"></a><span data-ttu-id="df1ed-105">Tipo de recurso subscribedSku</span><span class="sxs-lookup"><span data-stu-id="df1ed-105">subscribedSku resource type</span></span>

> <span data-ttu-id="df1ed-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="df1ed-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="df1ed-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="df1ed-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="df1ed-p103">Solo se admite la operación de lectura con las SKU suscritas; no se admiten las operaciones de creación, actualización y eliminación. No se admiten expresiones de filtro de consulta. Se hereda de [DirectoryObject](directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="df1ed-p103">Only the read operation is supported on subscribed SKUs; create, update, and delete are not supported. Query filter expressions are not supported. Inherits from [directoryObject](directoryobject.md).</span></span>


## <a name="methods"></a><span data-ttu-id="df1ed-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="df1ed-111">Methods</span></span>
| <span data-ttu-id="df1ed-112">Método</span><span class="sxs-lookup"><span data-stu-id="df1ed-112">Method</span></span>           | <span data-ttu-id="df1ed-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="df1ed-113">Return Type</span></span>    |<span data-ttu-id="df1ed-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="df1ed-114">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="df1ed-115">Get subscribedSku</span><span class="sxs-lookup"><span data-stu-id="df1ed-115">Get subscribedSku</span></span>](../api/subscribedsku-get.md) | [<span data-ttu-id="df1ed-116">subscribedSku</span><span class="sxs-lookup"><span data-stu-id="df1ed-116">subscribedSku</span></span>](subscribedsku.md) |<span data-ttu-id="df1ed-117">Lea las propiedades y relaciones del objeto subscribedSku.</span><span class="sxs-lookup"><span data-stu-id="df1ed-117">Read properties and relationships of subscribedSku object.</span></span>|
|[<span data-ttu-id="df1ed-118">Lista subscribedsku</span><span class="sxs-lookup"><span data-stu-id="df1ed-118">List subscribedsku</span></span>](../api/subscribedsku-list.md) | <span data-ttu-id="df1ed-119">Colección [subscribedSku](subscribedsku.md)</span><span class="sxs-lookup"><span data-stu-id="df1ed-119">[subscribedSku](subscribedsku.md) collection</span></span> |<span data-ttu-id="df1ed-120">Recupere la lista de suscripciones comerciales que ha adquirido una organización.</span><span class="sxs-lookup"><span data-stu-id="df1ed-120">Retrieve the list of commercial subscriptions that an organization has acquired.</span></span>|

## <a name="properties"></a><span data-ttu-id="df1ed-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="df1ed-121">Properties</span></span>
| <span data-ttu-id="df1ed-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="df1ed-122">Property</span></span>     | <span data-ttu-id="df1ed-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="df1ed-123">Type</span></span>   |<span data-ttu-id="df1ed-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="df1ed-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="df1ed-125">appliesTo</span><span class="sxs-lookup"><span data-stu-id="df1ed-125">appliesTo</span></span>|<span data-ttu-id="df1ed-126">String</span><span class="sxs-lookup"><span data-stu-id="df1ed-126">String</span></span>| <span data-ttu-id="df1ed-127">Por ejemplo, "usuario" o "empresa".</span><span class="sxs-lookup"><span data-stu-id="df1ed-127">For example, "User" or "Company".</span></span> |
|<span data-ttu-id="df1ed-128">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="df1ed-128">capabilityStatus</span></span>|<span data-ttu-id="df1ed-129">String</span><span class="sxs-lookup"><span data-stu-id="df1ed-129">String</span></span>| <span data-ttu-id="df1ed-130">Por ejemplo, "habilitado".</span><span class="sxs-lookup"><span data-stu-id="df1ed-130">For example, "Enabled".</span></span> |
|<span data-ttu-id="df1ed-131">consumedUnits</span><span class="sxs-lookup"><span data-stu-id="df1ed-131">consumedUnits</span></span>|<span data-ttu-id="df1ed-132">Int32</span><span class="sxs-lookup"><span data-stu-id="df1ed-132">Int32</span></span>| <span data-ttu-id="df1ed-133">El número de licencias asignadas.</span><span class="sxs-lookup"><span data-stu-id="df1ed-133">The number of licenses that have been assigned.</span></span> |
|<span data-ttu-id="df1ed-134">id</span><span class="sxs-lookup"><span data-stu-id="df1ed-134">id</span></span>|<span data-ttu-id="df1ed-135">String</span><span class="sxs-lookup"><span data-stu-id="df1ed-135">String</span></span>| <span data-ttu-id="df1ed-p104">El identificador único del recurso del objeto sku suscrito. Clave, no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="df1ed-p104">The unique identifier for the subscribed sku object. Key, not nullable.</span></span> |
|<span data-ttu-id="df1ed-138">prepaidUnits</span><span class="sxs-lookup"><span data-stu-id="df1ed-138">prepaidUnits</span></span>|[<span data-ttu-id="df1ed-139">licenseUnitsDetail</span><span class="sxs-lookup"><span data-stu-id="df1ed-139">licenseUnitsDetail</span></span>](licenseunitsdetail.md)| <span data-ttu-id="df1ed-140">Información sobre el número y el estado de las licencias prepagadas.</span><span class="sxs-lookup"><span data-stu-id="df1ed-140">Information about the number and status of prepaid licenses.</span></span> |
|<span data-ttu-id="df1ed-141">servicePlans</span><span class="sxs-lookup"><span data-stu-id="df1ed-141">servicePlans</span></span>|<span data-ttu-id="df1ed-142">Colección [servicePlanInfo](serviceplaninfo.md)</span><span class="sxs-lookup"><span data-stu-id="df1ed-142">[servicePlanInfo](serviceplaninfo.md) collection</span></span>| <span data-ttu-id="df1ed-p105">Información acerca de los planes de servicio que están disponibles con el SKU. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="df1ed-p105">Information about the service plans that are available with the SKU. Not nullable</span></span> |
|<span data-ttu-id="df1ed-145">skuId</span><span class="sxs-lookup"><span data-stu-id="df1ed-145">skuId</span></span>|<span data-ttu-id="df1ed-146">Guid</span><span class="sxs-lookup"><span data-stu-id="df1ed-146">Guid</span></span>| <span data-ttu-id="df1ed-147">El identificador único (GUID) para el SKU de servicio.</span><span class="sxs-lookup"><span data-stu-id="df1ed-147">The unique identifier (GUID) for the service SKU.</span></span> |
|<span data-ttu-id="df1ed-148">skuPartNumber</span><span class="sxs-lookup"><span data-stu-id="df1ed-148">skuPartNumber</span></span>|<span data-ttu-id="df1ed-149">String</span><span class="sxs-lookup"><span data-stu-id="df1ed-149">String</span></span>| <span data-ttu-id="df1ed-150">La parte numérica del SKU, por ejemplo: "AAD_PREMIUM" o "RMSBASIC".</span><span class="sxs-lookup"><span data-stu-id="df1ed-150">The SKU part number; for example: "AAD_PREMIUM" or "RMSBASIC".</span></span> |

## <a name="relationships"></a><span data-ttu-id="df1ed-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="df1ed-151">Relationships</span></span>
<span data-ttu-id="df1ed-152">Ninguno</span><span class="sxs-lookup"><span data-stu-id="df1ed-152">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="df1ed-153">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="df1ed-153">JSON representation</span></span>

<span data-ttu-id="df1ed-154">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="df1ed-154">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.subscribedSku"
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
