# <a name="list-posts"></a><span data-ttu-id="0edf3-101">Enumerar publicaciones</span><span class="sxs-lookup"><span data-stu-id="0edf3-101">List posts</span></span>

<span data-ttu-id="0edf3-p101">Obtiene las publicaciones del hilo especificado. Puede especificar la conversación primaria y el hilo, o bien, especificar el hilo sin hacer referencia a la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="0edf3-p101">Get the posts of the specified thread. You can specify both the parent conversation and the thread, or, you can specify the thread without referencing the parent conversation.</span></span>

## <a name="permissions"></a><span data-ttu-id="0edf3-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="0edf3-104">Permissions</span></span>
<span data-ttu-id="0edf3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0edf3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0edf3-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0edf3-107">Permission type</span></span>      | <span data-ttu-id="0edf3-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0edf3-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0edf3-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0edf3-109">Delegated (work or school account)</span></span> | <span data-ttu-id="0edf3-110">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="0edf3-110">Group.ReadWrite.All, Group.Read.All</span></span>    |
|<span data-ttu-id="0edf3-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0edf3-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0edf3-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0edf3-112">Not supported.</span></span>    |
|<span data-ttu-id="0edf3-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0edf3-113">Application</span></span> | <span data-ttu-id="0edf3-114">Group.ReadWrite.All, Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="0edf3-114">Group.ReadWrite.All, Group.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="0edf3-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0edf3-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/threads/{id}/posts
GET /groups/{id}/conversations/{id}/threads/{id}/posts

```
## <a name="optional-query-parameters"></a><span data-ttu-id="0edf3-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0edf3-116">Optional query parameters</span></span>
<span data-ttu-id="0edf3-117">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0edf3-117">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="0edf3-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0edf3-118">Request headers</span></span>
| <span data-ttu-id="0edf3-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0edf3-119">Header</span></span>       | <span data-ttu-id="0edf3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0edf3-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="0edf3-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="0edf3-121">Authorization</span></span>  | <span data-ttu-id="0edf3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0edf3-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="0edf3-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0edf3-124">Request body</span></span>
<span data-ttu-id="0edf3-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0edf3-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0edf3-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0edf3-126">Response</span></span>

<span data-ttu-id="0edf3-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Post](../resources/post.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0edf3-127">If successful, this method returns a `200 OK` response code and collection of [Post](../resources/post.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="0edf3-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0edf3-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="0edf3-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0edf3-129">Request</span></span>
<span data-ttu-id="0edf3-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0edf3-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_posts"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts
```
##### <a name="response"></a><span data-ttu-id="0edf3-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0edf3-131">Response</span></span>
<span data-ttu-id="0edf3-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0edf3-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.post",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 523

{
  "value": [
    {
      "body": {
        "contentType": "",
        "content": "content-value"
      },
      "receivedDateTime": "datetime-value",
      "hasAttachments": true,
      "from": {
        "emailAddress": {
          "name": "name-value",
          "address": "address-value"
        }
      },
      "sender": {
        "emailAddress": {
          "name": "name-value",
          "address": "address-value"
        }
      },
      "conversationThreadId": "conversationThreadId-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List posts",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
