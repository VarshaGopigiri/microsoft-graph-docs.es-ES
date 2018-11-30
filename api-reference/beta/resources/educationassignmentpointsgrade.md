---
title: tipo de recurso educationAssignmentPointsGrade
description: Cuando se establece una asignación a un tipo de categoría de puntos, cada envío tendrá este objeto asociado con la propiedad **submission.grade** . Esto crea una subclase de educationAssignmentGrade,
ms.openlocfilehash: 2439ac8946fea588bd7bc1afe7f1ff1042b9179a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085171"
---
# <a name="educationassignmentpointsgrade-resource-type"></a><span data-ttu-id="9eef7-104">tipo de recurso educationAssignmentPointsGrade</span><span class="sxs-lookup"><span data-stu-id="9eef7-104">educationAssignmentPointsGrade resource type</span></span>

> <span data-ttu-id="9eef7-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9eef7-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9eef7-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9eef7-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9eef7-107">Cuando se establece una asignación a un tipo de categoría de puntos, cada envío tendrá este objeto asociado con la propiedad **submission.grade** .</span><span class="sxs-lookup"><span data-stu-id="9eef7-107">When an assignment is set to a points grade type, each submission will have this object associated with the **submission.grade** property.</span></span> <span data-ttu-id="9eef7-108">Esto crea una subclase de [educationAssignmentGrade](educationassignmentgrade.md), que el que va a agregar datos a esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9eef7-108">This creates a subclass from [educationAssignmentGrade](educationassignmentgrade.md), which will add the who data to this property.</span></span> <span data-ttu-id="9eef7-109">Los puntos máx. se almacena en la propiedad **assignments.grading** .</span><span class="sxs-lookup"><span data-stu-id="9eef7-109">The max points is stored in the **assignments.grading** property.</span></span>


## <a name="properties"></a><span data-ttu-id="9eef7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9eef7-110">Properties</span></span>
| <span data-ttu-id="9eef7-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9eef7-111">Property</span></span>     | <span data-ttu-id="9eef7-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="9eef7-112">Type</span></span>   |<span data-ttu-id="9eef7-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="9eef7-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9eef7-114">points</span><span class="sxs-lookup"><span data-stu-id="9eef7-114">points</span></span>|<span data-ttu-id="9eef7-115">Single</span><span class="sxs-lookup"><span data-stu-id="9eef7-115">Single</span></span>|<span data-ttu-id="9eef7-116">Número de puntos de un profesor es dar a este objeto de envío.</span><span class="sxs-lookup"><span data-stu-id="9eef7-116">Number of points a teacher is giving this submission object.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9eef7-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9eef7-117">JSON representation</span></span>

<span data-ttu-id="9eef7-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9eef7-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationAssignmentPointsGrade"
}-->

```json
{
  "points": "Single"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationAssignmentPointsGrade resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->