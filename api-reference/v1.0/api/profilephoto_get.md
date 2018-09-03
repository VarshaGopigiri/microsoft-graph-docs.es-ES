# <a name="get-photo"></a><span data-ttu-id="2cdf7-101">Obtener foto</span><span class="sxs-lookup"><span data-stu-id="2cdf7-101">Get photo</span></span>

<span data-ttu-id="2cdf7-102">Obtenga el objeto [profilePhoto](../resources/profilephoto.md) especificado o sus metadatos (propiedades profilePhoto).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-102">Get the specified [profilePhoto](../resources/profilephoto.md) or its metadata (profilePhoto properties).</span></span>

> <span data-ttu-id="2cdf7-103">**Nota** Esta operación en la versión 1.0 admite solo un buzón profesional o educativo del usuario y no uno personal.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-103">**Note** This operation in version 1.0 supports only a user's work or school mailboxes and not personal mailboxes.</span></span>

<span data-ttu-id="2cdf7-104">Los tamaños de fotos HD admitidos en Office 365 son los siguientes: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504' y '648x648'.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-104">The supported sizes of HD photos on Office 365 are as follows: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504', and '648x648'.</span></span> <span data-ttu-id="2cdf7-105">Las fotos pueden ser de cualquier dimensión si se almacenan en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-105">Photos can be any dimension if they are stored in Azure Active Directory.</span></span>

<span data-ttu-id="2cdf7-106">Puede obtener los metadatos de la foto más grande disponible, o bien especifique un tamaño para obtener los metadatos de ese tamaño de foto.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-106">You can get the metadata of the largest available photo, or specify a size to get the metadata for that photo size.</span></span>
<span data-ttu-id="2cdf7-107">Si el tamaño solicitado no está disponible, puede obtener un tamaño menor que el usuario haya cargado y facilitado.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-107">If the size you request is not available, you can still get a smaller size that the user has uploaded and made available.</span></span>
<span data-ttu-id="2cdf7-108">Por ejemplo, si el usuario carga una foto de 504 x 504 píxeles, todos los tamaños de la foto salvo el de 648 x 648 estarán disponible para su descarga.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-108">For example, if the user uploads a photo that is 504x504 pixels, then all but the 648x648 size of photo will be available for download.</span></span>

## <a name="permissions"></a><span data-ttu-id="2cdf7-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="2cdf7-109">Permissions</span></span>

<span data-ttu-id="2cdf7-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2cdf7-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2cdf7-112">Permission type</span></span>      | <span data-ttu-id="2cdf7-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2cdf7-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-114">Delegated (work or school account)</span></span> | <span data-ttu-id="2cdf7-115">Tipo de recurso del **usuario**:</span><span class="sxs-lookup"><span data-stu-id="2cdf7-115">For **user** resource:</span></span><br/><span data-ttu-id="2cdf7-116">User.Read, User.ReadBasic.All, User.Read.All, User.ReadWrite, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2cdf7-116">User.Read, User.ReadBasic.All, User.Read.All, User.ReadWrite, User.ReadWrite.All</span></span><br /><br /><span data-ttu-id="2cdf7-117">Para el recurso de **grupo**:</span><span class="sxs-lookup"><span data-stu-id="2cdf7-117">For **group** resource:</span></span><br /><span data-ttu-id="2cdf7-118">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2cdf7-118">Group.Read.All, Group.ReadWrite.All</span></span><br /><br /><span data-ttu-id="2cdf7-119">Para el recurso de **contacto**:</span><span class="sxs-lookup"><span data-stu-id="2cdf7-119">For **contact** resource:</span></span><br /><span data-ttu-id="2cdf7-120">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2cdf7-120">Contacts.Read, Contacts.ReadWrite</span></span> |
|<span data-ttu-id="2cdf7-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2cdf7-122">No admitido</span><span class="sxs-lookup"><span data-stu-id="2cdf7-122">Not supported</span></span> |
|<span data-ttu-id="2cdf7-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2cdf7-123">Application</span></span>                        | <span data-ttu-id="2cdf7-124">Tipo de recurso del **usuario**:</span><span class="sxs-lookup"><span data-stu-id="2cdf7-124">For **user** resource:</span></span><br/><span data-ttu-id="2cdf7-125">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2cdf7-125">User.Read.All, User.ReadWrite.All</span></span><br /><br /><span data-ttu-id="2cdf7-126">Para el recurso de **grupo**:</span><span class="sxs-lookup"><span data-stu-id="2cdf7-126">For **group** resource:</span></span><br /><span data-ttu-id="2cdf7-127">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2cdf7-127">Group.Read.All, Group.ReadWrite.All</span></span><br /><br /><span data-ttu-id="2cdf7-128">Para el recurso de **contacto**:</span><span class="sxs-lookup"><span data-stu-id="2cdf7-128">For **contact** resource:</span></span><br /><span data-ttu-id="2cdf7-129">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2cdf7-129">Contacts.Read, Contacts.ReadWrite</span></span> |


