---
title: tipo de recurso educationSubmissionResource
description: 'Un contenedor alrededor de un recurso para su uso en una presentación. El contenedor agrega un puntero al recurso de asignación si esto se copió desde la asignación.  '
author: dipakboyed
localization_priority: Normal
ms.openlocfilehash: 8703072fccb77a2577db6ce0717647e79a47fdc8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875988"
---
# <a name="educationsubmissionresource-resource-type"></a><span data-ttu-id="348e4-104">tipo de recurso educationSubmissionResource</span><span class="sxs-lookup"><span data-stu-id="348e4-104">educationSubmissionResource resource type</span></span>

> <span data-ttu-id="348e4-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="348e4-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="348e4-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="348e4-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="348e4-107">Un contenedor alrededor de un recurso para su uso en una presentación.</span><span class="sxs-lookup"><span data-stu-id="348e4-107">A wrapper around a resource for use on a submission.</span></span> <span data-ttu-id="348e4-108">El contenedor agrega un puntero al recurso de asignación si esto se copió desde la asignación.</span><span class="sxs-lookup"><span data-stu-id="348e4-108">The wrapper adds a pointer to the assignment resource if this was copied from the assignment.</span></span>  


## <a name="methods"></a><span data-ttu-id="348e4-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="348e4-109">Methods</span></span>

| <span data-ttu-id="348e4-110">Método</span><span class="sxs-lookup"><span data-stu-id="348e4-110">Method</span></span>           | <span data-ttu-id="348e4-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="348e4-111">Return Type</span></span>    |<span data-ttu-id="348e4-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="348e4-112">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="348e4-113">Obtener educationSubmissionResource</span><span class="sxs-lookup"><span data-stu-id="348e4-113">Get educationSubmissionResource</span></span>](../api/educationsubmissionresource-get.md) | [<span data-ttu-id="348e4-114">educationSubmissionResource</span><span class="sxs-lookup"><span data-stu-id="348e4-114">educationSubmissionResource</span></span>](educationsubmissionresource.md) |<span data-ttu-id="348e4-115">Leer las propiedades y relaciones de un objeto **educationSubmissionResource** .</span><span class="sxs-lookup"><span data-stu-id="348e4-115">Read properties and relationships of an **educationSubmissionResource** object.</span></span>|
|[<span data-ttu-id="348e4-116">Delete</span><span class="sxs-lookup"><span data-stu-id="348e4-116">Delete</span></span>](../api/educationsubmissionresource-delete.md) | <span data-ttu-id="348e4-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="348e4-117">None</span></span> |<span data-ttu-id="348e4-118">Eliminación de un objeto **educationSubmissionResource** .</span><span class="sxs-lookup"><span data-stu-id="348e4-118">Delete an **educationSubmissionResource** object.</span></span> |

## <a name="properties"></a><span data-ttu-id="348e4-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="348e4-119">Properties</span></span>
| <span data-ttu-id="348e4-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="348e4-120">Property</span></span>     | <span data-ttu-id="348e4-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="348e4-121">Type</span></span>   |<span data-ttu-id="348e4-122">Description</span><span class="sxs-lookup"><span data-stu-id="348e4-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="348e4-123">assignmentResourceUrl</span><span class="sxs-lookup"><span data-stu-id="348e4-123">assignmentResourceUrl</span></span>|<span data-ttu-id="348e4-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="348e4-124">String</span></span>|<span data-ttu-id="348e4-125">Puntero a la asignación desde la que se ha copiado este recurso.</span><span class="sxs-lookup"><span data-stu-id="348e4-125">Pointer to the assignment from which this resource was copied.</span></span> <span data-ttu-id="348e4-126">Si es null, el alumno carga el recurso.</span><span class="sxs-lookup"><span data-stu-id="348e4-126">If this is null, the student uploaded the resource.</span></span>|
|<span data-ttu-id="348e4-127">id</span><span class="sxs-lookup"><span data-stu-id="348e4-127">id</span></span>|<span data-ttu-id="348e4-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="348e4-128">String</span></span>| <span data-ttu-id="348e4-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="348e4-129">Read-only.</span></span>|
|<span data-ttu-id="348e4-130">resource</span><span class="sxs-lookup"><span data-stu-id="348e4-130">resource</span></span>|[<span data-ttu-id="348e4-131">educationResource</span><span class="sxs-lookup"><span data-stu-id="348e4-131">educationResource</span></span>](educationresource.md)|<span data-ttu-id="348e4-132">Objeto de recurso.</span><span class="sxs-lookup"><span data-stu-id="348e4-132">Resource object.</span></span>|

## <a name="relationships"></a><span data-ttu-id="348e4-133">Relaciones</span><span class="sxs-lookup"><span data-stu-id="348e4-133">Relationships</span></span>
<span data-ttu-id="348e4-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="348e4-134">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="348e4-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="348e4-135">JSON representation</span></span>

<span data-ttu-id="348e4-136">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="348e4-136">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationSubmissionResource"
}-->

```json
{
  "assignmentResourceUrl": "String",
  "id": "String (identifier)",
  "resource": {"@odata.type": "microsoft.graph.educationResource"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationSubmissionResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
