# <a name="create-mailfolder"></a><span data-ttu-id="d6ef6-101">Create MailFolder</span><span class="sxs-lookup"><span data-stu-id="d6ef6-101">Create MailFolder</span></span>

<span data-ttu-id="d6ef6-102">Use esta API para crear un objeto mailfolder secundario.</span><span class="sxs-lookup"><span data-stu-id="d6ef6-102">Use this API to create a new child mailfolder.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d6ef6-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d6ef6-103">Prerequisites</span></span>
<span data-ttu-id="d6ef6-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="d6ef6-104">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="d6ef6-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d6ef6-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/{id}/childFolders
POST /users/{id | userPrincipalName}/mailFolders/{id}/childFolders
```

<span data-ttu-id="d6ef6-106">Especifique la carpeta principal en la dirección URL de consulta como identificador de la carpeta o el nombre de carpeta conocido `Inbox`, `Drafts`, `SentItems` o `DeletedItems`.</span><span class="sxs-lookup"><span data-stu-id="d6ef6-106">Specify the parent folder in the query URL as a folder ID, or the `Inbox`, `Drafts`, `SentItems`, or `DeletedItems` well-known folder name.</span></span>

## <a name="request-headers"></a><span data-ttu-id="d6ef6-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d6ef6-107">Request headers</span></span>
| <span data-ttu-id="d6ef6-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6ef6-108">Header</span></span>       | <span data-ttu-id="d6ef6-109">Valor</span><span class="sxs-lookup"><span data-stu-id="d6ef6-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="d6ef6-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="d6ef6-110">Authorization</span></span>  | <span data-ttu-id="d6ef6-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d6ef6-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="d6ef6-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d6ef6-113">Content-Type</span></span>  | <span data-ttu-id="d6ef6-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d6ef6-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d6ef6-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d6ef6-116">Request body</span></span>
<span data-ttu-id="d6ef6-p103">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros. **displayName** es la única propiedad que se puede escribir de un objeto [MailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="d6ef6-p103">In the request body, provide a JSON object with the following parameters. **displayName** is the only writable property for a [MailFolder](../resources/mailfolder.md) object.</span></span>

| <span data-ttu-id="d6ef6-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d6ef6-119">Parameter</span></span>    | <span data-ttu-id="d6ef6-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6ef6-120">Type</span></span>   |<span data-ttu-id="d6ef6-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d6ef6-121">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d6ef6-122">displayName</span><span class="sxs-lookup"><span data-stu-id="d6ef6-122">displayName</span></span>|<span data-ttu-id="d6ef6-123">String</span><span class="sxs-lookup"><span data-stu-id="d6ef6-123">String</span></span>|<span data-ttu-id="d6ef6-124">Nombre para mostrar de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="d6ef6-124">The display name of the new folder.</span></span>|

## <a name="response"></a><span data-ttu-id="d6ef6-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6ef6-125">Response</span></span>

<span data-ttu-id="d6ef6-126">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d6ef6-126">If successful, this method returns `201, Created` response code and [MailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d6ef6-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d6ef6-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d6ef6-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d6ef6-128">Request</span></span>
<span data-ttu-id="d6ef6-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d6ef6-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_mailfolder_from_mailfolder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/{id}/childFolders
Content-type: application/json
Content-length: 159

{
  "displayName": "displayName-value",
}
```

##### <a name="response"></a><span data-ttu-id="d6ef6-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d6ef6-130">Response</span></span>
<span data-ttu-id="d6ef6-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d6ef6-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.mailFolder"
} -->
```http
HTTP/1.1 200 OK
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
