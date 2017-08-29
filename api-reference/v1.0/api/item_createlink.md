# <a name="create-a-sharing-link-for-a-driveitem"></a><span data-ttu-id="1379f-101">Crear un vínculo para compartir para un DriveItem</span><span class="sxs-lookup"><span data-stu-id="1379f-101">Create a sharing link for a DriveItem</span></span>

<span data-ttu-id="1379f-102">Puede usar la acción **createLink** para compartir un [DriveItem](../resources/driveitem.md) mediante un vínculo para compartir.</span><span class="sxs-lookup"><span data-stu-id="1379f-102">You can use **createLink** action to share a [DriveItem](../resources/driveitem.md) via a sharing link.</span></span>

<span data-ttu-id="1379f-p101">La acción **createLink** creará un nuevo vínculo para compartir si el tipo de vínculo especificado no existe para la aplicación que realiza la llamada. Si ya existe el tipo de vínculo para compartir especificado para la aplicación, se devolverá el vínculo para compartir existente.</span><span class="sxs-lookup"><span data-stu-id="1379f-p101">The **createLink** action will create a new sharing link if the specified link type doesn't already exist for the calling application. If a sharing link of the specified type already exists for the app, the existing sharing link will be returned.</span></span>

<span data-ttu-id="1379f-105">Los recursos DriveItem heredan permisos de sus antecesores.</span><span class="sxs-lookup"><span data-stu-id="1379f-105">DriveItem resources inherit permissions from their ancestors.</span></span>

