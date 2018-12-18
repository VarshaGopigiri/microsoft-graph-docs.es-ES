---
title: Tipo de recurso educationTeacher
description: Información adicional que se agrega a un educationUser que se presenta cuando el primaryRole de un usuario es `teacher`.
author: mmast-msft
ms.openlocfilehash: a880c3908b70e0b9d7c580492f45183b8f15425d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334464"
---
# <a name="educationteacher-resource-type"></a><span data-ttu-id="36beb-103">Tipo de recurso educationTeacher</span><span class="sxs-lookup"><span data-stu-id="36beb-103">educationTeacher resource type</span></span>

<span data-ttu-id="36beb-104">Información adicional que se agrega a un [educationUser](educationuser.md) que se presenta cuando el primaryRole de un usuario es `teacher`.</span><span class="sxs-lookup"><span data-stu-id="36beb-104">Additional information added to an [educationUser](educationuser.md) that is present when the primaryRole of a user is `teacher`.</span></span>


## <a name="properties"></a><span data-ttu-id="36beb-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36beb-105">Properties</span></span>
| <span data-ttu-id="36beb-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="36beb-106">Property</span></span>     | <span data-ttu-id="36beb-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="36beb-107">Type</span></span>   |<span data-ttu-id="36beb-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="36beb-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="36beb-109">externalId</span><span class="sxs-lookup"><span data-stu-id="36beb-109">externalId</span></span>|<span data-ttu-id="36beb-110">String</span><span class="sxs-lookup"><span data-stu-id="36beb-110">String</span></span>| <span data-ttu-id="36beb-111">Identificador del profesor en el sistema de origen.</span><span class="sxs-lookup"><span data-stu-id="36beb-111">ID of the teacher in the source system.</span></span>|
|<span data-ttu-id="36beb-112">teacherNumber</span><span class="sxs-lookup"><span data-stu-id="36beb-112">teacherNumber</span></span>|<span data-ttu-id="36beb-113">String</span><span class="sxs-lookup"><span data-stu-id="36beb-113">String</span></span>|<span data-ttu-id="36beb-114">Número de profesor</span><span class="sxs-lookup"><span data-stu-id="36beb-114">Teacher number.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="36beb-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="36beb-115">JSON representation</span></span>

<span data-ttu-id="36beb-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="36beb-116">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationTeacher"
}-->

```json
{
  "externalId": "String",
  "teacherNumber": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationTeacher resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->