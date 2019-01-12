---
title: tipo de recurso educationAssignmentGrade
description: " Sin embargo, todos los tipos de clasificación (puntos, determinantes etc.) son subclases de este"
localization_priority: Normal
author: dipakboyed
ms.prod: education
ms.openlocfilehash: ecdd92c84399ee17d2808301d997830725fb5642
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982361"
---
# <a name="educationassignmentgrade-resource-type"></a><span data-ttu-id="3564f-103">tipo de recurso educationAssignmentGrade</span><span class="sxs-lookup"><span data-stu-id="3564f-103">educationAssignmentGrade resource type</span></span>

> <span data-ttu-id="3564f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3564f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3564f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3564f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3564f-106">Representa el objeto de **calificación** en una presentación.</span><span class="sxs-lookup"><span data-stu-id="3564f-106">Represents the **Grade** object on a Submission.</span></span> <span data-ttu-id="3564f-107">Esto es un tipo abstracto que nunca se crearán instancias; Sin embargo, todos los tipos de clasificación (puntos, determinantes etc.) son subclases de este tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="3564f-107">This is an abstract type that will never be instantiated; however, all types of grading (points, pass/fail, and so on) are subclasses of this resource type.</span></span> <span data-ttu-id="3564f-108">Este objeto también realiza un seguimiento de quién va a realizar la clasificación.</span><span class="sxs-lookup"><span data-stu-id="3564f-108">This object also tracks who is doing the grading.</span></span> <span data-ttu-id="3564f-109">Esta opción se usa la propiedad **submission.grade** .</span><span class="sxs-lookup"><span data-stu-id="3564f-109">This is used in the **submission.grade** property.</span></span>


## <a name="properties"></a><span data-ttu-id="3564f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3564f-110">Properties</span></span>
| <span data-ttu-id="3564f-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3564f-111">Property</span></span>     | <span data-ttu-id="3564f-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="3564f-112">Type</span></span>   |<span data-ttu-id="3564f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="3564f-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3564f-114">gradedBy</span><span class="sxs-lookup"><span data-stu-id="3564f-114">gradedBy</span></span>|[<span data-ttu-id="3564f-115">identitySet</span><span class="sxs-lookup"><span data-stu-id="3564f-115">identitySet</span></span>](identityset.md)| <span data-ttu-id="3564f-116">Usuario que hizo la clasificación.</span><span class="sxs-lookup"><span data-stu-id="3564f-116">User who did the grading.</span></span> |
|<span data-ttu-id="3564f-117">gradedDateTime</span><span class="sxs-lookup"><span data-stu-id="3564f-117">gradedDateTime</span></span>|<span data-ttu-id="3564f-118">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3564f-118">DateTimeOffset</span></span>| <span data-ttu-id="3564f-119">Momento en el tiempo cuando se aplicó la calificación a este objeto de envío.</span><span class="sxs-lookup"><span data-stu-id="3564f-119">Moment in time when the grade was applied to this submission object.</span></span> <span data-ttu-id="3564f-120">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="3564f-120">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="3564f-121">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="3564f-121">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3564f-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3564f-122">JSON representation</span></span>

<span data-ttu-id="3564f-123">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3564f-123">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationAssignmentGrade"
}-->

```json
{
  "gradedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "gradedDateTime": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationAssignmentGrade resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
