# <a name="list-contacts"></a><span data-ttu-id="71d9f-101">List contacts</span><span class="sxs-lookup"><span data-stu-id="71d9f-101">List contacts</span></span>

<span data-ttu-id="71d9f-102">Obtiene una colección de contactos de la carpeta de contactos predeterminada del usuario que inició sesión (`.../me/contacts`) o de la carpeta de contactos especificada.</span><span class="sxs-lookup"><span data-stu-id="71d9f-102">Get a contact collection from the default Contacts folder of the signed-in user (`.../me/contacts`), or from the specified contact folder.</span></span>
## <a name="permissions"></a><span data-ttu-id="71d9f-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="71d9f-103">Permissions</span></span>
<span data-ttu-id="71d9f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="71d9f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="71d9f-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71d9f-106">Permission type</span></span>      | <span data-ttu-id="71d9f-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71d9f-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="71d9f-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71d9f-108">Delegated (work or school account)</span></span> | <span data-ttu-id="71d9f-109">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="71d9f-109">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="71d9f-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71d9f-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="71d9f-111">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="71d9f-111">Contacts.Read, Contacts.ReadWrite</span></span>    |
|<span data-ttu-id="71d9f-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71d9f-112">Application</span></span> | <span data-ttu-id="71d9f-113">Contacts.Read, Contacts.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="71d9f-113">Contacts.Read, Contacts.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="71d9f-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71d9f-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
GET /users/{id | userPrincipalName}/contacts

GET /me/contactFolders/{id}/contacts
GET /users/{id | userPrincipalName}/contactFolders/{id}/contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="71d9f-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="71d9f-115">Optional query parameters</span></span>
<span data-ttu-id="71d9f-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71d9f-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="71d9f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71d9f-117">Request headers</span></span>
| <span data-ttu-id="71d9f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="71d9f-118">Name</span></span>       | <span data-ttu-id="71d9f-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="71d9f-119">Type</span></span> | <span data-ttu-id="71d9f-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="71d9f-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="71d9f-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="71d9f-121">Authorization</span></span>  | <span data-ttu-id="71d9f-122">string</span><span class="sxs-lookup"><span data-stu-id="71d9f-122">string</span></span>  | <span data-ttu-id="71d9f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="71d9f-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="71d9f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71d9f-125">Request body</span></span>
<span data-ttu-id="71d9f-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="71d9f-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="71d9f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71d9f-127">Response</span></span>

<span data-ttu-id="71d9f-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71d9f-128">If successful, this method returns a `200 OK` response code and collection of [Contact](../resources/contact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="71d9f-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71d9f-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="71d9f-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71d9f-130">Request</span></span>
<span data-ttu-id="71d9f-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71d9f-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contacts"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contactFolders/{id}/contacts
```
##### <a name="response"></a><span data-ttu-id="71d9f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71d9f-132">Response</span></span>
<span data-ttu-id="71d9f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71d9f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
