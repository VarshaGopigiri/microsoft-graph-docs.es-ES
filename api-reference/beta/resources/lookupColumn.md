---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: LookupColumn
ms.openlocfilehash: 92eb43dad2ceca173fba79ad7d40f51f488a992c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083209"
---
# <a name="lookupcolumn-resource-type"></a><span data-ttu-id="f0513-102">Tipo de recurso LookupColumn</span><span class="sxs-lookup"><span data-stu-id="f0513-102">LookupColumn resource type</span></span>

> <span data-ttu-id="f0513-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f0513-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f0513-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f0513-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f0513-105">El recurso **lookupColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna se buscan desde otro origen en el sitio.</span><span class="sxs-lookup"><span data-stu-id="f0513-105">The **lookupColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values are looked up from another source in the site.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f0513-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f0513-106">JSON representation</span></span>

<span data-ttu-id="f0513-107">A continuación se incluye una representación JSON de un recurso **LookupColumn**.</span><span class="sxs-lookup"><span data-stu-id="f0513-107">Here is a JSON representation of a **lookupColumn** resource.</span></span>
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

## <a name="properties"></a><span data-ttu-id="f0513-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0513-108">Properties</span></span>

| <span data-ttu-id="f0513-109">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="f0513-109">Property name</span></span>             | <span data-ttu-id="f0513-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f0513-110">Type</span></span>    | <span data-ttu-id="f0513-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0513-111">Description</span></span>
|:--------------------------|:--------|:---------------------------------------
| <span data-ttu-id="f0513-112">**allowMultipleValues**</span><span class="sxs-lookup"><span data-stu-id="f0513-112">**allowMultipleValues**</span></span>   | <span data-ttu-id="f0513-113">boolean</span><span class="sxs-lookup"><span data-stu-id="f0513-113">boolean</span></span> | <span data-ttu-id="f0513-114">Indica si se pueden seleccionar varios valores desde el origen.</span><span class="sxs-lookup"><span data-stu-id="f0513-114">Indicates whether multiple values can be selected from the source.</span></span>
| <span data-ttu-id="f0513-115">**allowUnlimitedLength**</span><span class="sxs-lookup"><span data-stu-id="f0513-115">**allowUnlimitedLength**</span></span>  | <span data-ttu-id="f0513-116">boolean</span><span class="sxs-lookup"><span data-stu-id="f0513-116">boolean</span></span> | <span data-ttu-id="f0513-117">Indica si los valores de la columna deben poder superar el límite estándar de 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="f0513-117">Indicates whether values in the column should be able to exceed the standard limit of 255 characters.</span></span>
| <span data-ttu-id="f0513-118">**columnName**</span><span class="sxs-lookup"><span data-stu-id="f0513-118">**columnName**</span></span>            | <span data-ttu-id="f0513-119">string</span><span class="sxs-lookup"><span data-stu-id="f0513-119">string</span></span>  | <span data-ttu-id="f0513-120">El nombre de la columna de origen de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f0513-120">The name of the lookup source column.</span></span>
| <span data-ttu-id="f0513-121">**listId**</span><span class="sxs-lookup"><span data-stu-id="f0513-121">**listId**</span></span>                | <span data-ttu-id="f0513-122">string</span><span class="sxs-lookup"><span data-stu-id="f0513-122">string</span></span>  | <span data-ttu-id="f0513-123">El identificador único de la lista de origen de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f0513-123">The unique identifier of the lookup source list.</span></span>
| <span data-ttu-id="f0513-124">**primaryLookupColumnId**</span><span class="sxs-lookup"><span data-stu-id="f0513-124">**primaryLookupColumnId**</span></span> | <span data-ttu-id="f0513-125">string</span><span class="sxs-lookup"><span data-stu-id="f0513-125">string</span></span>  | <span data-ttu-id="f0513-126">Si se especifica, esta columna es una *búsqueda secundaria*, que extrae un campo adicional del elemento de lista devuelto por la *búsqueda principal*.</span><span class="sxs-lookup"><span data-stu-id="f0513-126">If specified, this column is a *secondary lookup*, pulling an additional field from the list item looked up by the *primary lookup*.</span></span> <span data-ttu-id="f0513-127">Use el elemento de lista buscado en la búsqueda *principal* como origen de la columna indicada aquí.</span><span class="sxs-lookup"><span data-stu-id="f0513-127">Use the list item looked up by the *primary* as the source for the column named here.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/LookupColumn"
} -->
