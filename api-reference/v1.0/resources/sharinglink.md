---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharingLink
localization_priority: Normal
ms.openlocfilehash: 02a4c0251a5484edc7ba5e07095f44043c269ae5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27863556"
---
# <a name="sharinglink-resource-type"></a><span data-ttu-id="3ad95-102">Tipo de recurso SharingLink</span><span class="sxs-lookup"><span data-stu-id="3ad95-102">SharingLink resource type</span></span>

<span data-ttu-id="3ad95-103">El recurso **SharingLink** agrupa en una sola estructura los elementos de datos relacionados con vínculos.</span><span class="sxs-lookup"><span data-stu-id="3ad95-103">The **SharingLink** resource groups link-related data items into a single structure.</span></span>

<span data-ttu-id="3ad95-104">Si un recurso [**Permission**](permission.md) tiene una faceta **sharingLink** que no es NULL, el permiso representa un vínculo para compartir (a diferencia de los permisos concedidos a una persona o un grupo).</span><span class="sxs-lookup"><span data-stu-id="3ad95-104">If a [**Permission**](permission.md) resource has a non-null **sharingLink** facet, the permission represents a sharing link (as opposed to permissions granted to a person or group).</span></span>

## <a name="json-representation"></a><span data-ttu-id="3ad95-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3ad95-105">JSON representation</span></span>

<span data-ttu-id="3ad95-106">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3ad95-106">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="3ad95-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ad95-107">Properties</span></span>

| <span data-ttu-id="3ad95-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3ad95-108">Property</span></span>    | <span data-ttu-id="3ad95-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ad95-109">Type</span></span>          | <span data-ttu-id="3ad95-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ad95-110">Description</span></span>
|:------------|:--------------|:-------------------------------------
| <span data-ttu-id="3ad95-111">application</span><span class="sxs-lookup"><span data-stu-id="3ad95-111">application</span></span> | <span data-ttu-id="3ad95-112">[identity][]</span><span class="sxs-lookup"><span data-stu-id="3ad95-112">[identity][]</span></span>  | <span data-ttu-id="3ad95-113">La aplicación con la que está asociada el vínculo.</span><span class="sxs-lookup"><span data-stu-id="3ad95-113">The app the link is associated with.</span></span>
| <span data-ttu-id="3ad95-114">type</span><span class="sxs-lookup"><span data-stu-id="3ad95-114">type</span></span>        | <span data-ttu-id="3ad95-115">String</span><span class="sxs-lookup"><span data-stu-id="3ad95-115">String</span></span>        | <span data-ttu-id="3ad95-116">El tipo del vínculo creado.</span><span class="sxs-lookup"><span data-stu-id="3ad95-116">The type of the link created.</span></span>
| <span data-ttu-id="3ad95-117">scope</span><span class="sxs-lookup"><span data-stu-id="3ad95-117">scope</span></span>       | <span data-ttu-id="3ad95-118">String</span><span class="sxs-lookup"><span data-stu-id="3ad95-118">String</span></span>        | <span data-ttu-id="3ad95-p101">El ámbito del vínculo representado por este permiso. El valor `anonymous` indica que cualquier usuario puede usar el vínculo, `organization` indica que solo pueden usar el vínculo los usuarios que han iniciado sesión en el mismo inquilino.</span><span class="sxs-lookup"><span data-stu-id="3ad95-p101">The scope of the link represented by this permission. Value `anonymous` indicates the link is usable by anyone, `organization` indicates the link is only usable for users signed into the same tenant.</span></span>
| <span data-ttu-id="3ad95-121">webHtml</span><span class="sxs-lookup"><span data-stu-id="3ad95-121">webHtml</span></span>     | <span data-ttu-id="3ad95-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="3ad95-122">String</span></span>        | <span data-ttu-id="3ad95-123">Para los vínculos `embed`, esta propiedad contiene el código HTML para un elemento `<iframe>` que insertará el elemento en una página web.</span><span class="sxs-lookup"><span data-stu-id="3ad95-123">For `embed` links, this property contains the HTML code for an `<iframe>` element that will embed the item in a webpage.</span></span>
| <span data-ttu-id="3ad95-124">webUrl</span><span class="sxs-lookup"><span data-stu-id="3ad95-124">webUrl</span></span>      | <span data-ttu-id="3ad95-125">String</span><span class="sxs-lookup"><span data-stu-id="3ad95-125">String</span></span>        | <span data-ttu-id="3ad95-126">Una dirección URL que abre el elemento en el explorador en el sitio web de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="3ad95-126">A URL that opens the item in the browser on the OneDrive website.</span></span>

