---
title: Tipo de recurso educationTeacher
description: Información adicional que se agrega a un educationUser que se presenta cuando el primaryRole de un usuario es `teacher`.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: eece9080c34855d4546321b7605b47f4b2f231a6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875967"
---
# <a name="educationteacher-resource-type"></a><span data-ttu-id="f19f9-103">Tipo de recurso educationTeacher</span><span class="sxs-lookup"><span data-stu-id="f19f9-103">educationTeacher resource type</span></span>

> <span data-ttu-id="f19f9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f19f9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f19f9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f19f9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f19f9-106">Información adicional que se agrega a un [educationUser](educationuser.md) que se presenta cuando el primaryRole de un usuario es `teacher`.</span><span class="sxs-lookup"><span data-stu-id="f19f9-106">Additional information added to an [educationUser](educationuser.md) that is present when the primaryRole of a user is `teacher`.</span></span>


## <a name="properties"></a><span data-ttu-id="f19f9-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f19f9-107">Properties</span></span>
| <span data-ttu-id="f19f9-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f19f9-108">Property</span></span>     | <span data-ttu-id="f19f9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f19f9-109">Type</span></span>   |<span data-ttu-id="f19f9-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="f19f9-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f19f9-111">externalId</span><span class="sxs-lookup"><span data-stu-id="f19f9-111">externalId</span></span>|<span data-ttu-id="f19f9-112">String</span><span class="sxs-lookup"><span data-stu-id="f19f9-112">String</span></span>| <span data-ttu-id="f19f9-113">Identificador del profesor en el sistema de origen.</span><span class="sxs-lookup"><span data-stu-id="f19f9-113">ID of the teacher in the source system.</span></span>|
|<span data-ttu-id="f19f9-114">teacherNumber</span><span class="sxs-lookup"><span data-stu-id="f19f9-114">teacherNumber</span></span>|<span data-ttu-id="f19f9-115">String</span><span class="sxs-lookup"><span data-stu-id="f19f9-115">String</span></span>|<span data-ttu-id="f19f9-116">Número de profesor</span><span class="sxs-lookup"><span data-stu-id="f19f9-116">Teacher number.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f19f9-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f19f9-117">JSON representation</span></span>

<span data-ttu-id="f19f9-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f19f9-118">The following is a JSON representation of the resource.</span></span>

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
