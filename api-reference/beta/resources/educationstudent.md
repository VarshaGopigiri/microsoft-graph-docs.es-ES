---
title: Tipo de recurso educationStudent
description: Información adicional que se agrega a un educationUser que se presenta cuando el primaryRole de un usuario es `student`.
author: mmast-msft
ms.openlocfilehash: ce84c9f6abb71e99bf3d886e5bad9e7e97bcb513
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27313086"
---
# <a name="educationstudent-resource-type"></a><span data-ttu-id="fe775-103">Tipo de recurso educationStudent</span><span class="sxs-lookup"><span data-stu-id="fe775-103">educationStudent resource type</span></span>

> <span data-ttu-id="fe775-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fe775-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fe775-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fe775-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fe775-106">Información adicional que se agrega a un [educationUser](educationuser.md) que se presenta cuando el primaryRole de un usuario es `student`.</span><span class="sxs-lookup"><span data-stu-id="fe775-106">Additional information added to an [educationUser](educationuser.md) that is present when the primaryRole of a user is `student`.</span></span>

## <a name="properties"></a><span data-ttu-id="fe775-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fe775-107">Properties</span></span>
| <span data-ttu-id="fe775-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fe775-108">Property</span></span>     | <span data-ttu-id="fe775-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe775-109">Type</span></span>   |<span data-ttu-id="fe775-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe775-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fe775-111">birthDate</span><span class="sxs-lookup"><span data-stu-id="fe775-111">birthDate</span></span>|<span data-ttu-id="fe775-112">Date</span><span class="sxs-lookup"><span data-stu-id="fe775-112">Date</span></span>| <span data-ttu-id="fe775-113">Fecha de nacimiento del alumno.</span><span class="sxs-lookup"><span data-stu-id="fe775-113">Birth date of the student.</span></span>|
|<span data-ttu-id="fe775-114">externalId</span><span class="sxs-lookup"><span data-stu-id="fe775-114">externalId</span></span>|<span data-ttu-id="fe775-115">String</span><span class="sxs-lookup"><span data-stu-id="fe775-115">String</span></span>| <span data-ttu-id="fe775-116">Identificador del alumno en el sistema de origen.</span><span class="sxs-lookup"><span data-stu-id="fe775-116">ID of the student in the source system.</span></span>|
|<span data-ttu-id="fe775-117">gender</span><span class="sxs-lookup"><span data-stu-id="fe775-117">gender</span></span>|`educationGender enumeration`| <span data-ttu-id="fe775-118">Los valores posibles son: `female`, `male`, `other` y `unkownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="fe775-118">Possible values are: `female`, `male`, `other`, `unkownFutureValue`.</span></span>|
|<span data-ttu-id="fe775-119">grade</span><span class="sxs-lookup"><span data-stu-id="fe775-119">grade</span></span>|<span data-ttu-id="fe775-120">String</span><span class="sxs-lookup"><span data-stu-id="fe775-120">String</span></span>|<span data-ttu-id="fe775-121">Curso actual del alumno.</span><span class="sxs-lookup"><span data-stu-id="fe775-121">Current grade level of the student.</span></span>|
|<span data-ttu-id="fe775-122">graduationYear</span><span class="sxs-lookup"><span data-stu-id="fe775-122">graduationYear</span></span>|<span data-ttu-id="fe775-123">String</span><span class="sxs-lookup"><span data-stu-id="fe775-123">String</span></span>| <span data-ttu-id="fe775-124">Año de graduación del alumno en el centro educativo.</span><span class="sxs-lookup"><span data-stu-id="fe775-124">Year the student is graduating from the school.</span></span>|
|<span data-ttu-id="fe775-125">studentNumber</span><span class="sxs-lookup"><span data-stu-id="fe775-125">studentNumber</span></span>|<span data-ttu-id="fe775-126">String</span><span class="sxs-lookup"><span data-stu-id="fe775-126">String</span></span>| <span data-ttu-id="fe775-127">Número de alumno.</span><span class="sxs-lookup"><span data-stu-id="fe775-127">Student Number.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="fe775-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fe775-128">JSON representation</span></span>

<span data-ttu-id="fe775-129">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="fe775-129">The following is a JSON representation of the resource.</span></span>

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