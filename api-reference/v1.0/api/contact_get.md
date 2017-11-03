# <a name="get-contact"></a><span data-ttu-id="287de-101">Get contact</span><span class="sxs-lookup"><span data-stu-id="287de-101">Get contact</span></span>

<span data-ttu-id="287de-102">Recupera las propiedades y relaciones de un objeto contact.</span><span class="sxs-lookup"><span data-stu-id="287de-102">Retrieve the properties and relationships of a contact object.</span></span>


### <a name="get-contacts-in-another-users-contact-folder"></a><span data-ttu-id="287de-103">Obtener los contactos de la carpeta de contactos de otro usuario</span><span class="sxs-lookup"><span data-stu-id="287de-103">Get contacts in another user's contact folder</span></span>

<span data-ttu-id="287de-104">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los contactos de la carpeta de contactos de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="287de-104">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get contacts from another user's contact folder.</span></span> <span data-ttu-id="287de-105">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="287de-105">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="287de-106">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="287de-106">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="287de-107">Suponga que otro usuario, Garth, ha compartido una carpeta de contactos con John.</span><span class="sxs-lookup"><span data-stu-id="287de-107">Suppose another user, Garth, has shared a contact folder with John.</span></span> <span data-ttu-id="287de-108">Puede obtener un contacto de dicha carpeta compartida especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="287de-108">You can get a contact in that shared folder by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/contacts/{id}
```

<span data-ttu-id="287de-109">Esta capacidad se aplica a todas las operaciones de contactos GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="287de-109">This capability applies to all the supported GET contacts operations for an individual user, as listed in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="287de-110">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="287de-110">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="287de-111">Si Garth no ha compartido su carpeta de contactos con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="287de-111">If Garth has not shared his contact folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="287de-112">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener un contacto de las carpetas de contactos del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="287de-112">In such cases, specifying a user ID or user principal name only works for getting a contact in the signed-in user’s own contact folders, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts/{id}
```

<span data-ttu-id="287de-113">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="287de-113">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="287de-114">Uso compartido de carpetas de contactos, calendarios y carpetas de mensajes</span><span class="sxs-lookup"><span data-stu-id="287de-114">Shared contact folders, calendars, and message folders</span></span> 
- <span data-ttu-id="287de-115">Contactos, eventos y mensajes en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="287de-115">Contacts and events in shared folders</span></span>
- <span data-ttu-id="287de-116">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="287de-116">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="287de-117">Esta capacidad no está disponible en otras operaciones de contactos, eventos, mensajes y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="287de-117">This capability is not available in other operations for contacts, events, and their folders.</span></span>


