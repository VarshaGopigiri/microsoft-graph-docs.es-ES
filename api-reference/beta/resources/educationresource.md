---
title: tipo de recurso educationResource
description: Una superclase para todos los objetos de recursos en el sistema. Un recurso está asociado a una **asignación** o **envío**, que representa el objeto de aprendizaje que se va a
localization_priority: Normal
ms.openlocfilehash: 0608f3c0fb84f05404032bed611f0af887e7bb67
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27827562"
---
# <a name="educationresource-resource-type"></a><span data-ttu-id="59c53-104">tipo de recurso educationResource</span><span class="sxs-lookup"><span data-stu-id="59c53-104">educationResource resource type</span></span>

> <span data-ttu-id="59c53-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="59c53-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="59c53-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="59c53-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="59c53-107">Una superclase para todos los objetos de recursos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="59c53-107">A superclass for all resource objects in the system.</span></span> <span data-ttu-id="59c53-108">Un recurso está asociado a una **asignación** o **envío**, que representa el objeto de aprendizaje que se va a entregar o de la presentación.</span><span class="sxs-lookup"><span data-stu-id="59c53-108">A resource is associated with an **Assignment** and/or **Submission**, which represents the learning object that is being handed out or handed in.</span></span> <span data-ttu-id="59c53-109">No se puede crear una instancia un recurso directamente; debe realizar una subclase que representa el tipo de recurso que se va a utilizar.</span><span class="sxs-lookup"><span data-stu-id="59c53-109">You cannot instantiate a resource directly; you must make a subclass that will represent the type of resource being used.</span></span>

<span data-ttu-id="59c53-110">Este recurso almacena las propiedades comunes en todos los tipos de recursos.</span><span class="sxs-lookup"><span data-stu-id="59c53-110">This resource stores the common properties across all resource types.</span></span>


## <a name="properties"></a><span data-ttu-id="59c53-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="59c53-111">Properties</span></span>
| <span data-ttu-id="59c53-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59c53-112">Property</span></span>     | <span data-ttu-id="59c53-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="59c53-113">Type</span></span>   |<span data-ttu-id="59c53-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="59c53-114">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="59c53-115">createdBy</span><span class="sxs-lookup"><span data-stu-id="59c53-115">createdBy</span></span>|[<span data-ttu-id="59c53-116">identitySet</span><span class="sxs-lookup"><span data-stu-id="59c53-116">identitySet</span></span>](identityset.md)|<span data-ttu-id="59c53-117">Quién creó el recurso.</span><span class="sxs-lookup"><span data-stu-id="59c53-117">Who created the resource.</span></span>|
|<span data-ttu-id="59c53-118">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="59c53-118">createdDateTime</span></span>|<span data-ttu-id="59c53-119">Momento en el tiempo cuando se creó el recurso.</span><span class="sxs-lookup"><span data-stu-id="59c53-119">Moment in time when the resource was created.</span></span>  <span data-ttu-id="59c53-120">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="59c53-120">DateTimeOffset</span></span>|<span data-ttu-id="59c53-p105">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="59c53-p105">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="59c53-123">displayName</span><span class="sxs-lookup"><span data-stu-id="59c53-123">displayName</span></span>|<span data-ttu-id="59c53-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="59c53-124">String</span></span>|<span data-ttu-id="59c53-125">Nombre para mostrar del recurso.</span><span class="sxs-lookup"><span data-stu-id="59c53-125">Display name of resource.</span></span>|
|<span data-ttu-id="59c53-126">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="59c53-126">lastModifiedBy</span></span>|[<span data-ttu-id="59c53-127">identitySet</span><span class="sxs-lookup"><span data-stu-id="59c53-127">identitySet</span></span>](identityset.md)|<span data-ttu-id="59c53-128">¿Quién fue el último usuario para modificar el recurso.</span><span class="sxs-lookup"><span data-stu-id="59c53-128">Who was the last user to modify the resource.</span></span>|
|<span data-ttu-id="59c53-129">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="59c53-129">lastModifiedDateTime</span></span>|<span data-ttu-id="59c53-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="59c53-130">DateTimeOffset</span></span>|<span data-ttu-id="59c53-131">Momento en el tiempo cuando se modificó por última vez el recurso.</span><span class="sxs-lookup"><span data-stu-id="59c53-131">Moment in time when the resource was last modified.</span></span>  <span data-ttu-id="59c53-132">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC.</span><span class="sxs-lookup"><span data-stu-id="59c53-132">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time.</span></span> <span data-ttu-id="59c53-133">Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="59c53-133">For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|

## <a name="json-representation"></a><span data-ttu-id="59c53-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="59c53-134">JSON representation</span></span>

<span data-ttu-id="59c53-135">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="59c53-135">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationResource"
}-->

```json
{
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "displayName": "String",
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
