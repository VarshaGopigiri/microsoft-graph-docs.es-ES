---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ContentType
ms.openlocfilehash: cda50c2f20df14c733d3bf71e1b84d5b0df225a0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089612"
---
# <a name="contenttype-resource-type"></a><span data-ttu-id="cf509-102">Tipo de recurso ContentType</span><span class="sxs-lookup"><span data-stu-id="cf509-102">ContentType resource type</span></span>

> <span data-ttu-id="cf509-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cf509-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cf509-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cf509-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cf509-105">El recurso **contentType** representa un _tipo de contenido_ en SharePoint.</span><span class="sxs-lookup"><span data-stu-id="cf509-105">The **contentType** resource represents a _content type_ in SharePoint.</span></span>
<span data-ttu-id="cf509-106">Los tipos de contenido le permiten definir un conjunto de columnas que debe estar presente en cada objeto [**listItem**][listItem] en un recurso [**list**][list].</span><span class="sxs-lookup"><span data-stu-id="cf509-106">Content types allow you to define a set of columns that must be present on every [**listItem**][listItem] in a [**list**][list].</span></span>

[list]: list.md
[listItem]: listitem.md

## <a name="json-representation"></a><span data-ttu-id="cf509-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cf509-107">JSON representation</span></span>

<span data-ttu-id="cf509-108">A continuación se incluye una representación JSON de un recurso **contentType**.</span><span class="sxs-lookup"><span data-stu-id="cf509-108">Here is a JSON representation of a **contentType** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.contentType" } -->

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

## <a name="properties"></a><span data-ttu-id="cf509-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf509-109">Properties</span></span>

