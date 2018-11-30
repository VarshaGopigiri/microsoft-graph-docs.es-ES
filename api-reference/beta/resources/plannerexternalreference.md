---
title: Tipo de recurso plannerExternalReference
description: El recurso **plannerExternalReference** representa los metadatos de una referencia (los datos adjuntos como archivo, la dirección URL). Es el valor de pares de valor de la propiedad en el objeto externalReferences.
ms.openlocfilehash: ad892b5e9f9a741e7a4994c509ac704ad1ca62a6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084069"
---
# <a name="plannerexternalreference-resource-type"></a><span data-ttu-id="bea07-104">Tipo de recurso plannerExternalReference</span><span class="sxs-lookup"><span data-stu-id="bea07-104">plannerExternalReference resource type</span></span>

> <span data-ttu-id="bea07-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bea07-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bea07-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bea07-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bea07-p103">El recurso **plannerExternalReference** representa los metadatos de una referencia (datos adjuntos como archivo, URL, etc.). Es el valor de los pares propiedad-valor del objeto [externalReferences](plannerexternalreferences.md).</span><span class="sxs-lookup"><span data-stu-id="bea07-p103">The **plannerExternalReference** resource represents the metadata of a reference (attachments such as file, URL). It is the value of property-value pairs in the [externalReferences object](plannerexternalreferences.md).</span></span>



## <a name="properties"></a><span data-ttu-id="bea07-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bea07-109">Properties</span></span>
| <span data-ttu-id="bea07-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bea07-110">Property</span></span>     | <span data-ttu-id="bea07-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="bea07-111">Type</span></span>   |<span data-ttu-id="bea07-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bea07-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bea07-113">alias</span><span class="sxs-lookup"><span data-stu-id="bea07-113">alias</span></span>|<span data-ttu-id="bea07-114">String</span><span class="sxs-lookup"><span data-stu-id="bea07-114">String</span></span>|<span data-ttu-id="bea07-115">Nombre de alias para describir la referencia.</span><span class="sxs-lookup"><span data-stu-id="bea07-115">A name alias to describe the reference.</span></span>|
|<span data-ttu-id="bea07-116">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="bea07-116">lastModifiedBy</span></span>|[<span data-ttu-id="bea07-117">identitySet</span><span class="sxs-lookup"><span data-stu-id="bea07-117">identitySet</span></span>](identityset.md)|<span data-ttu-id="bea07-p104">Solo lectura. Id. del usuario que lo modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="bea07-p104">Read-only. User ID by which this is last modified.</span></span>|
|<span data-ttu-id="bea07-120">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="bea07-120">lastModifiedDateTime</span></span>|<span data-ttu-id="bea07-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bea07-121">DateTimeOffset</span></span>|<span data-ttu-id="bea07-p105">Solo lectura. Fecha y hora en que se modificó por última vez. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="bea07-p105">Read-only. Date and time at which this is last modified. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="bea07-126">previewPriority</span><span class="sxs-lookup"><span data-stu-id="bea07-126">previewPriority</span></span>|<span data-ttu-id="bea07-127">String</span><span class="sxs-lookup"><span data-stu-id="bea07-127">String</span></span>|<span data-ttu-id="bea07-128">Se usa para establecer el orden de prioridad relativo en el que aparecerá la referencia como una vista previa de la tarea.</span><span class="sxs-lookup"><span data-stu-id="bea07-128">Used to set the relative priority order in which the reference will be shown as a preview on the task.</span></span>|
|<span data-ttu-id="bea07-129">tipo</span><span class="sxs-lookup"><span data-stu-id="bea07-129">type</span></span>|<span data-ttu-id="bea07-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="bea07-130">String</span></span>|<span data-ttu-id="bea07-p106">Se usa para describir el tipo de la referencia. Los tipos son `PowerPoint`, `Word`, `Excel` y `Other`.</span><span class="sxs-lookup"><span data-stu-id="bea07-p106">Used to describe the type of the reference. Types include: `PowerPoint`, `Word`, `Excel`, `Other`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="bea07-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bea07-133">JSON representation</span></span>
<span data-ttu-id="bea07-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bea07-134">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerExternalReference"
}-->

```json
{
  "alias": "String",
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "previewPriority": "String",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerExternalReference resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->