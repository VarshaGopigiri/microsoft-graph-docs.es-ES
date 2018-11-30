---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: TextColumn
ms.openlocfilehash: 5ff280b6c969d9832e2f81f77dc32237f9905aad
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086638"
---
# <a name="textcolumn-resource-type"></a><span data-ttu-id="6e4b5-102">Tipo de recurso TextColumn</span><span class="sxs-lookup"><span data-stu-id="6e4b5-102">TextColumn resource type</span></span>

> <span data-ttu-id="6e4b5-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6e4b5-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6e4b5-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6e4b5-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6e4b5-105">El recurso **TextColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna son texto.</span><span class="sxs-lookup"><span data-stu-id="6e4b5-105">The **textColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values are text.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6e4b5-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6e4b5-106">JSON representation</span></span>

<span data-ttu-id="6e4b5-107">A continuación se incluye una representación JSON de un recurso **TextColumn**.</span><span class="sxs-lookup"><span data-stu-id="6e4b5-107">Here is a JSON representation of a **textColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.textColumn" } -->

```json
{
  "allowMultipleLines": true,
  "appendChangesToExistingText": false,
  "linesForEditing": 6,
  "maxLength": 300,
  "textType": "plain | richText"
}
```

## <a name="properties"></a><span data-ttu-id="6e4b5-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e4b5-108">Properties</span></span>

| <span data-ttu-id="6e4b5-109">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="6e4b5-109">Property name</span></span>                   | <span data-ttu-id="6e4b5-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e4b5-110">Type</span></span>   | <span data-ttu-id="6e4b5-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e4b5-111">Description</span></span>
|:--------------------------------|:-------|:-----------------------------------------------
| <span data-ttu-id="6e4b5-112">**allowMultipleLines**</span><span class="sxs-lookup"><span data-stu-id="6e4b5-112">**allowMultipleLines**</span></span>          | <span data-ttu-id="6e4b5-113">string</span><span class="sxs-lookup"><span data-stu-id="6e4b5-113">string</span></span> | <span data-ttu-id="6e4b5-114">Si se permiten varias líneas de texto.</span><span class="sxs-lookup"><span data-stu-id="6e4b5-114">Whether to allow multiple lines of text.</span></span>
| <span data-ttu-id="6e4b5-115">**appendChangesToExistingText**</span><span class="sxs-lookup"><span data-stu-id="6e4b5-115">**appendChangesToExistingText**</span></span> | <span data-ttu-id="6e4b5-116">string</span><span class="sxs-lookup"><span data-stu-id="6e4b5-116">string</span></span> | <span data-ttu-id="6e4b5-117">Si las actualizaciones de esta columna deben reemplazar el texto existente o anexarse a este.</span><span class="sxs-lookup"><span data-stu-id="6e4b5-117">Whether updates to this column should replace existing text, or append to it.</span></span>
| <span data-ttu-id="6e4b5-118">**linesForEditing**</span><span class="sxs-lookup"><span data-stu-id="6e4b5-118">**linesForEditing**</span></span>             | <span data-ttu-id="6e4b5-119">int</span><span class="sxs-lookup"><span data-stu-id="6e4b5-119">int</span></span>    | <span data-ttu-id="6e4b5-120">El tamaño del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="6e4b5-120">The size of the text box.</span></span>
| <span data-ttu-id="6e4b5-121">**maxLength**</span><span class="sxs-lookup"><span data-stu-id="6e4b5-121">**maxLength**</span></span>                   | <span data-ttu-id="6e4b5-122">int</span><span class="sxs-lookup"><span data-stu-id="6e4b5-122">int</span></span>    | <span data-ttu-id="6e4b5-123">El número máximo de caracteres del valor.</span><span class="sxs-lookup"><span data-stu-id="6e4b5-123">The maximum number of characters for the value.</span></span>
| <span data-ttu-id="6e4b5-124">**textType**</span><span class="sxs-lookup"><span data-stu-id="6e4b5-124">**textType**</span></span>                    | <span data-ttu-id="6e4b5-125">string</span><span class="sxs-lookup"><span data-stu-id="6e4b5-125">string</span></span> | <span data-ttu-id="6e4b5-126">El tipo de texto que se almacena.</span><span class="sxs-lookup"><span data-stu-id="6e4b5-126">The type of text being stored.</span></span> <span data-ttu-id="6e4b5-127">Debe ser `plain` o `richText`</span><span class="sxs-lookup"><span data-stu-id="6e4b5-127">Must be one of `plain` or `richText`</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/TextColumn"
} -->
