# <a name="list-contacts"></a><span data-ttu-id="e7642-101">List contacts</span><span class="sxs-lookup"><span data-stu-id="e7642-101">List contacts</span></span>

<span data-ttu-id="e7642-102">Obtiene una colección de contactos de la carpeta de contactos predeterminada del usuario que inició sesión.</span><span class="sxs-lookup"><span data-stu-id="e7642-102">Get a contact collection from the default Contacts folder of the signed-in user.</span></span>
## <a name="permissions"></a><span data-ttu-id="e7642-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="e7642-103">Permissions</span></span>
<span data-ttu-id="e7642-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e7642-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e7642-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e7642-106">Permission type</span></span>      | <span data-ttu-id="e7642-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e7642-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="e7642-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e7642-108">Delegated (work or school account)</span></span> | <span data-ttu-id="e7642-109">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e7642-109">Contacts.Read, Contacts.ReadWrite</span></span>    | 
|<span data-ttu-id="e7642-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e7642-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e7642-111">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e7642-111">Contacts.Read, Contacts.ReadWrite</span></span>    | 
|<span data-ttu-id="e7642-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e7642-112">Application</span></span> | <span data-ttu-id="e7642-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e7642-113">Contacts.Read, Contacts.ReadWrite</span></span> | 

## <a name="http-request"></a><span data-ttu-id="e7642-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e7642-114">HTTP request</span></span>

<span data-ttu-id="e7642-115">Para obtener todos los contactos del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="e7642-115">To get all the contacts in a user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
GET /users/{id | userPrincipalName}/contacts
```

<span data-ttu-id="e7642-116">Para obtener los contactos de una carpeta específica del buzón del usuario:</span><span class="sxs-lookup"><span data-stu-id="e7642-116">To get contacts in a specific folder in the user's mailbox:</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/contactfolders/{Id}/contacts
GET /users/{id | userPrincipalName}/contactfolders/{id}/contacts

GET /me/contactFolder/{id}/childFolders/{id}/.../contacts
GET /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e7642-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e7642-117">Optional query parameters</span></span>
<span data-ttu-id="e7642-118">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7642-118">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="e7642-119">Por ejemplo, puede usar el parámetro de consulta `$filter` para filtrar contactos en función del dominio de sus direcciones de correo:</span><span class="sxs-lookup"><span data-stu-id="e7642-119">For example, you can use the `$filter` query parameter to filter contacts based on the domain of their email addresses:</span></span>

`https://graph.microsoft.com/v1.0/me/contacts?$filter=emailAddresses/any(a:a/address eq '@domain.com')`



## <a name="request-headers"></a><span data-ttu-id="e7642-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e7642-120">Request headers</span></span>
| <span data-ttu-id="e7642-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7642-121">Header</span></span>       | <span data-ttu-id="e7642-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e7642-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e7642-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="e7642-123">Authorization</span></span>  | <span data-ttu-id="e7642-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e7642-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="e7642-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e7642-126">Content-Type</span></span>   | <span data-ttu-id="e7642-127">application/json</span><span class="sxs-lookup"><span data-stu-id="e7642-127">application/json</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="e7642-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e7642-128">Request body</span></span>
<span data-ttu-id="e7642-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e7642-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e7642-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7642-130">Response</span></span>

<span data-ttu-id="e7642-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e7642-131">If successful, this method returns a `200 OK` response code and collection of [Contact](../resources/contact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e7642-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e7642-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e7642-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e7642-133">Request</span></span>
<span data-ttu-id="e7642-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e7642-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contacts"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contacts
```


##### <a name="response"></a><span data-ttu-id="e7642-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e7642-135">Response</span></span>
<span data-ttu-id="e7642-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e7642-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
