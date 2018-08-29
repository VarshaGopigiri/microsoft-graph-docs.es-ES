---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ContentType
ms.openlocfilehash: cb16559aa9da3a885be1977bbd1466265d0a72f0
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23268336"
---
# <a name="contenttype-resource-type"></a><span data-ttu-id="fdb5e-102">Tipo de recurso ContentType</span><span class="sxs-lookup"><span data-stu-id="fdb5e-102">ContentType resource type</span></span>

<span data-ttu-id="fdb5e-103">El recurso **contentType** representa un _tipo de contenido_ en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-103">The **contentType** resource represents a _content type_ in SharePoint.</span></span>
<span data-ttu-id="fdb5e-104">Los tipos de contenido le permiten definir un conjunto de columnas que debe estar presente en cada objeto [**listItem**][listItem] en un recurso [**list**][list].</span><span class="sxs-lookup"><span data-stu-id="fdb5e-104">Content types allow you to define a set of columns that must be present on every [**listItem**][listItem] in a [**list**][list].</span></span>

[list]: list.md
[listItem]: listItem.md

## <a name="json-representation"></a><span data-ttu-id="fdb5e-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fdb5e-105">JSON representation</span></span>

<span data-ttu-id="fdb5e-106">A continuación se incluye una representación JSON de un recurso **contentType**.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-106">Here is a JSON representation of a **contentType** resource.</span></span>
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

## <a name="properties"></a><span data-ttu-id="fdb5e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fdb5e-107">Properties</span></span>

| <span data-ttu-id="fdb5e-108">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="fdb5e-108">Property name</span></span>     | <span data-ttu-id="fdb5e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdb5e-109">Type</span></span>                 | <span data-ttu-id="fdb5e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdb5e-110">Description</span></span>
|:------------------|:---------------------|:----------------------------------
| <span data-ttu-id="fdb5e-111">**description**</span><span class="sxs-lookup"><span data-stu-id="fdb5e-111">**description**</span></span>   | <span data-ttu-id="fdb5e-112">string</span><span class="sxs-lookup"><span data-stu-id="fdb5e-112">string</span></span>               | <span data-ttu-id="fdb5e-113">Texto descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-113">The descriptive text for the item.</span></span>
| <span data-ttu-id="fdb5e-114">**group**</span><span class="sxs-lookup"><span data-stu-id="fdb5e-114">**group**</span></span>         | <span data-ttu-id="fdb5e-115">string</span><span class="sxs-lookup"><span data-stu-id="fdb5e-115">string</span></span>               | <span data-ttu-id="fdb5e-116">El nombre del grupo al que pertenece este tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-116">The name of the group this content type belongs to.</span></span> <span data-ttu-id="fdb5e-117">Ayuda a organizar los tipos de contenido relacionados.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-117">Helps organize related content types.</span></span>
| <span data-ttu-id="fdb5e-118">**hidden**</span><span class="sxs-lookup"><span data-stu-id="fdb5e-118">**hidden**</span></span>        | <span data-ttu-id="fdb5e-119">boolean</span><span class="sxs-lookup"><span data-stu-id="fdb5e-119">boolean</span></span>              | <span data-ttu-id="fdb5e-120">Indica si el tipo de contenido está oculto en el menú "Nuevo" de la lista.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-120">Indicates whether the content type is hidden in the list's 'New' menu.</span></span>
| <span data-ttu-id="fdb5e-121">**id**</span><span class="sxs-lookup"><span data-stu-id="fdb5e-121">**id**</span></span>            | <span data-ttu-id="fdb5e-122">string</span><span class="sxs-lookup"><span data-stu-id="fdb5e-122">string</span></span>               | <span data-ttu-id="fdb5e-123">El identificador único del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-123">The unique identifier of the content type.</span></span>
| <span data-ttu-id="fdb5e-124">**inheritedFrom**</span><span class="sxs-lookup"><span data-stu-id="fdb5e-124">**inheritedFrom**</span></span> | <span data-ttu-id="fdb5e-125">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="fdb5e-125">[itemReference][]</span></span>    | <span data-ttu-id="fdb5e-126">Si este tipo de contenido se hereda de otro ámbito (por ejemplo, un sitio), proporciona una referencia al elemento en que se define el tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-126">If this content type is inherited from another scope (like a site), provides a reference to the item where the content type is defined.</span></span>
| <span data-ttu-id="fdb5e-127">**name**</span><span class="sxs-lookup"><span data-stu-id="fdb5e-127">**name**</span></span>          | <span data-ttu-id="fdb5e-128">cadena</span><span class="sxs-lookup"><span data-stu-id="fdb5e-128">string</span></span>               | <span data-ttu-id="fdb5e-129">El nombre del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-129">The name of the content type.</span></span>
| <span data-ttu-id="fdb5e-130">**order**</span><span class="sxs-lookup"><span data-stu-id="fdb5e-130">**order**</span></span>         | <span data-ttu-id="fdb5e-131">[contentTypeOrder][]</span><span class="sxs-lookup"><span data-stu-id="fdb5e-131">[contentTypeOrder][]</span></span> | <span data-ttu-id="fdb5e-132">Especifica el orden en el que aparece el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-132">Specifies the order in which the content type appears in the selection UI.</span></span>
| <span data-ttu-id="fdb5e-133">**parentId**</span><span class="sxs-lookup"><span data-stu-id="fdb5e-133">**parentId**</span></span>      | <span data-ttu-id="fdb5e-134">string</span><span class="sxs-lookup"><span data-stu-id="fdb5e-134">string</span></span>               | <span data-ttu-id="fdb5e-135">El identificador único del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-135">The unique identifier of the content type.</span></span>
| <span data-ttu-id="fdb5e-136">**readOnly**</span><span class="sxs-lookup"><span data-stu-id="fdb5e-136">**readOnly**</span></span>      | <span data-ttu-id="fdb5e-137">boolean</span><span class="sxs-lookup"><span data-stu-id="fdb5e-137">boolean</span></span>              | <span data-ttu-id="fdb5e-138">Si es `true`, no se puede modificar el tipo de contenido, a menos que este valor se establezca primero en `false`.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-138">If `true`, the content type cannot be modified unless this value is first set to `false`.</span></span>
| <span data-ttu-id="fdb5e-139">**sealed**</span><span class="sxs-lookup"><span data-stu-id="fdb5e-139">**sealed**</span></span>        | <span data-ttu-id="fdb5e-140">boolean</span><span class="sxs-lookup"><span data-stu-id="fdb5e-140">boolean</span></span>              | <span data-ttu-id="fdb5e-141">Si es `true`, los usuarios no pueden modificar el tipo de contenido, ni a través de operaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-141">If `true`, the content type cannot be modified by users or through push-down operations.</span></span> <span data-ttu-id="fdb5e-142">Solo los administradores de la colección de sitios pueden sellar o quitar el sello de los tipos de contenido.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-142">Only site collection administrators can seal or unseal content types.</span></span>

