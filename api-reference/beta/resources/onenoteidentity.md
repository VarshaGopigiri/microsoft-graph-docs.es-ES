---
title: tipo de recurso oneNoteIdentity
description: '**Compatibilidad con próximamente**'
ms.openlocfilehash: 09c4ee9882a420fb07c6a51be5f361b601573969
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089748"
---
# <a name="onenoteidentity-resource-type"></a><span data-ttu-id="95d12-103">tipo de recurso oneNoteIdentity</span><span class="sxs-lookup"><span data-stu-id="95d12-103">oneNoteIdentity resource type</span></span>

> <span data-ttu-id="95d12-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="95d12-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="95d12-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="95d12-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="95d12-106">**Compatibilidad con próximamente**</span><span class="sxs-lookup"><span data-stu-id="95d12-106">**Support coming soon**</span></span>

<span data-ttu-id="95d12-107">El tipo de OneNoteIdentity representa una identidad de un _usuario_.</span><span class="sxs-lookup"><span data-stu-id="95d12-107">The OneNoteIdentity type represents an identity of a _user_.</span></span>

<span data-ttu-id="95d12-108">En el futuro, este tipo se combinarán con [identidad](identity.md)</span><span class="sxs-lookup"><span data-stu-id="95d12-108">In future, this type will be merged with [Identity](identity.md)</span></span>


## <a name="json-representation"></a><span data-ttu-id="95d12-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="95d12-109">JSON representation</span></span>

<span data-ttu-id="95d12-110">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="95d12-110">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenoteidentity"
}-->

```json
{
  "displayName": "string",
  "id": "string"
}

```
## <a name="properties"></a><span data-ttu-id="95d12-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95d12-111">Properties</span></span>
| <span data-ttu-id="95d12-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="95d12-112">Property</span></span>     | <span data-ttu-id="95d12-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="95d12-113">Type</span></span>   |<span data-ttu-id="95d12-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="95d12-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="95d12-115">displayName</span><span class="sxs-lookup"><span data-stu-id="95d12-115">displayName</span></span>|<span data-ttu-id="95d12-116">string</span><span class="sxs-lookup"><span data-stu-id="95d12-116">string</span></span>|<span data-ttu-id="95d12-117">Nombre para mostrar de la identidad.</span><span class="sxs-lookup"><span data-stu-id="95d12-117">The identity's display name.</span></span>|
|<span data-ttu-id="95d12-118">id</span><span class="sxs-lookup"><span data-stu-id="95d12-118">id</span></span>|<span data-ttu-id="95d12-119">string</span><span class="sxs-lookup"><span data-stu-id="95d12-119">string</span></span>|<span data-ttu-id="95d12-120">Identificador único de la identidad.</span><span class="sxs-lookup"><span data-stu-id="95d12-120">Unique identifier for the identity.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "oneNoteIdentity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
