---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Compartir un archivo con un vínculo
localization_priority: Normal
ms.openlocfilehash: 03da273e25791e57ca3eaede86559a4e02675e16
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875316"
---
# <a name="create-a-sharing-link-for-a-driveitem"></a><span data-ttu-id="787e6-102">Crear un vínculo para compartir para un DriveItem</span><span class="sxs-lookup"><span data-stu-id="787e6-102">Create a sharing link for a DriveItem</span></span>

> <span data-ttu-id="787e6-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="787e6-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="787e6-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="787e6-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="787e6-105">Puede usar la acción **createLink** para compartir un [DriveItem](../resources/driveitem.md) mediante un vínculo para compartir.</span><span class="sxs-lookup"><span data-stu-id="787e6-105">You can use **createLink** action to share a [DriveItem](../resources/driveitem.md) via a sharing link.</span></span>

<span data-ttu-id="787e6-p102">La acción **createLink** creará un nuevo vínculo para compartir si el tipo de vínculo especificado no existe para la aplicación que realiza la llamada. Si ya existe el tipo de vínculo para compartir especificado para la aplicación, se devolverá el vínculo para compartir existente.</span><span class="sxs-lookup"><span data-stu-id="787e6-p102">The **createLink** action will create a new sharing link if the specified link type doesn't already exist for the calling application. If a sharing link of the specified type already exists for the app, the existing sharing link will be returned.</span></span>

<span data-ttu-id="787e6-108">Los recursos DriveItem heredan permisos de uso compartido de sus antecesores.</span><span class="sxs-lookup"><span data-stu-id="787e6-108">DriveItem resources inherit sharing permissions from their ancestors.</span></span>

## <a name="permissions"></a><span data-ttu-id="787e6-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="787e6-109">Permissions</span></span>

