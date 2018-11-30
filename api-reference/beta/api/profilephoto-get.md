---
title: Obtener foto
description: Obtenga el profilePhoto especificado o sus metadatos (propiedades de**profilePhoto** ).
ms.openlocfilehash: 6374680e37d409a89b61d3e2244b45ccb29869e7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091118"
---
# <a name="get-photo"></a><span data-ttu-id="19872-103">Obtener foto</span><span class="sxs-lookup"><span data-stu-id="19872-103">Get photo</span></span>

> <span data-ttu-id="19872-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="19872-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="19872-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="19872-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="19872-106">Obtenga el especificado [profilePhoto](../resources/profilephoto.md) o sus metadatos (propiedades de**profilePhoto** ).</span><span class="sxs-lookup"><span data-stu-id="19872-106">Get the specified [profilePhoto](../resources/profilephoto.md) or its metadata (**profilePhoto** properties).</span></span>

<span data-ttu-id="19872-107">Un GET foto operación primer intento para recuperar la foto especificada de Office 365.</span><span class="sxs-lookup"><span data-stu-id="19872-107">A GET photo operation first attempt to retrieve the specified photo from Office 365.</span></span> <span data-ttu-id="19872-108">Si la foto no está disponible en Office 365, la API intenta recuperar la foto de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19872-108">If the photo is not available in Office 365, the API attempts to retrieve the photo from Azure Active Directory.</span></span>

<span data-ttu-id="19872-109">Los tamaños de fotos HD admitidos en Office 365 son los siguientes: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504' y '648x648'.</span><span class="sxs-lookup"><span data-stu-id="19872-109">The supported sizes of HD photos on Office 365 are as follows: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504', and '648x648'.</span></span> <span data-ttu-id="19872-110">Las fotos pueden ser de cualquier dimensión si se almacenan en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19872-110">Photos can be any dimension if they are stored in Azure Active Directory.</span></span>

<span data-ttu-id="19872-111">Puede obtener los metadatos de la foto más grande disponible, o bien especifique un tamaño para obtener los metadatos de ese tamaño de foto.</span><span class="sxs-lookup"><span data-stu-id="19872-111">You can get the metadata of the largest available photo, or specify a size to get the metadata for that photo size.</span></span>
<span data-ttu-id="19872-112">Si el tamaño solicitado no está disponible, puede obtener un tamaño menor que el usuario haya cargado y facilitado.</span><span class="sxs-lookup"><span data-stu-id="19872-112">If the size you request is not available, you can still get a smaller size that the user has uploaded and made available.</span></span>
<span data-ttu-id="19872-113">Por ejemplo, si el usuario carga una foto de 504 x 504 píxeles, todos los tamaños de la foto salvo el de 648 x 648 estarán disponible para su descarga.</span><span class="sxs-lookup"><span data-stu-id="19872-113">For example, if the user uploads a photo that is 504x504 pixels, then all but the 648x648 size of photo will be available for download.</span></span>
<span data-ttu-id="19872-114">Si el tamaño especificado no está disponible en el buzón del usuario o en Azure Active Directory, se devolverá el tamaño de "1 x 1" con el resto de los metadatos.</span><span class="sxs-lookup"><span data-stu-id="19872-114">If the specified size is not available in the user's mailbox or in Azure Active Directory, the size of '1x1' is returned with the rest of metadata.</span></span>

## <a name="permissions"></a><span data-ttu-id="19872-115">Permisos</span><span class="sxs-lookup"><span data-stu-id="19872-115">Permissions</span></span>
<span data-ttu-id="19872-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="19872-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

> <span data-ttu-id="19872-118">**Nota:** La operación de foto GET en la versión beta es compatible con el trabajo, escuela o cuentas personales de un usuario.</span><span class="sxs-lookup"><span data-stu-id="19872-118">**Note:** The GET photo operation in beta supports a user's work, school, or personal accounts.</span></span> <span data-ttu-id="19872-119">La operación de metadatos de foto GET, sin embargo, admite sólo el usuario trabajo o escuela cuentas y cuentas no personales.</span><span class="sxs-lookup"><span data-stu-id="19872-119">The GET photo metadata operation, however, supports only the user's work or school accounts and not personal accounts.</span></span>

