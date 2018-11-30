---
title: Tipo de recurso licenseDetails
description: Contiene información sobre una licencia asignada a un usuario.
ms.openlocfilehash: 8c357617eea04151851a0e3a27c41937abd07b28
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030159"
---
# <a name="licensedetails-resource-type"></a><span data-ttu-id="1b199-103">Tipo de recurso licenseDetails</span><span class="sxs-lookup"><span data-stu-id="1b199-103">licenseDetails resource type</span></span>

<span data-ttu-id="1b199-104">Contiene información sobre una licencia asignada a un usuario.</span><span class="sxs-lookup"><span data-stu-id="1b199-104">Contains information about a license assigned to a user.</span></span>

## <a name="methods"></a><span data-ttu-id="1b199-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="1b199-105">Methods</span></span>

| <span data-ttu-id="1b199-106">Método</span><span class="sxs-lookup"><span data-stu-id="1b199-106">Method</span></span>           | <span data-ttu-id="1b199-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b199-107">Return Type</span></span>    |<span data-ttu-id="1b199-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b199-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="1b199-109">Enumerar licenseDetails</span><span class="sxs-lookup"><span data-stu-id="1b199-109">List licenseDetails</span></span>](../api/user-list-licensedetails.md) | <span data-ttu-id="1b199-110">Colección licenseDetails</span><span class="sxs-lookup"><span data-stu-id="1b199-110">licenseDetails collection</span></span> |<span data-ttu-id="1b199-111">Recupere una lista de objetos licenseDetails para un usuario.</span><span class="sxs-lookup"><span data-stu-id="1b199-111">Retrieve a list of licenseDetails objects for a user.</span></span>|

<!--|[Get licenseDetails](../api/licensedetails-get.md) | licenseDetails |Read properties and relationships of a licenseDetails object.|-->

## <a name="properties"></a><span data-ttu-id="1b199-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1b199-112">Properties</span></span>
| <span data-ttu-id="1b199-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1b199-113">Property</span></span>     | <span data-ttu-id="1b199-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="1b199-114">Type</span></span>   |<span data-ttu-id="1b199-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b199-115">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1b199-116">id</span><span class="sxs-lookup"><span data-stu-id="1b199-116">id</span></span>|<span data-ttu-id="1b199-117">String</span><span class="sxs-lookup"><span data-stu-id="1b199-117">String</span></span>| <span data-ttu-id="1b199-p101">Identificador único del objeto licenseDetails. Solo lectura, no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="1b199-p101">The unique identifier for the license detail object. Read-only, Key, Not nullable</span></span> |
|<span data-ttu-id="1b199-120">servicePlans</span><span class="sxs-lookup"><span data-stu-id="1b199-120">servicePlans</span></span>|<span data-ttu-id="1b199-121">Colección [servicePlanInfo](serviceplaninfo.md)</span><span class="sxs-lookup"><span data-stu-id="1b199-121">[servicePlanInfo](serviceplaninfo.md) collection</span></span>| <span data-ttu-id="1b199-p102">Información sobre los planes de servicio asignados a la licencia. Solo lectura, no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="1b199-p102">Information about the service plans assigned with the license. Read-only, Not nullable</span></span> |
|<span data-ttu-id="1b199-124">skuId</span><span class="sxs-lookup"><span data-stu-id="1b199-124">skuId</span></span>|<span data-ttu-id="1b199-125">Guid</span><span class="sxs-lookup"><span data-stu-id="1b199-125">Guid</span></span>| <span data-ttu-id="1b199-p103">Identificador único (GUID) del SKU de servicio. Es igual a la propiedad skuId en el objeto [SubscribedSku](subscribedsku.md) relacionado. Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1b199-p103">Unique identifier (GUID) for the service SKU. Equal to the skuId property on the related [SubscribedSku](subscribedsku.md) object. Read-only</span></span> |
|<span data-ttu-id="1b199-129">skuPartNumber</span><span class="sxs-lookup"><span data-stu-id="1b199-129">skuPartNumber</span></span>|<span data-ttu-id="1b199-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="1b199-130">String</span></span>| <span data-ttu-id="1b199-p104">Nombre para mostrar de SKU único. Es igual al skuPartNumber en el objeto [SubscribedSku](subscribedsku.md) relacionado; por ejemplo: "AAD_Premium". Solo lectura</span><span class="sxs-lookup"><span data-stu-id="1b199-p104">Unique SKU display name. Equal to the skuPartNumber on the related [SubscribedSku](subscribedsku.md) object; for example: "AAD_Premium". Read-only</span></span> |

## <a name="relationships"></a><span data-ttu-id="1b199-134">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1b199-134">Relationships</span></span>
<span data-ttu-id="1b199-135">Ninguno</span><span class="sxs-lookup"><span data-stu-id="1b199-135">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="1b199-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1b199-136">JSON representation</span></span>
<span data-ttu-id="1b199-137">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1b199-137">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
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