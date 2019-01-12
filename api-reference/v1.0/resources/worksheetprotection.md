---
title: Tipo de recurso WorksheetProtection
description: Representa la protección de un objeto de hoja.
author: lumine2008
localization_priority: Normal
ms.prod: excel
ms.openlocfilehash: c8a719d1be9f21edf1bef82d2aa058b45bbf2df8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27984237"
---
# <a name="worksheetprotection-resource-type"></a><span data-ttu-id="0becd-103">Tipo de recurso WorksheetProtection</span><span class="sxs-lookup"><span data-stu-id="0becd-103">WorksheetProtection resource type</span></span>

<span data-ttu-id="0becd-104">Representa la protección de un objeto de hoja.</span><span class="sxs-lookup"><span data-stu-id="0becd-104">Represents the protection of a sheet object.</span></span>


## <a name="methods"></a><span data-ttu-id="0becd-105">Métodos</span><span class="sxs-lookup"><span data-stu-id="0becd-105">Methods</span></span>

| <span data-ttu-id="0becd-106">Método</span><span class="sxs-lookup"><span data-stu-id="0becd-106">Method</span></span>           | <span data-ttu-id="0becd-107">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0becd-107">Return Type</span></span>    |<span data-ttu-id="0becd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0becd-108">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="0becd-109">Get WorksheetProtection</span><span class="sxs-lookup"><span data-stu-id="0becd-109">Get WorksheetProtection</span></span>](../api/worksheetprotection-get.md) | [<span data-ttu-id="0becd-110">WorkbookWorksheetProtection</span><span class="sxs-lookup"><span data-stu-id="0becd-110">WorkbookWorksheetProtection</span></span>](worksheetprotection.md) |<span data-ttu-id="0becd-111">Lee las propiedades y relaciones del objeto worksheetProtection.</span><span class="sxs-lookup"><span data-stu-id="0becd-111">Read properties and relationships of worksheetProtection object.</span></span>|
|[<span data-ttu-id="0becd-112">Protect</span><span class="sxs-lookup"><span data-stu-id="0becd-112">Protect</span></span>](../api/worksheetprotection-protect.md)|<span data-ttu-id="0becd-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0becd-113">None</span></span>|<span data-ttu-id="0becd-p101">Proteger una hoja de cálculo. Produce una excepción si se ha protegido la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0becd-p101">Protect a worksheet. It throws if the worksheet has been protected.</span></span>|
|[<span data-ttu-id="0becd-116">Unprotect</span><span class="sxs-lookup"><span data-stu-id="0becd-116">Unprotect</span></span>](../api/worksheetprotection-unprotect.md)|<span data-ttu-id="0becd-117">None</span><span class="sxs-lookup"><span data-stu-id="0becd-117">None</span></span>|<span data-ttu-id="0becd-118">Desprotege una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0becd-118">Unprotect a worksheet</span></span>|

## <a name="properties"></a><span data-ttu-id="0becd-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0becd-119">Properties</span></span>
| <span data-ttu-id="0becd-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0becd-120">Property</span></span>     | <span data-ttu-id="0becd-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="0becd-121">Type</span></span>   |<span data-ttu-id="0becd-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="0becd-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0becd-123">opciones</span><span class="sxs-lookup"><span data-stu-id="0becd-123">options</span></span>|[<span data-ttu-id="0becd-124">WorkbookWorksheetProtectionOptions</span><span class="sxs-lookup"><span data-stu-id="0becd-124">WorkbookWorksheetProtectionOptions</span></span>](worksheetprotectionoptions.md)|<span data-ttu-id="0becd-p102">Opciones de protección de la hoja. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0becd-p102">Sheet protection options. Read-only.</span></span>|
|<span data-ttu-id="0becd-127">protected</span><span class="sxs-lookup"><span data-stu-id="0becd-127">protected</span></span>|<span data-ttu-id="0becd-128">boolean</span><span class="sxs-lookup"><span data-stu-id="0becd-128">boolean</span></span>|<span data-ttu-id="0becd-p103">Indica si la hoja de cálculo está protegida.  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0becd-p103">Indicates if the worksheet is protected.  Read-only.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0becd-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0becd-131">JSON representation</span></span>

<span data-ttu-id="0becd-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0becd-132">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.workbookWorksheetProtection"
}-->

```json
{
  "protected": true,
  "options": { "@odata.type": "microsoft.graph.workbookWorksheetProtectionOptions" }
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
