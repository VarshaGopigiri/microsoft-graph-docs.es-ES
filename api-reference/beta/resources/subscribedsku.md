---
title: Tipo de recurso subscribedSku
description: " crear, update y delete no son compatibles. No se admiten expresiones de filtro de consulta. Se hereda de directoryObject."
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 01dbbf8727ab361b3763e2343e7cc72a3676848b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27960157"
---
# <a name="subscribedsku-resource-type"></a><span data-ttu-id="8c85d-105">Tipo de recurso subscribedSku</span><span class="sxs-lookup"><span data-stu-id="8c85d-105">subscribedSku resource type</span></span>

> <span data-ttu-id="8c85d-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8c85d-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8c85d-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8c85d-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8c85d-p103">Solo se admite la operación de lectura con las SKU suscritas; no se admiten las operaciones de creación, actualización y eliminación. No se admiten expresiones de filtro de consulta. Se hereda de [DirectoryObject](directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="8c85d-p103">Only the read operation is supported on subscribed SKUs; create, update, and delete are not supported. Query filter expressions are not supported. Inherits from [directoryObject](directoryobject.md).</span></span>


## <a name="methods"></a><span data-ttu-id="8c85d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="8c85d-111">Methods</span></span>
| <span data-ttu-id="8c85d-112">Método</span><span class="sxs-lookup"><span data-stu-id="8c85d-112">Method</span></span>           | <span data-ttu-id="8c85d-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c85d-113">Return Type</span></span>    |<span data-ttu-id="8c85d-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c85d-114">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="8c85d-115">Get subscribedSku</span><span class="sxs-lookup"><span data-stu-id="8c85d-115">Get subscribedSku</span></span>](../api/subscribedsku-get.md) | [<span data-ttu-id="8c85d-116">subscribedSku</span><span class="sxs-lookup"><span data-stu-id="8c85d-116">subscribedSku</span></span>](subscribedsku.md) |<span data-ttu-id="8c85d-117">Lea las propiedades y relaciones del objeto subscribedSku.</span><span class="sxs-lookup"><span data-stu-id="8c85d-117">Read properties and relationships of subscribedSku object.</span></span>|
|[<span data-ttu-id="8c85d-118">Lista subscribedsku</span><span class="sxs-lookup"><span data-stu-id="8c85d-118">List subscribedsku</span></span>](../api/subscribedsku-list.md) | <span data-ttu-id="8c85d-119">Colección [subscribedSku](subscribedsku.md)</span><span class="sxs-lookup"><span data-stu-id="8c85d-119">[subscribedSku](subscribedsku.md) collection</span></span> |<span data-ttu-id="8c85d-120">Recupere la lista de suscripciones comerciales que ha adquirido una organización.</span><span class="sxs-lookup"><span data-stu-id="8c85d-120">Retrieve the list of commercial subscriptions that an organization has acquired.</span></span>|

## <a name="properties"></a><span data-ttu-id="8c85d-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8c85d-121">Properties</span></span>
| <span data-ttu-id="8c85d-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8c85d-122">Property</span></span>     | <span data-ttu-id="8c85d-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c85d-123">Type</span></span>   |<span data-ttu-id="8c85d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c85d-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8c85d-125">appliesTo</span><span class="sxs-lookup"><span data-stu-id="8c85d-125">appliesTo</span></span>|<span data-ttu-id="8c85d-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="8c85d-126">String</span></span>| <span data-ttu-id="8c85d-127">Por ejemplo, "usuario" o "empresa".</span><span class="sxs-lookup"><span data-stu-id="8c85d-127">For example, "User" or "Company".</span></span> |
|<span data-ttu-id="8c85d-128">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="8c85d-128">capabilityStatus</span></span>|<span data-ttu-id="8c85d-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="8c85d-129">String</span></span>| <span data-ttu-id="8c85d-130">Por ejemplo, "habilitado".</span><span class="sxs-lookup"><span data-stu-id="8c85d-130">For example, "Enabled".</span></span> |
|<span data-ttu-id="8c85d-131">consumedUnits</span><span class="sxs-lookup"><span data-stu-id="8c85d-131">consumedUnits</span></span>|<span data-ttu-id="8c85d-132">Int32</span><span class="sxs-lookup"><span data-stu-id="8c85d-132">Int32</span></span>| <span data-ttu-id="8c85d-133">El número de licencias asignadas.</span><span class="sxs-lookup"><span data-stu-id="8c85d-133">The number of licenses that have been assigned.</span></span> |
|<span data-ttu-id="8c85d-134">id</span><span class="sxs-lookup"><span data-stu-id="8c85d-134">id</span></span>|<span data-ttu-id="8c85d-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="8c85d-135">String</span></span>| <span data-ttu-id="8c85d-p104">El identificador único del recurso del objeto sku suscrito. Clave, no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="8c85d-p104">The unique identifier for the subscribed sku object. Key, not nullable.</span></span> |
|<span data-ttu-id="8c85d-138">prepaidUnits</span><span class="sxs-lookup"><span data-stu-id="8c85d-138">prepaidUnits</span></span>|[<span data-ttu-id="8c85d-139">licenseUnitsDetail</span><span class="sxs-lookup"><span data-stu-id="8c85d-139">licenseUnitsDetail</span></span>](licenseunitsdetail.md)| <span data-ttu-id="8c85d-140">Información sobre el número y el estado de las licencias prepagadas.</span><span class="sxs-lookup"><span data-stu-id="8c85d-140">Information about the number and status of prepaid licenses.</span></span> |
|<span data-ttu-id="8c85d-141">servicePlans</span><span class="sxs-lookup"><span data-stu-id="8c85d-141">servicePlans</span></span>|<span data-ttu-id="8c85d-142">Colección [servicePlanInfo](serviceplaninfo.md)</span><span class="sxs-lookup"><span data-stu-id="8c85d-142">[servicePlanInfo](serviceplaninfo.md) collection</span></span>| <span data-ttu-id="8c85d-p105">Información acerca de los planes de servicio que están disponibles con el SKU. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="8c85d-p105">Information about the service plans that are available with the SKU. Not nullable</span></span> |
|<span data-ttu-id="8c85d-145">skuId</span><span class="sxs-lookup"><span data-stu-id="8c85d-145">skuId</span></span>|<span data-ttu-id="8c85d-146">Guid</span><span class="sxs-lookup"><span data-stu-id="8c85d-146">Guid</span></span>| <span data-ttu-id="8c85d-147">El identificador único (GUID) para el SKU de servicio.</span><span class="sxs-lookup"><span data-stu-id="8c85d-147">The unique identifier (GUID) for the service SKU.</span></span> |
|<span data-ttu-id="8c85d-148">skuPartNumber</span><span class="sxs-lookup"><span data-stu-id="8c85d-148">skuPartNumber</span></span>|<span data-ttu-id="8c85d-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="8c85d-149">String</span></span>| <span data-ttu-id="8c85d-150">La parte numérica del SKU, por ejemplo: "AAD_PREMIUM" o "RMSBASIC".</span><span class="sxs-lookup"><span data-stu-id="8c85d-150">The SKU part number; for example: "AAD_PREMIUM" or "RMSBASIC".</span></span> |

## <a name="relationships"></a><span data-ttu-id="8c85d-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8c85d-151">Relationships</span></span>
<span data-ttu-id="8c85d-152">Ninguno</span><span class="sxs-lookup"><span data-stu-id="8c85d-152">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="8c85d-153">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8c85d-153">JSON representation</span></span>

<span data-ttu-id="8c85d-154">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8c85d-154">Here is a JSON representation of the resource</span></span>

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
