---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: LookupColumn
ms.openlocfilehash: 07dba3c223ffc3993be1fc284572810a7aa3ccf8
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="lookupcolumn-resource-type"></a><span data-ttu-id="5a703-102">Tipo de recurso LookupColumn</span><span class="sxs-lookup"><span data-stu-id="5a703-102">LookupColumn resource type</span></span>

<span data-ttu-id="5a703-103">El recurso **lookupColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna se buscan desde otro origen en el sitio.</span><span class="sxs-lookup"><span data-stu-id="5a703-103">The **lookupColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's values are looked up from another source in the site.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5a703-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5a703-104">JSON representation</span></span>

<span data-ttu-id="5a703-105">A continuación se incluye una representación JSON de un recurso **LookupColumn**.</span><span class="sxs-lookup"><span data-stu-id="5a703-105">Here is a JSON representation of a **driveItem** resource.</span></span>
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

## <a name="properties"></a><span data-ttu-id="5a703-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a703-106">Properties</span></span>

| <span data-ttu-id="5a703-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="5a703-107">Property name</span></span>             | <span data-ttu-id="5a703-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5a703-108">Type</span></span>    | <span data-ttu-id="5a703-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a703-109">Description</span></span>
|:--------------------------|:--------|:---------------------------------------
| <span data-ttu-id="5a703-110">**allowMultipleValues**</span><span class="sxs-lookup"><span data-stu-id="5a703-110">**allowMultipleValues**</span></span>   | <span data-ttu-id="5a703-111">boolean</span><span class="sxs-lookup"><span data-stu-id="5a703-111">boolean</span></span> | <span data-ttu-id="5a703-112">Indica si se pueden seleccionar varios valores desde el origen.</span><span class="sxs-lookup"><span data-stu-id="5a703-112">Indicates whether multiple values can be selected from the source.</span></span>
| <span data-ttu-id="5a703-113">**allowUnlimitedLength**</span><span class="sxs-lookup"><span data-stu-id="5a703-113">**allowUnlimitedLength**</span></span>  | <span data-ttu-id="5a703-114">boolean</span><span class="sxs-lookup"><span data-stu-id="5a703-114">boolean</span></span> | <span data-ttu-id="5a703-115">Indica si los valores de la columna deben poder superar el límite estándar de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="5a703-115">Indicates whether values in the column should be able to exceed the standard limit of 255 characters.</span></span>
| <span data-ttu-id="5a703-116">**columnName**</span><span class="sxs-lookup"><span data-stu-id="5a703-116">**columnName**</span></span>            | <span data-ttu-id="5a703-117">string</span><span class="sxs-lookup"><span data-stu-id="5a703-117">string</span></span>  | <span data-ttu-id="5a703-118">El nombre de la columna de origen de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5a703-118">The name of the lookup source column.</span></span>
| <span data-ttu-id="5a703-119">**listId**</span><span class="sxs-lookup"><span data-stu-id="5a703-119">**listId**</span></span>                | <span data-ttu-id="5a703-120">string</span><span class="sxs-lookup"><span data-stu-id="5a703-120">string</span></span>  | <span data-ttu-id="5a703-121">El identificador único de la lista de origen de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="5a703-121">The unique identifier of the lookup source list.</span></span>
| <span data-ttu-id="5a703-122">**primaryLookupColumnId**</span><span class="sxs-lookup"><span data-stu-id="5a703-122">**primaryLookupColumnId**</span></span> | <span data-ttu-id="5a703-123">string</span><span class="sxs-lookup"><span data-stu-id="5a703-123">string</span></span>  | <span data-ttu-id="5a703-124">Si se especifica, esta columna es una *búsqueda secundaria*, que extrae un campo adicional del elemento de lista devuelto por la *búsqueda principal*.</span><span class="sxs-lookup"><span data-stu-id="5a703-124">If specified, this column is a *secondary lookup*, pulling an additional field from the list item looked up by the *primary lookup*.</span></span> <span data-ttu-id="5a703-125">Use el elemento de lista buscado en la búsqueda *principal* como origen de la columna indicada aquí.</span><span class="sxs-lookup"><span data-stu-id="5a703-125">Use the list item looked up by the *primary* as the source for the column named here.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/LookupColumn"
} -->