|<span data-ttu-id="19872-120">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="19872-120">Permission type</span></span>      | <span data-ttu-id="19872-121">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="19872-121">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="19872-122">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="19872-122">Delegated (work or school account)</span></span> | <span data-ttu-id="19872-123">Tipo de recurso del **usuario**:</span><span class="sxs-lookup"><span data-stu-id="19872-123">For **user** resource:</span></span><br/><span data-ttu-id="19872-124">User.Read, User.ReadBasic.All, User.Read.All, User.ReadWrite, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="19872-124">User.Read, User.ReadBasic.All, User.Read.All, User.ReadWrite, User.ReadWrite.All</span></span><br /><br /><span data-ttu-id="19872-125">Para el recurso de **grupo**:</span><span class="sxs-lookup"><span data-stu-id="19872-125">For **group** resource:</span></span><br /><span data-ttu-id="19872-126">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="19872-126">Group.Read.All, Group.ReadWrite.All</span></span><br /><br /><span data-ttu-id="19872-127">Para el recurso de **contacto**:</span><span class="sxs-lookup"><span data-stu-id="19872-127">For **contact** resource:</span></span><br /><span data-ttu-id="19872-128">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="19872-128">Contacts.Read, Contacts.ReadWrite</span></span> |
|<span data-ttu-id="19872-129">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="19872-129">Delegated (personal Microsoft account)</span></span>  <br /> <span data-ttu-id="19872-130">**Nota**: no se admite la operación de metadatos.</span><span class="sxs-lookup"><span data-stu-id="19872-130">**Note**: Metadata operation is not supported.</span></span> | <span data-ttu-id="19872-131">Tipo de recurso del **usuario**:</span><span class="sxs-lookup"><span data-stu-id="19872-131">For **user** resource:</span></span><br/><span data-ttu-id="19872-132">User.Read, User.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="19872-132">User.Read, User.ReadWrite</span></span><br /><br /><span data-ttu-id="19872-133">Para el recurso de **contacto**:</span><span class="sxs-lookup"><span data-stu-id="19872-133">For **contact** resource:</span></span><br /><span data-ttu-id="19872-134">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="19872-134">Contacts.Read, Contacts.ReadWrite</span></span> |
|<span data-ttu-id="19872-135">Aplicación</span><span class="sxs-lookup"><span data-stu-id="19872-135">Application</span></span>                        | <span data-ttu-id="19872-136">Tipo de recurso del **usuario**:</span><span class="sxs-lookup"><span data-stu-id="19872-136">For **user** resource:</span></span><br/><span data-ttu-id="19872-137">User.Read.All, User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="19872-137">User.Read.All, User.ReadWrite.All</span></span><br /><br /><span data-ttu-id="19872-138">Para el recurso de **grupo**:</span><span class="sxs-lookup"><span data-stu-id="19872-138">For **group** resource:</span></span><br /><span data-ttu-id="19872-139">Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="19872-139">Group.Read.All, Group.ReadWrite.All</span></span><br /><br /><span data-ttu-id="19872-140">Para el recurso de **contacto**:</span><span class="sxs-lookup"><span data-stu-id="19872-140">For **contact** resource:</span></span><br /><span data-ttu-id="19872-141">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="19872-141">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="19872-142">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="19872-142">HTTP request</span></span> 

### <a name="get-the-photo"></a><span data-ttu-id="19872-143">Obtener la foto</span><span class="sxs-lookup"><span data-stu-id="19872-143">Get the photo</span></span>
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
### <a name="get-the-metadata-of-the-photo"></a><span data-ttu-id="19872-144">Obtener los metadatos de la foto</span><span class="sxs-lookup"><span data-stu-id="19872-144">Get the metadata of the photo</span></span>
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

### <a name="get-the-metadata-for-a-specific-photo-size"></a><span data-ttu-id="19872-145">Obtener los metadatos para un tamaño de foto específica</span><span class="sxs-lookup"><span data-stu-id="19872-145">Get the metadata for a specific photo size</span></span>
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

## <a name="path-parameters"></a><span data-ttu-id="19872-146">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="19872-146">Path parameters</span></span>