| <span data-ttu-id="cf509-110">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="cf509-110">Property name</span></span>     | <span data-ttu-id="cf509-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf509-111">Type</span></span>                 | <span data-ttu-id="cf509-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf509-112">Description</span></span>
|:------------------|:---------------------|:----------------------------------
| <span data-ttu-id="cf509-113">**description**</span><span class="sxs-lookup"><span data-stu-id="cf509-113">**description**</span></span>   | <span data-ttu-id="cf509-114">string</span><span class="sxs-lookup"><span data-stu-id="cf509-114">string</span></span>               | <span data-ttu-id="cf509-115">Texto descriptivo del elemento.</span><span class="sxs-lookup"><span data-stu-id="cf509-115">The descriptive text for the item.</span></span>
| <span data-ttu-id="cf509-116">**group**</span><span class="sxs-lookup"><span data-stu-id="cf509-116">**group**</span></span>         | <span data-ttu-id="cf509-117">string</span><span class="sxs-lookup"><span data-stu-id="cf509-117">string</span></span>               | <span data-ttu-id="cf509-118">El nombre del grupo al que pertenece este tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="cf509-118">The name of the group this content type belongs to.</span></span> <span data-ttu-id="cf509-119">Ayuda a organizar los tipos de contenido relacionados.</span><span class="sxs-lookup"><span data-stu-id="cf509-119">Helps organize related content types.</span></span>
| <span data-ttu-id="cf509-120">**hidden**</span><span class="sxs-lookup"><span data-stu-id="cf509-120">**hidden**</span></span>        | <span data-ttu-id="cf509-121">boolean</span><span class="sxs-lookup"><span data-stu-id="cf509-121">boolean</span></span>              | <span data-ttu-id="cf509-122">Indica si el tipo de contenido está oculto en el menú "Nuevo" de la lista.</span><span class="sxs-lookup"><span data-stu-id="cf509-122">Indicates whether the content type is hidden in the list's 'New' menu.</span></span>
| <span data-ttu-id="cf509-123">**id**</span><span class="sxs-lookup"><span data-stu-id="cf509-123">**id**</span></span>            | <span data-ttu-id="cf509-124">string</span><span class="sxs-lookup"><span data-stu-id="cf509-124">string</span></span>               | <span data-ttu-id="cf509-125">El identificador único del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="cf509-125">The unique identifier of the content type.</span></span>
| <span data-ttu-id="cf509-126">**inheritedFrom**</span><span class="sxs-lookup"><span data-stu-id="cf509-126">**inheritedFrom**</span></span> | <span data-ttu-id="cf509-127">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="cf509-127">[itemReference][]</span></span>    | <span data-ttu-id="cf509-128">Si este tipo de contenido se hereda de otro ámbito (por ejemplo, un sitio), proporciona una referencia al elemento en que se define el tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="cf509-128">If this content type is inherited from another scope (like a site), provides a reference to the item where the content type is defined.</span></span>
| <span data-ttu-id="cf509-129">**name**</span><span class="sxs-lookup"><span data-stu-id="cf509-129">**name**</span></span>          | <span data-ttu-id="cf509-130">string</span><span class="sxs-lookup"><span data-stu-id="cf509-130">string</span></span>               | <span data-ttu-id="cf509-131">El nombre del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="cf509-131">The name of the content type.</span></span>
| <span data-ttu-id="cf509-132">**order**</span><span class="sxs-lookup"><span data-stu-id="cf509-132">**order**</span></span>         | <span data-ttu-id="cf509-133">[contentTypeOrder][]</span><span class="sxs-lookup"><span data-stu-id="cf509-133">[contentTypeOrder][]</span></span> | <span data-ttu-id="cf509-134">Especifica el orden en el que aparece el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="cf509-134">Specifies the order in which the content type appears in the selection UI.</span></span>
| <span data-ttu-id="cf509-135">**parentId**</span><span class="sxs-lookup"><span data-stu-id="cf509-135">**parentId**</span></span>      | <span data-ttu-id="cf509-136">string</span><span class="sxs-lookup"><span data-stu-id="cf509-136">string</span></span>               | <span data-ttu-id="cf509-137">El identificador único del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="cf509-137">The unique identifier of the content type.</span></span>
| <span data-ttu-id="cf509-138">**readOnly**</span><span class="sxs-lookup"><span data-stu-id="cf509-138">**readOnly**</span></span>      | <span data-ttu-id="cf509-139">boolean</span><span class="sxs-lookup"><span data-stu-id="cf509-139">boolean</span></span>              | <span data-ttu-id="cf509-140">Si es `true`, no se puede modificar el tipo de contenido, a menos que este valor se establezca primero en `false`.</span><span class="sxs-lookup"><span data-stu-id="cf509-140">If `true`, the content type cannot be modified unless this value is first set to `false`.</span></span>
| <span data-ttu-id="cf509-141">**sealed**</span><span class="sxs-lookup"><span data-stu-id="cf509-141">**sealed**</span></span>        | <span data-ttu-id="cf509-142">boolean</span><span class="sxs-lookup"><span data-stu-id="cf509-142">boolean</span></span>              | <span data-ttu-id="cf509-143">Si es `true`, los usuarios no pueden modificar el tipo de contenido, ni a través de operaciones de inserción.</span><span class="sxs-lookup"><span data-stu-id="cf509-143">If `true`, the content type cannot be modified by users or through push-down operations.</span></span> <span data-ttu-id="cf509-144">Solo los administradores de la colección de sitios pueden sellar o quitar el sello de los tipos de contenido.</span><span class="sxs-lookup"><span data-stu-id="cf509-144">Only site collection administrators can seal or unseal content types.</span></span>

## <a name="relationships"></a><span data-ttu-id="cf509-145">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cf509-145">Relationships</span></span>

| <span data-ttu-id="cf509-146">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="cf509-146">Property name</span></span>   | <span data-ttu-id="cf509-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="cf509-147">Type</span></span>                      | <span data-ttu-id="cf509-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf509-148">Description</span></span>
|:----------------|:--------------------------|:-------------------------------
| <span data-ttu-id="cf509-149">**columnLinks**</span><span class="sxs-lookup"><span data-stu-id="cf509-149">**columnLinks**</span></span> | <span data-ttu-id="cf509-150">Colección [columnLink][]</span><span class="sxs-lookup"><span data-stu-id="cf509-150">[columnLink][] collection</span></span> | <span data-ttu-id="cf509-151">La colección de columnas que requiere este tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="cf509-151">The collection of columns that are required by this content type</span></span>

<span data-ttu-id="cf509-152">Vea [Introducción a los tipos de contenido y publicación del tipo de contenido][contentTypeIntro] para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="cf509-152">See [Introduction to content types and content type publishing][contentTypeIntro] for more information.</span></span>

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
