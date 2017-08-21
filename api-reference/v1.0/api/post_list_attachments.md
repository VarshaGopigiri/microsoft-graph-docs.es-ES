# <a name="list-attachments"></a><span data-ttu-id="b1f07-101">List attachments</span><span class="sxs-lookup"><span data-stu-id="b1f07-101">List attachments</span></span>

<span data-ttu-id="b1f07-102">Recupera una lista de objetos [attachment](../resources/attachment.md) asociados a una publicación.</span><span class="sxs-lookup"><span data-stu-id="b1f07-102">Retrieve a list of [attachment](../resources/attachment.md) objects attached to a post.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b1f07-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b1f07-103">Prerequisites</span></span>
<span data-ttu-id="b1f07-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="b1f07-104">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="b1f07-105">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="b1f07-105">Group.Read.All</span></span>
* <span data-ttu-id="b1f07-106">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b1f07-106">Group.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="b1f07-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b1f07-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="b1f07-108">Datos adjuntos para un [post](../resources/post.md) de un [thread](../resources/conversationthread.md) perteneciente a una [conversation](../resources/conversation.md) de un grupo.</span><span class="sxs-lookup"><span data-stu-id="b1f07-108">Attachments for a [post](../resources/post.md) in a [thread](../resources/conversationthread.md) belonging to a [conversation](../resources/conversation.md) of a group.</span></span>
```http
GET /groups/{id}/threads/{id}/posts/{id}/attachments
GET /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b1f07-109">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b1f07-109">Optional query parameters</span></span>
<span data-ttu-id="b1f07-110">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1f07-110">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b1f07-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b1f07-111">Request headers</span></span>
| <span data-ttu-id="b1f07-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1f07-112">Header</span></span>       | <span data-ttu-id="b1f07-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b1f07-113">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b1f07-114">Authorization</span><span class="sxs-lookup"><span data-stu-id="b1f07-114">Authorization</span></span>  | <span data-ttu-id="b1f07-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b1f07-p101">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b1f07-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b1f07-117">Request body</span></span>
<span data-ttu-id="b1f07-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b1f07-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b1f07-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1f07-119">Response</span></span>

<span data-ttu-id="b1f07-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b1f07-120">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b1f07-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b1f07-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b1f07-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b1f07-122">Request</span></span>
<span data-ttu-id="b1f07-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b1f07-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="b1f07-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b1f07-124">Response</span></span>
<span data-ttu-id="b1f07-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b1f07-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
      "id": "id-value",
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "datetime-value",
      "isInline": false,
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
