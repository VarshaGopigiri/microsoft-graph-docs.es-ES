---
title: Tipo de recurso de aplicación
description: Representa la aplicación de Excel que administra el libro.
localization_priority: Normal
author: lumine2008
ms.prod: excel
ms.openlocfilehash: 250141ff6c6da3a81a1b3492908bc2e04b5a0605
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27921979"
---
# <a name="application-resource-type"></a><span data-ttu-id="e363d-103">Tipo de recurso de aplicación</span><span class="sxs-lookup"><span data-stu-id="e363d-103">Application resource type</span></span>

> <span data-ttu-id="e363d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="e363d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="e363d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="e363d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="e363d-106">Representa la aplicación de Excel que administra el libro.</span><span class="sxs-lookup"><span data-stu-id="e363d-106">Represents the Excel application that manages the workbook.</span></span>


## <a name="methods"></a><span data-ttu-id="e363d-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="e363d-107">Methods</span></span>

| <span data-ttu-id="e363d-108">Método</span><span class="sxs-lookup"><span data-stu-id="e363d-108">Method</span></span>           | <span data-ttu-id="e363d-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e363d-109">Return Type</span></span>    |<span data-ttu-id="e363d-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e363d-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="e363d-111">Obtener la aplicación</span><span class="sxs-lookup"><span data-stu-id="e363d-111">Get Application</span></span>](../api/excelapplication-get.md) | [<span data-ttu-id="e363d-112">Application</span><span class="sxs-lookup"><span data-stu-id="e363d-112">Application</span></span>](application.md) |<span data-ttu-id="e363d-113">Leer las propiedades y las relaciones del objeto application.</span><span class="sxs-lookup"><span data-stu-id="e363d-113">Read properties and relationships of application object.</span></span>|
|[<span data-ttu-id="e363d-114">Calculate</span><span class="sxs-lookup"><span data-stu-id="e363d-114">Calculate</span></span>](../api/excelapplication-calculate.md)|<span data-ttu-id="e363d-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e363d-115">None</span></span>|<span data-ttu-id="e363d-116">Recalcula todos los libros abiertos actualmente en Excel.</span><span class="sxs-lookup"><span data-stu-id="e363d-116">Recalculate all currently opened workbooks in Excel.</span></span>|

## <a name="properties"></a><span data-ttu-id="e363d-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e363d-117">Properties</span></span>
| <span data-ttu-id="e363d-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e363d-118">Property</span></span>     | <span data-ttu-id="e363d-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="e363d-119">Type</span></span>   |<span data-ttu-id="e363d-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e363d-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e363d-121">calculationMode</span><span class="sxs-lookup"><span data-stu-id="e363d-121">calculationMode</span></span>|<span data-ttu-id="e363d-122">string</span><span class="sxs-lookup"><span data-stu-id="e363d-122">string</span></span>|<span data-ttu-id="e363d-123">Devuelve el modo de cálculo que se usa en el libro.</span><span class="sxs-lookup"><span data-stu-id="e363d-123">Returns the calculation mode used in the workbook.</span></span> <span data-ttu-id="e363d-124">Los valores posibles son: `Automatic`, `AutomaticExceptTables` y `Manual`.</span><span class="sxs-lookup"><span data-stu-id="e363d-124">Possible values are: `Automatic`, `AutomaticExceptTables`, `Manual`.</span></span> <span data-ttu-id="e363d-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e363d-125">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e363d-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e363d-126">Relationships</span></span>
<span data-ttu-id="e363d-127">Ninguno</span><span class="sxs-lookup"><span data-stu-id="e363d-127">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="e363d-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e363d-128">JSON representation</span></span>

<span data-ttu-id="e363d-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e363d-129">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.application"
}-->

```json
{
  "calculationMode": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Application resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
