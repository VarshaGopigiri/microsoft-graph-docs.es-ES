---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: SharingLink
localization_priority: Normal
ms.openlocfilehash: c303436aafbdbb5167a992f405036b5e00e4d635
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27856395"
---
# <a name="sharinglink-resource-type"></a><span data-ttu-id="ded4e-102">tipo de recurso sharingLink</span><span class="sxs-lookup"><span data-stu-id="ded4e-102">sharingLink resource type</span></span>

> <span data-ttu-id="ded4e-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ded4e-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ded4e-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ded4e-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ded4e-105">El recurso **sharingLink** agrupa los elementos de datos relacionados con el vínculo en una única estructura.</span><span class="sxs-lookup"><span data-stu-id="ded4e-105">The **sharingLink** resource groups link-related data items into a single structure.</span></span>

<span data-ttu-id="ded4e-106">Si un recurso de [**permiso**](permission.md) tiene una faceta distintos de null **sharingLink** , el permiso representa un vínculo de uso compartido (a diferencia de los permisos concedidos a una persona o un grupo).</span><span class="sxs-lookup"><span data-stu-id="ded4e-106">If a [**permission**](permission.md) resource has a non-null **sharingLink** facet, the permission represents a sharing link (as opposed to permissions granted to a person or group).</span></span>

## <a name="json-representation"></a><span data-ttu-id="ded4e-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ded4e-107">JSON representation</span></span>

<span data-ttu-id="ded4e-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ded4e-108">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "application", "scope" ],
  "@odata.type": "microsoft.graph.sharingLink"
}-->

