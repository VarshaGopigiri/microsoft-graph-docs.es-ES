---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: LookupColumn
localization_priority: Normal
ms.openlocfilehash: 41e643019d842a365c333efa3c3a6861c51a7fc7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892103"
---
# <a name="lookupcolumn-resource-type"></a><span data-ttu-id="cb3be-102">Tipo de recurso LookupColumn</span><span class="sxs-lookup"><span data-stu-id="cb3be-102">LookupColumn resource type</span></span>

<span data-ttu-id="cb3be-103">El recurso **lookupColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna se buscan desde otro origen en el sitio.</span><span class="sxs-lookup"><span data-stu-id="cb3be-103">The **lookupColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values are looked up from another source in the site.</span></span>

## <a name="json-representation"></a><span data-ttu-id="cb3be-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cb3be-104">JSON representation</span></span>

<span data-ttu-id="cb3be-105">A continuación se incluye una representación JSON de un recurso **LookupColumn**.</span><span class="sxs-lookup"><span data-stu-id="cb3be-105">Here is a JSON representation of a **lookupColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.lookupColumn" } -->

```json
{
  "allowMultipleValues": true,
  "allowUnlimitedLength": false,
  "columnName": "string",
  "listId": "string",
  "primaryLookupColumnId": "string"
}
```

## <a name="properties"></a><span data-ttu-id="cb3be-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb3be-106">Properties</span></span>

| <span data-ttu-id="cb3be-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="cb3be-107">Property name</span></span>             | <span data-ttu-id="cb3be-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb3be-108">Type</span></span>    | <span data-ttu-id="cb3be-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb3be-109">Description</span></span>
|:--------------------------|:--------|:---------------------------------------
| <span data-ttu-id="cb3be-110">**allowMultipleValues**</span><span class="sxs-lookup"><span data-stu-id="cb3be-110">**allowMultipleValues**</span></span>   | <span data-ttu-id="cb3be-111">boolean</span><span class="sxs-lookup"><span data-stu-id="cb3be-111">boolean</span></span> | <span data-ttu-id="cb3be-112">Indica si se pueden seleccionar varios valores desde el origen.</span><span class="sxs-lookup"><span data-stu-id="cb3be-112">Indicates whether multiple values can be selected from the source.</span></span>
| <span data-ttu-id="cb3be-113">**allowUnlimitedLength**</span><span class="sxs-lookup"><span data-stu-id="cb3be-113">**allowUnlimitedLength**</span></span>  | <span data-ttu-id="cb3be-114">boolean</span><span class="sxs-lookup"><span data-stu-id="cb3be-114">boolean</span></span> | <span data-ttu-id="cb3be-115">Indica si los valores de la columna deben poder superar el límite estándar de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="cb3be-115">Indicates whether values in the column should be able to exceed the standard limit of 255 characters.</span></span>
| <span data-ttu-id="cb3be-116">**columnName**</span><span class="sxs-lookup"><span data-stu-id="cb3be-116">**columnName**</span></span>            | <span data-ttu-id="cb3be-117">string</span><span class="sxs-lookup"><span data-stu-id="cb3be-117">string</span></span>  | <span data-ttu-id="cb3be-118">El nombre de la columna de origen de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cb3be-118">The name of the lookup source column.</span></span>
| <span data-ttu-id="cb3be-119">**listId**</span><span class="sxs-lookup"><span data-stu-id="cb3be-119">**listId**</span></span>                | <span data-ttu-id="cb3be-120">string</span><span class="sxs-lookup"><span data-stu-id="cb3be-120">string</span></span>  | <span data-ttu-id="cb3be-121">El identificador único de la lista de origen de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="cb3be-121">The unique identifier of the lookup source list.</span></span>
| <span data-ttu-id="cb3be-122">**primaryLookupColumnId**</span><span class="sxs-lookup"><span data-stu-id="cb3be-122">**primaryLookupColumnId**</span></span> | <span data-ttu-id="cb3be-123">string</span><span class="sxs-lookup"><span data-stu-id="cb3be-123">string</span></span>  | <span data-ttu-id="cb3be-124">Si se especifica, esta columna es una *búsqueda secundaria*, que extrae un campo adicional del elemento de lista devuelto por la *búsqueda principal*.</span><span class="sxs-lookup"><span data-stu-id="cb3be-124">If specified, this column is a *secondary lookup*, pulling an additional field from the list item looked up by the *primary lookup*.</span></span> <span data-ttu-id="cb3be-125">Use el elemento de lista buscado en la búsqueda *principal* como origen de la columna indicada aquí.</span><span class="sxs-lookup"><span data-stu-id="cb3be-125">Use the list item looked up by the *primary* as the source for the column named here.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/LookupColumn"
} -->
