# <a name="create-mailfolder"></a><span data-ttu-id="2e13a-101">Create MailFolder</span><span class="sxs-lookup"><span data-stu-id="2e13a-101">Create MailFolder</span></span>

<span data-ttu-id="2e13a-102">Use esta API para crear una carpeta de correo en la carpeta raíz del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="2e13a-102">Use this API to create a new mail folder in the root folder of the user's mailbox.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2e13a-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2e13a-103">Prerequisites</span></span>
<span data-ttu-id="2e13a-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="2e13a-104">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="2e13a-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2e13a-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/mailFolders
```
## <a name="request-headers"></a><span data-ttu-id="2e13a-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2e13a-106">Request headers</span></span>
| <span data-ttu-id="2e13a-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e13a-107">Header</span></span>       | <span data-ttu-id="2e13a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="2e13a-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2e13a-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="2e13a-109">Authorization</span></span>  | <span data-ttu-id="2e13a-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2e13a-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="2e13a-112">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2e13a-112">Content-Type</span></span>  | <span data-ttu-id="2e13a-113">application/json</span><span class="sxs-lookup"><span data-stu-id="2e13a-113">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2e13a-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2e13a-114">Request body</span></span>
<span data-ttu-id="2e13a-p102">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros. **displayName** es la única propiedad que se puede escribir de un objeto [MailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="2e13a-p102">In the request body, provide a JSON object with the following parameters. **displayName** is the only writable property for a [MailFolder](../resources/mailfolder.md) object.</span></span>

| <span data-ttu-id="2e13a-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2e13a-117">Parameter</span></span>    | <span data-ttu-id="2e13a-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="2e13a-118">Type</span></span>   |<span data-ttu-id="2e13a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e13a-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2e13a-120">displayName</span><span class="sxs-lookup"><span data-stu-id="2e13a-120">displayName</span></span>|<span data-ttu-id="2e13a-121">String</span><span class="sxs-lookup"><span data-stu-id="2e13a-121">String</span></span>|<span data-ttu-id="2e13a-122">Nombre para mostrar de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="2e13a-122">The display name of the new folder.</span></span>|

## <a name="response"></a><span data-ttu-id="2e13a-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e13a-123">Response</span></span>

<span data-ttu-id="2e13a-124">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y un objeto [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2e13a-124">If successful, this method returns `201, Created` response code and a [MailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2e13a-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2e13a-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2e13a-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2e13a-126">Request</span></span>
<span data-ttu-id="2e13a-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2e13a-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_mailfolder_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value"
}
```

##### <a name="response"></a><span data-ttu-id="2e13a-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e13a-128">Response</span></span>
<span data-ttu-id="2e13a-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2e13a-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 179

{
  "displayName": "displayName-value",
  "parentFolderId": "parentFolderId-value",
  "childFolderCount": 99,
  "unreadItemCount": 99,
  "totalItemCount": 99,
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create MailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