<span data-ttu-id="787e6-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="787e6-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="787e6-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="787e6-112">Permission type</span></span>      | <span data-ttu-id="787e6-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="787e6-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="787e6-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="787e6-114">Delegated (work or school account)</span></span> | <span data-ttu-id="787e6-115">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="787e6-115">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="787e6-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="787e6-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="787e6-117">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="787e6-117">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="787e6-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="787e6-118">Application</span></span> | <span data-ttu-id="787e6-119">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="787e6-119">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="787e6-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="787e6-120">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{driveId}/items/{itemId}/createLink
POST /groups/{groupId}/drive/items/{itemId}/createLink
POST /me/drive/items/{itemId}/createLink
POST /sites/{siteId}/drive/items/{itemId}/createLink
POST /users/{userId}/drive/items/{itemId}/createLink
```

### <a name="request-body"></a><span data-ttu-id="787e6-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="787e6-121">Request body</span></span>

<span data-ttu-id="787e6-122">El cuerpo de la solicitud define las propiedades del vínculo para compartir que solicita su aplicación.</span><span class="sxs-lookup"><span data-stu-id="787e6-122">The body of the request defines properties of the sharing link your application is requesting.</span></span>
<span data-ttu-id="787e6-123">La solicitud debe ser un objeto JSON con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="787e6-123">The request should be a JSON object with the following properties.</span></span>

|   <span data-ttu-id="787e6-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="787e6-124">Name</span></span>    |  <span data-ttu-id="787e6-125">Tipo</span><span class="sxs-lookup"><span data-stu-id="787e6-125">Type</span></span>  |                                 <span data-ttu-id="787e6-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="787e6-126">Description</span></span>                                  |
| :-------- | :----- | :--------------------------------------------------------------------------- |
| <span data-ttu-id="787e6-127">**type**</span><span class="sxs-lookup"><span data-stu-id="787e6-127">**type**</span></span>  | <span data-ttu-id="787e6-128">string</span><span class="sxs-lookup"><span data-stu-id="787e6-128">string</span></span> | <span data-ttu-id="787e6-p105">El tipo de vínculo para compartir que se creará. `view`, `edit` o `embed`.</span><span class="sxs-lookup"><span data-stu-id="787e6-p105">The type of sharing link to create. Either `view`, `edit`, or `embed`.</span></span>       |
| <span data-ttu-id="787e6-131">**ámbito**</span><span class="sxs-lookup"><span data-stu-id="787e6-131">**scope**</span></span> | <span data-ttu-id="787e6-132">string</span><span class="sxs-lookup"><span data-stu-id="787e6-132">string</span></span> | <span data-ttu-id="787e6-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="787e6-133">Optional.</span></span> <span data-ttu-id="787e6-134">El ámbito del vínculo que se creará.</span><span class="sxs-lookup"><span data-stu-id="787e6-134">The scope of link to create.</span></span> <span data-ttu-id="787e6-135">`anonymous` o `organization`.</span><span class="sxs-lookup"><span data-stu-id="787e6-135">Either `anonymous` or `organization`.</span></span> |


### <a name="link-types"></a><span data-ttu-id="787e6-136">Tipos de vínculos</span><span class="sxs-lookup"><span data-stu-id="787e6-136">Link types</span></span>

<span data-ttu-id="787e6-137">Se pueden usar los siguientes valores para el parámetro de **tipo**.</span><span class="sxs-lookup"><span data-stu-id="787e6-137">The following values are allowed for the **type** parameter.</span></span>

| <span data-ttu-id="787e6-138">Valor del tipo</span><span class="sxs-lookup"><span data-stu-id="787e6-138">Type value</span></span> | <span data-ttu-id="787e6-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="787e6-139">Description</span></span>                                                                                  |
|:-----------|:---------------------------------------------------------------------------------------------|
| `view`     | <span data-ttu-id="787e6-140">Crea un vínculo de solo lectura para el objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="787e6-140">Creates a read-only link to the DriveItem.</span></span>                                                        |
| `edit`     | <span data-ttu-id="787e6-141">Crea un vínculo de lectura y escritura para el objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="787e6-141">Creates a read-write link to the DriveItem.</span></span>                                                       |
| `embed`    | <span data-ttu-id="787e6-142">Crea un vínculo insertable para el objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="787e6-142">Creates an embeddable link to the DriveItem.</span></span> <span data-ttu-id="787e6-143">Esta opción solo está disponible para archivos en OneDrive Personal.</span><span class="sxs-lookup"><span data-stu-id="787e6-143">This option is only available for files in OneDrive personal.</span></span> |

### <a name="scope-types"></a><span data-ttu-id="787e6-144">Tipos de ámbitos</span><span class="sxs-lookup"><span data-stu-id="787e6-144">Scope types</span></span>

<span data-ttu-id="787e6-145">Se permiten los siguientes valores para el parámetro **scope**.</span><span class="sxs-lookup"><span data-stu-id="787e6-145">The following values are allowed for the **scope** parameter.</span></span>
<span data-ttu-id="787e6-146">Si el parámetro **scope** no se especifica, se crea el tipo de vínculo predeterminado para la organización.</span><span class="sxs-lookup"><span data-stu-id="787e6-146">If the **scope** parameter is not specified, the default link type for the organization is created.</span></span>

| <span data-ttu-id="787e6-147">Valor del tipo</span><span class="sxs-lookup"><span data-stu-id="787e6-147">Type value</span></span>     | <span data-ttu-id="787e6-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="787e6-148">Description</span></span>                                                                                                                   |
|:---------------|:------------------------------------------------------------------------------------------------------------------------------|
| `anonymous`    | <span data-ttu-id="787e6-149">Crea un vínculo al objeto DriveItem accesible para cualquier usuario con el vínculo.</span><span class="sxs-lookup"><span data-stu-id="787e6-149">Creates a link to the DriveItem accessible to anyone with the link.</span></span> <span data-ttu-id="787e6-150">Un administrador puede deshabilitar los vínculos anónimos.</span><span class="sxs-lookup"><span data-stu-id="787e6-150">Anonymous links may be disabled by an administrator.</span></span>                 |
| `organization` | <span data-ttu-id="787e6-151">Crea un vínculo al objeto DriveItem accesible para cualquier usuario de la organización del usuario.</span><span class="sxs-lookup"><span data-stu-id="787e6-151">Creates a link to the DriveItem accessible to anyone within the user's organization.</span></span> <span data-ttu-id="787e6-152">El ámbito del vínculo de la organización no está disponible para OneDrive Personal.</span><span class="sxs-lookup"><span data-stu-id="787e6-152">Organization link scope is not available for OneDrive personal.</span></span> |

## <a name="response"></a><span data-ttu-id="787e6-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="787e6-153">Response</span></span>

<span data-ttu-id="787e6-154">Si se ejecuta correctamente, este método devuelve un recurso [Permission](../resources/permission.md) único en el cuerpo de la respuesta que representa los permiso de uso compartido solicitados.</span><span class="sxs-lookup"><span data-stu-id="787e6-154">If successful, this method returns a single [Permission](../resources/permission.md) resource in the response body that represents the requested sharing permissions.</span></span>

<span data-ttu-id="787e6-155">La respuesta será `201 Created` si se crea un nuevo vínculo para compartir el elemento o `200 OK` si se devuelve un vínculo existente.</span><span class="sxs-lookup"><span data-stu-id="787e6-155">The response will be `201 Created` if a new sharing link is created for the item or `200 OK` if an existing link is returned.</span></span>

## <a name="example"></a><span data-ttu-id="787e6-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="787e6-156">Example</span></span>

<span data-ttu-id="787e6-157">En el ejemplo siguiente, se solicita un vínculo para compartir que se creará para el objeto DriveItem especificado por {itemId} en el OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="787e6-157">The following example requests a sharing link to be created for the DriveItem specified by {itemId} in the user's OneDrive.</span></span>
<span data-ttu-id="787e6-158">El vínculo para compartir está configurado para que sea de solo lectura y lo pueda usar cualquier usuario que tenga el vínculo.</span><span class="sxs-lookup"><span data-stu-id="787e6-158">The sharing link is configured to be read-only and usable by anyone with the link.</span></span>

### <a name="request"></a><span data-ttu-id="787e6-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="787e6-159">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "item_createlink"
}-->

```http
POST /me/drive/items/{itemId}/createLink
Content-type: application/json

