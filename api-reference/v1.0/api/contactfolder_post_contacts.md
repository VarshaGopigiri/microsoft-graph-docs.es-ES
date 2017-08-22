# <a name="create-contact"></a><span data-ttu-id="b6101-101">Create Contact</span><span class="sxs-lookup"><span data-stu-id="b6101-101">Create Contact</span></span>

<span data-ttu-id="b6101-102">Agrega un contacto a la carpeta de contactos raíz o al extremo de `contacts` de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="b6101-102">Add a contact to the root Contacts folder or to the `contacts` endpoint of another contact folder.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b6101-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b6101-103">Prerequisites</span></span>
<span data-ttu-id="b6101-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="b6101-104">One of the following **scopes** is required to execute this API: *Contacts.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="b6101-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6101-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contacts
POST /users/{id | userPrincipalName}/contacts

POST /me/contactFolders/{id}/contacts
POST /users/{id | userPrincipalName}/contactFolders/{id}/contacts
```
## <a name="request-headers"></a><span data-ttu-id="b6101-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6101-106">Request headers</span></span>
## <a name="request-headers"></a><span data-ttu-id="b6101-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6101-107">Request headers</span></span>
| <span data-ttu-id="b6101-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6101-108">Header</span></span>       | <span data-ttu-id="b6101-109">Valor</span><span class="sxs-lookup"><span data-stu-id="b6101-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b6101-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="b6101-110">Authorization</span></span>  | <span data-ttu-id="b6101-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6101-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b6101-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b6101-113">Content-Type</span></span>  | <span data-ttu-id="b6101-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6101-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b6101-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6101-116">Request body</span></span>
<span data-ttu-id="b6101-117">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="b6101-117">In the request body, supply a JSON representation of [Contact](../resources/contact.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="b6101-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6101-118">Response</span></span>

<span data-ttu-id="b6101-119">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6101-119">If successful, this method returns `201, Created` response code and [Contact](../resources/contact.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b6101-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6101-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b6101-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6101-121">Request</span></span>
<span data-ttu-id="b6101-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6101-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contact_from_contactfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/contactFolders/{id}/contacts
Content-type: application/json
Content-length: 210

{
  "parentFolderId": "parentFolderId-value",
  "birthday": "datetime-value",
  "fileAs": "fileAs-value",
  "displayName": "displayName-value",
  "givenName": "givenName-value",
  "initials": "initials-value"
}
```
<span data-ttu-id="b6101-123">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="b6101-123">In the request body, supply a JSON representation of [contact](../resources/contact.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="b6101-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6101-124">Response</span></span>
<span data-ttu-id="b6101-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6101-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 210

{
  "parentFolderId": "parentFolderId-value",
  "birthday": "datetime-value",
  "fileAs": "fileAs-value",
  "displayName": "displayName-value",
  "givenName": "givenName-value",
  "initials": "initials-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->