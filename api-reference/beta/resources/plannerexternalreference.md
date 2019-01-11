---
title: Tipo de recurso plannerExternalReference
description: El recurso **plannerExternalReference** representa los metadatos de una referencia (los datos adjuntos como archivo, la dirección URL). Es el valor de pares de valor de la propiedad en el objeto externalReferences.
localization_priority: Normal
ms.openlocfilehash: 104fd17698d57339de5c0d7a2ec4c5f42b254f49
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833787"
---
# <a name="plannerexternalreference-resource-type"></a><span data-ttu-id="34d98-104">Tipo de recurso plannerExternalReference</span><span class="sxs-lookup"><span data-stu-id="34d98-104">plannerExternalReference resource type</span></span>

> <span data-ttu-id="34d98-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="34d98-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="34d98-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="34d98-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="34d98-p103">El recurso **plannerExternalReference** representa los metadatos de una referencia (datos adjuntos como archivo, URL, etc.). Es el valor de los pares propiedad-valor del objeto [externalReferences](plannerexternalreferences.md).</span><span class="sxs-lookup"><span data-stu-id="34d98-p103">The **plannerExternalReference** resource represents the metadata of a reference (attachments such as file, URL). It is the value of property-value pairs in the [externalReferences object](plannerexternalreferences.md).</span></span>



## <a name="properties"></a><span data-ttu-id="34d98-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="34d98-109">Properties</span></span>
| <span data-ttu-id="34d98-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="34d98-110">Property</span></span>     | <span data-ttu-id="34d98-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="34d98-111">Type</span></span>   |<span data-ttu-id="34d98-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="34d98-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="34d98-113">alias</span><span class="sxs-lookup"><span data-stu-id="34d98-113">alias</span></span>|<span data-ttu-id="34d98-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="34d98-114">String</span></span>|<span data-ttu-id="34d98-115">Nombre de alias para describir la referencia.</span><span class="sxs-lookup"><span data-stu-id="34d98-115">A name alias to describe the reference.</span></span>|
|<span data-ttu-id="34d98-116">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="34d98-116">lastModifiedBy</span></span>|[<span data-ttu-id="34d98-117">identitySet</span><span class="sxs-lookup"><span data-stu-id="34d98-117">identitySet</span></span>](identityset.md)|<span data-ttu-id="34d98-p104">Solo lectura. Id. del usuario que lo modificó por última vez.</span><span class="sxs-lookup"><span data-stu-id="34d98-p104">Read-only. User ID by which this is last modified.</span></span>|
|<span data-ttu-id="34d98-120">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="34d98-120">lastModifiedDateTime</span></span>|<span data-ttu-id="34d98-121">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="34d98-121">DateTimeOffset</span></span>|<span data-ttu-id="34d98-p105">Solo lectura. Fecha y hora en que se modificó por última vez. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, la medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="34d98-p105">Read-only. Date and time at which this is last modified. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="34d98-126">previewPriority</span><span class="sxs-lookup"><span data-stu-id="34d98-126">previewPriority</span></span>|<span data-ttu-id="34d98-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="34d98-127">String</span></span>|<span data-ttu-id="34d98-128">Se usa para establecer el orden de prioridad relativo en el que aparecerá la referencia como una vista previa de la tarea.</span><span class="sxs-lookup"><span data-stu-id="34d98-128">Used to set the relative priority order in which the reference will be shown as a preview on the task.</span></span>|
|<span data-ttu-id="34d98-129">tipo</span><span class="sxs-lookup"><span data-stu-id="34d98-129">type</span></span>|<span data-ttu-id="34d98-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="34d98-130">String</span></span>|<span data-ttu-id="34d98-p106">Se usa para describir el tipo de la referencia. Los tipos son `PowerPoint`, `Word`, `Excel` y `Other`.</span><span class="sxs-lookup"><span data-stu-id="34d98-p106">Used to describe the type of the reference. Types include: `PowerPoint`, `Word`, `Excel`, `Other`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="34d98-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="34d98-133">JSON representation</span></span>
<span data-ttu-id="34d98-134">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="34d98-134">Here is a JSON representation of the resource.</span></span>

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
