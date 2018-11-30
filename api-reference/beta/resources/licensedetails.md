---
title: Tipo de recurso licenseDetails
description: Contiene información sobre una licencia asignada a un usuario.
ms.openlocfilehash: dd56026d2c1d230fe6bb25b78ff8ababa01f577b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090729"
---
# <a name="licensedetails-resource-type"></a><span data-ttu-id="5eec7-103">Tipo de recurso licenseDetails</span><span class="sxs-lookup"><span data-stu-id="5eec7-103">licenseDetails resource type</span></span>

> <span data-ttu-id="5eec7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5eec7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5eec7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5eec7-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5eec7-106">Contiene información sobre una licencia asignada a un usuario.</span><span class="sxs-lookup"><span data-stu-id="5eec7-106">Contains information about a license assigned to a user.</span></span>

## <a name="methods"></a><span data-ttu-id="5eec7-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="5eec7-107">Methods</span></span>

| <span data-ttu-id="5eec7-108">Método</span><span class="sxs-lookup"><span data-stu-id="5eec7-108">Method</span></span>           | <span data-ttu-id="5eec7-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5eec7-109">Return Type</span></span>    |<span data-ttu-id="5eec7-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5eec7-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="5eec7-111">Enumerar licenseDetails</span><span class="sxs-lookup"><span data-stu-id="5eec7-111">List licenseDetails</span></span>](../api/user-list-licensedetails.md) | <span data-ttu-id="5eec7-112">Colección licenseDetails</span><span class="sxs-lookup"><span data-stu-id="5eec7-112">licenseDetails collection</span></span> |<span data-ttu-id="5eec7-113">Recupere una lista de objetos licenseDetails para un usuario.</span><span class="sxs-lookup"><span data-stu-id="5eec7-113">Retrieve a list of licenseDetails objects for a user.</span></span>|

<!--|[Get licenseDetails](../api/licensedetails-get.md) | licenseDetails |Read properties and relationships of a licenseDetails object.|-->

## <a name="properties"></a><span data-ttu-id="5eec7-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5eec7-114">Properties</span></span>
| <span data-ttu-id="5eec7-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5eec7-115">Property</span></span>     | <span data-ttu-id="5eec7-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="5eec7-116">Type</span></span>   |<span data-ttu-id="5eec7-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="5eec7-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5eec7-118">id</span><span class="sxs-lookup"><span data-stu-id="5eec7-118">id</span></span>|<span data-ttu-id="5eec7-119">String</span><span class="sxs-lookup"><span data-stu-id="5eec7-119">String</span></span>| <span data-ttu-id="5eec7-p102">Identificador único del objeto licenseDetails. Solo lectura, no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="5eec7-p102">The unique identifier for the license detail object. Read-only, Key, Not nullable</span></span> |
|<span data-ttu-id="5eec7-122">servicePlans</span><span class="sxs-lookup"><span data-stu-id="5eec7-122">servicePlans</span></span>|<span data-ttu-id="5eec7-123">Colección [servicePlanInfo](serviceplaninfo.md)</span><span class="sxs-lookup"><span data-stu-id="5eec7-123">[servicePlanInfo](serviceplaninfo.md) collection</span></span>| <span data-ttu-id="5eec7-p103">Información sobre los planes de servicio asignados a la licencia. Solo lectura, no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="5eec7-p103">Information about the service plans assigned with the license. Read-only, Not nullable</span></span> |
|<span data-ttu-id="5eec7-126">skuId</span><span class="sxs-lookup"><span data-stu-id="5eec7-126">skuId</span></span>|<span data-ttu-id="5eec7-127">Guid</span><span class="sxs-lookup"><span data-stu-id="5eec7-127">Guid</span></span>| <span data-ttu-id="5eec7-p104">Identificador único (GUID) del SKU de servicio. Es igual a la propiedad skuId en el objeto [SubscribedSku](subscribedsku.md) relacionado. Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5eec7-p104">Unique identifier (GUID) for the service SKU. Equal to the skuId property on the related [SubscribedSku](subscribedsku.md) object. Read-only</span></span> |
|<span data-ttu-id="5eec7-131">skuPartNumber</span><span class="sxs-lookup"><span data-stu-id="5eec7-131">skuPartNumber</span></span>|<span data-ttu-id="5eec7-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="5eec7-132">String</span></span>| <span data-ttu-id="5eec7-p105">Nombre para mostrar de SKU único. Es igual al skuPartNumber en el objeto [SubscribedSku](subscribedsku.md) relacionado; por ejemplo: "AAD_Premium". Solo lectura</span><span class="sxs-lookup"><span data-stu-id="5eec7-p105">Unique SKU display name. Equal to the skuPartNumber on the related [SubscribedSku](subscribedsku.md) object; for example: "AAD_Premium". Read-only</span></span> |

## <a name="relationships"></a><span data-ttu-id="5eec7-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5eec7-136">Relationships</span></span>
<span data-ttu-id="5eec7-137">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5eec7-137">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="5eec7-138">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5eec7-138">JSON representation</span></span>
<span data-ttu-id="5eec7-139">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5eec7-139">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.licenseDetails"
}-->

```json
{
  "id": "String (identifier)",
  "servicePlans": [{"@odata.type": "microsoft.graph.servicePlanInfo"}],
  "skuId": "Guid",
  "skuPartNumber": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "licenseDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->