## <a name="permissions"></a><span data-ttu-id="287de-118">Permisos</span><span class="sxs-lookup"><span data-stu-id="287de-118">Permissions</span></span>
<span data-ttu-id="287de-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="287de-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="287de-121">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="287de-121">Permission type</span></span>      | <span data-ttu-id="287de-122">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="287de-122">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="287de-123">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="287de-123">Delegated (work or school account)</span></span> | <span data-ttu-id="287de-124">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="287de-124">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="287de-125">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="287de-125">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="287de-126">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="287de-126">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="287de-127">Aplicación</span><span class="sxs-lookup"><span data-stu-id="287de-127">Application</span></span> | <span data-ttu-id="287de-128">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="287de-128">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="287de-129">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="287de-129">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="287de-130">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="287de-130">A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
GET /me/contacts/{id}
GET /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="287de-131">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="287de-131">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
GET /me/contactfolders/{Id}/contacts/{id}
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts/{id}
```
<span data-ttu-id="287de-p106">[contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="287de-p106">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
GET /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="287de-134">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="287de-134">Optional query parameters</span></span>
|<span data-ttu-id="287de-135">Nombre</span><span class="sxs-lookup"><span data-stu-id="287de-135">Name</span></span>|<span data-ttu-id="287de-136">Valor</span><span class="sxs-lookup"><span data-stu-id="287de-136">Value</span></span>|<span data-ttu-id="287de-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="287de-137">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="287de-138">$expand</span><span class="sxs-lookup"><span data-stu-id="287de-138">$expand</span></span>|<span data-ttu-id="287de-139">string</span><span class="sxs-lookup"><span data-stu-id="287de-139">string</span></span>|<span data-ttu-id="287de-p107">Lista separada por comas de relaciones para expandir e incluir en la respuesta. Consulte la tabla de relaciones del objeto [contact](../resources/contact.md) para saber los nombres admitidos.</span><span class="sxs-lookup"><span data-stu-id="287de-p107">Comma-separated list of relationships to expand and include in the response. See the relationships table of the [contact](../resources/contact.md) object for supported names.</span></span> |
|<span data-ttu-id="287de-142">$select</span><span class="sxs-lookup"><span data-stu-id="287de-142">$select</span></span>|<span data-ttu-id="287de-143">string</span><span class="sxs-lookup"><span data-stu-id="287de-143">string</span></span>|<span data-ttu-id="287de-144">Lista separada por comas de propiedades para incluir en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="287de-144">Comma-separated list of properties to include in the response.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="287de-145">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="287de-145">Request headers</span></span>
| <span data-ttu-id="287de-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="287de-146">Header</span></span>       | <span data-ttu-id="287de-147">Valor</span><span class="sxs-lookup"><span data-stu-id="287de-147">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="287de-148">Authorization</span><span class="sxs-lookup"><span data-stu-id="287de-148">Authorization</span></span>  | <span data-ttu-id="287de-p108">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="287de-p108">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="287de-151">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="287de-151">Request body</span></span>
<span data-ttu-id="287de-152">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="287de-152">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="287de-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="287de-153">Response</span></span>

<span data-ttu-id="287de-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="287de-154">If successful, this method returns a `200 OK` response code and [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="287de-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="287de-155">Example</span></span>
##### <a name="request"></a><span data-ttu-id="287de-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="287de-156">Request</span></span>
<span data-ttu-id="287de-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="287de-157">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contact"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts/{id}
```
##### <a name="response"></a><span data-ttu-id="287de-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="287de-158">Response</span></span>
<span data-ttu-id="287de-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="287de-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1977

{
  "id": "AAMkAGI2THk0AAA=",
  "createdDateTime": "2014-10-19T23:08:24Z",
  "lastModifiedDateTime": "2014-10-19T23:08:24Z",
  "changeKey": "EQAAABYAAACd9nJ/tVysQos2hTfspaWRAAADTIa4",
  "categories": [],
  "parentFolderId": "AAMkAGI2AAEOAAA=",
  "birthday": "1974-07-22",
  "fileAs": "Fort, Garth",
  "displayName": "Garth Fort",
  "givenName": "Garth",
  "initials": "G.F.",
  "middleName": null,
  "nickName": "Garth",
  "surname": "Fort",
  "title": null,
  "yomiGivenName": null,
  "yomiSurname": null,
  "yomiCompanyName": null,
  "generation": null,
  "emailAddresses": [
    {
      "name": "Garth",
      "address": "garth@a830edad9050849NDA1.onmicrosoft.com"
    }
  ],
  "imAddresses": [
    "sip:garthf@a830edad9050849nda1.onmicrosoft.com"
  ],
  "jobTitle": "Web Marketing Manager",
  "companyName": "Contoso, Inc.",
  "department": "Sales & Marketing",
  "officeLocation": "20/1101",
  "profession": null,
  "businessHomePage": "http://www.contoso.com",
  "assistantName": null,
  "manager": null,
  "homePhones": [],
  "mobilePhone": null,
  "businessPhones": [
    "+1 918 555 0101"
  ],
  "homeAddress": {},
  "businessAddress": {
      "street": "10 Contoso Way",
      "city": "Redmond",
      "state": "WA",
      "countryOrRegion": "USA",
      "postalCode": "98075"  
  },
  "otherAddress": {},
  "spouseName": null,
  "personalNotes": null,
  "children": []
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
