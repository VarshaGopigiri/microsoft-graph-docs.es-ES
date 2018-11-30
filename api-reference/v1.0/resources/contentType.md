---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ContentType
ms.openlocfilehash: 38142299b06313da43637fd0a15ba95f3da362e2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030118"
---
# <a name="contenttype-resource-type"></a><span data-ttu-id="e4e25-102">Tipo de recurso ContentType</span><span class="sxs-lookup"><span data-stu-id="e4e25-102">ContentType resource type</span></span>

<span data-ttu-id="e4e25-103">El recurso **contentType** representa un _tipo de contenido_ en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="e4e25-103">The **contentType** resource represents a _content type_ in SharePoint.</span></span>
<span data-ttu-id="e4e25-104">Los tipos de contenido le permiten definir un conjunto de columnas que debe estar presente en cada objeto [**listItem**][listItem] en un recurso [**list**][list].</span><span class="sxs-lookup"><span data-stu-id="e4e25-104">Content types allow you to define a set of columns that must be present on every [**listItem**][listItem] in a [**list**][list].</span></span>

[list]: list.md
[listItem]: listitem.md

## <a name="json-representation"></a><span data-ttu-id="e4e25-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e4e25-105">JSON representation</span></span>

<span data-ttu-id="e4e25-106">A continuación se incluye una representación JSON de un recurso **contentType**.</span><span class="sxs-lookup"><span data-stu-id="e4e25-106">Here is a JSON representation of a **contentType** resource.</span></span>
<!-- {
  "blockType": "resource",
 "baseType": "microsoft.graph.entity",
 "@odata.type": "microsoft.graph.contentType" } -->

```json
{
  "description": "string",
  "group": "string",
  "hidden": false,
  "id": "string",
  "inheritedFrom": { "@type": "microsoft.graph.itemReference" },
  "name": "string",
  "order": { "@type": "microsoft.graph.contentTypeOrder" },
  "parentId": "string",
  "readOnly": false,
  "sealed": false,

  "columnLinks": [{ "@type": "microsoft.graph.columnLink" }]
}
```

## <a name="properties"></a><span data-ttu-id="e4e25-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e4e25-107">Properties</span></span>

