---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ListInfo
localization_priority: Normal
ms.openlocfilehash: c1a29099264c46f32e09b375a97ff49c13c99c6f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858460"
---
# <a name="listinfo-resource"></a><span data-ttu-id="1e294-102">Recurso ListInfo</span><span class="sxs-lookup"><span data-stu-id="1e294-102">ListInfo resource</span></span>

> <span data-ttu-id="1e294-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1e294-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1e294-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1e294-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="1e294-105">El tipo complejo **ListInfo** proporciona información adicional sobre un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="1e294-105">The **listInfo** complex type provides additional information about a [list][].</span></span>

[list]: list.md

## <a name="json-representation"></a><span data-ttu-id="1e294-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1e294-107">JSON representation</span></span>

<span data-ttu-id="1e294-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1e294-108">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="1e294-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e294-109">Properties</span></span>

| <span data-ttu-id="1e294-110">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="1e294-110">Property name</span></span>           | <span data-ttu-id="1e294-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e294-111">Type</span></span>    | <span data-ttu-id="1e294-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e294-112">Description</span></span>
|:------------------------|:--------|:------------------------------------------------
| <span data-ttu-id="1e294-113">**contentTypesEnabled**</span><span class="sxs-lookup"><span data-stu-id="1e294-113">**contentTypesEnabled**</span></span> | <span data-ttu-id="1e294-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="1e294-114">Boolean</span></span> | <span data-ttu-id="1e294-115">Si es `true`, indica que los tipos de contenido están habilitados para esta lista.</span><span class="sxs-lookup"><span data-stu-id="1e294-115">If `true`, indicates that content types are enabled for this list.</span></span>
| <span data-ttu-id="1e294-116">**hidden**</span><span class="sxs-lookup"><span data-stu-id="1e294-116">**hidden**</span></span>              | <span data-ttu-id="1e294-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="1e294-117">Boolean</span></span> | <span data-ttu-id="1e294-118">Si es `true`, indica que la lista no es visible normalmente en la experiencia del usuario de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="1e294-118">If `true`, indicates that the list is not normally visible in the SharePoint user experience.</span></span>
| <span data-ttu-id="1e294-119">**template**</span><span class="sxs-lookup"><span data-stu-id="1e294-119">**template**</span></span>            | <span data-ttu-id="1e294-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="1e294-120">String</span></span>  | <span data-ttu-id="1e294-121">Un valor enumerado que representa la plantilla de lista base usada al crear la lista.</span><span class="sxs-lookup"><span data-stu-id="1e294-121">An enumerated value that represents the base list template used in creating the list.</span></span> <span data-ttu-id="1e294-122">Los valores posibles incluyen `documentLibrary`, `genericList`, `task`, `survey`, `announcements`, `contacts` y más.</span><span class="sxs-lookup"><span data-stu-id="1e294-122">Possible values include `documentLibrary`, `genericList`, `task`, `survey`, `announcements`, `contacts`, and more.</span></span>

### <a name="remarks"></a><span data-ttu-id="1e294-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e294-123">Remarks</span></span>

<span data-ttu-id="1e294-124">Mientras que la mayoría de las listas creadas por usuarios tendrán uno de los valores mencionados anteriormente, también son posibles otros valores.</span><span class="sxs-lookup"><span data-stu-id="1e294-124">While most lists created by users will have one of the values listed above, other values are possible as well.</span></span>
<span data-ttu-id="1e294-125">La aplicación debe estar preparada para controlar los valores que no figuran aquí.</span><span class="sxs-lookup"><span data-stu-id="1e294-125">Your app should be prepared to handle any values that are not listed here.</span></span>
<span data-ttu-id="1e294-126">Para los desarrolladores familiarizados con las API de OMSC de SharePoint, el valor `template` corresponde a la enumeración `SPListTemplateType`.</span><span class="sxs-lookup"><span data-stu-id="1e294-126">For developers familiar with SharePoint's CSOM APIs, the `template` value corresponds to the `SPListTemplateType` enumeration.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