|<span data-ttu-id="19872-147">**Parámetro**</span><span class="sxs-lookup"><span data-stu-id="19872-147">**Parameter**</span></span>|<span data-ttu-id="19872-148">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="19872-148">**Type**</span></span>|<span data-ttu-id="19872-149">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="19872-149">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="19872-150">size</span><span class="sxs-lookup"><span data-stu-id="19872-150">size</span></span>  |<span data-ttu-id="19872-151">String</span><span class="sxs-lookup"><span data-stu-id="19872-151">String</span></span>  | <span data-ttu-id="19872-152">Un tamaño de foto.</span><span class="sxs-lookup"><span data-stu-id="19872-152">A photo size.</span></span> <span data-ttu-id="19872-153">Los tamaños de fotos HD admitidos en Office 365 son los siguientes: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504' y '648x648'.</span><span class="sxs-lookup"><span data-stu-id="19872-153">The supported sizes of HD photos on Office 365 are as follows: '48x48', '64x64', '96x96', '120x120', '240x240', '360x360','432x432', '504x504', and '648x648'.</span></span> <span data-ttu-id="19872-154">Las fotos pueden ser de cualquier dimensión si se almacenan en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="19872-154">Photos can be any dimension if they are stored in Azure Active Directory.</span></span> |

## <a name="optional-query-parameters"></a><span data-ttu-id="19872-155">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="19872-155">Optional query parameters</span></span>
<span data-ttu-id="19872-156">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19872-156">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="19872-157">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="19872-157">Request headers</span></span>
| <span data-ttu-id="19872-158">Nombre</span><span class="sxs-lookup"><span data-stu-id="19872-158">Name</span></span>       | <span data-ttu-id="19872-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="19872-159">Type</span></span> | <span data-ttu-id="19872-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="19872-160">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="19872-161">Authorization</span><span class="sxs-lookup"><span data-stu-id="19872-161">Authorization</span></span>  | <span data-ttu-id="19872-162">string</span><span class="sxs-lookup"><span data-stu-id="19872-162">string</span></span>  | <span data-ttu-id="19872-p108">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="19872-p108">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="19872-165">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="19872-165">Request body</span></span>
<span data-ttu-id="19872-166">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="19872-166">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="19872-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="19872-167">Response</span></span>
### <a name="response-for-getting-the-photo"></a><span data-ttu-id="19872-168">Respuesta para obtener la foto</span><span class="sxs-lookup"><span data-stu-id="19872-168">Response for getting the photo</span></span>
<span data-ttu-id="19872-p109">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y los datos binarios de la foto solicitada.  Si no hay ninguna foto, la operación devuelve `404 Not Found`.</span><span class="sxs-lookup"><span data-stu-id="19872-p109">If successful, this method returns a `200 OK` response code and binary data of the requested photo.  If no photo exists, the operation returns `404 Not Found`.</span></span>
### <a name="response-for-getting-the-metadata-of-the-photo"></a><span data-ttu-id="19872-171">Respuesta para obtener los metadatos de la foto</span><span class="sxs-lookup"><span data-stu-id="19872-171">Response for getting the metadata of the photo</span></span>
<span data-ttu-id="19872-172">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [profilePhoto](../resources/profilephoto.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="19872-172">If successful, this method returns a `200 OK` response code and [profilePhoto](../resources/profilephoto.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="19872-173">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="19872-173">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="19872-174">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="19872-174">Request 1</span></span>
<span data-ttu-id="19872-175">Esta solicitud obtiene la foto del usuario que ha iniciado sesión, en el tamaño más grande disponible.</span><span class="sxs-lookup"><span data-stu-id="19872-175">This request gets the photo for the signed-in user, in the largest available size.</span></span>

<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/beta/me/photo/$value
Content-Type: image/jpg
```

##### <a name="response-1"></a><span data-ttu-id="19872-176">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="19872-176">Response 1</span></span>
<span data-ttu-id="19872-p110">Contiene los datos binarios de la foto solicitada. El código de respuesta HTTP es 200.</span><span class="sxs-lookup"><span data-stu-id="19872-p110">Contains the binary data of the requested photo. The HTTP response code is 200.</span></span>

##### <a name="request-2"></a><span data-ttu-id="19872-179">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="19872-179">Request 2</span></span>
<span data-ttu-id="19872-180">Esta solicitud recibe la foto de 48x48 para el usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="19872-180">This request gets the 48x48 photo for the signed-in user.</span></span>

<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/beta/me/photos/48x48/$value
Content-Type: image/jpg
```

##### <a name="response-2"></a><span data-ttu-id="19872-181">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="19872-181">Response 2</span></span>
<span data-ttu-id="19872-182">Contiene los datos binarios de la foto de 48x48 solicitada.</span><span class="sxs-lookup"><span data-stu-id="19872-182">Contains the binary data of the requested 48x48 photo.</span></span> <span data-ttu-id="19872-183">El código de respuesta HTTP es 200.</span><span class="sxs-lookup"><span data-stu-id="19872-183">The HTTP response code is 200.</span></span>

##### <a name="request-3"></a><span data-ttu-id="19872-184">Solicitud 3</span><span class="sxs-lookup"><span data-stu-id="19872-184">Request 3</span></span>
<span data-ttu-id="19872-185">Esta solicitud obtiene los metadatos de la foto del usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="19872-185">This request gets the metadata of the user photo of the signed-in user.</span></span>

<!-- {
  "blockType": "ignored"
}-->
```http
GET https://graph.microsoft.com/beta/me/photo
```

##### <a name="response-3"></a><span data-ttu-id="19872-186">Respuesta 3</span><span class="sxs-lookup"><span data-stu-id="19872-186">Response 3</span></span>
<span data-ttu-id="19872-p112">Los siguientes datos de respuesta muestran los metadatos de la foto. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar.</span><span class="sxs-lookup"><span data-stu-id="19872-p112">The following response data shows the photo metadata. Note: The response object shown here may be truncated for brevity.</span></span>

<!-- {
  "blockType": "ignored"
}-->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/photo/$entity",
    "@odata.id": "https://graph.microsoft.com/beta/users('ddfcd489-628b-7d04-b48b-20075df800e5@1717622f-1d94-c0d4-9d74-f907ad6677b4')/photo",
    "@odata.mediaContentType": "image/jpeg",
    "@odata.mediaEtag": "\"BA09D118\"",
    "id": "240X240",
    "width": 240,
    "height": 240
}
```

<span data-ttu-id="19872-p113">Los datos de respuesta siguientes muestran el contenido de una respuesta cuando aún no se ha cargado ninguna foto para el usuario. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar.</span><span class="sxs-lookup"><span data-stu-id="19872-p113">The following response data shows the contents of a response when a photo hasn't already been uploaded for the user. Note: The response object shown here may be truncated for brevity.</span></span>

<!-- {
  "blockType": "ignored"
}-->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/beta/$metadata#Me/photo/$entity",
    "@odata.id": "https://graph.microsoft.com/beta/users('ddfcd489-628b-7d04-b48b-20075df800e5@1717622f-1d94-c0d4-9d74-f907ad6677b4')/photo",
    "@odata.mediaContentType": "image/gif",
    "@odata.mediaEtag": "",
    "id": "1X1",
    "width": 1,
    "height": 1
}
```
## <a name="using-the-binary-data-of-the-requested-photo"></a><span data-ttu-id="19872-191">Usar los datos binarios de la foto solicitada</span><span class="sxs-lookup"><span data-stu-id="19872-191">Using the binary data of the requested photo</span></span>

<span data-ttu-id="19872-192">Cuando use el punto de conexión `/photo/$value` para obtener los datos binarios de una foto de perfil, tendrá que convertir los datos en una cadena en base 64 para agregarlos como datos adjuntos de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="19872-192">When you use the `/photo/$value` endpoint to get the binary data for a profile photo, you'll need to convert the data into a base-64 string in order to add it as an email attachment.</span></span> <span data-ttu-id="19872-193">Este es un ejemplo de JavaScript de cómo crear una matriz que se puede pasar como valor del parámetro `Attachments` de un [mensaje de Outlook](user-post-messages.md).</span><span class="sxs-lookup"><span data-stu-id="19872-193">Here is an example in JavaScript of how to create an array that you can pass as the value of the `Attachments` parameter of an [Outlook Message](user-post-messages.md).</span></span>

      const attachments = [{
        '@odata.type': '#microsoft.graph.fileAttachment',
        ContentBytes: file.toString('base64'),
        Name: 'mypic.jpg'
      }];

<span data-ttu-id="19872-194">Vea el [Ejemplo de conexión a Microsoft Graph de Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample) para obtener una implementación de este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="19872-194">See the [Microsoft Graph Connect Sample for Node.js](https://github.com/microsoftgraph/nodejs-connect-rest-sample) for an implementation of this example.</span></span>

<span data-ttu-id="19872-195">Si quiere que la imagen aparezca en una página web, cree un objeto en memoria de la imagen y conviértalo en el origen de un elemento Image.</span><span class="sxs-lookup"><span data-stu-id="19872-195">If you want to display the image on a web page, create an in-memory object from the image and make that object the source of an image element.</span></span> <span data-ttu-id="19872-196">Este es un ejemplo de JavaScript de esta operación.</span><span class="sxs-lookup"><span data-stu-id="19872-196">Here is an example in JavaScript of this operation.</span></span>

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
