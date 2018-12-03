---
title: tipo de recurso educationLinkResource
description: Una subclase de educationResource. Este recurso es un vínculo y no tener todos los datos asociados con él.
ms.openlocfilehash: 314bd87998ada178484401b2122f0936f87e51a0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088534"
---
# <a name="educationlinkresource-resource-type"></a><span data-ttu-id="677ac-104">tipo de recurso educationLinkResource</span><span class="sxs-lookup"><span data-stu-id="677ac-104">educationLinkResource resource type</span></span>

> <span data-ttu-id="677ac-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="677ac-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="677ac-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="677ac-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="677ac-107">Una subclase de [educationResource](educationresource.md).</span><span class="sxs-lookup"><span data-stu-id="677ac-107">A subclass of [educationResource](educationresource.md).</span></span> <span data-ttu-id="677ac-108">Este recurso es un vínculo y no tener todos los datos asociados con él.</span><span class="sxs-lookup"><span data-stu-id="677ac-108">This resource is a link and does not have any additional data associated with it.</span></span>


## <a name="properties"></a><span data-ttu-id="677ac-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="677ac-109">Properties</span></span>
| <span data-ttu-id="677ac-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="677ac-110">Property</span></span>     | <span data-ttu-id="677ac-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="677ac-111">Type</span></span>   |<span data-ttu-id="677ac-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="677ac-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="677ac-113">vincular</span><span class="sxs-lookup"><span data-stu-id="677ac-113">link</span></span>|<span data-ttu-id="677ac-114">String</span><span class="sxs-lookup"><span data-stu-id="677ac-114">String</span></span>|<span data-ttu-id="677ac-115">Dirección URL del recurso.</span><span class="sxs-lookup"><span data-stu-id="677ac-115">URL to the resource.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="677ac-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="677ac-116">JSON representation</span></span>

<span data-ttu-id="677ac-117">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="677ac-117">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationLinkResource"
}-->

```json
{
  "link": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationLinkResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->