| <span data-ttu-id="e4e25-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="e4e25-108">Property name</span></span>     | <span data-ttu-id="e4e25-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4e25-109">Type</span></span>                 | <span data-ttu-id="e4e25-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4e25-110">Description</span></span>
|:------------------|:---------------------|:----------------------------------
| <span data-ttu-id="e4e25-111">**description**</span><span class="sxs-lookup"><span data-stu-id="e4e25-111">**description**</span></span>   | <span data-ttu-id="e4e25-112">string</span><span class="sxs-lookup"><span data-stu-id="e4e25-112">string</span></span>               | <span data-ttu-id="e4e25-113">Texto descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="e4e25-113">The descriptive text for the item.</span></span>
| <span data-ttu-id="e4e25-114">**group**</span><span class="sxs-lookup"><span data-stu-id="e4e25-114">**group**</span></span>         | <span data-ttu-id="e4e25-115">string</span><span class="sxs-lookup"><span data-stu-id="e4e25-115">string</span></span>               | <span data-ttu-id="e4e25-116">El nombre del grupo al que pertenece este tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="e4e25-116">The name of the group this content type belongs to.</span></span> <span data-ttu-id="e4e25-117">Ayuda a organizar los tipos de contenido relacionados.</span><span class="sxs-lookup"><span data-stu-id="e4e25-117">Helps organize related content types.</span></span>
| <span data-ttu-id="e4e25-118">**hidden**</span><span class="sxs-lookup"><span data-stu-id="e4e25-118">**hidden**</span></span>        | <span data-ttu-id="e4e25-119">boolean</span><span class="sxs-lookup"><span data-stu-id="e4e25-119">boolean</span></span>              | <span data-ttu-id="e4e25-120">Indica si el tipo de contenido está oculto en el menú "Nuevo" de la lista.</span><span class="sxs-lookup"><span data-stu-id="e4e25-120">Indicates whether the content type is hidden in the list's 'New' menu.</span></span>
| <span data-ttu-id="e4e25-121">**id**</span><span class="sxs-lookup"><span data-stu-id="e4e25-121">**id**</span></span>            | <span data-ttu-id="e4e25-122">string</span><span class="sxs-lookup"><span data-stu-id="e4e25-122">string</span></span>               | <span data-ttu-id="e4e25-123">El identificador único del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="e4e25-123">The unique identifier of the content type.</span></span>
| <span data-ttu-id="e4e25-124">**inheritedFrom**</span><span class="sxs-lookup"><span data-stu-id="e4e25-124">**inheritedFrom**</span></span> | <span data-ttu-id="e4e25-125">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="e4e25-125">[itemReference][]</span></span>    | <span data-ttu-id="e4e25-126">Si este tipo de contenido se hereda de otro ámbito (por ejemplo, un sitio), proporciona una referencia al elemento en que se define el tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="e4e25-126">If this content type is inherited from another scope (like a site), provides a reference to the item where the content type is defined.</span></span>
| <span data-ttu-id="e4e25-127">**name**</span><span class="sxs-lookup"><span data-stu-id="e4e25-127">**name**</span></span>          | <span data-ttu-id="e4e25-128">string</span><span class="sxs-lookup"><span data-stu-id="e4e25-128">string</span></span>               | <span data-ttu-id="e4e25-129">El nombre del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="e4e25-129">The name of the content type.</span></span>
| <span data-ttu-id="e4e25-130">**order**</span><span class="sxs-lookup"><span data-stu-id="e4e25-130">**order**</span></span>         | <span data-ttu-id="e4e25-131">[contentTypeOrder][]</span><span class="sxs-lookup"><span data-stu-id="e4e25-131">[contentTypeOrder][]</span></span> | <span data-ttu-id="e4e25-132">Especifica el orden en el que aparece el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="e4e25-132">Specifies the order in which the content type appears in the selection UI.</span></span>
| <span data-ttu-id="e4e25-133">**parentId**</span><span class="sxs-lookup"><span data-stu-id="e4e25-133">**parentId**</span></span>      | <span data-ttu-id="e4e25-134">string</span><span class="sxs-lookup"><span data-stu-id="e4e25-134">string</span></span>               | <span data-ttu-id="e4e25-135">El identificador único del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="e4e25-135">The unique identifier of the content type.</span></span>
| <span data-ttu-id="e4e25-136">**readOnly**</span><span class="sxs-lookup"><span data-stu-id="e4e25-136">**readOnly**</span></span>      | <span data-ttu-id="e4e25-137">boolean</span><span class="sxs-lookup"><span data-stu-id="e4e25-137">boolean</span></span>              | <span data-ttu-id="e4e25-138">Si es `true`, no se puede modificar el tipo de contenido, a menos que este valor se establezca primero en `false`.</span><span class="sxs-lookup"><span data-stu-id="e4e25-138">If `true`, the content type cannot be modified unless this value is first set to `false`.</span></span>
| <span data-ttu-id="e4e25-139">**sealed**</span><span class="sxs-lookup"><span data-stu-id="e4e25-139">**sealed**</span></span>        | <span data-ttu-id="e4e25-140">boolean</span><span class="sxs-lookup"><span data-stu-id="e4e25-140">boolean</span></span>              | <span data-ttu-id="e4e25-141">Si es `true`, los usuarios no pueden modificar el tipo de contenido, ni a través de operaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="e4e25-141">If `true`, the content type cannot be modified by users or through push-down operations.</span></span> <span data-ttu-id="e4e25-142">Solo los administradores de la colección de sitios pueden sellar o quitar el sello de los tipos de contenido.</span><span class="sxs-lookup"><span data-stu-id="e4e25-142">Only site collection administrators can seal or unseal content types.</span></span>

## <a name="relationships"></a><span data-ttu-id="e4e25-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e4e25-143">Relationships</span></span>

| <span data-ttu-id="e4e25-144">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="e4e25-144">Property name</span></span>   | <span data-ttu-id="e4e25-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4e25-145">Type</span></span>                      | <span data-ttu-id="e4e25-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4e25-146">Description</span></span>
|:----------------|:--------------------------|:-------------------------------
| <span data-ttu-id="e4e25-147">**columnLinks**</span><span class="sxs-lookup"><span data-stu-id="e4e25-147">**columnLinks**</span></span> | <span data-ttu-id="e4e25-148">Colección [columnLink][]</span><span class="sxs-lookup"><span data-stu-id="e4e25-148">[columnLink][] collection</span></span> | <span data-ttu-id="e4e25-149">La colección de columnas que requiere este tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="e4e25-149">The collection of columns that are required by this content type</span></span>

<span data-ttu-id="e4e25-150">Vea [Introducción a los tipos de contenido y publicación del tipo de contenido][contentTypeIntro] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="e4e25-150">See [Introduction to content types and content type publishing][contentTypeIntro] for more information.</span></span>

[columnLink]: columnlink.md
[contentTypeIntro]: https://support.office.com/en-us/article/Introduction-to-content-types-and-content-type-publishing-e1277a2e-a1e8-4473-9126-91a0647766e5
[itemReference]: itemreference.md
[contentTypeOrder]: contenttypeorder.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentType"
} -->
