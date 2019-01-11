---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: TextColumn
localization_priority: Normal
ms.openlocfilehash: d064253cfad141d5879afb52451ca28fa2aeca67
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860882"
---
# <a name="textcolumn-resource-type"></a><span data-ttu-id="3526b-102">Tipo de recurso TextColumn</span><span class="sxs-lookup"><span data-stu-id="3526b-102">TextColumn resource type</span></span>

<span data-ttu-id="3526b-103">El recurso **TextColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna son texto.</span><span class="sxs-lookup"><span data-stu-id="3526b-103">The **textColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values are text.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3526b-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3526b-104">JSON representation</span></span>

<span data-ttu-id="3526b-105">A continuación se incluye una representación JSON de un recurso **TextColumn**.</span><span class="sxs-lookup"><span data-stu-id="3526b-105">Here is a JSON representation of a **textColumn** resource.</span></span>
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

## <a name="properties"></a><span data-ttu-id="3526b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3526b-106">Properties</span></span>

| <span data-ttu-id="3526b-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="3526b-107">Property name</span></span>                   | <span data-ttu-id="3526b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3526b-108">Type</span></span>    | <span data-ttu-id="3526b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3526b-109">Description</span></span>
|:--------------------------------|:--------|:---------------------------------
| <span data-ttu-id="3526b-110">**allowMultipleLines**</span><span class="sxs-lookup"><span data-stu-id="3526b-110">**allowMultipleLines**</span></span>          | <span data-ttu-id="3526b-111">boolean</span><span class="sxs-lookup"><span data-stu-id="3526b-111">boolean</span></span> | <span data-ttu-id="3526b-112">Si se permiten varias líneas de texto.</span><span class="sxs-lookup"><span data-stu-id="3526b-112">Whether to allow multiple lines of text.</span></span>
| <span data-ttu-id="3526b-113">**appendChangesToExistingText**</span><span class="sxs-lookup"><span data-stu-id="3526b-113">**appendChangesToExistingText**</span></span> | <span data-ttu-id="3526b-114">boolean</span><span class="sxs-lookup"><span data-stu-id="3526b-114">boolean</span></span> | <span data-ttu-id="3526b-115">Si las actualizaciones de esta columna deben reemplazar el texto existente o anexarse a este.</span><span class="sxs-lookup"><span data-stu-id="3526b-115">Whether updates to this column should replace existing text, or append to it.</span></span>
| <span data-ttu-id="3526b-116">**linesForEditing**</span><span class="sxs-lookup"><span data-stu-id="3526b-116">**linesForEditing**</span></span>             | <span data-ttu-id="3526b-117">int32</span><span class="sxs-lookup"><span data-stu-id="3526b-117">int32</span></span>   | <span data-ttu-id="3526b-118">El tamaño del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="3526b-118">The size of the text box.</span></span>
| <span data-ttu-id="3526b-119">**maxLength**</span><span class="sxs-lookup"><span data-stu-id="3526b-119">**maxLength**</span></span>                   | <span data-ttu-id="3526b-120">int32</span><span class="sxs-lookup"><span data-stu-id="3526b-120">int32</span></span>   | <span data-ttu-id="3526b-121">El número máximo de caracteres del valor.</span><span class="sxs-lookup"><span data-stu-id="3526b-121">The maximum number of characters for the value.</span></span>
| <span data-ttu-id="3526b-122">**textType**</span><span class="sxs-lookup"><span data-stu-id="3526b-122">**textType**</span></span>                    | <span data-ttu-id="3526b-123">string</span><span class="sxs-lookup"><span data-stu-id="3526b-123">string</span></span>  | <span data-ttu-id="3526b-124">El tipo de texto que se almacena.</span><span class="sxs-lookup"><span data-stu-id="3526b-124">The type of text being stored.</span></span> <span data-ttu-id="3526b-125">Debe ser `plain` o `richText`</span><span class="sxs-lookup"><span data-stu-id="3526b-125">Must be one of `plain` or `richText`</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/textcolumn.md:
      Found potential enums in resource example that weren't defined in a table:(plain,richText) are in resource, but () are in table"
  ],
  "tocPath": "Resources/TextColumn"
} -->
