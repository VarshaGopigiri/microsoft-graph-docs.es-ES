---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharingLink
ms.openlocfilehash: 7b7729899d134fa1d5de7debb1f209ec5aadd70d
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="sharinglink-resource-type"></a><span data-ttu-id="36af5-102">Tipo de recurso SharingLink</span><span class="sxs-lookup"><span data-stu-id="36af5-102">SharingLink resource type</span></span>

<span data-ttu-id="36af5-103">El recurso **SharingLink** agrupa en una sola estructura los elementos de datos relacionados con vínculos.</span><span class="sxs-lookup"><span data-stu-id="36af5-103">The **SharingLink** resource groups link-related data items into a single structure.</span></span>

<span data-ttu-id="36af5-104">Si un recurso [**Permission**](permission.md) tiene una faceta **sharingLink** que no es NULL, el permiso representa un vínculo para compartir (a diferencia de los permisos concedidos a una persona o un grupo).</span><span class="sxs-lookup"><span data-stu-id="36af5-104">If a [**Permission**](permission.md) resource has a non-null **sharingLink** facet, the permission represents a sharing link (as opposed to permissions granted to a person or group).</span></span>

## <a name="json-representation"></a><span data-ttu-id="36af5-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="36af5-105">JSON representation</span></span>

<span data-ttu-id="36af5-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="36af5-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "application", "scope" ],
  "@odata.type": "microsoft.graph.sharingLink"
}-->

