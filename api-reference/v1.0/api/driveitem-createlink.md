---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Compartir un archivo con un vínculo
localization_priority: Normal
ms.openlocfilehash: 222917a869487f8e0fd893d641436f001354dfb1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27871130"
---
# <a name="create-a-sharing-link-for-a-driveitem"></a><span data-ttu-id="7498d-102">Crear un vínculo para compartir para un DriveItem</span><span class="sxs-lookup"><span data-stu-id="7498d-102">Create a sharing link for a DriveItem</span></span>

<span data-ttu-id="7498d-103">Puede usar la acción **createLink** para compartir un [DriveItem](../resources/driveitem.md) mediante un vínculo para compartir.</span><span class="sxs-lookup"><span data-stu-id="7498d-103">You can use **createLink** action to share a [DriveItem](../resources/driveitem.md) via a sharing link.</span></span>

<span data-ttu-id="7498d-p101">La acción **createLink** creará un nuevo vínculo para compartir si el tipo de vínculo especificado no existe para la aplicación que realiza la llamada. Si ya existe el tipo de vínculo para compartir especificado para la aplicación, se devolverá el vínculo para compartir existente.</span><span class="sxs-lookup"><span data-stu-id="7498d-p101">The **createLink** action will create a new sharing link if the specified link type doesn't already exist for the calling application. If a sharing link of the specified type already exists for the app, the existing sharing link will be returned.</span></span>

<span data-ttu-id="7498d-106">Los recursos DriveItem heredan permisos de uso compartido de sus antecesores.</span><span class="sxs-lookup"><span data-stu-id="7498d-106">DriveItem resources inherit sharing permissions from their ancestors.</span></span>

## <a name="permissions"></a><span data-ttu-id="7498d-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="7498d-107">Permissions</span></span>

