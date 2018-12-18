---
title: Tipo de recurso WorksheetProtection
description: Representa la protección de un objeto de hoja.
author: lumine2008
ms.openlocfilehash: 91415b067fbe54333e32d1a2ed84bce5025b7d3a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339210"
---
# <a name="worksheetprotection-resource-type"></a><span data-ttu-id="15359-103">Tipo de recurso WorksheetProtection</span><span class="sxs-lookup"><span data-stu-id="15359-103">WorksheetProtection resource type</span></span>

> <span data-ttu-id="15359-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="15359-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="15359-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="15359-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="15359-106">Representa la protección de un objeto de hoja.</span><span class="sxs-lookup"><span data-stu-id="15359-106">Represents the protection of a sheet object.</span></span>


## <a name="methods"></a><span data-ttu-id="15359-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="15359-107">Methods</span></span>

| <span data-ttu-id="15359-108">Método</span><span class="sxs-lookup"><span data-stu-id="15359-108">Method</span></span>           | <span data-ttu-id="15359-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="15359-109">Return Type</span></span>    |<span data-ttu-id="15359-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="15359-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="15359-111">Get WorksheetProtection</span><span class="sxs-lookup"><span data-stu-id="15359-111">Get WorksheetProtection</span></span>](../api/worksheetprotection-get.md) | [<span data-ttu-id="15359-112">WorksheetProtection</span><span class="sxs-lookup"><span data-stu-id="15359-112">WorksheetProtection</span></span>](worksheetprotection.md) |<span data-ttu-id="15359-113">Lee las propiedades y relaciones del objeto worksheetProtection.</span><span class="sxs-lookup"><span data-stu-id="15359-113">Read properties and relationships of worksheetProtection object.</span></span>|
|[<span data-ttu-id="15359-114">Protect</span><span class="sxs-lookup"><span data-stu-id="15359-114">Protect</span></span>](../api/worksheetprotection-protect.md)|<span data-ttu-id="15359-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="15359-115">None</span></span>|<span data-ttu-id="15359-p102">Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="15359-p102">Protect a worksheet. It throws if the worksheet has been protected.</span></span>|
|[<span data-ttu-id="15359-118">Unprotect</span><span class="sxs-lookup"><span data-stu-id="15359-118">Unprotect</span></span>](../api/worksheetprotection-unprotect.md)|<span data-ttu-id="15359-119">None</span><span class="sxs-lookup"><span data-stu-id="15359-119">None</span></span>|<span data-ttu-id="15359-120">Desprotege una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="15359-120">Unprotect a worksheet</span></span>|

## <a name="properties"></a><span data-ttu-id="15359-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15359-121">Properties</span></span>
| <span data-ttu-id="15359-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="15359-122">Property</span></span>     | <span data-ttu-id="15359-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="15359-123">Type</span></span>   |<span data-ttu-id="15359-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="15359-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="15359-125">protected</span><span class="sxs-lookup"><span data-stu-id="15359-125">protected</span></span>|<span data-ttu-id="15359-126">boolean</span><span class="sxs-lookup"><span data-stu-id="15359-126">boolean</span></span>|<span data-ttu-id="15359-p103">Indica si la hoja de cálculo está protegida.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="15359-p103">Indicates if the worksheet is protected.  Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="15359-129">Relaciones</span><span class="sxs-lookup"><span data-stu-id="15359-129">Relationships</span></span>
| <span data-ttu-id="15359-130">Relación</span><span class="sxs-lookup"><span data-stu-id="15359-130">Relationship</span></span> | <span data-ttu-id="15359-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="15359-131">Type</span></span>   |<span data-ttu-id="15359-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="15359-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="15359-133">opciones</span><span class="sxs-lookup"><span data-stu-id="15359-133">options</span></span>|[<span data-ttu-id="15359-134">WorksheetProtectionOptions</span><span class="sxs-lookup"><span data-stu-id="15359-134">WorksheetProtectionOptions</span></span>](worksheetprotectionoptions.md)|<span data-ttu-id="15359-p104">Opciones de protección de la hoja. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="15359-p104">Sheet protection options. Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="15359-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="15359-137">JSON representation</span></span>

<span data-ttu-id="15359-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="15359-138">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.worksheetProtection"
}-->

```json
{
  "protected": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "WorksheetProtection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->