# <a name="mailfolder-copy"></a><span data-ttu-id="f2867-101">mailFolder: copy</span><span class="sxs-lookup"><span data-stu-id="f2867-101">mailFolder: copy</span></span>

<span data-ttu-id="f2867-102">Copia un objeto mailfolder y su contenido en otro objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="f2867-102">Copy a mailfolder and its contents to another mailfolder.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f2867-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f2867-103">Prerequisites</span></span>
<span data-ttu-id="f2867-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="f2867-104">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="f2867-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f2867-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/mailFolders/{id}/copy
POST /users/{id | userPrincipalName}/mailFolders/{id}/copy
```
## <a name="request-headers"></a><span data-ttu-id="f2867-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f2867-106">Request headers</span></span>
| <span data-ttu-id="f2867-107">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2867-107">Header</span></span>       | <span data-ttu-id="f2867-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f2867-108">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="f2867-109">Authorization</span><span class="sxs-lookup"><span data-stu-id="f2867-109">Authorization</span></span>  | <span data-ttu-id="f2867-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f2867-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="f2867-112">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f2867-112">Content-Type</span></span>  | <span data-ttu-id="f2867-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f2867-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="f2867-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f2867-115">Request body</span></span>
<span data-ttu-id="f2867-116">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="f2867-116">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="f2867-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f2867-117">Parameter</span></span>    | <span data-ttu-id="f2867-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="f2867-118">Type</span></span>   |<span data-ttu-id="f2867-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2867-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f2867-120">destinationId</span><span class="sxs-lookup"><span data-stu-id="f2867-120">destinationId</span></span>|<span data-ttu-id="f2867-121">String</span><span class="sxs-lookup"><span data-stu-id="f2867-121">String</span></span>|<span data-ttu-id="f2867-122">Identificador de la carpeta o el nombre de carpeta conocido *Inbox*, *Drafts*, *SentItems* o *DeletedItems*.</span><span class="sxs-lookup"><span data-stu-id="f2867-122">The folder ID, or the *Inbox*, *Drafts*, *SentItems*, or *DeletedItems* well-known folder name.</span></span>|

## <a name="response"></a><span data-ttu-id="f2867-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2867-123">Response</span></span>

<span data-ttu-id="f2867-124">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [MailFolder](../resources/mailfolder.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2867-124">If successful, this method returns `200, OK` response code and [MailFolder](../resources/mailfolder.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f2867-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2867-125">Example</span></span>
<span data-ttu-id="f2867-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f2867-126">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f2867-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f2867-127">Request</span></span>
<span data-ttu-id="f2867-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2867-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "mailfolder_copy"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/mailFolders/{id}/copy
Content-type: application/json
Content-length: 44

{
  "destinationId": "destinationId-value"
}
```

##### <a name="response"></a><span data-ttu-id="f2867-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2867-129">Response</span></span>
<span data-ttu-id="f2867-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f2867-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "mailFolder: copy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