```json
{
  "application": { "@odata.type": "microsoft.graph.identity" },
  "type": "view | edit | embed",
  "scope": "anonymous | organization",
  "webHtml": "string",
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="36af5-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="36af5-107">Properties</span></span>

| <span data-ttu-id="36af5-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="36af5-108">Property</span></span>    | <span data-ttu-id="36af5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="36af5-109">Type</span></span>          | <span data-ttu-id="36af5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="36af5-110">Description</span></span>
|:------------|:--------------|:-------------------------------------
| <span data-ttu-id="36af5-111">application</span><span class="sxs-lookup"><span data-stu-id="36af5-111">application</span></span> | <span data-ttu-id="36af5-112">[identity][]</span><span class="sxs-lookup"><span data-stu-id="36af5-112">[identity][]</span></span>  | <span data-ttu-id="36af5-113">La aplicación con la que está asociada el vínculo.</span><span class="sxs-lookup"><span data-stu-id="36af5-113">The app the link is associated with.</span></span>
| <span data-ttu-id="36af5-114">type</span><span class="sxs-lookup"><span data-stu-id="36af5-114">type</span></span>        | <span data-ttu-id="36af5-115">String</span><span class="sxs-lookup"><span data-stu-id="36af5-115">String</span></span>        | <span data-ttu-id="36af5-116">El tipo del vínculo creado.</span><span class="sxs-lookup"><span data-stu-id="36af5-116">The type of the link created.</span></span>
| <span data-ttu-id="36af5-117">scope</span><span class="sxs-lookup"><span data-stu-id="36af5-117">scope</span></span>       | <span data-ttu-id="36af5-118">String</span><span class="sxs-lookup"><span data-stu-id="36af5-118">String</span></span>        | <span data-ttu-id="36af5-p101">El ámbito del vínculo representado por este permiso. El valor `anonymous` indica que cualquier usuario puede usar el vínculo, `organization` indica que solo pueden usar el vínculo los usuarios que han iniciado sesión en el mismo inquilino.</span><span class="sxs-lookup"><span data-stu-id="36af5-p101">The scope of the link represented by this permission. Value `anonymous` indicates the link is usable by anyone, `organization` indicates the link is only usable for users signed into the same tenant.</span></span>
| <span data-ttu-id="36af5-121">webHtml</span><span class="sxs-lookup"><span data-stu-id="36af5-121">webHtml</span></span>     | <span data-ttu-id="36af5-122">String</span><span class="sxs-lookup"><span data-stu-id="36af5-122">String</span></span>        | <span data-ttu-id="36af5-123">Para los vínculos `embed`, esta propiedad contiene el código HTML para un elemento `<iframe>` que insertará el elemento en una página web.</span><span class="sxs-lookup"><span data-stu-id="36af5-123">For embeddable links, this property contains the HTML code for an  element that will embed the item in a webpage.</span></span>
| <span data-ttu-id="36af5-124">webUrl</span><span class="sxs-lookup"><span data-stu-id="36af5-124">webUrl</span></span>      | <span data-ttu-id="36af5-125">String</span><span class="sxs-lookup"><span data-stu-id="36af5-125">String</span></span>        | <span data-ttu-id="36af5-126">Una dirección URL que abre el elemento en el explorador en el sitio web de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="36af5-126">A URL that opens the item in the browser on the OneDrive website.</span></span>

[Identity]: identity.md

## <a name="type-enumeration"></a><span data-ttu-id="36af5-128">Enumeración de tipos</span><span class="sxs-lookup"><span data-stu-id="36af5-128">Type enumeration</span></span>

<span data-ttu-id="36af5-129">Esta tabla define los valores posibles de la propiedad **type**:</span><span class="sxs-lookup"><span data-stu-id="36af5-129">This table defines the possible values for the **type** property:</span></span>

| <span data-ttu-id="36af5-130">Valor</span><span class="sxs-lookup"><span data-stu-id="36af5-130">Value</span></span>   | <span data-ttu-id="36af5-131">Rol</span><span class="sxs-lookup"><span data-stu-id="36af5-131">Role</span></span>    | <span data-ttu-id="36af5-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="36af5-132">Description</span></span>
|:--------|:--------|:---------------------------------------------------------
| `view`  | `read`  | <span data-ttu-id="36af5-133">Un vínculo para compartir de solo vista, que permite el acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="36af5-133">A view-only sharing link, allowing read-only access.</span></span>
| `edit`  | `write` | <span data-ttu-id="36af5-134">Un vínculo para compartir de edición, que permite el acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="36af5-134">An edit sharing link, allowing read-write access.</span></span>
| `embed` | `read`  | <span data-ttu-id="36af5-135">Un vínculo para compartir de solo vista que puede usarse para insertar contenido en una página web de host.</span><span class="sxs-lookup"><span data-stu-id="36af5-135">A view-only sharing link that can be used to embed content into a host webpage.</span></span> <span data-ttu-id="36af5-136">La opción de inserción de vínculos no está disponible en OneDrive para la Empresa o SharePoint.</span><span class="sxs-lookup"><span data-stu-id="36af5-136">Embed links are not available for OneDrive for Business or SharePoint.</span></span>

## <a name="scope-enumeration"></a><span data-ttu-id="36af5-137">Enumeración del ámbito</span><span class="sxs-lookup"><span data-stu-id="36af5-137">Scope enumeration</span></span>

| <span data-ttu-id="36af5-138">Valor</span><span class="sxs-lookup"><span data-stu-id="36af5-138">Value</span></span>          | <span data-ttu-id="36af5-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="36af5-139">Description</span></span>                                                                                                                 |
|:---------------|:----------------------------------------------------------------------------------------------------------------------------|
| `anonymous`    | <span data-ttu-id="36af5-140">El vínculo para compartir está disponible para que lo use cualquier usuario.</span><span class="sxs-lookup"><span data-stu-id="36af5-140">The sharing link is available for anyone to use.</span></span>                                                                            |
| `organization` | <span data-ttu-id="36af5-p103">El vínculo para compartir está disponible para que lo use cualquier usuario de la misma organización (inquilino). No está disponible para OneDrive Personal.</span><span class="sxs-lookup"><span data-stu-id="36af5-p103">The sharing link is available for anyone within the same organization (tenant) to use. Not available for OneDrive Personal.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The sharing link facet provides information about how a file is shared.",
  "keywords": "sharing,sharing link, sharing url, webUrl",
  "section": "documentation",
  "tocPath": "Facets/SharingLink"
} -->
