---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: LookupColumn
localization_priority: Normal
ms.openlocfilehash: 1c7ab364777e1e3f82bb78d8e0940cf4f85576a0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27885711"
---
# <a name="lookupcolumn-resource-type"></a><span data-ttu-id="54d70-102">Tipo de recurso LookupColumn</span><span class="sxs-lookup"><span data-stu-id="54d70-102">LookupColumn resource type</span></span>

> <span data-ttu-id="54d70-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="54d70-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="54d70-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="54d70-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="54d70-105">El recurso **lookupColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna se buscan desde otro origen en el sitio.</span><span class="sxs-lookup"><span data-stu-id="54d70-105">The **lookupColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values are looked up from another source in the site.</span></span>

## <a name="json-representation"></a><span data-ttu-id="54d70-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="54d70-106">JSON representation</span></span>

<span data-ttu-id="54d70-107">A continuación se incluye una representación JSON de un recurso **LookupColumn**.</span><span class="sxs-lookup"><span data-stu-id="54d70-107">Here is a JSON representation of a **lookupColumn** resource.</span></span>
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

## <a name="properties"></a><span data-ttu-id="54d70-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="54d70-108">Properties</span></span>

| <span data-ttu-id="54d70-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="54d70-109">Property name</span></span>             | <span data-ttu-id="54d70-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="54d70-110">Type</span></span>    | <span data-ttu-id="54d70-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="54d70-111">Description</span></span>
|:--------------------------|:--------|:---------------------------------------
| <span data-ttu-id="54d70-112">**allowMultipleValues**</span><span class="sxs-lookup"><span data-stu-id="54d70-112">**allowMultipleValues**</span></span>   | <span data-ttu-id="54d70-113">boolean</span><span class="sxs-lookup"><span data-stu-id="54d70-113">boolean</span></span> | <span data-ttu-id="54d70-114">Indica si se pueden seleccionar varios valores desde el origen.</span><span class="sxs-lookup"><span data-stu-id="54d70-114">Indicates whether multiple values can be selected from the source.</span></span>
| <span data-ttu-id="54d70-115">**allowUnlimitedLength**</span><span class="sxs-lookup"><span data-stu-id="54d70-115">**allowUnlimitedLength**</span></span>  | <span data-ttu-id="54d70-116">boolean</span><span class="sxs-lookup"><span data-stu-id="54d70-116">boolean</span></span> | <span data-ttu-id="54d70-117">Indica si los valores de la columna deben poder superar el límite estándar de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="54d70-117">Indicates whether values in the column should be able to exceed the standard limit of 255 characters.</span></span>
| <span data-ttu-id="54d70-118">**columnName**</span><span class="sxs-lookup"><span data-stu-id="54d70-118">**columnName**</span></span>            | <span data-ttu-id="54d70-119">string</span><span class="sxs-lookup"><span data-stu-id="54d70-119">string</span></span>  | <span data-ttu-id="54d70-120">El nombre de la columna de origen de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="54d70-120">The name of the lookup source column.</span></span>
| <span data-ttu-id="54d70-121">**listId**</span><span class="sxs-lookup"><span data-stu-id="54d70-121">**listId**</span></span>                | <span data-ttu-id="54d70-122">string</span><span class="sxs-lookup"><span data-stu-id="54d70-122">string</span></span>  | <span data-ttu-id="54d70-123">El identificador único de la lista de origen de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="54d70-123">The unique identifier of the lookup source list.</span></span>
| <span data-ttu-id="54d70-124">**primaryLookupColumnId**</span><span class="sxs-lookup"><span data-stu-id="54d70-124">**primaryLookupColumnId**</span></span> | <span data-ttu-id="54d70-125">string</span><span class="sxs-lookup"><span data-stu-id="54d70-125">string</span></span>  | <span data-ttu-id="54d70-126">Si se especifica, esta columna es una *búsqueda secundaria*, que extrae un campo adicional del elemento de lista devuelto por la *búsqueda principal*.</span><span class="sxs-lookup"><span data-stu-id="54d70-126">If specified, this column is a *secondary lookup*, pulling an additional field from the list item looked up by the *primary lookup*.</span></span> <span data-ttu-id="54d70-127">Use el elemento de lista buscado en la búsqueda *principal* como origen de la columna indicada aquí.</span><span class="sxs-lookup"><span data-stu-id="54d70-127">Use the list item looked up by the *primary* as the source for the column named here.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/LookupColumn"
} -->
