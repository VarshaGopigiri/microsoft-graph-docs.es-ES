---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: TextColumn
ms.openlocfilehash: 80e41b379b9b4ce51a3ee6c910447a22f43356c3
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="textcolumn-resource-type"></a><span data-ttu-id="6beba-102">Tipo de recurso TextColumn</span><span class="sxs-lookup"><span data-stu-id="6beba-102">TextColumn resource type</span></span>

<span data-ttu-id="6beba-103">El recurso **TextColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna son texto.</span><span class="sxs-lookup"><span data-stu-id="6beba-103">The **textColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's values are text.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6beba-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6beba-104">JSON representation</span></span>

<span data-ttu-id="6beba-105">A continuación se incluye una representación JSON de un recurso **TextColumn**.</span><span class="sxs-lookup"><span data-stu-id="6beba-105">Here is a JSON representation of a **baseItem** resource.</span></span>
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

## <a name="properties"></a><span data-ttu-id="6beba-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6beba-106">Properties</span></span>

| <span data-ttu-id="6beba-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="6beba-107">Property name</span></span>                   | <span data-ttu-id="6beba-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="6beba-108">Type</span></span>   | <span data-ttu-id="6beba-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="6beba-109">Description</span></span>
|:--------------------------------|:-------|:-----------------------------------------------
| <span data-ttu-id="6beba-110">**allowMultipleLines**</span><span class="sxs-lookup"><span data-stu-id="6beba-110">**allowMultipleLines**</span></span>          | <span data-ttu-id="6beba-111">string</span><span class="sxs-lookup"><span data-stu-id="6beba-111">string</span></span> | <span data-ttu-id="6beba-112">Si se permiten varias líneas de texto.</span><span class="sxs-lookup"><span data-stu-id="6beba-112">Whether to allow multiple lines of text.</span></span>
| <span data-ttu-id="6beba-113">**appendChangesToExistingText**</span><span class="sxs-lookup"><span data-stu-id="6beba-113">**appendChangesToExistingText**</span></span> | <span data-ttu-id="6beba-114">string</span><span class="sxs-lookup"><span data-stu-id="6beba-114">string</span></span> | <span data-ttu-id="6beba-115">Si las actualizaciones de esta columna deben reemplazar el texto existente o anexarse a este.</span><span class="sxs-lookup"><span data-stu-id="6beba-115">Whether updates to this column should replace existing text, or append to it.</span></span>
| <span data-ttu-id="6beba-116">**linesForEditing**</span><span class="sxs-lookup"><span data-stu-id="6beba-116">**linesForEditing**</span></span>             | <span data-ttu-id="6beba-117">int</span><span class="sxs-lookup"><span data-stu-id="6beba-117">int</span></span>    | <span data-ttu-id="6beba-118">El tamaño del cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="6beba-118">The size of the text box.</span></span>
| <span data-ttu-id="6beba-119">**maxLength**</span><span class="sxs-lookup"><span data-stu-id="6beba-119">**maxLength**</span></span>                   | <span data-ttu-id="6beba-120">int</span><span class="sxs-lookup"><span data-stu-id="6beba-120">int</span></span>    | <span data-ttu-id="6beba-121">El número máximo de caracteres del valor.</span><span class="sxs-lookup"><span data-stu-id="6beba-121">The maximum number of characters for the value.</span></span>
| <span data-ttu-id="6beba-122">**textType**</span><span class="sxs-lookup"><span data-stu-id="6beba-122">**textType**</span></span>                    | <span data-ttu-id="6beba-123">string</span><span class="sxs-lookup"><span data-stu-id="6beba-123">string</span></span> | <span data-ttu-id="6beba-124">El tipo de texto que se almacena.</span><span class="sxs-lookup"><span data-stu-id="6beba-124">The type of text being stored.</span></span> <span data-ttu-id="6beba-125">Debe ser `plain` o `richText`</span><span class="sxs-lookup"><span data-stu-id="6beba-125">Must be one of `plain` or `richText`</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/TextColumn"
} -->
