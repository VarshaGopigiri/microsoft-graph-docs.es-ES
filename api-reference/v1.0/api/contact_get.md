# <a name="get-contact"></a><span data-ttu-id="694df-101">Get contact</span><span class="sxs-lookup"><span data-stu-id="694df-101">Get contact</span></span>

<span data-ttu-id="694df-102">Recupera las propiedades y relaciones de un objeto contact.</span><span class="sxs-lookup"><span data-stu-id="694df-102">Retrieve the properties and relationships of a contact object.</span></span>

<span data-ttu-id="694df-103">Hay dos escenarios donde una aplicación puede obtener un contacto en la carpeta de contactos de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="694df-103">There are two scenarios where an app can get a contact in another user's contact folder:</span></span>

* <span data-ttu-id="694df-104">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="694df-104">If the app has application permissions, or,</span></span>
* <span data-ttu-id="694df-105">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido una carpeta de contactos con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="694df-105">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a contact folder with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="694df-106">Consulte los [Detalles y un ejemplo](../../../concepts/outlook-get-shared-contacts-folders.md).</span><span class="sxs-lookup"><span data-stu-id="694df-106">See [details and an example](../../../concepts/outlook-get-shared-contacts-folders.md).</span></span>


## <a name="permissions"></a><span data-ttu-id="694df-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="694df-107">Permissions</span></span>
<span data-ttu-id="694df-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="694df-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="694df-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="694df-110">Permission type</span></span>      | <span data-ttu-id="694df-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="694df-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="694df-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="694df-112">Delegated (work or school account)</span></span> | <span data-ttu-id="694df-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="694df-113">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="694df-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="694df-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="694df-115">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="694df-115">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="694df-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="694df-116">Application</span></span> | <span data-ttu-id="694df-117">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="694df-117">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="694df-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="694df-118">HTTP request</span></span>
<span data-ttu-id="694df-119"><!-- { "blockType": "ignored" } -->Un [contacto](../resources/contact.md) desde predeterminado de un usuario [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="694df-119"><!-- { "blockType": "ignored" } --> A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
GET /me/contacts/{id}
GET /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="694df-120">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="694df-120">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
GET /me/contactfolders/{Id}/contacts/{id}
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts/{id}
```
<span data-ttu-id="694df-p103">[contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="694df-p103">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
GET /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="694df-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="694df-123">Optional query parameters</span></span>
|<span data-ttu-id="694df-124">Nombre</span><span class="sxs-lookup"><span data-stu-id="694df-124">Name</span></span>|<span data-ttu-id="694df-125">Valor</span><span class="sxs-lookup"><span data-stu-id="694df-125">Value</span></span>|<span data-ttu-id="694df-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="694df-126">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="694df-127">$expand</span><span class="sxs-lookup"><span data-stu-id="694df-127">$expand</span></span>|<span data-ttu-id="694df-128">string</span><span class="sxs-lookup"><span data-stu-id="694df-128">string</span></span>|<span data-ttu-id="694df-p104">Lista separada por comas de relaciones para expandir e incluir en la respuesta. Consulte la tabla de relaciones del objeto [contact](../resources/contact.md) para saber los nombres admitidos.</span><span class="sxs-lookup"><span data-stu-id="694df-p104">Comma-separated list of relationships to expand and include in the response. See the relationships table of the [contact](../resources/contact.md) object for supported names.</span></span> |
|<span data-ttu-id="694df-131">$select</span><span class="sxs-lookup"><span data-stu-id="694df-131">$select</span></span>|<span data-ttu-id="694df-132">string</span><span class="sxs-lookup"><span data-stu-id="694df-132">string</span></span>|<span data-ttu-id="694df-133">Lista separada por comas de propiedades para incluir en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="694df-133">Comma-separated list of properties to include in the response.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="694df-134">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="694df-134">Request headers</span></span>
| <span data-ttu-id="694df-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="694df-135">Header</span></span>       | <span data-ttu-id="694df-136">Valor</span><span class="sxs-lookup"><span data-stu-id="694df-136">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="694df-137">Authorization</span><span class="sxs-lookup"><span data-stu-id="694df-137">Authorization</span></span>  | <span data-ttu-id="694df-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="694df-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="694df-140">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="694df-140">Request body</span></span>
<span data-ttu-id="694df-141">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="694df-141">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="694df-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="694df-142">Response</span></span>

<span data-ttu-id="694df-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="694df-143">If successful, this method returns a `200 OK` response code and [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="694df-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="694df-144">Example</span></span>
##### <a name="request"></a><span data-ttu-id="694df-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="694df-145">Request</span></span>
<span data-ttu-id="694df-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="694df-146">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contact"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts/{id}
```
##### <a name="response"></a><span data-ttu-id="694df-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="694df-147">Response</span></span>
<span data-ttu-id="694df-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="694df-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "businessHomePage": "https://www.contoso.com",
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
