# <a name="list-contacts"></a><span data-ttu-id="03dae-101">List contacts</span><span class="sxs-lookup"><span data-stu-id="03dae-101">List contacts</span></span>

<span data-ttu-id="03dae-102">Obtiene una colección de contactos de la carpeta de contactos predeterminada del usuario que inició sesión (`.../me/contacts`) o de la carpeta de contactos especificada.</span><span class="sxs-lookup"><span data-stu-id="03dae-102">Get a contact collection from the default Contacts folder of the signed-in user (`.../me/contacts`), or from the specified contact folder.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="03dae-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03dae-103">Prerequisites</span></span>
<span data-ttu-id="03dae-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Contacts.Read; Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="03dae-104">One of the following scopes is required to execute this API: Contacts.Read; Contacts.ReadWrite</span></span>
## <a name="http-request"></a><span data-ttu-id="03dae-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03dae-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/contacts
GET /users/{id | userPrincipalName}/contacts

GET /me/contactFolders/{id}/contacts
GET /users/{id | userPrincipalName}/contactFolders/{id}/contacts
```
## <a name="optional-query-parameters"></a><span data-ttu-id="03dae-106">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="03dae-106">Optional query parameters</span></span>
<span data-ttu-id="03dae-107">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03dae-107">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="03dae-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03dae-108">Request headers</span></span>
| <span data-ttu-id="03dae-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="03dae-109">Name</span></span>       | <span data-ttu-id="03dae-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="03dae-110">Type</span></span> | <span data-ttu-id="03dae-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="03dae-111">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="03dae-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="03dae-112">Authorization</span></span>  | <span data-ttu-id="03dae-113">string</span><span class="sxs-lookup"><span data-stu-id="03dae-113">string</span></span>  | <span data-ttu-id="03dae-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="03dae-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="03dae-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03dae-116">Request body</span></span>
<span data-ttu-id="03dae-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="03dae-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="03dae-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03dae-118">Response</span></span>

<span data-ttu-id="03dae-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03dae-119">If successful, this method returns a `200 OK` response code and collection of [Contact](../resources/contact.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="03dae-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03dae-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="03dae-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03dae-121">Request</span></span>
<span data-ttu-id="03dae-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03dae-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_contacts"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/contactFolders/{id}/contacts
```
##### <a name="response"></a><span data-ttu-id="03dae-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03dae-123">Response</span></span>
<span data-ttu-id="03dae-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="03dae-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
