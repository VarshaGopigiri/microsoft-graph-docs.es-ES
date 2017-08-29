# <a name="get-eventmessage"></a><span data-ttu-id="3499b-101">Get eventMessage</span><span class="sxs-lookup"><span data-stu-id="3499b-101">Get eventMessage</span></span>

<span data-ttu-id="3499b-102">Recupera las propiedades y relaciones del objeto [eventMessage](../resources/eventmessage.md).</span><span class="sxs-lookup"><span data-stu-id="3499b-102">Retrieve the properties and relationships of [eventMessage](../resources/eventmessage.md) object.</span></span>

<span data-ttu-id="3499b-103">Actualmente, esta operación devuelve los cuerpos de los mensajes de evento solo en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="3499b-103">Currently, this operation returns event message bodies in only HTML format.</span></span>

## <a name="permissions"></a><span data-ttu-id="3499b-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="3499b-104">Permissions</span></span>
<span data-ttu-id="3499b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3499b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3499b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3499b-107">Permission type</span></span>      | <span data-ttu-id="3499b-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3499b-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3499b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3499b-109">Delegated (work or school account)</span></span> | <span data-ttu-id="3499b-110">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="3499b-110">Mail.Read</span></span>    |
|<span data-ttu-id="3499b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3499b-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3499b-112">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="3499b-112">Mail.Read</span></span>    |
|<span data-ttu-id="3499b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3499b-113">Application</span></span> | <span data-ttu-id="3499b-114">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="3499b-114">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="3499b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3499b-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}
GET /users/{id | userPrincipalName}/messages/{id}

GET /me/mailFolders/{id}/messages/{id}
GET /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="3499b-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3499b-116">Optional query parameters</span></span>
<span data-ttu-id="3499b-117">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3499b-117">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3499b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3499b-118">Request headers</span></span>
| <span data-ttu-id="3499b-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="3499b-119">Name</span></span>       | <span data-ttu-id="3499b-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="3499b-120">Type</span></span> | <span data-ttu-id="3499b-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="3499b-121">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="3499b-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3499b-122">Authorization</span></span>  | <span data-ttu-id="3499b-123">string</span><span class="sxs-lookup"><span data-stu-id="3499b-123">string</span></span>  | <span data-ttu-id="3499b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3499b-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3499b-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3499b-126">Request body</span></span>
<span data-ttu-id="3499b-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3499b-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3499b-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3499b-128">Response</span></span>

<span data-ttu-id="3499b-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [eventMessage](../resources/eventmessage.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3499b-129">If successful, this method returns a `200 OK` response code and [eventMessage](../resources/eventmessage.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3499b-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3499b-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3499b-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3499b-131">Request</span></span>
<span data-ttu-id="3499b-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3499b-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_eventmessage"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="3499b-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3499b-133">Response</span></span>
<span data-ttu-id="3499b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3499b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.eventmessage"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "html",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value",
  "meetingMessageType": "meetingMessageType-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get eventMessage",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
