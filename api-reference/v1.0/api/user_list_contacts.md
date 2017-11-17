# <a name="list-contacts"></a><span data-ttu-id="5d4d1-101">List contacts</span><span class="sxs-lookup"><span data-stu-id="5d4d1-101">List contacts</span></span>

<span data-ttu-id="5d4d1-102">Obtiene una colección de contactos de la carpeta de contactos predeterminada del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-102">Get a contact collection from the default Contacts folder of the signed-in user.</span></span>


### <a name="get-contacts-in-another-users-contact-folder"></a><span data-ttu-id="5d4d1-103">Obtener los contactos de la carpeta de contactos de otro usuario</span><span class="sxs-lookup"><span data-stu-id="5d4d1-103">Get contacts in another user's contact folder</span></span>

<span data-ttu-id="5d4d1-104">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los contactos de la carpeta de contactos de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-104">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get contacts from another user's contact folder.</span></span> <span data-ttu-id="5d4d1-105">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-105">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="5d4d1-106">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-106">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="5d4d1-107">Suponga que otro usuario, Garth, ha compartido una carpeta de contactos con John.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-107">Suppose another user, Garth, has shared a contact folder with John.</span></span> <span data-ttu-id="5d4d1-108">Puede obtener los contactos de dicha carpeta compartida especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-108">You can get the contacts in that shared folder by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/contacts
```

<span data-ttu-id="5d4d1-109">Esta capacidad se aplica a todas las operaciones de contactos GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-109">This capability applies to all the supported GET contacts operations for an individual user, as listed in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="5d4d1-110">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-110">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="5d4d1-111">Si Garth no ha compartido su carpeta de contactos con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-111">If Garth has not shared his contact folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="5d4d1-112">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener los contactos de las carpetas de contactos del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="5d4d1-112">In such cases, specifying a user ID or user principal name only works for getting contacts in the signed-in user’s own contact folders, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
```

<span data-ttu-id="5d4d1-113">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="5d4d1-113">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="5d4d1-114">Uso compartido de carpetas de contactos, calendarios y carpetas de mensajes</span><span class="sxs-lookup"><span data-stu-id="5d4d1-114">Shared contact folders, calendars, and message folders</span></span> 
- <span data-ttu-id="5d4d1-115">Contactos, eventos y mensajes en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="5d4d1-115">Contacts and events in shared folders</span></span>
- <span data-ttu-id="5d4d1-116">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="5d4d1-116">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="5d4d1-117">Esta capacidad no está disponible en otras operaciones de contactos, eventos, mensajes y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-117">This capability is not available in other operations for contacts, events, and their folders.</span></span>


## <a name="permissions"></a><span data-ttu-id="5d4d1-118">Permisos</span><span class="sxs-lookup"><span data-stu-id="5d4d1-118">Permissions</span></span>
<span data-ttu-id="5d4d1-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5d4d1-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5d4d1-121">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5d4d1-121">Permission type</span></span>      | <span data-ttu-id="5d4d1-122">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5d4d1-122">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5d4d1-123">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5d4d1-123">Delegated (work or school account)</span></span> | <span data-ttu-id="5d4d1-124">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5d4d1-124">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="5d4d1-125">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5d4d1-125">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5d4d1-126">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5d4d1-126">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="5d4d1-127">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5d4d1-127">Application</span></span> | <span data-ttu-id="5d4d1-128">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="5d4d1-128">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="5d4d1-129">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5d4d1-129">HTTP request</span></span>

<span data-ttu-id="5d4d1-130">Para obtener todos los contactos del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="5d4d1-130">To get all the contacts in a user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
GET /users/{id | userPrincipalName}/contacts
```

<span data-ttu-id="5d4d1-131">Para obtener los contactos de una carpeta específica del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="5d4d1-131">To get contacts in a specific folder in the user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders/{Id}/contacts
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts

GET /me/contactFolder/{id}/childFolders/{id}/.../contacts
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="5d4d1-132">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5d4d1-132">Optional query parameters</span></span>
<span data-ttu-id="5d4d1-133">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-133">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="5d4d1-134">Por ejemplo, puede usar el parámetro de consulta `$filter` para filtrar contactos en función del dominio de sus direcciones de correo:</span><span class="sxs-lookup"><span data-stu-id="5d4d1-134">For example, you can use the `$filter` query parameter to filter contacts based on the domain of their email addresses:</span></span>

`https://graph.microsoft.com/v1.0/me/contacts?$filter=emailAddresses/any(a:a/address eq '@domain.com')`



## <a name="request-headers"></a><span data-ttu-id="5d4d1-135">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5d4d1-135">Request headers</span></span>
| <span data-ttu-id="5d4d1-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d4d1-136">Header</span></span>       | <span data-ttu-id="5d4d1-137">Valor</span><span class="sxs-lookup"><span data-stu-id="5d4d1-137">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5d4d1-138">Authorization</span><span class="sxs-lookup"><span data-stu-id="5d4d1-138">Authorization</span></span>  | <span data-ttu-id="5d4d1-p106">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-p106">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="5d4d1-141">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5d4d1-141">Content-Type</span></span>   | <span data-ttu-id="5d4d1-142">application/json</span><span class="sxs-lookup"><span data-stu-id="5d4d1-142">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5d4d1-143">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5d4d1-143">Request body</span></span>
<span data-ttu-id="5d4d1-144">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-144">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5d4d1-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d4d1-145">Response</span></span>

<span data-ttu-id="5d4d1-146">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-146">If successful, this method returns a `200 OK` response code and collection of [Contact](../resources/contact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="5d4d1-147">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5d4d1-147">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5d4d1-148">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5d4d1-148">Request</span></span>
<span data-ttu-id="5d4d1-149">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-149">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contacts"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts
```


##### <a name="response"></a><span data-ttu-id="5d4d1-150">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5d4d1-150">Response</span></span>
<span data-ttu-id="5d4d1-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5d4d1-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