```json
{
  "application": { "@odata.type": "microsoft.graph.identity" },
  "preventsDownload": false,
  "type": "view | edit | embed",
  "scope": "anonymous | organization",
  "webHtml": "string",
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="ded4e-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ded4e-109">Properties</span></span>

| <span data-ttu-id="ded4e-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ded4e-110">Property</span></span>       | <span data-ttu-id="ded4e-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ded4e-111">Type</span></span>          | <span data-ttu-id="ded4e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ded4e-112">Description</span></span>
|:---------------|:--------------|:-------------------------------------
| <span data-ttu-id="ded4e-113">application</span><span class="sxs-lookup"><span data-stu-id="ded4e-113">application</span></span>    | <span data-ttu-id="ded4e-114">[identity][]</span><span class="sxs-lookup"><span data-stu-id="ded4e-114">[identity][]</span></span>  | <span data-ttu-id="ded4e-115">La aplicación con la que está asociada el vínculo.</span><span class="sxs-lookup"><span data-stu-id="ded4e-115">The app the link is associated with.</span></span>
| <span data-ttu-id="ded4e-116">type</span><span class="sxs-lookup"><span data-stu-id="ded4e-116">type</span></span>           | <span data-ttu-id="ded4e-117">String</span><span class="sxs-lookup"><span data-stu-id="ded4e-117">String</span></span>        | <span data-ttu-id="ded4e-118">El tipo del vínculo creado.</span><span class="sxs-lookup"><span data-stu-id="ded4e-118">The type of the link created.</span></span>
| <span data-ttu-id="ded4e-119">scope</span><span class="sxs-lookup"><span data-stu-id="ded4e-119">scope</span></span>          | <span data-ttu-id="ded4e-120">String</span><span class="sxs-lookup"><span data-stu-id="ded4e-120">String</span></span>        | <span data-ttu-id="ded4e-p102">El ámbito del vínculo representado por este permiso. El valor `anonymous` indica que cualquier usuario puede usar el vínculo, `organization` indica que solo pueden usar el vínculo los usuarios que han iniciado sesión en el mismo inquilino.</span><span class="sxs-lookup"><span data-stu-id="ded4e-p102">The scope of the link represented by this permission. Value `anonymous` indicates the link is usable by anyone, `organization` indicates the link is only usable for users signed into the same tenant.</span></span>
| <span data-ttu-id="ded4e-123">preventsDownload</span><span class="sxs-lookup"><span data-stu-id="ded4e-123">preventsDownload</span></span> | <span data-ttu-id="ded4e-124">Booleano</span><span class="sxs-lookup"><span data-stu-id="ded4e-124">Boolean</span></span>       | <span data-ttu-id="ded4e-125">Si es true, a continuación, el usuario sólo puede usar este vínculo para ver el elemento en la web y no puede usar para descargar el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="ded4e-125">If true then the user can only use this link to view the item on the web, and cannot use it to download the contents of the item.</span></span> <span data-ttu-id="ded4e-126">Sólo para OneDrive para profesionales y SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ded4e-126">Only for OneDrive for Business and SharePoint.</span></span>
| <span data-ttu-id="ded4e-127">webHtml</span><span class="sxs-lookup"><span data-stu-id="ded4e-127">webHtml</span></span>        | <span data-ttu-id="ded4e-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="ded4e-128">String</span></span>        | <span data-ttu-id="ded4e-129">Para los vínculos `embed`, esta propiedad contiene el código HTML para un elemento `<iframe>` que insertará el elemento en una página web.</span><span class="sxs-lookup"><span data-stu-id="ded4e-129">For `embed` links, this property contains the HTML code for an `<iframe>` element that will embed the item in a webpage.</span></span>
| <span data-ttu-id="ded4e-130">webUrl</span><span class="sxs-lookup"><span data-stu-id="ded4e-130">webUrl</span></span>         | <span data-ttu-id="ded4e-131">String</span><span class="sxs-lookup"><span data-stu-id="ded4e-131">String</span></span>        | <span data-ttu-id="ded4e-132">Una dirección URL que abre el elemento en el explorador en el sitio web de OneDrive.</span><span class="sxs-lookup"><span data-stu-id="ded4e-132">A URL that opens the item in the browser on the OneDrive website.</span></span>

[Identity]: identity.md

### <a name="type-options"></a><span data-ttu-id="ded4e-134">Opciones de tipo</span><span class="sxs-lookup"><span data-stu-id="ded4e-134">Type options</span></span>

<span data-ttu-id="ded4e-135">En la tabla siguiente define los valores posibles para la propiedad **type** .</span><span class="sxs-lookup"><span data-stu-id="ded4e-135">The following table defines the possible values for the **type** property.</span></span>

| <span data-ttu-id="ded4e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="ded4e-136">Value</span></span>    | <span data-ttu-id="ded4e-137">Rol</span><span class="sxs-lookup"><span data-stu-id="ded4e-137">Role</span></span>     | <span data-ttu-id="ded4e-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="ded4e-138">Description</span></span>
|:---------|:---------|:---------------------------------------------------------
| `view`   | `read`   | <span data-ttu-id="ded4e-139">Un vínculo para compartir de solo vista, que permite el acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ded4e-139">A view-only sharing link, allowing read-only access.</span></span>
| `edit`   | `write`  | <span data-ttu-id="ded4e-140">Un vínculo para compartir de edición, que permite el acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ded4e-140">An edit sharing link, allowing read-write access.</span></span>
| `embed`  | `read`   | <span data-ttu-id="ded4e-141">Un vínculo para compartir de solo vista que puede usarse para insertar contenido en una página web de host.</span><span class="sxs-lookup"><span data-stu-id="ded4e-141">A view-only sharing link that can be used to embed content into a host webpage.</span></span> <span data-ttu-id="ded4e-142">La opción de inserción de vínculos no está disponible en OneDrive para la Empresa o SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ded4e-142">Embed links are not available for OneDrive for Business or SharePoint.</span></span>

### <a name="scope-options"></a><span data-ttu-id="ded4e-143">Opciones de ámbito</span><span class="sxs-lookup"><span data-stu-id="ded4e-143">Scope options</span></span>

<span data-ttu-id="ded4e-144">En la tabla siguiente define los valores posibles para la propiedad de **ámbito** .</span><span class="sxs-lookup"><span data-stu-id="ded4e-144">The following table defines the possible values for the **scope** property.</span></span>

| <span data-ttu-id="ded4e-145">Valor</span><span class="sxs-lookup"><span data-stu-id="ded4e-145">Value</span></span>            | <span data-ttu-id="ded4e-146">Description</span><span class="sxs-lookup"><span data-stu-id="ded4e-146">Description</span></span>
|:-----------------|:------------------------------------------------------------
| `anonymous`      | <span data-ttu-id="ded4e-147">Cualquier usuario con el vínculo tiene acceso, sin necesidad de iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="ded4e-147">Anyone with the link has access, without needing to sign in.</span></span> <span data-ttu-id="ded4e-148">Esto puede incluir personas fuera de la organización.</span><span class="sxs-lookup"><span data-stu-id="ded4e-148">This may include people outside of your organization.</span></span>
| `organization`   | <span data-ttu-id="ded4e-149">Cualquier usuario que ha iniciado sesión en su organización (inquilino) puede usar el vínculo para obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="ded4e-149">Anyone signed into your organization (tenant) can use the link to get access.</span></span> <span data-ttu-id="ded4e-150">Sólo está disponible en OneDrive para profesionales y SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ded4e-150">Only available in OneDrive for Business and SharePoint.</span></span>
| `existingAccess` | <span data-ttu-id="ded4e-151">Sólo los usuarios que ya se hayan concedido el acceso al elemento a través de otros medios pueden obtener acceso al elemento con este vínculo.</span><span class="sxs-lookup"><span data-stu-id="ded4e-151">Only people who have already been granted access to the item through other means can access the item using this link.</span></span> <span data-ttu-id="ded4e-152">Sólo está disponible en OneDrive para profesionales y SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ded4e-152">Only available in OneDrive for Business and SharePoint.</span></span>
| `users`          | <span data-ttu-id="ded4e-153">El vínculo concede acceso sólo a una lista específica de personas.</span><span class="sxs-lookup"><span data-stu-id="ded4e-153">The link grants access only to a specific list of people.</span></span> <span data-ttu-id="ded4e-154">Sólo está disponible en OneDrive para profesionales y SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ded4e-154">Only available in OneDrive for Business and SharePoint.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "The sharing link facet provides information about how a file is shared.",
  "keywords": "sharing,sharing link, sharing url, webUrl",
  "section": "documentation",
  "tocPath": ""
}-->
