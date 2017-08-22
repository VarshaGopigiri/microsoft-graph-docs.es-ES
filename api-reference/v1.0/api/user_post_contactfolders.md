# <a name="create-contactfolder"></a><span data-ttu-id="e5239-101">Create ContactFolder</span><span class="sxs-lookup"><span data-stu-id="e5239-101">Create ContactFolder</span></span>

<span data-ttu-id="e5239-102">Crea una contactFolder en la carpeta predeterminada de contactos del usuario.</span><span class="sxs-lookup"><span data-stu-id="e5239-102">Create a new contactFolder under the user's default contacts folder.</span></span>

<span data-ttu-id="e5239-103">También se puede [crear una contactfolder como elemento secundario de cualquier carpeta de contacto especificada](contactfolder_post_childfolders.md).</span><span class="sxs-lookup"><span data-stu-id="e5239-103">You can also [create a new contactfolder as a child of any specified contact folder](contactfolder_post_childfolders.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e5239-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e5239-104">Prerequisites</span></span>
<span data-ttu-id="e5239-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Contacts.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="e5239-105">One of the following **scopes** is required to execute this API: *Contacts.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="e5239-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5239-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/contactFolders
```
## <a name="request-headers"></a><span data-ttu-id="e5239-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5239-107">Request headers</span></span>
| <span data-ttu-id="e5239-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5239-108">Header</span></span>       | <span data-ttu-id="e5239-109">Valor</span><span class="sxs-lookup"><span data-stu-id="e5239-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="e5239-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="e5239-110">Authorization</span></span>  | <span data-ttu-id="e5239-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e5239-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="e5239-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e5239-113">Content-Type</span></span>  | <span data-ttu-id="e5239-114">application/json</span><span class="sxs-lookup"><span data-stu-id="e5239-114">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e5239-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e5239-115">Request body</span></span>
<span data-ttu-id="e5239-116">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [ContactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="e5239-116">In the request body, supply a JSON representation of [ContactFolder](../resources/contactfolder.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="e5239-117">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5239-117">Response</span></span>

<span data-ttu-id="e5239-118">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [ContactFolder](../resources/contactfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5239-118">If successful, this method returns `201, Created` response code and [ContactFolder](../resources/contactfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e5239-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5239-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e5239-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5239-120">Request</span></span>
<span data-ttu-id="e5239-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5239-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_contactfolder_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/contactFolders
Content-type: application/json
Content-length: 84

{
  "parentFolderId": "parentFolderId-value",
  "displayName": "displayName-value"
}
```
<span data-ttu-id="e5239-122">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [contactFolder](../resources/contactfolder.md).</span><span class="sxs-lookup"><span data-stu-id="e5239-122">In the request body, supply a JSON representation of [contactFolder](../resources/contactfolder.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="e5239-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5239-123">Response</span></span>
<span data-ttu-id="e5239-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e5239-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contactFolder"
} -->
```http
HTTP/1.1 201 Created
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