[Identity]: identity.md

## <a name="type-options"></a><span data-ttu-id="3ad95-128">Opciones de tipo</span><span class="sxs-lookup"><span data-stu-id="3ad95-128">Type options</span></span>

<span data-ttu-id="3ad95-129">Esta tabla define los valores posibles de la propiedad **type**:</span><span class="sxs-lookup"><span data-stu-id="3ad95-129">This table defines the possible values for the **type** property:</span></span>

| <span data-ttu-id="3ad95-130">Valor</span><span class="sxs-lookup"><span data-stu-id="3ad95-130">Value</span></span>   | <span data-ttu-id="3ad95-131">Rol</span><span class="sxs-lookup"><span data-stu-id="3ad95-131">Role</span></span>    | <span data-ttu-id="3ad95-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ad95-132">Description</span></span>
|:--------|:--------|:---------------------------------------------------------
| `view`  | `read`  | <span data-ttu-id="3ad95-133">Un vínculo para compartir de solo vista, que permite el acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3ad95-133">A view-only sharing link, allowing read-only access.</span></span>
| `edit`  | `write` | <span data-ttu-id="3ad95-134">Un vínculo para compartir de edición, que permite el acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3ad95-134">An edit sharing link, allowing read-write access.</span></span>
| `embed` | `read`  | <span data-ttu-id="3ad95-135">Un vínculo para compartir de solo vista que puede usarse para insertar contenido en una página web de host.</span><span class="sxs-lookup"><span data-stu-id="3ad95-135">A view-only sharing link that can be used to embed content into a host webpage.</span></span> <span data-ttu-id="3ad95-136">La opción de inserción de vínculos no está disponible en OneDrive para la Empresa o SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3ad95-136">Embed links are not available for OneDrive for Business or SharePoint.</span></span>

## <a name="scope-options"></a><span data-ttu-id="3ad95-137">Opciones de ámbito</span><span class="sxs-lookup"><span data-stu-id="3ad95-137">Scope options</span></span>

| <span data-ttu-id="3ad95-138">Valor</span><span class="sxs-lookup"><span data-stu-id="3ad95-138">Value</span></span>          | <span data-ttu-id="3ad95-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ad95-139">Description</span></span>
|:---------------|:------------------------------------------------------------
| `anonymous`    | <span data-ttu-id="3ad95-140">Cualquier usuario con el vínculo tiene acceso, sin necesidad de iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="3ad95-140">Anyone with the link has access, without needing to sign in.</span></span> <span data-ttu-id="3ad95-141">Esto puede incluir personas fuera de la organización.</span><span class="sxs-lookup"><span data-stu-id="3ad95-141">This may include people outside of your organization.</span></span>
| `organization` | <span data-ttu-id="3ad95-142">Cualquier usuario que ha iniciado sesión en su organización (inquilino) puede usar el vínculo para obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="3ad95-142">Anyone signed into your organization (tenant) can use the link to get access.</span></span> <span data-ttu-id="3ad95-143">Sólo está disponible en OneDrive para profesionales y SharePoint.</span><span class="sxs-lookup"><span data-stu-id="3ad95-143">Only available in OneDrive for Business and SharePoint.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The sharing link facet provides information about how a file is shared.",
  "keywords": "sharing,sharing link, sharing url, webUrl",
  "section": "documentation",
  "suppressions": [
    "Warning: /api-reference/v1.0/resources/sharinglink.md:
      Found potential enums in resource example that weren't defined in a table:(view,edit,embed) are in resource, but () are in table",
    "Warning: /api-reference/v1.0/resources/sharinglink.md:
      Found potential enums in resource example that weren't defined in a table:(anonymous,organization) are in resource, but () are in table"
  ],
  "tocPath": "Facets/SharingLink"
} -->
