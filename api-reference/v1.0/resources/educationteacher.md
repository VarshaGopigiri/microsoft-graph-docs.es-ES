---
title: Tipo de recurso educationTeacher
description: Información adicional que se agrega a un educationUser que se presenta cuando el primaryRole de un usuario es `teacher`.
ms.openlocfilehash: 59d3334b7a01b0dd39c357f6598085cd78d1e3ac
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029451"
---
# <a name="educationteacher-resource-type"></a><span data-ttu-id="3fab8-103">Tipo de recurso educationTeacher</span><span class="sxs-lookup"><span data-stu-id="3fab8-103">educationTeacher resource type</span></span>

<span data-ttu-id="3fab8-104">Información adicional que se agrega a un [educationUser](educationuser.md) que se presenta cuando el primaryRole de un usuario es `teacher`.</span><span class="sxs-lookup"><span data-stu-id="3fab8-104">Additional information added to an [educationUser](educationuser.md) that is present when the primaryRole of a user is `teacher`.</span></span>


## <a name="properties"></a><span data-ttu-id="3fab8-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3fab8-105">Properties</span></span>
| <span data-ttu-id="3fab8-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3fab8-106">Property</span></span>     | <span data-ttu-id="3fab8-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="3fab8-107">Type</span></span>   |<span data-ttu-id="3fab8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3fab8-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3fab8-109">externalId</span><span class="sxs-lookup"><span data-stu-id="3fab8-109">externalId</span></span>|<span data-ttu-id="3fab8-110">String</span><span class="sxs-lookup"><span data-stu-id="3fab8-110">String</span></span>| <span data-ttu-id="3fab8-111">Identificador del profesor en el sistema de origen.</span><span class="sxs-lookup"><span data-stu-id="3fab8-111">ID of the teacher in the source system.</span></span>|
|<span data-ttu-id="3fab8-112">teacherNumber</span><span class="sxs-lookup"><span data-stu-id="3fab8-112">teacherNumber</span></span>|<span data-ttu-id="3fab8-113">String</span><span class="sxs-lookup"><span data-stu-id="3fab8-113">String</span></span>|<span data-ttu-id="3fab8-114">Número de profesor</span><span class="sxs-lookup"><span data-stu-id="3fab8-114">Teacher number.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3fab8-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3fab8-115">JSON representation</span></span>

<span data-ttu-id="3fab8-116">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3fab8-116">The following is a JSON representation of the resource.</span></span>

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