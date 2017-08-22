# <a name="create-contactfolder"></a><span data-ttu-id="5fcd3-101">Create ContactFolder</span><span class="sxs-lookup"><span data-stu-id="5fcd3-101">Create ContactFolder</span></span>

<span data-ttu-id="5fcd3-102">Crea una contactFolder como elemento secundario de una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="5fcd3-102">Create a new contactFolder as a child of a specified folder.</span></span> 

<span data-ttu-id="5fcd3-103">También se puede [crear una contactFolder en la carpeta predeterminada de contactos del usuario](user_post_contactfolders.md).</span><span class="sxs-lookup"><span data-stu-id="5fcd3-103">You can also [create a new contactFolder under the user's default contact folder](user_post_contactfolders.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5fcd3-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5fcd3-104">Prerequisites</span></span>
<span data-ttu-id="5fcd3-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="5fcd3-105">One of the following **scopes** is required to execute this API: *Contacts.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="5fcd3-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5fcd3-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/contactFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/contactFolders/{id}/childFolders
```
## <a name="request-headers"></a><span data-ttu-id="5fcd3-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5fcd3-107">Request headers</span></span>
| <span data-ttu-id="5fcd3-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fcd3-108">Header</span></span>       | <span data-ttu-id="5fcd3-109">Valor</span><span class="sxs-lookup"><span data-stu-id="5fcd3-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5fcd3-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="5fcd3-110">Authorization</span></span>  | <span data-ttu-id="5fcd3-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5fcd3-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="5fcd3-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5fcd3-113">Content-Type</span></span>  | <span data-ttu-id="5fcd3-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5fcd3-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5fcd3-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5fcd3-116">Request body</span></span>
<span data-ttu-id="5fcd3-117">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ContactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="5fcd3-117">In the request body, supply a JSON representation of [ContactFolder](../resources/contactfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="5fcd3-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5fcd3-118">Response</span></span>

<span data-ttu-id="5fcd3-119">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5fcd3-119">If successful, this method returns `201, Created` response code and [ContactFolder](../resources/contactfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5fcd3-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5fcd3-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5fcd3-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5fcd3-121">Request</span></span>
<span data-ttu-id="5fcd3-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5fcd3-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contactfolder_from_contactfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/contactFolders/{id}/childFolders
Content-type: application/json
Content-length: 84

{
  "displayName": "displayName-value"
}
```
<span data-ttu-id="5fcd3-123">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="5fcd3-123">In the request body, supply a JSON representation of [contactFolder](../resources/contactfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="5fcd3-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5fcd3-124">Response</span></span>
<span data-ttu-id="5fcd3-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5fcd3-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 104

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create ContactFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
