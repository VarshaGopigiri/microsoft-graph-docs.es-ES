---
title: Tipo de recurso educationTeacher
description: Información adicional que se agrega a un educationUser que se presenta cuando el primaryRole de un usuario es `teacher`.
ms.openlocfilehash: 37fd46ee00f82b518d91969b1793147be859efdf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083141"
---
# <a name="educationteacher-resource-type"></a><span data-ttu-id="0c49c-103">Tipo de recurso educationTeacher</span><span class="sxs-lookup"><span data-stu-id="0c49c-103">educationTeacher resource type</span></span>

> <span data-ttu-id="0c49c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0c49c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0c49c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0c49c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="0c49c-106">Información adicional que se agrega a un [educationUser](educationuser.md) que se presenta cuando el primaryRole de un usuario es `teacher`.</span><span class="sxs-lookup"><span data-stu-id="0c49c-106">Additional information added to an [educationUser](educationuser.md) that is present when the primaryRole of a user is `teacher`.</span></span>


## <a name="properties"></a><span data-ttu-id="0c49c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c49c-107">Properties</span></span>
| <span data-ttu-id="0c49c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0c49c-108">Property</span></span>     | <span data-ttu-id="0c49c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c49c-109">Type</span></span>   |<span data-ttu-id="0c49c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c49c-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0c49c-111">externalId</span><span class="sxs-lookup"><span data-stu-id="0c49c-111">externalId</span></span>|<span data-ttu-id="0c49c-112">String</span><span class="sxs-lookup"><span data-stu-id="0c49c-112">String</span></span>| <span data-ttu-id="0c49c-113">Identificador del profesor en el sistema de origen.</span><span class="sxs-lookup"><span data-stu-id="0c49c-113">ID of the teacher in the source system.</span></span>|
|<span data-ttu-id="0c49c-114">teacherNumber</span><span class="sxs-lookup"><span data-stu-id="0c49c-114">teacherNumber</span></span>|<span data-ttu-id="0c49c-115">String</span><span class="sxs-lookup"><span data-stu-id="0c49c-115">String</span></span>|<span data-ttu-id="0c49c-116">Número de profesor</span><span class="sxs-lookup"><span data-stu-id="0c49c-116">Teacher number.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0c49c-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0c49c-117">JSON representation</span></span>

<span data-ttu-id="0c49c-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0c49c-118">The following is a JSON representation of the resource.</span></span>

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