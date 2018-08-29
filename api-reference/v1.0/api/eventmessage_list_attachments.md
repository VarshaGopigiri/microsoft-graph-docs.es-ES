# <a name="list-attachments"></a><span data-ttu-id="ccb68-101">List attachments</span><span class="sxs-lookup"><span data-stu-id="ccb68-101">List attachments</span></span>

<span data-ttu-id="ccb68-102">Recupera una lista de objetos attachment.</span><span class="sxs-lookup"><span data-stu-id="ccb68-102">Retrieve a list of attachment objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="ccb68-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="ccb68-103">Permissions</span></span>
<span data-ttu-id="ccb68-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ccb68-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ccb68-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ccb68-106">Permission type</span></span>      | <span data-ttu-id="ccb68-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ccb68-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ccb68-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ccb68-108">Delegated (work or school account)</span></span> | <span data-ttu-id="ccb68-109">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="ccb68-109">Mail.Read</span></span>    |
|<span data-ttu-id="ccb68-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ccb68-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ccb68-111">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="ccb68-111">Mail.Read</span></span>    |
|<span data-ttu-id="ccb68-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ccb68-112">Application</span></span> | <span data-ttu-id="ccb68-113">Mail.Read</span><span class="sxs-lookup"><span data-stu-id="ccb68-113">Mail.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="ccb68-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ccb68-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/messages/{id}/attachments
GET /users/{id | userPrincipalName}/messages/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="ccb68-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="ccb68-115">Optional query parameters</span></span>
<span data-ttu-id="ccb68-116">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ccb68-116">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="ccb68-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ccb68-117">Request headers</span></span>
| <span data-ttu-id="ccb68-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="ccb68-118">Name</span></span>       | <span data-ttu-id="ccb68-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccb68-119">Type</span></span> | <span data-ttu-id="ccb68-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccb68-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ccb68-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="ccb68-121">Authorization</span></span>  | <span data-ttu-id="ccb68-122">cadena</span><span class="sxs-lookup"><span data-stu-id="ccb68-122">string</span></span>  | <span data-ttu-id="ccb68-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ccb68-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ccb68-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ccb68-125">Request body</span></span>
<span data-ttu-id="ccb68-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ccb68-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ccb68-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ccb68-127">Response</span></span>

<span data-ttu-id="ccb68-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ccb68-128">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ccb68-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ccb68-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ccb68-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ccb68-130">Request</span></span>
<span data-ttu-id="ccb68-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ccb68-131">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/messages/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="ccb68-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ccb68-132">Response</span></span>
<span data-ttu-id="ccb68-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ccb68-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "collection(microsoft.graph.attachment)",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "value": [
    {
      "@odata.type": "microsoft.graph.fileAttachment",
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "base64-contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "datetime-value",
      "id": "id-value",
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
