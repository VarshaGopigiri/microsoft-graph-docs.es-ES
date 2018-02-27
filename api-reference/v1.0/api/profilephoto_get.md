# <a name="get-photo"></a><span data-ttu-id="63994-101">Obtener foto</span><span class="sxs-lookup"><span data-stu-id="63994-101">Get photo</span></span>

<span data-ttu-id="63994-102">Obtenga el objeto [profilePhoto](../resources/profilephoto.md) especificado o sus metadatos (propiedades profilePhoto).</span><span class="sxs-lookup"><span data-stu-id="63994-102">Get the specified [profilePhoto](../resources/profilephoto.md) or its metadata (profilePhoto properties).</span></span>

<span data-ttu-id="63994-103">Una operación GET busca la foto especificada en el buzón del usuario de Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="63994-103">A GET operation looks for the specified photo in the user's mailbox on Exchange Online.</span></span>

> <span data-ttu-id="63994-104">**Nota** Esta operación en la versión 1.0 admite solo un buzón profesional o educativo del usuario y no uno personal.</span><span class="sxs-lookup"><span data-stu-id="63994-104">**Note** This operation in version 1.0 supports only a user's work or school mailboxes and not personal mailboxes.</span></span>

## <a name="permissions"></a><span data-ttu-id="63994-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="63994-105">Permissions</span></span>
<span data-ttu-id="63994-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="63994-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

*   <span data-ttu-id="63994-108">Foto de perfil de cualquier usuario del inquilino, incluido el usuario que inició sesión: User.ReadBasic.All; User.Read.All; User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63994-108">Profile photo of any user in the tenant including the signed-in user - User.ReadBasic.All, User.Read.All, User.ReadWrite.All</span></span>
*   <span data-ttu-id="63994-109">Foto de perfil específicamente del usuario que inició sesión: User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63994-109">Profile photo of specifically the signed-in user - User.Read, User.ReadWrite, User.ReadBasic.All, User.Read.All, User.ReadWrite.All</span></span>
* <span data-ttu-id="63994-110">Foto de perfil de un **grupo**: Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63994-110">Profile photo of a **group** - Group.Read.All, Group.ReadWrite.All</span></span>
* <span data-ttu-id="63994-111">Foto de un **contacto**: Contacts.Read; Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="63994-111">Photo of a **contact** - Contacts.Read, Contacts.ReadWrite</span></span>

## <a name="http-request-to-get-the-photo"></a><span data-ttu-id="63994-112">Solicitud HTTP para obtener la foto</span><span class="sxs-lookup"><span data-stu-id="63994-112">HTTP request to get the photo</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/photo/$value
GET /users/{id | userPrincipalName}/photo/$value
GET /groups/{id}/photo/$value
GET /me/contacts/{id}/photo/$value
GET /users/{id | userPrincipalName}/contacts/{id}/photo/$value
GET /me/contactfolders/{contactFolderId}/contacts/{id}/photo/$value
GET /users/{id | userPrincipalName}/contactfolders/{contactFolderId}/contacts/{id}/photo/$value
```
## <a name="http-request-to-get-the-metadata-of-the-photo"></a><span data-ttu-id="63994-113">Solicitud HTTP para obtener los metadatos de la foto</span><span class="sxs-lookup"><span data-stu-id="63994-113">HTTP request to get the metadata of the photo</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/photo
GET /users/{id | userPrincipalName}/photo
GET /groups/{id}/photo
GET /me/contacts/{id}/photo
GET /users/{id | userPrincipalName}/contacts/{id}/photo
GET /me/contactfolders/{contactFolderId}/contacts/{id}/photo
GET /users/{id | userPrincipalName}/contactfolders/{contactFolderId}/contacts/{id}/photo
```

