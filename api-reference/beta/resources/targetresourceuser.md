---
title: tipo de recurso targetResourceUser
description: Indica el objeto de usuario que se ha agregado, actualiza o elimina los administradores como parte de la actividad de auditoría. Deriva el recurso targetResource.
localization_priority: Normal
ms.openlocfilehash: 9c71ead1b358b72a1b531abac56018fa71d084e8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831932"
---
# <a name="targetresourceuser-resource-type"></a><span data-ttu-id="f1228-104">tipo de recurso targetResourceUser</span><span class="sxs-lookup"><span data-stu-id="f1228-104">targetResourceUser resource type</span></span>
<span data-ttu-id="f1228-105">Indica el objeto de usuario que se ha agregado, actualiza o elimina los administradores como parte de la actividad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="f1228-105">Indicates the user object that was added, updated or deleted by admins as part of audit activity.</span></span> <span data-ttu-id="f1228-106">Deriva el recurso [targetResource](targetresource.md) .</span><span class="sxs-lookup"><span data-stu-id="f1228-106">Derived from the [targetResource](targetresource.md) resource.</span></span>


## <a name="properties"></a><span data-ttu-id="f1228-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f1228-107">Properties</span></span>
| <span data-ttu-id="f1228-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f1228-108">Property</span></span>     | <span data-ttu-id="f1228-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1228-109">Type</span></span>   |<span data-ttu-id="f1228-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1228-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f1228-111">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f1228-111">userPrincipalName</span></span>|<span data-ttu-id="f1228-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="f1228-112">String</span></span>|<span data-ttu-id="f1228-113">Indica el identificador único del usuario.</span><span class="sxs-lookup"><span data-stu-id="f1228-113">Indicates the Unique Id of the User.</span></span> <span data-ttu-id="f1228-114">Hace referencia al identificador de usuario para un usuario específico.</span><span class="sxs-lookup"><span data-stu-id="f1228-114">Refers to User Id for a specific user.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f1228-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f1228-115">JSON representation</span></span>

<span data-ttu-id="f1228-116">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f1228-116">Here is a JSON representation of the resource.</span></span>

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
