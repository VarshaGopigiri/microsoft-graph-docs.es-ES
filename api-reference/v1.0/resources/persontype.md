---
title: Tipo de recurso personType
description: Representa el tipo de contacto.
ms.openlocfilehash: 3938be8d1dd0bf4a4934de4bbcd7862185971128
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029388"
---
# <a name="persontype-resource-type"></a><span data-ttu-id="f9855-103">Tipo de recurso personType</span><span class="sxs-lookup"><span data-stu-id="f9855-103">personType resource type</span></span>

<span data-ttu-id="f9855-104">Representa el tipo de contacto.</span><span class="sxs-lookup"><span data-stu-id="f9855-104">Represents the type of person.</span></span>


## <a name="json-representation"></a><span data-ttu-id="f9855-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f9855-105">JSON representation</span></span>

<span data-ttu-id="f9855-106">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f9855-106">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.personType"
}-->

```json
{
  "class": "string",
  "subclass": "string"
}

```
## <a name="properties"></a><span data-ttu-id="f9855-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f9855-107">Properties</span></span>
| <span data-ttu-id="f9855-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f9855-108">Property</span></span>     | <span data-ttu-id="f9855-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9855-109">Type</span></span>   |<span data-ttu-id="f9855-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9855-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f9855-111">class</span><span class="sxs-lookup"><span data-stu-id="f9855-111">class</span></span>|<span data-ttu-id="f9855-112">String</span><span class="sxs-lookup"><span data-stu-id="f9855-112">String</span></span>|<span data-ttu-id="f9855-113">El tipo de origen de datos, como Person.</span><span class="sxs-lookup"><span data-stu-id="f9855-113">The type of data source, such as Person.</span></span>|
|<span data-ttu-id="f9855-114">subclass</span><span class="sxs-lookup"><span data-stu-id="f9855-114">subclass</span></span>|<span data-ttu-id="f9855-115">String</span><span class="sxs-lookup"><span data-stu-id="f9855-115">String</span></span>|<span data-ttu-id="f9855-116">El tipo secundario del origen de datos, como OrganizationUser.</span><span class="sxs-lookup"><span data-stu-id="f9855-116">The secondary type of data source, such as OrganizationUser.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "personType resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