## <a name="permissions"></a><span data-ttu-id="1379f-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="1379f-106">Permissions</span></span>
<span data-ttu-id="1379f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1379f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1379f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1379f-109">Permission type</span></span>      | <span data-ttu-id="1379f-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1379f-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1379f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1379f-111">Delegated (work or school account)</span></span> | <span data-ttu-id="1379f-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1379f-112">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="1379f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1379f-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1379f-114">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1379f-114">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="1379f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1379f-115">Application</span></span> | <span data-ttu-id="1379f-116">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1379f-116">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="1379f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1379f-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/items/{item-id}/createLink
POST /me/drive/root:/{item-path}:/createLink
POST /groups/{group-id}/drive/items/{item-id}/createLink
POST /drives/{drive-id}/items/{item-id}/createLink
```

## <a name="request-body"></a><span data-ttu-id="1379f-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1379f-118">Request body</span></span>
<span data-ttu-id="1379f-p103">El cuerpo de la solicitud define el tipo de vínculo para compartir que busca su aplicación. La solicitud debe ser un objeto JSON con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="1379f-p103">The body of the request defines the type of sharing link your application is looking for. The request should be a JSON object with this property.</span></span>

| <span data-ttu-id="1379f-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="1379f-121">Name</span></span>      | <span data-ttu-id="1379f-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="1379f-122">Type</span></span>   | <span data-ttu-id="1379f-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="1379f-123">Description</span></span>                                                                  |
|:----------|:-------|:-----------------------------------------------------------------------------|
| <span data-ttu-id="1379f-124">**type**</span><span class="sxs-lookup"><span data-stu-id="1379f-124">**type**</span></span>  | <span data-ttu-id="1379f-125">string</span><span class="sxs-lookup"><span data-stu-id="1379f-125">string</span></span> | <span data-ttu-id="1379f-p104">El tipo de vínculo para compartir que se creará. `view`, `edit` o `embed`.</span><span class="sxs-lookup"><span data-stu-id="1379f-p104">The type of sharing link to create. Either `view`, `edit`, or `embed`.</span></span>       |
| <span data-ttu-id="1379f-128">**ámbito**</span><span class="sxs-lookup"><span data-stu-id="1379f-128">**scope**</span></span> | <span data-ttu-id="1379f-129">string</span><span class="sxs-lookup"><span data-stu-id="1379f-129">string</span></span> | <span data-ttu-id="1379f-p105">El ámbito del vínculo que se creará. `anonymous` o `organization`. Opcional.</span><span class="sxs-lookup"><span data-stu-id="1379f-p105">The scope of link to create. Either `anonymous` or `organization`. Optional.</span></span> |

## <a name="link-types"></a><span data-ttu-id="1379f-133">Tipos de vínculos</span><span class="sxs-lookup"><span data-stu-id="1379f-133">Link types</span></span>
<span data-ttu-id="1379f-134">Se pueden usar los siguientes valores para el parámetro de **tipo**.</span><span class="sxs-lookup"><span data-stu-id="1379f-134">The following values are allowed for the **type** parameter.</span></span>

| <span data-ttu-id="1379f-135">Valor del tipo</span><span class="sxs-lookup"><span data-stu-id="1379f-135">Type value</span></span> | <span data-ttu-id="1379f-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="1379f-136">Description</span></span>                                                                                  |
|:-----------|:---------------------------------------------------------------------------------------------|
| `view`     | <span data-ttu-id="1379f-137">Crea un vínculo de solo lectura para el elemento.</span><span class="sxs-lookup"><span data-stu-id="1379f-137">Creates a read-only link to the item.</span></span>                                                        |
| `edit`     | <span data-ttu-id="1379f-138">Crea un vínculo de solo escritura para el elemento.</span><span class="sxs-lookup"><span data-stu-id="1379f-138">Creates a read-write link to the item.</span></span>                                                       |
| `embed`    | <span data-ttu-id="1379f-p106">Crea un vínculo insertable para el elemento. Esta opción solo está disponible para OneDrive Personal.</span><span class="sxs-lookup"><span data-stu-id="1379f-p106">Creates an embeddable link to the item. This option is only available for OneDrive Personal.</span></span> |

## <a name="scope-types"></a><span data-ttu-id="1379f-141">Tipos de ámbitos</span><span class="sxs-lookup"><span data-stu-id="1379f-141">Scope types</span></span>
<span data-ttu-id="1379f-p107">Se permiten los siguientes valores para el parámetro de **ámbito**. Este parámetro es opcional. Si no se especifica el parámetro de **ámbito**, se creará el vínculo más permisivo que esté disponible.</span><span class="sxs-lookup"><span data-stu-id="1379f-p107">The following values are allowed for the **scope** parameter. This is an optional parameter. If the **scope** parameter is not specified, the most permissive link available will be created.</span></span>

| <span data-ttu-id="1379f-145">Valor del tipo</span><span class="sxs-lookup"><span data-stu-id="1379f-145">Type value</span></span>     | <span data-ttu-id="1379f-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="1379f-146">Description</span></span>                                                                                                                   |
|:---------------|:------------------------------------------------------------------------------------------------------------------------------|
| `anonymous`    | <span data-ttu-id="1379f-p108">Crea un vínculo accesible para cualquier usuario para el elemento. El Administrador de inquilinos puede deshabilitar los vínculos anónimos.</span><span class="sxs-lookup"><span data-stu-id="1379f-p108">Creates a link to the item accessible to anyone. Anonymous links may be disabled by the tenant administrator.</span></span>                 |
| `organization` | <span data-ttu-id="1379f-p109">Crea un vínculo accesible dentro de una organización para el elemento. El ámbito del vínculo de organizaciones no está disponible para OneDrive Personal.</span><span class="sxs-lookup"><span data-stu-id="1379f-p109">Creates a link to the item accessible within an organization. Organization link scope is not available for OneDrive Personal.</span></span> |

## <a name="response"></a><span data-ttu-id="1379f-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1379f-151">Response</span></span>

<span data-ttu-id="1379f-152">Si se ejecuta correctamente, este método devuelve un recurso de [permiso](../resources/permission.md) único en el cuerpo de la respuesta que representa el permiso solicitado para compartir un vínculo.</span><span class="sxs-lookup"><span data-stu-id="1379f-152">If successful, this method returns a single [Permission](../resources/permission.md) resource in the response body that represents the requested sharing link permission.</span></span>

<span data-ttu-id="1379f-153">El servicio buscará primero en los permisos actuales y comprobará si ya existe uno del mismo **tipo** para la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="1379f-153">The service will first look at the current permissions and check if one already exists that has the same **type** for the calling application.</span></span>

<span data-ttu-id="1379f-154">La respuesta será `201 Created` si se crea un nuevo vínculo para compartir el elemento o `200 OK` si se devuelve un vínculo existente.</span><span class="sxs-lookup"><span data-stu-id="1379f-154">The response will be `201 Created` if a new sharing link is created for the item or `200 OK` if an existing link is returned.</span></span>

## <a name="example"></a><span data-ttu-id="1379f-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1379f-155">Example</span></span>
<span data-ttu-id="1379f-156">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="1379f-156">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="1379f-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1379f-157">Request</span></span>
<span data-ttu-id="1379f-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1379f-158">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "item_createlink"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/root:/{item-path}:/createLink
Content-type: application/json

{
  "type": "view",
  "scope": "anonymous"
}
```

##### <a name="response"></a><span data-ttu-id="1379f-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1379f-159">Response</span></span>

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

