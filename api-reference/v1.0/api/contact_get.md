# <a name="get-contact"></a><span data-ttu-id="f1b37-101">Get contact</span><span class="sxs-lookup"><span data-stu-id="f1b37-101">Get contact</span></span>

<span data-ttu-id="f1b37-102">Recupera las propiedades y relaciones de un objeto contact.</span><span class="sxs-lookup"><span data-stu-id="f1b37-102">Retrieve the properties and relationships of a contact object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f1b37-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f1b37-103">Prerequisites</span></span>
<span data-ttu-id="f1b37-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Contacts.Read; Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="f1b37-104">One of the following scopes is required to execute this API: Contacts.Read; Contacts.ReadWrite</span></span>
## <a name="http-request"></a><span data-ttu-id="f1b37-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f1b37-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="f1b37-106">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="f1b37-106">A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
GET /me/contacts/{id}
GET /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="f1b37-107">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="f1b37-107">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
GET /me/contactfolders/{Id}/contacts/{id}
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts/{id}
```
<span data-ttu-id="f1b37-p101">[contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="f1b37-p101">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
GET /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="f1b37-110">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f1b37-110">Optional query parameters</span></span>
|<span data-ttu-id="f1b37-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="f1b37-111">Name</span></span>|<span data-ttu-id="f1b37-112">Valor</span><span class="sxs-lookup"><span data-stu-id="f1b37-112">Value</span></span>|<span data-ttu-id="f1b37-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1b37-113">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="f1b37-114">$expand</span><span class="sxs-lookup"><span data-stu-id="f1b37-114">$expand</span></span>|<span data-ttu-id="f1b37-115">string</span><span class="sxs-lookup"><span data-stu-id="f1b37-115">string</span></span>|<span data-ttu-id="f1b37-p102">Lista separada por comas de relaciones para expandir e incluir en la respuesta. Consulte la tabla de relaciones del objeto [contact](../resources/contact.md) para saber los nombres admitidos.</span><span class="sxs-lookup"><span data-stu-id="f1b37-p102">Comma-separated list of relationships to expand and include in the response. See the relationships table of the [contact](../resources/contact.md) object for supported names.</span></span> |
|<span data-ttu-id="f1b37-118">$select</span><span class="sxs-lookup"><span data-stu-id="f1b37-118">$select</span></span>|<span data-ttu-id="f1b37-119">string</span><span class="sxs-lookup"><span data-stu-id="f1b37-119">string</span></span>|<span data-ttu-id="f1b37-120">Lista separada por comas de propiedades para incluir en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1b37-120">Comma-separated list of properties to include in the response.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="f1b37-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f1b37-121">Request headers</span></span>
| <span data-ttu-id="f1b37-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1b37-122">Header</span></span>       | <span data-ttu-id="f1b37-123">Valor</span><span class="sxs-lookup"><span data-stu-id="f1b37-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="f1b37-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="f1b37-124">Authorization</span></span>  | <span data-ttu-id="f1b37-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f1b37-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="f1b37-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f1b37-127">Request body</span></span>
<span data-ttu-id="f1b37-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f1b37-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f1b37-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1b37-129">Response</span></span>

<span data-ttu-id="f1b37-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f1b37-130">If successful, this method returns a `200 OK` response code and [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="f1b37-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f1b37-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f1b37-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f1b37-132">Request</span></span>
<span data-ttu-id="f1b37-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f1b37-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contact"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts/{id}
```
##### <a name="response"></a><span data-ttu-id="f1b37-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f1b37-134">Response</span></span>
<span data-ttu-id="f1b37-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f1b37-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