{
  "type": "view",
  "scope": "anonymous"
}
```

### <a name="response"></a><span data-ttu-id="787e6-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="787e6-160">Response</span></span>

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

## <a name="creating-company-sharable-links"></a><span data-ttu-id="787e6-161">Crear vínculos de empresa para compartir</span><span class="sxs-lookup"><span data-stu-id="787e6-161">Creating company sharable links</span></span>

<span data-ttu-id="787e6-162">OneDrive para la Empresa y SharePoint admiten vínculos de empresa para compartir.</span><span class="sxs-lookup"><span data-stu-id="787e6-162">OneDrive for Business and SharePoint support company sharable links.</span></span>
<span data-ttu-id="787e6-163">Son similares a los vínculos anónimos, pero solo funcionan para los miembros de la organización propietaria.</span><span class="sxs-lookup"><span data-stu-id="787e6-163">These are similar to anonymous links, except they only work for members of the owning organization.</span></span>
<span data-ttu-id="787e6-164">Para crear un vínculo de empresa para compartir, utilice el parámetro de **ámbito** con un valor de `organization`.</span><span class="sxs-lookup"><span data-stu-id="787e6-164">To create a company sharable link, use the **scope** parameter with a value of `organization`.</span></span>

### <a name="request"></a><span data-ttu-id="787e6-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="787e6-165">Request</span></span>

<!-- { "blockType": "request", "name": "create-link-scoped", "scopes": "files.readwrite service.sharepoint" } -->

```http
POST /me/drive/items/{item-id}/createLink
Content-Type: application/json

{
  "type": "edit",
  "scope": "organization"
}
```

### <a name="response"></a><span data-ttu-id="787e6-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="787e6-166">Response</span></span>

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

## <a name="creating-embeddable-links"></a><span data-ttu-id="787e6-167">Crear vínculos insertables</span><span class="sxs-lookup"><span data-stu-id="787e6-167">Creating embeddable links</span></span>

<span data-ttu-id="787e6-p113">Cuando se utiliza el tipo de vínculo `embed`, la webUrl que se devuelve se puede insertar en un elemento HTML `<iframe>`. Cuando se crea un vínculo para insertar, la propiedad `webHtml` contiene el código HTML de un `<iframe>` para hospedar el contenido.</span><span class="sxs-lookup"><span data-stu-id="787e6-p113">When using the `embed` link type, the webUrl returned can be embedded in an `<iframe>` HTML element. When an embed link is created the `webHtml` property contains the HTML code for an `<iframe>` to host the content.</span></span>

<span data-ttu-id="787e6-170">**Nota:** La acción de insertar vínculos solo se admite en OneDrive Personal.</span><span class="sxs-lookup"><span data-stu-id="787e6-170">**Note:** Embed links are only supported for OneDrive personal.</span></span>

### <a name="request"></a><span data-ttu-id="787e6-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="787e6-171">Request</span></span>

<!-- { "blockType": "request", "name": "create-embedded-link", "scopes": "files.readwrite service.onedrive" } -->

```http
POST /me/drive/items/{item-id}/createLink
Content-Type: application/json

{
  "type": "embed"
}
```

### <a name="response"></a><span data-ttu-id="787e6-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="787e6-172">Response</span></span>

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
    "webUrl": "https://onedive.live.com/...",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  }
}
```

## <a name="remarks"></a><span data-ttu-id="787e6-173">Comentarios</span><span class="sxs-lookup"><span data-stu-id="787e6-173">Remarks</span></span>

* <span data-ttu-id="787e6-174">Los vínculos creados con esta acción no caducan a menos que la organización fuerce una política de caducidad de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="787e6-174">Links created using this action do not expire unless a default expiration policy is enforced for the organization.</span></span>
* <span data-ttu-id="787e6-175">Los vínculos se pueden ver en los permisos de uso compartido del elemento y los puede eliminar un propietario del elemento.</span><span class="sxs-lookup"><span data-stu-id="787e6-175">Links are visible in the sharing permissions for the item and can be removed by an owner of the item.</span></span>
* <span data-ttu-id="787e6-176">Los vínculos siempre señalan la versión actual de un elemento, a menos que el elemento esté desprotegido (solo en SharePoint).</span><span class="sxs-lookup"><span data-stu-id="787e6-176">Links always point to the current version of a item unless the item is checked out (SharePoint only).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "Create a new sharing link for an item.",
  "keywords": "create,sharing,sharing link",
  "section": "documentation",
  "tocPath": "Sharing/Create link"
} -->