<span data-ttu-id="7498d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7498d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7498d-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7498d-110">Permission type</span></span>      | <span data-ttu-id="7498d-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7498d-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7498d-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7498d-112">Delegated (work or school account)</span></span> | <span data-ttu-id="7498d-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7498d-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="7498d-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7498d-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7498d-115">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7498d-115">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="7498d-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7498d-116">Application</span></span> | <span data-ttu-id="7498d-117">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7498d-117">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="7498d-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7498d-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/createLink
POST /groups/{groupId}/drive/items/{itemId}/createLink
POST /me/drive/items/{itemId}/createLink
POST /sites/{siteId}/drive/items/{itemId}/createLink
POST /users/{userId}/drive/items/{itemId}/createLink
```

### <a name="request-body"></a><span data-ttu-id="7498d-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7498d-119">Request body</span></span>

<span data-ttu-id="7498d-120">El cuerpo de la solicitud define las propiedades del vínculo para compartir que solicita su aplicación.</span><span class="sxs-lookup"><span data-stu-id="7498d-120">The body of the request defines properties of the sharing link your application is requesting.</span></span>
<span data-ttu-id="7498d-121">La solicitud debe ser un objeto JSON con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="7498d-121">The request should be a JSON object with the following properties.</span></span>

|   <span data-ttu-id="7498d-122">Nombre</span><span class="sxs-lookup"><span data-stu-id="7498d-122">Name</span></span>    |  <span data-ttu-id="7498d-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="7498d-123">Type</span></span>  |                                 <span data-ttu-id="7498d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="7498d-124">Description</span></span>                                  |
| :-------- | :----- | :--------------------------------------------------------------------------- |
| <span data-ttu-id="7498d-125">**type**</span><span class="sxs-lookup"><span data-stu-id="7498d-125">**type**</span></span>  | <span data-ttu-id="7498d-126">string</span><span class="sxs-lookup"><span data-stu-id="7498d-126">string</span></span> | <span data-ttu-id="7498d-p104">El tipo de vínculo para compartir que se creará. `view`, `edit` o `embed`.</span><span class="sxs-lookup"><span data-stu-id="7498d-p104">The type of sharing link to create. Either `view`, `edit`, or `embed`.</span></span>       |
| <span data-ttu-id="7498d-129">**ámbito**</span><span class="sxs-lookup"><span data-stu-id="7498d-129">**scope**</span></span> | <span data-ttu-id="7498d-130">string</span><span class="sxs-lookup"><span data-stu-id="7498d-130">string</span></span> | <span data-ttu-id="7498d-131">Opcional.</span><span class="sxs-lookup"><span data-stu-id="7498d-131">Optional.</span></span> <span data-ttu-id="7498d-132">El ámbito del vínculo que se creará.</span><span class="sxs-lookup"><span data-stu-id="7498d-132">The scope of link to create.</span></span> <span data-ttu-id="7498d-133">`anonymous` o `organization`.</span><span class="sxs-lookup"><span data-stu-id="7498d-133">Either `anonymous` or `organization`.</span></span> |


### <a name="link-types"></a><span data-ttu-id="7498d-134">Tipos de vínculos</span><span class="sxs-lookup"><span data-stu-id="7498d-134">Link types</span></span>

<span data-ttu-id="7498d-135">Se pueden usar los siguientes valores para el parámetro de **tipo**.</span><span class="sxs-lookup"><span data-stu-id="7498d-135">The following values are allowed for the **type** parameter.</span></span>

| <span data-ttu-id="7498d-136">Valor del tipo</span><span class="sxs-lookup"><span data-stu-id="7498d-136">Type value</span></span> | <span data-ttu-id="7498d-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="7498d-137">Description</span></span>                                                                                  |
|:-----------|:---------------------------------------------------------------------------------------------|
| `view`     | <span data-ttu-id="7498d-138">Crea un vínculo de solo lectura para el objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="7498d-138">Creates a read-only link to the DriveItem.</span></span>                                                        |
| `edit`     | <span data-ttu-id="7498d-139">Crea un vínculo de lectura y escritura para el objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="7498d-139">Creates a read-write link to the DriveItem.</span></span>                                                       |
| `embed`    | <span data-ttu-id="7498d-140">Crea un vínculo insertable para el objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="7498d-140">Creates an embeddable link to the DriveItem.</span></span> <span data-ttu-id="7498d-141">Esta opción solo está disponible para archivos en OneDrive Personal.</span><span class="sxs-lookup"><span data-stu-id="7498d-141">This option is only available for files in OneDrive personal.</span></span> |

### <a name="scope-types"></a><span data-ttu-id="7498d-142">Tipos de ámbitos</span><span class="sxs-lookup"><span data-stu-id="7498d-142">Scope types</span></span>

<span data-ttu-id="7498d-143">Se permiten los siguientes valores para el parámetro **scope**.</span><span class="sxs-lookup"><span data-stu-id="7498d-143">The following values are allowed for the **scope** parameter.</span></span>
<span data-ttu-id="7498d-144">Si el parámetro **scope** no se especifica, se crea el tipo de vínculo predeterminado para la organización.</span><span class="sxs-lookup"><span data-stu-id="7498d-144">If the **scope** parameter is not specified, the default link type for the organization is created.</span></span>

| <span data-ttu-id="7498d-145">Valor</span><span class="sxs-lookup"><span data-stu-id="7498d-145">Value</span></span>          | <span data-ttu-id="7498d-146">Description</span><span class="sxs-lookup"><span data-stu-id="7498d-146">Description</span></span>
|:---------------|:------------------------------------------------------------
| `anonymous`    | <span data-ttu-id="7498d-147">Cualquier usuario con el vínculo tiene acceso, sin necesidad de iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="7498d-147">Anyone with the link has access, without needing to sign in.</span></span> <span data-ttu-id="7498d-148">Esto puede incluir personas fuera de la organización.</span><span class="sxs-lookup"><span data-stu-id="7498d-148">This may include people outside of your organization.</span></span> <span data-ttu-id="7498d-149">Compatibilidad con vínculo anónimo puede ser deshabilitado por un administrador.</span><span class="sxs-lookup"><span data-stu-id="7498d-149">Anonymous link support may be disabled by an administrator.</span></span>
| `organization` | <span data-ttu-id="7498d-150">Cualquier usuario que ha iniciado sesión en su organización (inquilino) puede usar el vínculo para obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="7498d-150">Anyone signed into your organization (tenant) can use the link to get access.</span></span> <span data-ttu-id="7498d-151">Sólo está disponible en OneDrive para profesionales y SharePoint.</span><span class="sxs-lookup"><span data-stu-id="7498d-151">Only available in OneDrive for Business and SharePoint.</span></span>


## <a name="response"></a><span data-ttu-id="7498d-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7498d-152">Response</span></span>

<span data-ttu-id="7498d-153">Si se ejecuta correctamente, este método devuelve un recurso [Permission](../resources/permission.md) único en el cuerpo de la respuesta que representa los permiso de uso compartido solicitados.</span><span class="sxs-lookup"><span data-stu-id="7498d-153">If successful, this method returns a single [Permission](../resources/permission.md) resource in the response body that represents the requested sharing permissions.</span></span>

<span data-ttu-id="7498d-154">La respuesta será `201 Created` si se crea un nuevo vínculo para compartir el elemento o `200 OK` si se devuelve un vínculo existente.</span><span class="sxs-lookup"><span data-stu-id="7498d-154">The response will be `201 Created` if a new sharing link is created for the item or `200 OK` if an existing link is returned.</span></span>

## <a name="example"></a><span data-ttu-id="7498d-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7498d-155">Example</span></span>

<span data-ttu-id="7498d-156">En el ejemplo siguiente, se solicita un vínculo para compartir que se creará para el objeto DriveItem especificado por {itemId} en el OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="7498d-156">The following example requests a sharing link to be created for the DriveItem specified by {itemId} in the user's OneDrive.</span></span>
<span data-ttu-id="7498d-157">El vínculo para compartir está configurado para que sea de solo lectura y lo pueda usar cualquier usuario que tenga el vínculo.</span><span class="sxs-lookup"><span data-stu-id="7498d-157">The sharing link is configured to be read-only and usable by anyone with the link.</span></span>

### <a name="request"></a><span data-ttu-id="7498d-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7498d-158">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create-link"
}-->

```http
POST /me/drive/items/{item-id}/createLink
Content-type: application/json