## <a name="http-request-to-get-the-photo"></a><span data-ttu-id="2cdf7-130">Solicitud HTTP para obtener la foto</span><span class="sxs-lookup"><span data-stu-id="2cdf7-130">HTTP request to get the photo</span></span>
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
## <a name="http-request-to-get-the-metadata-of-the-photo"></a><span data-ttu-id="2cdf7-131">Solicitud HTTP para obtener los metadatos de la foto</span><span class="sxs-lookup"><span data-stu-id="2cdf7-131">HTTP request to get the metadata of the photo</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/photo
GET /me/photos
GET /users/{id | userPrincipalName}/photo
GET /groups/{id}/photo
GET /me/contacts/{id}/photo
GET /users/{id | userPrincipalName}/contacts/{id}/photo
GET /me/contactfolders/{contactFolderId}/contacts/{id}/photo
GET /users/{id | userPrincipalName}/contactfolders/{contactFolderId}/contacts/{id}/photo
```

## <a name="http-request-to-get-the-metadata-for-a-specific-photo-size"></a><span data-ttu-id="2cdf7-132">Solicitud HTTP para obtener los metadatos para un tamaño de foto determinado</span><span class="sxs-lookup"><span data-stu-id="2cdf7-132">HTTP request to get the metadata for a specific photo size</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/photos/{size}
GET /users/{id | userPrincipalName}/photos/{size}
GET /groups/{id}/photos/{size}
GET /me/contacts/{id}/photos/{size}
GET /users/{id | userPrincipalName}/contacts/{id}/photos/{size}
GET /me/contactfolders/{contactFolderId}/contacts/{id}/photos/{size}
GET /users/{id | userPrincipalName}/contactfolders/{contactFolderId}/contacts/{id}/photos/{size}
```

## <a name="parameters"></a><span data-ttu-id="2cdf7-133">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cdf7-133">Parameters</span></span>

|<span data-ttu-id="2cdf7-134">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2cdf7-134">Parameter</span></span>|<span data-ttu-id="2cdf7-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="2cdf7-135">Type</span></span>|<span data-ttu-id="2cdf7-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cdf7-136">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2cdf7-137">size</span><span class="sxs-lookup"><span data-stu-id="2cdf7-137">size</span></span>  |<span data-ttu-id="2cdf7-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="2cdf7-138">String</span></span>  | <span data-ttu-id="2cdf7-139">Un tamaño de foto.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-139">A photo size.</span></span> <span data-ttu-id="2cdf7-140">Los tamaños de fotos HD admitidos en Office 365 son los siguientes: '48x48', '64x64', '96x96', '120x120', '240x240',</span><span class="sxs-lookup"><span data-stu-id="2cdf7-140">The supported sizes of HD photos on Office 365 are as follows: '48x48', '64x64', '96x96', '120x120', '240x240',</span></span> 
<span data-ttu-id="2cdf7-141">'360x360','432x432', '504x504' y '648x648'.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-141">'360x360','432x432', '504x504', and '648x648'.</span></span> <span data-ttu-id="2cdf7-142">Las fotos pueden ser de cualquier dimensión si se almacenan en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-142">Photos can be any dimension if they are stored in Azure Active Directory.</span></span> |

