# <a name="get-contactfolder"></a><span data-ttu-id="5c93a-101">Get contactFolder</span><span class="sxs-lookup"><span data-stu-id="5c93a-101">Get contactFolder</span></span>

<span data-ttu-id="5c93a-102">Obtiene una carpeta de contactos mediante el id. de carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="5c93a-102">Get a contact folder by using the contact folder ID.</span></span>


### <a name="get-another-users-contact-folder"></a><span data-ttu-id="5c93a-103">Obtener la carpeta de contactos de otro usuario</span><span class="sxs-lookup"><span data-stu-id="5c93a-103">Get another user's contact folder</span></span>

<span data-ttu-id="5c93a-104">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener la carpeta de contactos de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="5c93a-104">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to a get contact folder of another user's.</span></span> <span data-ttu-id="5c93a-105">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="5c93a-105">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="5c93a-106">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="5c93a-106">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="5c93a-107">Suponga que otro usuario, Garth, ha compartido una carpeta de contactos con John.</span><span class="sxs-lookup"><span data-stu-id="5c93a-107">Suppose another user, Garth, has shared a contact folder with John.</span></span> <span data-ttu-id="5c93a-108">Puede obtener dicha carpeta compartida especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="5c93a-108">You can get that shared folder by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/contactFolders/{id}
```

<span data-ttu-id="5c93a-109">Esta capacidad se aplica a todas las operaciones de carpeta de contactos GET compatibles para un usuario individual, como se describe en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="5c93a-109">This capability applies to all GET contact folder operations for an individual user, as described in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="5c93a-110">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="5c93a-110">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="5c93a-111">Si Garth no ha compartido su carpeta de contactos con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="5c93a-111">If Garth has not shared his contact folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="5c93a-112">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener una carpeta de contactos del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="5c93a-112">In such cases, specifying a user ID or user principal name only works for getting a contact folder of the signed-in user’s, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contactFolders/{id}
```

<span data-ttu-id="5c93a-113">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="5c93a-113">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="5c93a-114">Carpetas de contactos compartidas</span><span class="sxs-lookup"><span data-stu-id="5c93a-114">Shared contact folders</span></span>
- <span data-ttu-id="5c93a-115">Calendarios compartidos</span><span class="sxs-lookup"><span data-stu-id="5c93a-115">Shared calendars</span></span>
- <span data-ttu-id="5c93a-116">Contactos y eventos en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="5c93a-116">Contacts and events in shared folders</span></span>
- <span data-ttu-id="5c93a-117">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="5c93a-117">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="5c93a-118">Esta capacidad no está disponible en otras operaciones de contactos, eventos y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="5c93a-118">This capability is not available in other operations for contacts, events, and their folders.</span></span>


## <a name="permissions"></a><span data-ttu-id="5c93a-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="5c93a-119">Permissions</span></span>
<span data-ttu-id="5c93a-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5c93a-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5c93a-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5c93a-122">Permission type</span></span>      | <span data-ttu-id="5c93a-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5c93a-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5c93a-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5c93a-124">Delegated (work or school account)</span></span> | <span data-ttu-id="5c93a-125">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5c93a-125">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="5c93a-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5c93a-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5c93a-127">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5c93a-127">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="5c93a-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5c93a-128">Application</span></span> | <span data-ttu-id="5c93a-129">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5c93a-129">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="5c93a-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5c93a-130">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactFolders/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="5c93a-131">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5c93a-131">Optional query parameters</span></span>
<span data-ttu-id="5c93a-132">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c93a-132">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="5c93a-133">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5c93a-133">Request headers</span></span>
| <span data-ttu-id="5c93a-134">Nombre</span><span class="sxs-lookup"><span data-stu-id="5c93a-134">Name</span></span>       | <span data-ttu-id="5c93a-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c93a-135">Type</span></span> | <span data-ttu-id="5c93a-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c93a-136">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="5c93a-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="5c93a-137">Authorization</span></span>  | <span data-ttu-id="5c93a-138">string</span><span class="sxs-lookup"><span data-stu-id="5c93a-138">string</span></span>  | <span data-ttu-id="5c93a-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5c93a-p106">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="5c93a-141">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="5c93a-141">Request body</span></span>
<span data-ttu-id="5c93a-142">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5c93a-142">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5c93a-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c93a-143">Response</span></span>

<span data-ttu-id="5c93a-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5c93a-144">If successful, this method returns a `200 OK` response code and [contactFolder](../resources/contactfolder.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="5c93a-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5c93a-145">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5c93a-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5c93a-146">Request</span></span>
<span data-ttu-id="5c93a-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5c93a-147">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contactfolder"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contactFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="5c93a-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5c93a-148">Response</span></span>
<span data-ttu-id="5c93a-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5c93a-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 104

{
  "displayName": "Finance",
  "id": "AAMkAGI2TKI5AAA=",
  "parentFolderId": "AAMkAGI2AAEOAAA="
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get contactFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
