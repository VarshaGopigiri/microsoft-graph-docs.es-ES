---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: ListInfo
ms.openlocfilehash: fb955a89c8dfb7b399d15f00666f21899abdc33d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085482"
---
# <a name="listinfo-resource"></a><span data-ttu-id="bfe0f-102">Recurso ListInfo</span><span class="sxs-lookup"><span data-stu-id="bfe0f-102">ListInfo resource</span></span>

> <span data-ttu-id="bfe0f-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bfe0f-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bfe0f-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bfe0f-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bfe0f-105">El tipo complejo **ListInfo** proporciona información adicional sobre un recurso [list][].</span><span class="sxs-lookup"><span data-stu-id="bfe0f-105">The **listInfo** complex type provides additional information about a [list][].</span></span>

[list]: list.md

## <a name="json-representation"></a><span data-ttu-id="bfe0f-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bfe0f-107">JSON representation</span></span>

<span data-ttu-id="bfe0f-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bfe0f-108">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="bfe0f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bfe0f-109">Properties</span></span>

| <span data-ttu-id="bfe0f-110">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="bfe0f-110">Property name</span></span>           | <span data-ttu-id="bfe0f-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="bfe0f-111">Type</span></span>    | <span data-ttu-id="bfe0f-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bfe0f-112">Description</span></span>
|:------------------------|:--------|:------------------------------------------------
| <span data-ttu-id="bfe0f-113">**contentTypesEnabled**</span><span class="sxs-lookup"><span data-stu-id="bfe0f-113">**contentTypesEnabled**</span></span> | <span data-ttu-id="bfe0f-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="bfe0f-114">Boolean</span></span> | <span data-ttu-id="bfe0f-115">Si es `true`, indica que los tipos de contenido están habilitados para esta lista.</span><span class="sxs-lookup"><span data-stu-id="bfe0f-115">If `true`, indicates that content types are enabled for this list.</span></span>
| <span data-ttu-id="bfe0f-116">**hidden**</span><span class="sxs-lookup"><span data-stu-id="bfe0f-116">**hidden**</span></span>              | <span data-ttu-id="bfe0f-117">Booleano</span><span class="sxs-lookup"><span data-stu-id="bfe0f-117">Boolean</span></span> | <span data-ttu-id="bfe0f-118">Si es `true`, indica que la lista no es visible normalmente en la experiencia del usuario de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="bfe0f-118">If `true`, indicates that the list is not normally visible in the SharePoint user experience.</span></span>
| <span data-ttu-id="bfe0f-119">**template**</span><span class="sxs-lookup"><span data-stu-id="bfe0f-119">**template**</span></span>            | <span data-ttu-id="bfe0f-120">String</span><span class="sxs-lookup"><span data-stu-id="bfe0f-120">String</span></span>  | <span data-ttu-id="bfe0f-121">Un valor enumerado que representa la plantilla de lista base usada al crear la lista.</span><span class="sxs-lookup"><span data-stu-id="bfe0f-121">An enumerated value that represents the base list template used in creating the list.</span></span> <span data-ttu-id="bfe0f-122">Los valores posibles incluyen `documentLibrary`, `genericList`, `task`, `survey`, `announcements`, `contacts` y más.</span><span class="sxs-lookup"><span data-stu-id="bfe0f-122">Possible values include `documentLibrary`, `genericList`, `task`, `survey`, `announcements`, `contacts`, and more.</span></span>

### <a name="remarks"></a><span data-ttu-id="bfe0f-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bfe0f-123">Remarks</span></span>

<span data-ttu-id="bfe0f-124">Mientras que la mayoría de las listas creadas por usuarios tendrán uno de los valores mencionados anteriormente, también son posibles otros valores.</span><span class="sxs-lookup"><span data-stu-id="bfe0f-124">While most lists created by users will have one of the values listed above, other values are possible as well.</span></span>
<span data-ttu-id="bfe0f-125">La aplicación debe estar preparada para controlar los valores que no figuran aquí.</span><span class="sxs-lookup"><span data-stu-id="bfe0f-125">Your app should be prepared to handle any values that are not listed here.</span></span>
<span data-ttu-id="bfe0f-126">Para los desarrolladores familiarizados con las API de OMSC de SharePoint, el valor `template` corresponde a la enumeración `SPListTemplateType`.</span><span class="sxs-lookup"><span data-stu-id="bfe0f-126">For developers familiar with SharePoint's CSOM APIs, the `template` value corresponds to the `SPListTemplateType` enumeration.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