## <a name="relationships"></a><span data-ttu-id="fdb5e-143">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fdb5e-143">Relationships</span></span>

| <span data-ttu-id="fdb5e-144">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="fdb5e-144">Property name</span></span>   | <span data-ttu-id="fdb5e-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="fdb5e-145">Type</span></span>                      | <span data-ttu-id="fdb5e-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="fdb5e-146">Description</span></span>
|:----------------|:--------------------------|:-------------------------------
| <span data-ttu-id="fdb5e-147">**columnLinks**</span><span class="sxs-lookup"><span data-stu-id="fdb5e-147">**columnLinks**</span></span> | <span data-ttu-id="fdb5e-148">Colección [columnLink][]</span><span class="sxs-lookup"><span data-stu-id="fdb5e-148">[columnLink][] collection</span></span> | <span data-ttu-id="fdb5e-149">La colección de columnas que requiere este tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="fdb5e-149">The collection of columns that are required by this content type</span></span>

<span data-ttu-id="fdb5e-150">Vea [Introducción a los tipos de contenido y publicación del tipo de contenido][contentTypeIntro] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="fdb5e-150">See [Introduction to content types and content type publishing][contentTypeIntro] for more information.</span></span>

[columnLink]: columnLink.md
[contentTypeIntro]: https://support.office.com/en-us/article/Introduction-to-content-types-and-content-type-publishing-e1277a2e-a1e8-4473-9126-91a0647766e5
[itemReference]: itemReference.md
[contentTypeOrder]: contentTypeOrder.md

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentType"
} -->
