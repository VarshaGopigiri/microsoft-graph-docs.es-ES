# <a name="create-contact"></a><span data-ttu-id="3a124-101">Create Contact</span><span class="sxs-lookup"><span data-stu-id="3a124-101">Create Contact</span></span>

<span data-ttu-id="3a124-102">Agrega un contacto a la carpeta de contactos raíz o al extremo de contactos de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="3a124-102">Add a contact to the root Contacts folder or to the contacts endpoint of another contact folder.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3a124-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3a124-103">Prerequisites</span></span>
<span data-ttu-id="3a124-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="3a124-104">One of the following **scopes** is required to execute this API: *Contacts.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="3a124-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3a124-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contacts
POST /users/{id | userPrincipalName}/contacts
POST /me/contactFolders/{contactFolderId}/contacts
POST /users/{id | userPrincipalName}/contactFolders/{contactFolderId}/contacts
```
## <a name="request-headers"></a><span data-ttu-id="3a124-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3a124-106">Request headers</span></span>
| <span data-ttu-id="3a124-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a124-107">Header</span></span>       | <span data-ttu-id="3a124-108">Valor</span><span class="sxs-lookup"><span data-stu-id="3a124-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3a124-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="3a124-109">Authorization</span></span>  | <span data-ttu-id="3a124-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3a124-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="3a124-112">Content-Type</span><span class="sxs-lookup"><span data-stu-id="3a124-112">Content-Type</span></span>  | <span data-ttu-id="3a124-113">application/json</span><span class="sxs-lookup"><span data-stu-id="3a124-113">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3a124-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3a124-114">Request body</span></span>
<span data-ttu-id="3a124-115">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="3a124-115">In the request body, supply a JSON representation of [Contact](../resources/contact.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="3a124-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a124-116">Response</span></span>

<span data-ttu-id="3a124-117">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Contact](../resources/contact.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3a124-117">If successful, this method returns `201, Created` response code and [Contact](../resources/contact.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3a124-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3a124-118">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3a124-119">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3a124-119">Request</span></span>
<span data-ttu-id="3a124-120">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3a124-120">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contact_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/contacts
Content-type: application/json

{
  "givenName": "Pavel",
  "surname": "Bansky",
  "emailAddresses": [
    {
      "address": "pavelb@fabrikam.onmicrosoft.com",
      "name": "Pavel Bansky"
    }
  ],
  "businessPhones": [
    "+1 732 555 0102"
  ]
}
```
<span data-ttu-id="3a124-121">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contact](../resources/contact.md).</span><span class="sxs-lookup"><span data-stu-id="3a124-121">In the request body, supply a JSON representation of [contact](../resources/contact.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="3a124-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3a124-122">Response</span></span>
<span data-ttu-id="3a124-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3a124-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "id-value",
  "createdDateTime": "2015-11-09T02:14:32Z",
  "lastModifiedDateTime": "2015-11-09T02:14:32Z",
   "displayName": "Pavel Bansky"
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
