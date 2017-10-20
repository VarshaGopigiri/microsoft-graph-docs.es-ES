# <a name="get-contact"></a><span data-ttu-id="72580-101">Get contact</span><span class="sxs-lookup"><span data-stu-id="72580-101">Get contact</span></span>

<span data-ttu-id="72580-102">Recupera las propiedades y relaciones de un objeto contact.</span><span class="sxs-lookup"><span data-stu-id="72580-102">Retrieve the properties and relationships of a contact object.</span></span>


### <a name="get-contacts-in-another-users-contact-folder"></a><span data-ttu-id="72580-103">Obtener los contactos de la carpeta de contactos de otro usuario</span><span class="sxs-lookup"><span data-stu-id="72580-103">Get contacts in another user's contact folder</span></span>

<span data-ttu-id="72580-104">Si dispone de permisos de la aplicación o si tiene los [permisos](#permissions) delegados apropiados de un usuario, es posible obtener los contactos de la carpeta de contactos de otro usuario.</span><span class="sxs-lookup"><span data-stu-id="72580-104">If you have application permissions, or if you have the appropriate delegated [permissions](#permissions) from one user, it's possible to get contacts from another user's contact folder.</span></span> <span data-ttu-id="72580-105">Esta sección se centra en escenarios que implican permisos delegados.</span><span class="sxs-lookup"><span data-stu-id="72580-105">This section focuses on scenarios that involve delegated permissions.</span></span>

<span data-ttu-id="72580-106">Por ejemplo, su aplicación ha adquirido permisos delegados del usuario John.</span><span class="sxs-lookup"><span data-stu-id="72580-106">For example, your app has acquired delegated permissions from the user, John.</span></span> <span data-ttu-id="72580-107">Suponga que otro usuario, Garth, ha compartido una carpeta de contactos con John.</span><span class="sxs-lookup"><span data-stu-id="72580-107">Suppose another user, Garth, has shared a contact folder with John.</span></span> <span data-ttu-id="72580-108">Puede obtener un contacto de dicha carpeta compartida especificando el identificador de usuario de Garth (o su nombre principal de usuario) en la consulta de ejemplo que se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="72580-108">You can get a contact in that shared folder by specifying Garth’s user ID (or user principal name) in the example query shown below.</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /users/{Garth-id | Garth-userPrincipalName}/contacts/{id}
```

<span data-ttu-id="72580-109">Esta capacidad se aplica a todas las operaciones de contactos GET compatibles para un usuario individual, como se muestra en la sección [solicitud HTTP](#http-request) a continuación.</span><span class="sxs-lookup"><span data-stu-id="72580-109">This capability applies to all the supported GET contacts operations for an individual user, as listed in the [HTTP request](#http-request) section below.</span></span> <span data-ttu-id="72580-110">También se aplica si Garth ha delegado todo el buzón en John.</span><span class="sxs-lookup"><span data-stu-id="72580-110">It also applies if Garth has delegated his entire mailbox to John.</span></span>

<span data-ttu-id="72580-111">Si Garth no ha compartido su carpeta de contactos con John ni ha delegado su buzón en John, especificar el identificador de usuario del Garth o el nombre principal de usuario en esas operaciones GET devolverá un error.</span><span class="sxs-lookup"><span data-stu-id="72580-111">If Garth has not shared his contact folder with John, nor has he delegated his mailbox to John, specifying Garth’s user ID or user principal name in those GET operations will return an error.</span></span> <span data-ttu-id="72580-112">En tales casos, especificar un identificador de usuario o un nombre principal de usuario solo funciona para obtener un contacto de las carpetas de contactos del usuario que ha iniciado sesión, y la consulta es equivalente a usar el método abreviado de /me:</span><span class="sxs-lookup"><span data-stu-id="72580-112">In such cases, specifying a user ID or user principal name only works for getting a contact in the signed-in user’s own contact folders, and the query is equivalent to using the /me shortcut:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts/{id}
```

<span data-ttu-id="72580-113">Esta capacidad solo está disponible en las operaciones GET de:</span><span class="sxs-lookup"><span data-stu-id="72580-113">This capability is available in only GET operations of:</span></span>

- <span data-ttu-id="72580-114">Carpetas de contactos compartidas</span><span class="sxs-lookup"><span data-stu-id="72580-114">Shared contact folders</span></span>
- <span data-ttu-id="72580-115">Calendarios compartidos</span><span class="sxs-lookup"><span data-stu-id="72580-115">Shared calendars</span></span>
- <span data-ttu-id="72580-116">Contactos y eventos en carpetas compartidas</span><span class="sxs-lookup"><span data-stu-id="72580-116">Contacts and events in shared folders</span></span>
- <span data-ttu-id="72580-117">Los recursos anteriores en buzones delegados</span><span class="sxs-lookup"><span data-stu-id="72580-117">The above resources in delegated mailboxes</span></span>

<span data-ttu-id="72580-118">Esta capacidad no está disponible en otras operaciones de contactos, eventos y sus carpetas.</span><span class="sxs-lookup"><span data-stu-id="72580-118">This capability is not available in other operations for contacts, events, and their folders.</span></span>


## <a name="permissions"></a><span data-ttu-id="72580-119">Permisos</span><span class="sxs-lookup"><span data-stu-id="72580-119">Permissions</span></span>
<span data-ttu-id="72580-p105">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="72580-p105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="72580-122">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="72580-122">Permission type</span></span>      | <span data-ttu-id="72580-123">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="72580-123">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="72580-124">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="72580-124">Delegated (work or school account)</span></span> | <span data-ttu-id="72580-125">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="72580-125">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="72580-126">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="72580-126">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="72580-127">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="72580-127">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="72580-128">Aplicación</span><span class="sxs-lookup"><span data-stu-id="72580-128">Application</span></span> | <span data-ttu-id="72580-129">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="72580-129">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="72580-130">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="72580-130">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="72580-131">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="72580-131">A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
GET /me/contacts/{id}
GET /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="72580-132">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="72580-132">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
GET /me/contactfolders/{Id}/contacts/{id}
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts/{id}
```
<span data-ttu-id="72580-p106">Un [contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="72580-p106">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
GET /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="72580-135">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="72580-135">Optional query parameters</span></span>
|<span data-ttu-id="72580-136">Nombre</span><span class="sxs-lookup"><span data-stu-id="72580-136">Name</span></span>|<span data-ttu-id="72580-137">Valor</span><span class="sxs-lookup"><span data-stu-id="72580-137">Value</span></span>|<span data-ttu-id="72580-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="72580-138">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="72580-139">$expand</span><span class="sxs-lookup"><span data-stu-id="72580-139">$expand</span></span>|<span data-ttu-id="72580-140">string</span><span class="sxs-lookup"><span data-stu-id="72580-140">string</span></span>|<span data-ttu-id="72580-p107">Lista separada por comas de relaciones para expandir e incluir en la respuesta. Consulte la tabla de relaciones del objeto [contact](../resources/contact.md) para saber los nombres admitidos.</span><span class="sxs-lookup"><span data-stu-id="72580-p107">Comma-separated list of relationships to expand and include in the response. See the relationships table of the [contact](../resources/contact.md) object for supported names.</span></span> |
|<span data-ttu-id="72580-143">$select</span><span class="sxs-lookup"><span data-stu-id="72580-143">$select</span></span>|<span data-ttu-id="72580-144">string</span><span class="sxs-lookup"><span data-stu-id="72580-144">string</span></span>|<span data-ttu-id="72580-145">Lista separada por comas de propiedades para incluir en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72580-145">Comma-separated list of properties to include in the response.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="72580-146">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="72580-146">Request headers</span></span>
| <span data-ttu-id="72580-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="72580-147">Header</span></span>       | <span data-ttu-id="72580-148">Valor</span><span class="sxs-lookup"><span data-stu-id="72580-148">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="72580-149">Authorization</span><span class="sxs-lookup"><span data-stu-id="72580-149">Authorization</span></span>  | <span data-ttu-id="72580-p108">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="72580-p108">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="72580-152">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="72580-152">Request body</span></span>
<span data-ttu-id="72580-153">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="72580-153">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="72580-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72580-154">Response</span></span>

<span data-ttu-id="72580-155">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="72580-155">If successful, this method returns a `200 OK` response code and [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="72580-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="72580-156">Example</span></span>
##### <a name="request"></a><span data-ttu-id="72580-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="72580-157">Request</span></span>
<span data-ttu-id="72580-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="72580-158">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contact"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts/{id}
```
##### <a name="response"></a><span data-ttu-id="72580-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="72580-159">Response</span></span>
<span data-ttu-id="72580-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="72580-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
