---
title: tipo de recurso targetResourceUser
description: Indica el objeto de usuario que se ha agregado, actualiza o elimina los administradores como parte de la actividad de auditoría. Deriva el recurso targetResource.
ms.openlocfilehash: 632d0551b3aba434c3309c8c874947708eb9a9f5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086431"
---
# <a name="targetresourceuser-resource-type"></a><span data-ttu-id="b6d4f-104">tipo de recurso targetResourceUser</span><span class="sxs-lookup"><span data-stu-id="b6d4f-104">targetResourceUser resource type</span></span>
<span data-ttu-id="b6d4f-105">Indica el objeto de usuario que se ha agregado, actualiza o elimina los administradores como parte de la actividad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="b6d4f-105">Indicates the user object that was added, updated or deleted by admins as part of audit activity.</span></span> <span data-ttu-id="b6d4f-106">Deriva el recurso [targetResource](targetresource.md) .</span><span class="sxs-lookup"><span data-stu-id="b6d4f-106">Derived from the [targetResource](targetresource.md) resource.</span></span>


## <a name="properties"></a><span data-ttu-id="b6d4f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6d4f-107">Properties</span></span>
| <span data-ttu-id="b6d4f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b6d4f-108">Property</span></span>     | <span data-ttu-id="b6d4f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6d4f-109">Type</span></span>   |<span data-ttu-id="b6d4f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6d4f-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b6d4f-111">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="b6d4f-111">userPrincipalName</span></span>|<span data-ttu-id="b6d4f-112">String</span><span class="sxs-lookup"><span data-stu-id="b6d4f-112">String</span></span>|<span data-ttu-id="b6d4f-113">Indica el identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="b6d4f-113">Indicates the Unique Id of the User.</span></span> <span data-ttu-id="b6d4f-114">Hace referencia al identificador de usuario para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="b6d4f-114">Refers to User Id for a specific user.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b6d4f-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b6d4f-115">JSON representation</span></span>

<span data-ttu-id="b6d4f-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b6d4f-116">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.targetResourceUser"
}-->

```json
{
  "userPrincipalName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "targetResourceUser resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->