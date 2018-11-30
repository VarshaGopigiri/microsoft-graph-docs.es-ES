---
title: Tipo de recurso de aplicación
description: Representa la aplicación de Excel que administra el libro.
ms.openlocfilehash: 1772d69b55d03bf62d983a6dfb818dca651ebbd6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086373"
---
# <a name="application-resource-type"></a><span data-ttu-id="9b78e-103">Tipo de recurso de aplicación</span><span class="sxs-lookup"><span data-stu-id="9b78e-103">Application resource type</span></span>

> <span data-ttu-id="9b78e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9b78e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9b78e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9b78e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="9b78e-106">Representa la aplicación de Excel que administra el libro.</span><span class="sxs-lookup"><span data-stu-id="9b78e-106">Represents the Excel application that manages the workbook.</span></span>


## <a name="methods"></a><span data-ttu-id="9b78e-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="9b78e-107">Methods</span></span>

| <span data-ttu-id="9b78e-108">Método</span><span class="sxs-lookup"><span data-stu-id="9b78e-108">Method</span></span>           | <span data-ttu-id="9b78e-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b78e-109">Return Type</span></span>    |<span data-ttu-id="9b78e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b78e-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9b78e-111">Obtener la aplicación</span><span class="sxs-lookup"><span data-stu-id="9b78e-111">Get Application</span></span>](../api/excelapplication-get.md) | [<span data-ttu-id="9b78e-112">Application</span><span class="sxs-lookup"><span data-stu-id="9b78e-112">Application</span></span>](application.md) |<span data-ttu-id="9b78e-113">Leer las propiedades y las relaciones del objeto application.</span><span class="sxs-lookup"><span data-stu-id="9b78e-113">Read properties and relationships of application object.</span></span>|
|[<span data-ttu-id="9b78e-114">Calculate</span><span class="sxs-lookup"><span data-stu-id="9b78e-114">Calculate</span></span>](../api/excelapplication-calculate.md)|<span data-ttu-id="9b78e-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9b78e-115">None</span></span>|<span data-ttu-id="9b78e-116">Recalcula todos los libros abiertos actualmente en Excel.</span><span class="sxs-lookup"><span data-stu-id="9b78e-116">Recalculate all currently opened workbooks in Excel.</span></span>|

## <a name="properties"></a><span data-ttu-id="9b78e-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b78e-117">Properties</span></span>
| <span data-ttu-id="9b78e-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9b78e-118">Property</span></span>     | <span data-ttu-id="9b78e-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="9b78e-119">Type</span></span>   |<span data-ttu-id="9b78e-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9b78e-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9b78e-121">calculationMode</span><span class="sxs-lookup"><span data-stu-id="9b78e-121">calculationMode</span></span>|<span data-ttu-id="9b78e-122">string</span><span class="sxs-lookup"><span data-stu-id="9b78e-122">string</span></span>|<span data-ttu-id="9b78e-123">Devuelve el modo de cálculo que se usa en el libro.</span><span class="sxs-lookup"><span data-stu-id="9b78e-123">Returns the calculation mode used in the workbook.</span></span> <span data-ttu-id="9b78e-124">Los valores posibles son: `Automatic`, `AutomaticExceptTables` y `Manual`.</span><span class="sxs-lookup"><span data-stu-id="9b78e-124">Possible values are: `Automatic`, `AutomaticExceptTables`, `Manual`.</span></span> <span data-ttu-id="9b78e-125">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9b78e-125">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9b78e-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9b78e-126">Relationships</span></span>
<span data-ttu-id="9b78e-127">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9b78e-127">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="9b78e-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9b78e-128">JSON representation</span></span>

<span data-ttu-id="9b78e-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9b78e-129">Here is a JSON representation of the resource.</span></span>

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