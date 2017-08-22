# <a name="list-attachments"></a><span data-ttu-id="03362-101">List attachments</span><span class="sxs-lookup"><span data-stu-id="03362-101">List attachments</span></span>

<span data-ttu-id="03362-102">Recupera una lista de objetos [attachment](../resources/attachment.md) asociados a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="03362-102">Retrieve a list of [attachment](../resources/attachment.md) objects attached to a message.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="03362-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03362-103">Prerequisites</span></span>
<span data-ttu-id="03362-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.Read*</span><span class="sxs-lookup"><span data-stu-id="03362-104">One of the following **scopes** is required to execute this API: *Mail.Read*</span></span> 
## <a name="http-request"></a><span data-ttu-id="03362-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03362-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="03362-106">Datos adjuntos de un [message](../resources/message.md) en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="03362-106">Attachments for a [message](../resources/message.md) in a user's mailbox.</span></span>
```http
GET /me/messages/{id}/attachments
GET /users/{id | userPrincipalName}/messages/{id}/attachments
```
<span data-ttu-id="03362-107">Datos adjuntos de un [message](../resources/message.md) contenido en una [mailFolder](../resources/mailfolder.md) de nivel superior en el buzón de un usuario.</span><span class="sxs-lookup"><span data-stu-id="03362-107">Attachments for a [message](../resources/message.md) contained in a top level [mailFolder](../resources/mailfolder.md) in a user's mailbox.</span></span>
```http
GET /me/mailFolders/{id}/messages/{id}/attachments
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/attachments
```
<span data-ttu-id="03362-p101">Datos adjuntos de un [message](../resources/message.md) contenido en una carpeta secundaria de una [mailFolder](../resources/mailfolder.md) en el buzón de un usuario.  El ejemplo siguiente muestra un nivel de anidamiento, pero un mensaje puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="03362-p101">Attachments for a [message](../resources/message.md) contained in a child folder of a [mailFolder](../resources/mailfolder.md) in a user's mailbox.  The example below shows one level of nesting, but a message can be located in a child of a child and so on.</span></span>
```http
GET /me/mailFolders/{id}/childFolders/{id}/.../messages/{id}/attachments/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/childFolders/{id}/messages/{id}/attachments/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="03362-110">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="03362-110">Optional query parameters</span></span>
<span data-ttu-id="03362-111">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03362-111">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="03362-112">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03362-112">Request headers</span></span>
| <span data-ttu-id="03362-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="03362-113">Name</span></span>       | <span data-ttu-id="03362-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="03362-114">Type</span></span> | <span data-ttu-id="03362-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="03362-115">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="03362-116">Authorization</span><span class="sxs-lookup"><span data-stu-id="03362-116">Authorization</span></span>  | <span data-ttu-id="03362-117">string</span><span class="sxs-lookup"><span data-stu-id="03362-117">string</span></span>  | <span data-ttu-id="03362-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="03362-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="03362-120">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03362-120">Request body</span></span>
<span data-ttu-id="03362-121">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="03362-121">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="03362-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03362-122">Response</span></span>

<span data-ttu-id="03362-123">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03362-123">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="03362-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03362-124">Example</span></span>
##### <a name="request"></a><span data-ttu-id="03362-125">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03362-125">Request</span></span>
<span data-ttu-id="03362-126">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03362-126">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="03362-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03362-127">Response</span></span>
<span data-ttu-id="03362-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="03362-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "value": [
    {
      "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "datetime-value",
      "id": "id-value",
      "isInline": false,
      "isContactPhoto": false,
      "name": "name-value",
      "size": 99
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List attachments",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->