## <a name="creating-company-sharable-links"></a><span data-ttu-id="1379f-160">Crear vínculos de empresa para compartir</span><span class="sxs-lookup"><span data-stu-id="1379f-160">Creating company sharable links</span></span>

<span data-ttu-id="1379f-p110">OneDrive para la Empresa y SharePoint admiten vínculos de empresa para compartir. Son similares a los vínculos anónimos, pero solo funcionan para los miembros del inquilino propietario. Para crear un vínculo de empresa para compartir, utilice el parámetro de **ámbito** con un valor de `organization`.</span><span class="sxs-lookup"><span data-stu-id="1379f-p110">OneDrive for Business and SharePoint support company sharable links. These are similar to anonymous links, except they only work for members of the owning tenant. To create a company sharable link, use the **scope** parameter with a value of `organization`.</span></span>

## <a name="http-request"></a><span data-ttu-id="1379f-164">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1379f-164">HTTP request</span></span>

<!-- { "blockType": "request", "name": "create-link-scoped", "scopes": "files.readwrite service.sharepoint" } -->
```
POST https://graph.microsoft.com/v1.0/me/drive/items/{item-id}/createLink
Content-Type: application/json

{
  "type": "edit",
  "scope": "organization"
}
```

## <a name="http-response"></a><span data-ttu-id="1379f-165">Respuesta HTTP</span><span class="sxs-lookup"><span data-stu-id="1379f-165">HTTP response</span></span>

<span data-ttu-id="1379f-166">La respuesta será `201 Created` si se crea un nuevo vínculo para compartir el elemento o `200 OK` si se devuelve un vínculo existente.</span><span class="sxs-lookup"><span data-stu-id="1379f-166">The response will be `201 Created` if a new sharing link is created for the item or `200 OK` if an existing link is returned.</span></span>

<!-- { "blockType": "response", "@odata.type": "microsoft.graph.permission" } -->
```http
HTTP/1.1 201 Created
Content-Type: application/json

{
  "id": "123ABC",
  "roles": ["write"],
  "link": {
    "type": "view",
    "scope": "organization",
    "webUrl": "https://contoso-my.sharepoint.com/personal/ellen_contoso_com/...",
    "application": {
      "id": "1234",
      "displayName": "Sample Application"
    },
  }
}
```

## <a name="embeddable-links"></a><span data-ttu-id="1379f-167">Vínculos insertables</span><span class="sxs-lookup"><span data-stu-id="1379f-167">Embeddable links</span></span>

<span data-ttu-id="1379f-p111">Cuando se utiliza el tipo de vínculo `embed`, la webUrl que se devuelve se puede insertar en un elemento HTML `<iframe>`. Cuando se crea un vínculo para insertar, la propiedad `webHtml` contiene el código HTML de un `<iframe>` para hospedar el contenido.</span><span class="sxs-lookup"><span data-stu-id="1379f-p111">When using the `embed` link type, the webUrl returned can be embedded in an `<iframe>` HTML element. When an embed link is created the `webHtml` property contains the HTML code for an `<iframe>` to host the content.</span></span>

<span data-ttu-id="1379f-170">**Nota**: Los vínculos para insertar solo se admiten en [unidades](../resources/drive.md) donde el **driveType** es `personal`.</span><span class="sxs-lookup"><span data-stu-id="1379f-170">**Note:** Embed links are only supported in [Drives](../resources/drive.md) where the **driveType** is `personal`.</span></span>

## <a name="remarks"></a><span data-ttu-id="1379f-171">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1379f-171">Remarks</span></span>

* <span data-ttu-id="1379f-172">Los vínculos creados con esta acción no caducan a menos que la organización fuerce una política de caducidad de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1379f-172">Links created using this action do not expire unless a default expiration policy is enforced for the organization.</span></span>
* <span data-ttu-id="1379f-173">Los vínculos se pueden ver en los permisos de uso compartido del elemento y los puede eliminar un propietario del elemento.</span><span class="sxs-lookup"><span data-stu-id="1379f-173">Links are visible in the sharing permissions for the item and can be removed by an owner of the item.</span></span>
* <span data-ttu-id="1379f-174">Los vínculos siempre señalan la versión actual de un elemento, a menos que el elemento esté desprotegido (solo en SharePoint).</span><span class="sxs-lookup"><span data-stu-id="1379f-174">Links always point to the current version of a item unless the item is checked out (SharePoint only).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "item: createLink",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Create sharing link"
} -->
