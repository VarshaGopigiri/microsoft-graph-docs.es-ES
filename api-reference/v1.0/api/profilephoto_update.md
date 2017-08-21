# <a name="update-profilephoto"></a><span data-ttu-id="6f55d-101">Update profilephoto</span><span class="sxs-lookup"><span data-stu-id="6f55d-101">Update profilephoto</span></span>

<span data-ttu-id="6f55d-p101">Actualiza la foto del **user** que inició sesión o el **group** o **contact** especificado. Puesto que actualmente hay un límite de 4 MB en el tamaño total de cada solicitud REST, esto limita el tamaño de la foto que puede agregar a menos de 4 MB.</span><span class="sxs-lookup"><span data-stu-id="6f55d-p101">Update the photo for the signed-in **user**, or the specified **group** or **contact**. Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the photo you can add to under 4MB.</span></span>

<span data-ttu-id="6f55d-104">Puede usar PATCH o PUT para esta operación en la versión 1.0.</span><span class="sxs-lookup"><span data-stu-id="6f55d-104">You can use either PATCH or PUT for this operation in version 1.0.</span></span>

> <span data-ttu-id="6f55d-105">**Nota** Esta operación en la versión 1.0 admite solo un buzón de usuario de trabajo o escuela y no uno personal.</span><span class="sxs-lookup"><span data-stu-id="6f55d-105">**Note** This operation in version 1.0 supports only a user's work or school mailboxes and not personal mailboxes.</span></span>


## <a name="prerequisites"></a><span data-ttu-id="6f55d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6f55d-106">Prerequisites</span></span>
<span data-ttu-id="6f55d-107">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="6f55d-107">One of the following **scopes** is required to execute this API for:</span></span>

- <span data-ttu-id="6f55d-108">Foto de perfil del **usuario** que inició sesión - *User.ReadWrite*, *User.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="6f55d-108">Profile photo of the signed-in **user** - *User.ReadWrite*, *User.ReadWrite.All*</span></span>
- <span data-ttu-id="6f55d-109">Foto de perfil de un **grupo** - *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="6f55d-109">Profile photo of a **group** - *Group.ReadWrite.All*</span></span>
- <span data-ttu-id="6f55d-110">Foto de un **contacto** - *Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="6f55d-110">Photo of a **contact** - *Contacts.ReadWrite*</span></span>

> <span data-ttu-id="6f55d-p102">**Nota** Para actualizar la foto de un usuario de la organización, la aplicación debe tener el permiso de aplicación User.ReadWrite.All y llamar a esta API bajo su propia identidad, no en nombre de un usuario. Para obtener más información, consulte cómo [obtener acceso sin un usuario que ha iniciado sesión](../../../concepts/auth_v2_service.md).</span><span class="sxs-lookup"><span data-stu-id="6f55d-p102">**Note** To update the photo of any user in the organization, your app must have the User.ReadWrite.All application permission and call this API under its own identity, not on behalf of a user. To learn more, see [get access without a signed-in user](../../../concepts/auth_v2_service.md).</span></span>

## <a name="http-request-to-update-the-photo"></a><span data-ttu-id="6f55d-113">Solicitud HTTP para actualizar la foto</span><span class="sxs-lookup"><span data-stu-id="6f55d-113">HTTP request to update the photo</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/photo/$value
PATCH /users/{id | userPrincipalName}/photo/$value
PATCH /groups/{id}/photo/$value
PATCH /me/contacts/{id}/photo/$value
PATCH /users/{id | userPrincipalName}/contacts/{id}/photo/$value
PATCH /me/contactfolders/{contactFolderId}/contacts/{id}/photo/$value
PATCH /users/{id | userPrincipalName}/contactfolders/{contactFolderId}/contacts/{id}/photo/$value

PUT /me/photo/$value
PUT /users/{id | userPrincipalName}/photo/$value
PUT /groups/{id}/photo/$value
PUT /me/contacts/{id}/photo/$value
PUT /users/{id | userPrincipalName}/contacts/{id}/photo/$value
PUT /me/contactfolders/{contactFolderId}/contacts/{id}/photo/$value
PUT /users/{id | userPrincipalName}/contactfolders/{contactFolderId}/contacts/{id}/photo/$value
```
## <a name="request-headers"></a><span data-ttu-id="6f55d-114">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f55d-114">Request headers</span></span>
| <span data-ttu-id="6f55d-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f55d-115">Header</span></span>       | <span data-ttu-id="6f55d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6f55d-116">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6f55d-117">Authorization</span><span class="sxs-lookup"><span data-stu-id="6f55d-117">Authorization</span></span>  | <span data-ttu-id="6f55d-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f55d-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="6f55d-120">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6f55d-120">Content-Type</span></span>  | <span data-ttu-id="6f55d-p104">image/jpeg. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f55d-p104">image/jpeg. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="6f55d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f55d-123">Request body</span></span>
<span data-ttu-id="6f55d-124">En el cuerpo de la solicitud, incluya los datos binarios de la foto.</span><span class="sxs-lookup"><span data-stu-id="6f55d-124">In the request body, include the binary data of the photo in the request body.</span></span>

## <a name="response"></a><span data-ttu-id="6f55d-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f55d-125">Response</span></span>

<span data-ttu-id="6f55d-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK`.</span><span class="sxs-lookup"><span data-stu-id="6f55d-126">If successful, this method returns a `200 OK` response code.</span></span>
## <a name="example"></a><span data-ttu-id="6f55d-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f55d-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6f55d-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f55d-128">Request</span></span>
<span data-ttu-id="6f55d-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f55d-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_profilephoto"
}-->
```http
PUT https://graph.microsoft.com/v1.0/me/photo/$value
Content-type: image/jpeg

Binary data for the image

```
##### <a name="response"></a><span data-ttu-id="6f55d-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f55d-130">Response</span></span>
<span data-ttu-id="6f55d-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f55d-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.profilePhoto"
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update profilephoto",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
