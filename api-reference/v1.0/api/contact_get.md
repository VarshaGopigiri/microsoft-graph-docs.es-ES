# <a name="get-contact"></a><span data-ttu-id="8a2e8-101">Get contact</span><span class="sxs-lookup"><span data-stu-id="8a2e8-101">Get contact</span></span>

<span data-ttu-id="8a2e8-102">Recupera las propiedades y relaciones de un objeto contact.</span><span class="sxs-lookup"><span data-stu-id="8a2e8-102">Retrieve the properties and relationships of a contact object.</span></span>
## <a name="permissions"></a><span data-ttu-id="8a2e8-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="8a2e8-103">Permissions</span></span>
<span data-ttu-id="8a2e8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8a2e8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8a2e8-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a2e8-106">Permission type</span></span>      | <span data-ttu-id="8a2e8-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a2e8-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="8a2e8-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a2e8-108">Delegated (work or school account)</span></span> | <span data-ttu-id="8a2e8-109">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a2e8-109">Contacts.Read, Contacts.ReadWrite</span></span>    | 
|<span data-ttu-id="8a2e8-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a2e8-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8a2e8-111">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a2e8-111">Contacts.Read, Contacts.ReadWrite</span></span>    | 
|<span data-ttu-id="8a2e8-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a2e8-112">Application</span></span> | <span data-ttu-id="8a2e8-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a2e8-113">Contacts.Read, Contacts.ReadWrite</span></span> | 

## <a name="http-request"></a><span data-ttu-id="8a2e8-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a2e8-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="8a2e8-115">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8a2e8-115">A [contact](../resources/contact.md) from a user's default [contactFolder](../resources/contactfolder.md).</span></span>
```http
GET /me/contacts/{id}
GET /users/{id | userPrincipalName}/contacts/{id}
```
<span data-ttu-id="8a2e8-116">Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8a2e8-116">A [contact](../resources/contact.md) from a user's top level [contactFolder](../resources/contactfolder.md).</span></span>
```http
GET /me/contactfolders/{Id}/contacts/{id}
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts/{id}
```
<span data-ttu-id="8a2e8-p102">[contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="8a2e8-p102">A [contact](../resources/contact.md) contained in a child folder of a [contactFolder](../resources/mailfolder.md). The example below shows one level of nesting, but a contact can be located in a child of a child and so on.</span></span>
```http
GET /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="8a2e8-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8a2e8-119">Optional query parameters</span></span>
|<span data-ttu-id="8a2e8-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="8a2e8-120">Name</span></span>|<span data-ttu-id="8a2e8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8a2e8-121">Value</span></span>|<span data-ttu-id="8a2e8-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a2e8-122">Description</span></span>|
|:---------------|:--------|:-------|
|<span data-ttu-id="8a2e8-123">$expand</span><span class="sxs-lookup"><span data-stu-id="8a2e8-123">$expand</span></span>|<span data-ttu-id="8a2e8-124">string</span><span class="sxs-lookup"><span data-stu-id="8a2e8-124">string</span></span>|<span data-ttu-id="8a2e8-p103">Lista separada por comas de relaciones para expandir e incluir en la respuesta. Consulte la tabla de relaciones del objeto [contact](../resources/contact.md) para saber los nombres admitidos.</span><span class="sxs-lookup"><span data-stu-id="8a2e8-p103">Comma-separated list of relationships to expand and include in the response. See the relationships table of the [contact](../resources/contact.md) object for supported names.</span></span> |
|<span data-ttu-id="8a2e8-127">$select</span><span class="sxs-lookup"><span data-stu-id="8a2e8-127">$select</span></span>|<span data-ttu-id="8a2e8-128">string</span><span class="sxs-lookup"><span data-stu-id="8a2e8-128">string</span></span>|<span data-ttu-id="8a2e8-129">Lista separada por comas de propiedades para incluir en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a2e8-129">Comma-separated list of properties to include in the response.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="8a2e8-130">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a2e8-130">Request headers</span></span>
| <span data-ttu-id="8a2e8-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8a2e8-131">Header</span></span>       | <span data-ttu-id="8a2e8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8a2e8-132">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8a2e8-133">Authorization</span><span class="sxs-lookup"><span data-stu-id="8a2e8-133">Authorization</span></span>  | <span data-ttu-id="8a2e8-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a2e8-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8a2e8-136">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a2e8-136">Request body</span></span>
<span data-ttu-id="8a2e8-137">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8a2e8-137">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8a2e8-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a2e8-138">Response</span></span>

<span data-ttu-id="8a2e8-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a2e8-139">If successful, this method returns a `200 OK` response code and [contact](../resources/contact.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8a2e8-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a2e8-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8a2e8-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a2e8-141">Request</span></span>
<span data-ttu-id="8a2e8-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a2e8-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contact"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts/{id}
```
##### <a name="response"></a><span data-ttu-id="8a2e8-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a2e8-143">Response</span></span>
<span data-ttu-id="8a2e8-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8a2e8-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