## <a name="optional-query-parameters"></a><span data-ttu-id="63994-114">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="63994-114">Optional query parameters</span></span>
<span data-ttu-id="63994-115">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63994-115">This method supports the [OData Query Parameters](http://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="63994-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63994-116">Request headers</span></span>
| <span data-ttu-id="63994-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="63994-117">Name</span></span>       | <span data-ttu-id="63994-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="63994-118">Type</span></span> | <span data-ttu-id="63994-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="63994-119">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="63994-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="63994-120">Authorization</span></span>  | <span data-ttu-id="63994-121">string</span><span class="sxs-lookup"><span data-stu-id="63994-121">string</span></span>  | <span data-ttu-id="63994-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="63994-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="63994-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63994-124">Request body</span></span>
<span data-ttu-id="63994-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="63994-125">Do not supply a request body for this method.</span></span>
## <a name="response-for-getting-the-photo"></a><span data-ttu-id="63994-126">Respuesta para obtener la foto</span><span class="sxs-lookup"><span data-stu-id="63994-126">Response for getting the photo</span></span>
<span data-ttu-id="63994-p103">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y los datos binarios de la foto solicitada.  Si no hay ninguna foto, la operación devuelve `404 Not Found`.</span><span class="sxs-lookup"><span data-stu-id="63994-p103">If successful, this method returns a `200 OK` response code and binary data of the requested photo.  If no photo exists, the operation returns `404 Not Found`.</span></span>
## <a name="response-for-getting-the-metadata-of-the-photo"></a><span data-ttu-id="63994-129">Respuesta para obtener los metadatos de la foto</span><span class="sxs-lookup"><span data-stu-id="63994-129">Response for getting the metadata of the photo</span></span>
<span data-ttu-id="63994-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [profilePhoto](../resources/profilePhoto.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63994-130">If successful, this method returns a `200 OK` response code and [profilePhoto](../resources/profilePhoto.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="63994-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63994-131">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="63994-132">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="63994-132">Request 1</span></span>
<span data-ttu-id="63994-133">Esta solicitud obtiene la foto del usuario que ha iniciado sesión, en el tamaño más grande disponible.</span><span class="sxs-lookup"><span data-stu-id="63994-133">This request gets the photo for the signed-in user, in the largest available size.</span></span>
<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/photo/$value
```

##### <a name="response-1"></a><span data-ttu-id="63994-134">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="63994-134">Response 1</span></span>
<span data-ttu-id="63994-p104">Contiene los datos binarios de la foto solicitada. El código de respuesta HTTP es 200.</span><span class="sxs-lookup"><span data-stu-id="63994-p104">Contains the binary data of the requested photo. The HTTP response code is 200.</span></span>

##### <a name="request-2"></a><span data-ttu-id="63994-137">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="63994-137">Request 2</span></span>
<span data-ttu-id="63994-138">Esta solicitud obtiene los metadatos de la foto del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="63994-138">This request gets the metadata of the user photo of the signed-in user.</span></span>
<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/photo
```

##### <a name="response-2"></a><span data-ttu-id="63994-139">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="63994-139">Response 2</span></span>

<span data-ttu-id="63994-p105">Los siguientes datos de respuesta muestran los metadatos de la foto. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar.</span><span class="sxs-lookup"><span data-stu-id="63994-p105">The following response data shows the photo metadata. Note: The response object shown here may be truncated for brevity.</span></span>
<!-- {
  "blockType": "ignored"
}-->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/photo/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-7d04-b48b-20075df800e5@1717622f-1d94-c0d4-9d74-f907ad6677b4')/photo",
    "@odata.mediaContentType": "image/jpeg",
    "@odata.mediaEtag": "\"BA09D118\"",
    "id": "240X240",
    "width": 240,
    "height": 240
}
```

<span data-ttu-id="63994-p106">Los datos de respuesta siguientes muestran el contenido de una respuesta cuando aún no se ha cargado ninguna foto para el usuario. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar.</span><span class="sxs-lookup"><span data-stu-id="63994-p106">The following response data shows the contents of a response when a photo hasn't already been uploaded for the user. Note: The response object shown here may be truncated for brevity.</span></span>

<!-- {
  "blockType": "ignored"
}-->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#Me/photo/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-7d04-b48b-20075df800e5@1717622f-1d94-c0d4-9d74-f907ad6677b4')/photo",
    "@odata.mediaContentType": "image/gif",
    "@odata.mediaEtag": "",
    "id": "1X1",
    "width": 1,
    "height": 1
}
```
## <a name="using-the-binary-data-of-the-requested-photo"></a><span data-ttu-id="63994-144">Usar los datos binarios de la foto solicitada</span><span class="sxs-lookup"><span data-stu-id="63994-144">Using the binary data of the requested photo</span></span>

<span data-ttu-id="63994-145">Cuando use el punto de conexión `/photo/$value` para obtener los datos binarios de una foto de perfil, tendrá que convertir los datos en una cadena en base 64 para agregarlos como datos adjuntos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="63994-145">When you use the `/photo/$value` endpoint to get the binary data for a profile photo, you'll need to convert the data into a base-64 string in order to add it as an email attachment.</span></span> <span data-ttu-id="63994-146">Este es un ejemplo de JavaScript de cómo crear una matriz que se puede pasar como valor del parámetro `Attachments` de un [mensaje de Outlook](user_post_messages.md).</span><span class="sxs-lookup"><span data-stu-id="63994-146">Here is an example in JavaScript of how to create an array that you can pass as the value of the `Attachments` parameter of an [Outlook Message](user_post_messages.md).</span></span>

      const attachments = [{
        '@odata.type': '#microsoft.graph.fileAttachment',
        ContentBytes: file.toString('base64'),
        Name: 'mypic.jpg'
      }];

<span data-ttu-id="63994-147">Vea el [Ejemplo de conexión a Microsoft Graph de Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample) para obtener una implementación de este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="63994-147">See the [Microsoft Graph Connect Sample for Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample) for an implementation of this example.</span></span>

<span data-ttu-id="63994-148">Si quiere que la imagen aparezca en una página web, cree un objeto en memoria de la imagen y conviértalo en el origen de un elemento Image.</span><span class="sxs-lookup"><span data-stu-id="63994-148">If you want to display the image on a web page, create an in-memory object from the image and make that object the source of an image element.</span></span> <span data-ttu-id="63994-149">Este es un ejemplo de JavaScript de esta operación.</span><span class="sxs-lookup"><span data-stu-id="63994-149">Here is an example in JavaScript of this operation.</span></span>

    const url = window.URL || window.webkitURL;
    const blobUrl = url.createObjectURL(image.data);
    document.getElementById(imageElement).setAttribute("src", blobUrl);

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