## <a name="optional-query-parameters"></a><span data-ttu-id="2cdf7-143">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="2cdf7-143">Optional query parameters</span></span>
<span data-ttu-id="2cdf7-144">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-144">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="2cdf7-145">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2cdf7-145">Request headers</span></span>
| <span data-ttu-id="2cdf7-146">Nombre</span><span class="sxs-lookup"><span data-stu-id="2cdf7-146">Name</span></span>       | <span data-ttu-id="2cdf7-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="2cdf7-147">Type</span></span> | <span data-ttu-id="2cdf7-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cdf7-148">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="2cdf7-149">Authorization</span><span class="sxs-lookup"><span data-stu-id="2cdf7-149">Authorization</span></span>  | <span data-ttu-id="2cdf7-150">cadena</span><span class="sxs-lookup"><span data-stu-id="2cdf7-150">string</span></span>  | <span data-ttu-id="2cdf7-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2cdf7-153">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2cdf7-153">Request body</span></span>
<span data-ttu-id="2cdf7-154">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-154">Do not supply a request body for this method.</span></span>
## <a name="response-for-getting-the-photo"></a><span data-ttu-id="2cdf7-155">Respuesta para obtener la foto</span><span class="sxs-lookup"><span data-stu-id="2cdf7-155">Response for getting the photo</span></span>
<span data-ttu-id="2cdf7-p107">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y los datos binarios de la foto solicitada.  Si no hay ninguna foto, la operación devuelve `404 Not Found`.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-p107">If successful, this method returns a `200 OK` response code and binary data of the requested photo.  If no photo exists, the operation returns `404 Not Found`.</span></span>
## <a name="response-for-getting-the-metadata-of-the-photo"></a><span data-ttu-id="2cdf7-158">Respuesta para obtener los metadatos de la foto</span><span class="sxs-lookup"><span data-stu-id="2cdf7-158">Response for getting the metadata of the photo</span></span>
<span data-ttu-id="2cdf7-159">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [profilePhoto](../resources/profilePhoto.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-159">If successful, this method returns a `200 OK` response code and [profilePhoto](../resources/profilePhoto.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2cdf7-160">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cdf7-160">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="2cdf7-161">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="2cdf7-161">Request 1</span></span>
<span data-ttu-id="2cdf7-162">Esta solicitud obtiene la foto del usuario que ha iniciado sesión, en el tamaño más grande disponible.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-162">This request gets the photo for the signed-in user, in the largest available size.</span></span>
<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/photo/$value
```

##### <a name="response-1"></a><span data-ttu-id="2cdf7-163">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="2cdf7-163">Response 1</span></span>
<span data-ttu-id="2cdf7-p108">Contiene los datos binarios de la foto solicitada. El código de respuesta HTTP es 200.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-p108">Contains the binary data of the requested photo. The HTTP response code is 200.</span></span>

##### <a name="request-2"></a><span data-ttu-id="2cdf7-166">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="2cdf7-166">Request 2</span></span>
<span data-ttu-id="2cdf7-167">Esta solicitud recibe la foto de 48x48 para el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-167">This request gets the 48x48 photo for the signed-in user.</span></span>

<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/photos/48x48/$value
Content-Type: image/jpg
```

##### <a name="response-2"></a><span data-ttu-id="2cdf7-168">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="2cdf7-168">Response 2</span></span>
<span data-ttu-id="2cdf7-169">Contiene los datos binarios de la foto de 48x48 solicitada.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-169">Contains the binary data of the requested 48x48 photo.</span></span> <span data-ttu-id="2cdf7-170">El código de respuesta HTTP es 200.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-170">The HTTP response code is 200.</span></span>

##### <a name="request-3"></a><span data-ttu-id="2cdf7-171">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="2cdf7-171">Request 3</span></span>
<span data-ttu-id="2cdf7-172">Esta solicitud obtiene los metadatos de la foto del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-172">This request gets the metadata of the user photo of the signed-in user.</span></span>
<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/photo
```

##### <a name="response-3"></a><span data-ttu-id="2cdf7-173">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="2cdf7-173">Response 3</span></span>

<span data-ttu-id="2cdf7-p110">Los siguientes datos de respuesta muestran los metadatos de la foto. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-p110">The following response data shows the photo metadata. Note: The response object shown here may be truncated for brevity.</span></span>
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

<span data-ttu-id="2cdf7-p111">Los datos de respuesta siguientes muestran el contenido de una respuesta cuando aún no se ha cargado ninguna foto para el usuario. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-p111">The following response data shows the contents of a response when a photo hasn't already been uploaded for the user. Note: The response object shown here may be truncated for brevity.</span></span>

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
## <a name="using-the-binary-data-of-the-requested-photo"></a><span data-ttu-id="2cdf7-178">Usar los datos binarios de la foto solicitada</span><span class="sxs-lookup"><span data-stu-id="2cdf7-178">Using the binary data of the requested photo</span></span>

<span data-ttu-id="2cdf7-179">Cuando use el punto de conexión `/photo/$value` para obtener los datos binarios de una foto de perfil, tendrá que convertir los datos en una cadena en base 64 para agregarlos como datos adjuntos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-179">When you use the `/photo/$value` endpoint to get the binary data for a profile photo, you'll need to convert the data into a base-64 string in order to add it as an email attachment.</span></span> <span data-ttu-id="2cdf7-180">Este es un ejemplo de JavaScript de cómo crear una matriz que se puede pasar como valor del parámetro `Attachments` de un [mensaje de Outlook](user_post_messages.md).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-180">Here is an example in JavaScript of how to create an array that you can pass as the value of the `Attachments` parameter of an [Outlook Message](user_post_messages.md).</span></span>

      const attachments = [{
        '@odata.type': '#microsoft.graph.fileAttachment',
        ContentBytes: file.toString('base64'),
        Name: 'mypic.jpg'
      }];

<span data-ttu-id="2cdf7-181">Vea el [Ejemplo de conexión a Microsoft Graph de Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample) para obtener una implementación de este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-181">See the [Microsoft Graph Connect Sample for Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample) for an implementation of this example.</span></span>

<span data-ttu-id="2cdf7-182">Si quiere que la imagen aparezca en una página web, cree un objeto en memoria de la imagen y conviértalo en el origen de un elemento Image.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-182">If you want to display the image on a web page, create an in-memory object from the image and make that object the source of an image element.</span></span> <span data-ttu-id="2cdf7-183">Este es un ejemplo de JavaScript de esta operación.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-183">Here is an example in JavaScript of this operation.</span></span>

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
