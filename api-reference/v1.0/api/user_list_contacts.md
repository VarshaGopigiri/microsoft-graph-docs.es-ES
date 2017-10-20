# <a name="list-contacts"></a><span data-ttu-id="53b04-101">List contacts</span><span class="sxs-lookup"><span data-stu-id="53b04-101">List contacts</span></span>

<span data-ttu-id="53b04-102">Obtiene una colección de contactos de la carpeta de contactos predeterminada del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="53b04-102">Get a contact collection from the default Contacts folder of the signed-in user.</span></span>


### <a name="get-contacts-in-another-users-contact-folder"></a><span data-ttu-id="53b04-103">Obtener los contactos de la carpeta de contactos de otro usuario</span><span class="sxs-lookup"><span data-stu-id="53b04-103">Get contacts in another user's contact folder</span></span>

<span data-ttu-id="53b04-104">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los contactos de la carpeta de contactos de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="53b04-104">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get contacts from another user's contact folder.</span></span> <span data-ttu-id="53b04-105">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="53b04-105">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="53b04-106">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="53b04-106">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="53b04-107">Suponga que otro usuario, Garth, ha compartido una carpeta de contactos con John.</span><span class="sxs-lookup"><span data-stu-id="53b04-107">Suppose another user, Garth, has shared a contact folder with John.</span></span> <span data-ttu-id="53b04-108">Puede obtener los contactos de dicha carpeta compartida especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="53b04-108">You can get the contacts in that shared folder by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/contacts
```

<span data-ttu-id="53b04-109">Esta capacidad se aplica a todas las operaciones de contactos GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="53b04-109">This capability applies to all the supported GET contacts operations for an individual user, as listed in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="53b04-110">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="53b04-110">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="53b04-111">Si Garth no ha compartido su carpeta de contactos con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="53b04-111">If Garth has not shared his contact folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="53b04-112">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener los contactos de las carpetas de contactos del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="53b04-112">In such cases, specifying a user ID or user principal name only works for getting contacts in the signed-in user’s own contact folders, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
```

<span data-ttu-id="53b04-113">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="53b04-113">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="53b04-114">Carpetas de contactos compartidas</span><span class="sxs-lookup"><span data-stu-id="53b04-114">Shared contact folders</span></span>
- <span data-ttu-id="53b04-115">Calendarios compartidos</span><span class="sxs-lookup"><span data-stu-id="53b04-115">Shared calendars</span></span>
- <span data-ttu-id="53b04-116">Contactos y eventos en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="53b04-116">Contacts and events in shared folders</span></span>
- <span data-ttu-id="53b04-117">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="53b04-117">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="53b04-118">Esta capacidad no está disponible en otras operaciones de contactos, eventos y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="53b04-118">This capability is not available in other operations for contacts, events, and their folders.</span></span>


## <a name="permissions"></a><span data-ttu-id="53b04-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="53b04-119">Permissions</span></span>
<span data-ttu-id="53b04-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="53b04-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="53b04-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="53b04-122">Permission type</span></span>      | <span data-ttu-id="53b04-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="53b04-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="53b04-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="53b04-124">Delegated (work or school account)</span></span> | <span data-ttu-id="53b04-125">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="53b04-125">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="53b04-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="53b04-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="53b04-127">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="53b04-127">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="53b04-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="53b04-128">Application</span></span> | <span data-ttu-id="53b04-129">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="53b04-129">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="53b04-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="53b04-130">HTTP request</span></span>

<span data-ttu-id="53b04-131">Para obtener todos los contactos del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="53b04-131">To get all the contacts in a user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
GET /users/{id | userPrincipalName}/contacts
```

<span data-ttu-id="53b04-132">Para obtener los contactos de una carpeta específica del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="53b04-132">To get contacts in a specific folder in the user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders/{Id}/contacts
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts

GET /me/contactFolder/{id}/childFolders/{id}/.../contacts
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="53b04-133">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="53b04-133">Optional query parameters</span></span>
<span data-ttu-id="53b04-134">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53b04-134">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="53b04-135">Por ejemplo, puede usar el parámetro de consulta `$filter` para filtrar contactos en función del dominio de sus direcciones de correo:</span><span class="sxs-lookup"><span data-stu-id="53b04-135">For example, you can use the `$filter` query parameter to filter contacts based on the domain of their email addresses:</span></span>

`https://graph.microsoft.com/v1.0/me/contacts?$filter=emailAddresses/any(a:a/address eq '@domain.com')`



## <a name="request-headers"></a><span data-ttu-id="53b04-136">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="53b04-136">Request headers</span></span>
| <span data-ttu-id="53b04-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53b04-137">Header</span></span>       | <span data-ttu-id="53b04-138">Valor</span><span class="sxs-lookup"><span data-stu-id="53b04-138">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="53b04-139">Authorization</span><span class="sxs-lookup"><span data-stu-id="53b04-139">Authorization</span></span>  | <span data-ttu-id="53b04-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="53b04-p106">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="53b04-142">Content-Type</span><span class="sxs-lookup"><span data-stu-id="53b04-142">Content-Type</span></span>   | <span data-ttu-id="53b04-143">application/json</span><span class="sxs-lookup"><span data-stu-id="53b04-143">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="53b04-144">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="53b04-144">Request body</span></span>
<span data-ttu-id="53b04-145">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="53b04-145">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="53b04-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53b04-146">Response</span></span>

<span data-ttu-id="53b04-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="53b04-147">If successful, this method returns a `200 OK` response code and collection of [Contact](../resources/contact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="53b04-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="53b04-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="53b04-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="53b04-149">Request</span></span>
<span data-ttu-id="53b04-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="53b04-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contacts"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts
```


##### <a name="response"></a><span data-ttu-id="53b04-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="53b04-151">Response</span></span>
<span data-ttu-id="53b04-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="53b04-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 263

{
  "value": [
    {
      "parentFolderId": "parentFolderId-value",
      "birthday": "datetime-value",
      "fileAs": "fileAs-value",
      "displayName": "displayName-value",
      "givenName": "givenName-value",
      "initials": "initials-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List contacts",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
