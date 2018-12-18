---
title: Tipo de recurso educationStudent
description: Información adicional que se agrega a un educationUser que se presenta cuando el primaryRole de un usuario es `student`.
author: mmast-msft
ms.openlocfilehash: e24cf9adb9a4e7da70a3011b027e19a9d4cc4808
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27344061"
---
# <a name="educationstudent-resource-type"></a><span data-ttu-id="b5168-103">Tipo de recurso educationStudent</span><span class="sxs-lookup"><span data-stu-id="b5168-103">educationStudent resource type</span></span>

<span data-ttu-id="b5168-104">Información adicional que se agrega a un [educationUser](educationuser.md) que se presenta cuando el primaryRole de un usuario es `student`.</span><span class="sxs-lookup"><span data-stu-id="b5168-104">Additional information added to an [educationUser](educationuser.md) that is present when the primaryRole of a user is `student`.</span></span>

## <a name="properties"></a><span data-ttu-id="b5168-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5168-105">Properties</span></span>
| <span data-ttu-id="b5168-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b5168-106">Property</span></span>     | <span data-ttu-id="b5168-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5168-107">Type</span></span>   |<span data-ttu-id="b5168-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5168-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b5168-109">birthDate</span><span class="sxs-lookup"><span data-stu-id="b5168-109">birthDate</span></span>|<span data-ttu-id="b5168-110">Date</span><span class="sxs-lookup"><span data-stu-id="b5168-110">Date</span></span>| <span data-ttu-id="b5168-111">Fecha de nacimiento del alumno.</span><span class="sxs-lookup"><span data-stu-id="b5168-111">Birth date of the student.</span></span>|
|<span data-ttu-id="b5168-112">externalId</span><span class="sxs-lookup"><span data-stu-id="b5168-112">externalId</span></span>|<span data-ttu-id="b5168-113">String</span><span class="sxs-lookup"><span data-stu-id="b5168-113">String</span></span>| <span data-ttu-id="b5168-114">Identificador del alumno en el sistema de origen.</span><span class="sxs-lookup"><span data-stu-id="b5168-114">ID of the student in the source system.</span></span>|
|<span data-ttu-id="b5168-115">gender</span><span class="sxs-lookup"><span data-stu-id="b5168-115">gender</span></span>|<span data-ttu-id="b5168-116">educationGender</span><span class="sxs-lookup"><span data-stu-id="b5168-116">educationGender</span></span>| <span data-ttu-id="b5168-117">Los valores posibles son: `female`, `male`, `other`, `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="b5168-117">The possible values are: `female`, `male`, `other`, `unknownFutureValue`.</span></span>|
|<span data-ttu-id="b5168-118">grade</span><span class="sxs-lookup"><span data-stu-id="b5168-118">grade</span></span>|<span data-ttu-id="b5168-119">String</span><span class="sxs-lookup"><span data-stu-id="b5168-119">String</span></span>|<span data-ttu-id="b5168-120">Curso actual del alumno.</span><span class="sxs-lookup"><span data-stu-id="b5168-120">Current grade level of the student.</span></span>|
|<span data-ttu-id="b5168-121">graduationYear</span><span class="sxs-lookup"><span data-stu-id="b5168-121">graduationYear</span></span>|<span data-ttu-id="b5168-122">String</span><span class="sxs-lookup"><span data-stu-id="b5168-122">String</span></span>| <span data-ttu-id="b5168-123">Año de graduación del alumno en el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="b5168-123">Year the student is graduating from the school.</span></span>|
|<span data-ttu-id="b5168-124">studentNumber</span><span class="sxs-lookup"><span data-stu-id="b5168-124">studentNumber</span></span>|<span data-ttu-id="b5168-125">String</span><span class="sxs-lookup"><span data-stu-id="b5168-125">String</span></span>| <span data-ttu-id="b5168-126">Número de alumno.</span><span class="sxs-lookup"><span data-stu-id="b5168-126">Student Number.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b5168-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b5168-127">JSON representation</span></span>

<span data-ttu-id="b5168-128">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b5168-128">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationStudent"
}-->

```json
{
  "birthDate": "String (timestamp)",
  "externalId": "String",
  "gender": "educationGender",
  "grade": "String",
  "graduationYear": "String",
  "studentNumber": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationStudent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
