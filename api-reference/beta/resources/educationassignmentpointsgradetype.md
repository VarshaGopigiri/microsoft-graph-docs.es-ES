---
title: tipo de recurso educationAssignmentPointsGradeType
description: Se utiliza con la propiedad **assignments.grading** . Esto es una subclase de educationAssignmentGradeType.
ms.openlocfilehash: 5c170540e99003a78df0550d4d6542c07df8f1ff
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090155"
---
# <a name="educationassignmentpointsgradetype-resource-type"></a><span data-ttu-id="eca78-104">tipo de recurso educationAssignmentPointsGradeType</span><span class="sxs-lookup"><span data-stu-id="eca78-104">educationAssignmentPointsGradeType resource type</span></span>

> <span data-ttu-id="eca78-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eca78-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eca78-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eca78-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eca78-107">Se utiliza con la propiedad **assignments.grading** .</span><span class="sxs-lookup"><span data-stu-id="eca78-107">Used with the **assignments.grading** property.</span></span> <span data-ttu-id="eca78-108">Esto es una subclase de [educationAssignmentGradeType](educationassignmentgradetype.md).</span><span class="sxs-lookup"><span data-stu-id="eca78-108">This is a subclass of [educationAssignmentGradeType](educationassignmentgradetype.md).</span></span>

<span data-ttu-id="eca78-109">Esto indica que la asignación es clasificada y almacena el número máximo de puntos de que cada alumno puede lograr en este elemento de trabajo.</span><span class="sxs-lookup"><span data-stu-id="eca78-109">This indicates that the assignment is graded and stores the maximum number of points each student can achieve on this work item.</span></span> <span data-ttu-id="eca78-110">Cuando se establece en una asignación, cada envío obtendrá una propiedad [educationAssignmentPointsGrade](educationassignmentpointsgrade.md) asociada para el almacenamiento de los puntos de cada alumno.</span><span class="sxs-lookup"><span data-stu-id="eca78-110">When this is set on an assignment, each submission will get an [educationAssignmentPointsGrade](educationassignmentpointsgrade.md) property associated with it for the storage of each student's points.</span></span>

## <a name="properties"></a><span data-ttu-id="eca78-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eca78-111">Properties</span></span>
| <span data-ttu-id="eca78-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eca78-112">Property</span></span>     | <span data-ttu-id="eca78-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="eca78-113">Type</span></span>   |<span data-ttu-id="eca78-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="eca78-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="eca78-115">maxPoints</span><span class="sxs-lookup"><span data-stu-id="eca78-115">maxPoints</span></span>|<span data-ttu-id="eca78-116">Single</span><span class="sxs-lookup"><span data-stu-id="eca78-116">Single</span></span>| <span data-ttu-id="eca78-117">Max puntos posibles para esta asignación.</span><span class="sxs-lookup"><span data-stu-id="eca78-117">Max points possible for this assignment.</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="eca78-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="eca78-118">JSON representation</span></span>

<span data-ttu-id="eca78-119">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="eca78-119">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationAssignmentPointsGradeType"
}-->

```json
{
  "maxPoints": "Single"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationAssignmentPointsGradeType resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->