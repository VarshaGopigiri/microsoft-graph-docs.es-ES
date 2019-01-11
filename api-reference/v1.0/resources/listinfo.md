---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ListInfo
localization_priority: Normal
ms.openlocfilehash: 881a150f750fa947888a60b4c22ceeb5b0c826d2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27830733"
---
# <a name="listinfo-resource"></a><span data-ttu-id="ccaa8-102">Recurso ListInfo</span><span class="sxs-lookup"><span data-stu-id="ccaa8-102">ListInfo resource</span></span>

<span data-ttu-id="ccaa8-103">El tipo complejo **ListInfo** proporciona información adicional sobre un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="ccaa8-103">The **listInfo** complex type provides additional information about a [list][].</span></span>

[list]: list.md

## <a name="json-representation"></a><span data-ttu-id="ccaa8-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ccaa8-105">JSON representation</span></span>

<span data-ttu-id="ccaa8-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
  ],
  "@odata.type": "microsoft.graph.listInfo"
}-->

```json
{
  "contentTypesEnabled": false,
  "hidden": false,
  "template": "documentLibrary | genericList | tasks | survey | links | announcements | contacts | ..."
}
```

## <a name="properties"></a><span data-ttu-id="ccaa8-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ccaa8-107">Properties</span></span>

| <span data-ttu-id="ccaa8-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="ccaa8-108">Property name</span></span>           | <span data-ttu-id="ccaa8-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccaa8-109">Type</span></span>    | <span data-ttu-id="ccaa8-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccaa8-110">Description</span></span>
|:------------------------|:--------|:------------------------------------------------
| <span data-ttu-id="ccaa8-111">**contentTypesEnabled**</span><span class="sxs-lookup"><span data-stu-id="ccaa8-111">**contentTypesEnabled**</span></span> | <span data-ttu-id="ccaa8-112">Booleano</span><span class="sxs-lookup"><span data-stu-id="ccaa8-112">Boolean</span></span> | <span data-ttu-id="ccaa8-113">Si es `true`, indica que los tipos de contenido están habilitados para esta lista.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-113">If `true`, indicates that content types are enabled for this list.</span></span>
| <span data-ttu-id="ccaa8-114">**hidden**</span><span class="sxs-lookup"><span data-stu-id="ccaa8-114">**hidden**</span></span>              | <span data-ttu-id="ccaa8-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="ccaa8-115">Boolean</span></span> | <span data-ttu-id="ccaa8-116">Si es `true`, indica que la lista no es visible normalmente en la experiencia del usuario de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-116">If `true`, indicates that the list is not normally visible in the SharePoint user experience.</span></span>
| <span data-ttu-id="ccaa8-117">**template**</span><span class="sxs-lookup"><span data-stu-id="ccaa8-117">**template**</span></span>            | <span data-ttu-id="ccaa8-118">Cadena</span><span class="sxs-lookup"><span data-stu-id="ccaa8-118">String</span></span>  | <span data-ttu-id="ccaa8-119">Un valor enumerado que representa la plantilla de lista base usada al crear la lista.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-119">An enumerated value that represents the base list template used in creating the list.</span></span> <span data-ttu-id="ccaa8-120">Los valores posibles incluyen `documentLibrary`, `genericList`, `task`, `survey`, `announcements`, `contacts` y más.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-120">Possible values include `documentLibrary`, `genericList`, `task`, `survey`, `announcements`, `contacts`, and more.</span></span>

### <a name="remarks"></a><span data-ttu-id="ccaa8-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ccaa8-121">Remarks</span></span>

<span data-ttu-id="ccaa8-122">Mientras que la mayoría de las listas creadas por usuarios tendrán uno de los valores mencionados anteriormente, también son posibles otros valores.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-122">While most lists created by users will have one of the values listed above, other values are possible as well.</span></span>
<span data-ttu-id="ccaa8-123">La aplicación debe estar preparada para controlar los valores que no figuran aquí.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-123">Your app should be prepared to handle any values that are not listed here.</span></span>
<span data-ttu-id="ccaa8-124">Para los desarrolladores familiarizados con las API de OMSC de SharePoint, el valor `template` corresponde a la enumeración `SPListTemplateType`.</span><span class="sxs-lookup"><span data-stu-id="ccaa8-124">For developers familiar with SharePoint's CSOM APIs, the `template` value corresponds to the `SPListTemplateType` enumeration.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/listinfo.md:
      Found potential enums in resource example that weren't defined in a table:(documentLibrary,genericList,tasks,survey,links,announcements,contacts,...) are in resource, but () are in table"
  ],
  "tocPath": ""
}-->