{
  "type": "view",
  "scope": "anonymous"
}
```

### <a name="response"></a><span data-ttu-id="7498d-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7498d-159">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission" } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "123ABC",
  "roles": ["write"],
  "link": {
    "type": "view",
    "scope": "anonymous",
    "webUrl": "https://1drv.ms/A6913278E564460AA616C71B28AD6EB6",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  }
}
```

## <a name="creating-company-sharable-links"></a><span data-ttu-id="7498d-160">Crear vínculos de empresa para compartir</span><span class="sxs-lookup"><span data-stu-id="7498d-160">Creating company sharable links</span></span>

<span data-ttu-id="7498d-161">OneDrive para la Empresa y SharePoint admiten vínculos de empresa para compartir.</span><span class="sxs-lookup"><span data-stu-id="7498d-161">OneDrive for Business and SharePoint support company sharable links.</span></span>
<span data-ttu-id="7498d-162">Son similares a los vínculos anónimos, pero solo funcionan para los miembros de la organización propietaria.</span><span class="sxs-lookup"><span data-stu-id="7498d-162">These are similar to anonymous links, except they only work for members of the owning organization.</span></span>
<span data-ttu-id="7498d-163">Para crear un vínculo de empresa para compartir, utilice el parámetro de **ámbito** con un valor de `organization`.</span><span class="sxs-lookup"><span data-stu-id="7498d-163">To create a company sharable link, use the **scope** parameter with a value of `organization`.</span></span>

### <a name="request"></a><span data-ttu-id="7498d-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7498d-164">Request</span></span>

<!-- { "blockType": "request", "name": "create-link-scoped", "scopes": "files.readwrite", "tags": "service.sharepoint" } -->

```http
POST /me/drive/items/{item-id}/createLink
Content-Type: application/json

{
  "type": "edit",
  "scope": "organization"
}
```

### <a name="response"></a><span data-ttu-id="7498d-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7498d-165">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission" } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "123ABC",
  "roles": ["write"],
  "link": {
    "type": "edit",
    "scope": "organization",
    "webUrl": "https://contoso-my.sharepoint.com/personal/ellen_contoso_com/...",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  }
}
```

## <a name="creating-embeddable-links"></a><span data-ttu-id="7498d-166">Crear vínculos insertables</span><span class="sxs-lookup"><span data-stu-id="7498d-166">Creating embeddable links</span></span>

<span data-ttu-id="7498d-p112">Cuando se utiliza el tipo de vínculo `embed`, la webUrl que se devuelve se puede insertar en un elemento HTML `<iframe>`. Cuando se crea un vínculo para insertar, la propiedad `webHtml` contiene el código HTML de un `<iframe>` para hospedar el contenido.</span><span class="sxs-lookup"><span data-stu-id="7498d-p112">When using the `embed` link type, the webUrl returned can be embedded in an `<iframe>` HTML element. When an embed link is created the `webHtml` property contains the HTML code for an `<iframe>` to host the content.</span></span>

<span data-ttu-id="7498d-169">**Nota:** La acción de insertar vínculos solo se admite en OneDrive Personal.</span><span class="sxs-lookup"><span data-stu-id="7498d-169">**Note:** Embed links are only supported for OneDrive personal.</span></span>

### <a name="request"></a><span data-ttu-id="7498d-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7498d-170">Request</span></span>

<!-- { "blockType": "request", "name": "create-embedded-link", "scopes": "files.readwrite", "tags": "service.onedrive service.graph" } -->

```http
POST /me/drive/items/{item-id}/createLink
Content-Type: application/json

{
  "type": "embed"
}
```

### <a name="response"></a><span data-ttu-id="7498d-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7498d-171">Response</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission" } -->

```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "123ABC",
  "roles": ["read"],
  "link": {
    "type": "embed",
    "webHtml": "<IFRAME src=\"https://onedrive.live.com/...\"></IFRAME>",
    "webUrl": "https://onedrive.live.com/...",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  }
}
```

## <a name="remarks"></a><span data-ttu-id="7498d-172">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7498d-172">Remarks</span></span>

* <span data-ttu-id="7498d-173">Los vínculos creados con esta acción no caducan a menos que la organización fuerce una política de caducidad de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7498d-173">Links created using this action do not expire unless a default expiration policy is enforced for the organization.</span></span>
* <span data-ttu-id="7498d-174">Los vínculos se pueden ver en los permisos de uso compartido del elemento y los puede eliminar un propietario del elemento.</span><span class="sxs-lookup"><span data-stu-id="7498d-174">Links are visible in the sharing permissions for the item and can be removed by an owner of the item.</span></span>
* <span data-ttu-id="7498d-175">Los vínculos siempre señalan la versión actual de un elemento, a menos que el elemento esté desprotegido (solo en SharePoint).</span><span class="sxs-lookup"><span data-stu-id="7498d-175">Links always point to the current version of a item unless the item is checked out (SharePoint only).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Create a new sharing link for an item.",
  "keywords": "create,sharing,sharing link",
  "section": "documentation",
  "tocPath": "Sharing/Create link"
} -->
