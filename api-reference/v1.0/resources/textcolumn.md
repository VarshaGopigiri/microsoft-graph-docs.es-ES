---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: TextColumn
ms.openlocfilehash: b5c41091b9193aabc36ee04e9dcc310bfc110af1
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23264290"
---
# <a name="textcolumn-resource-type"></a><span data-ttu-id="29656-102">Tipo de recurso TextColumn</span><span class="sxs-lookup"><span data-stu-id="29656-102">TextColumn resource type</span></span>

<span data-ttu-id="29656-103">El recurso **TextColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna son texto.</span><span class="sxs-lookup"><span data-stu-id="29656-103">The **textColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's values are text.</span></span>

## <a name="json-representation"></a><span data-ttu-id="29656-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="29656-104">JSON representation</span></span>

<span data-ttu-id="29656-105">A continuación se incluye una representación JSON de un recurso **TextColumn**.</span><span class="sxs-lookup"><span data-stu-id="29656-105">Here is a JSON representation of a **textColumn** resource.</span></span>
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

## <a name="properties"></a><span data-ttu-id="29656-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="29656-106">Properties</span></span>

| <span data-ttu-id="29656-107">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="29656-107">Property name</span></span>                   | <span data-ttu-id="29656-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="29656-108">Type</span></span>    | <span data-ttu-id="29656-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="29656-109">Description</span></span>
|:--------------------------------|:--------|:---------------------------------
| <span data-ttu-id="29656-110">**allowMultipleLines**</span><span class="sxs-lookup"><span data-stu-id="29656-110">**allowMultipleLines**</span></span>          | <span data-ttu-id="29656-111">booleano</span><span class="sxs-lookup"><span data-stu-id="29656-111">boolean</span></span> | <span data-ttu-id="29656-112">Si se permiten varias líneas de texto.</span><span class="sxs-lookup"><span data-stu-id="29656-112">Whether to allow multiple lines of text.</span></span>
| <span data-ttu-id="29656-113">**appendChangesToExistingText**</span><span class="sxs-lookup"><span data-stu-id="29656-113">**appendChangesToExistingText**</span></span> | <span data-ttu-id="29656-114">booleano</span><span class="sxs-lookup"><span data-stu-id="29656-114">boolean</span></span> | <span data-ttu-id="29656-115">Si las actualizaciones de esta columna deben reemplazar el texto existente o anexarse a este.</span><span class="sxs-lookup"><span data-stu-id="29656-115">Whether updates to this column should replace existing text, or append to it.</span></span>
| <span data-ttu-id="29656-116">**linesForEditing**</span><span class="sxs-lookup"><span data-stu-id="29656-116">**linesForEditing**</span></span>             | <span data-ttu-id="29656-117">int32</span><span class="sxs-lookup"><span data-stu-id="29656-117">int32</span></span>   | <span data-ttu-id="29656-118">El tamaño del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="29656-118">The size of the text box.</span></span>
| <span data-ttu-id="29656-119">**maxLength**</span><span class="sxs-lookup"><span data-stu-id="29656-119">**maxLength**</span></span>                   | <span data-ttu-id="29656-120">int32</span><span class="sxs-lookup"><span data-stu-id="29656-120">int32</span></span>   | <span data-ttu-id="29656-121">El número máximo de caracteres del valor.</span><span class="sxs-lookup"><span data-stu-id="29656-121">The maximum number of characters for the value.</span></span>
| <span data-ttu-id="29656-122">**textType**</span><span class="sxs-lookup"><span data-stu-id="29656-122">**textType**</span></span>                    | <span data-ttu-id="29656-123">cadena</span><span class="sxs-lookup"><span data-stu-id="29656-123">string</span></span>  | <span data-ttu-id="29656-124">El tipo de texto que se almacena.</span><span class="sxs-lookup"><span data-stu-id="29656-124">The type of text being stored.</span></span> <span data-ttu-id="29656-125">Debe ser `plain` o `richText`</span><span class="sxs-lookup"><span data-stu-id="29656-125">Must be one of `plain` or `richText`</span></span>

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
