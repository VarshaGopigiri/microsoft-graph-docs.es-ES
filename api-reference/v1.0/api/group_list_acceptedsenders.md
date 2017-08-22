# <a name="list-acceptedsenders"></a><span data-ttu-id="b6756-101">List acceptedSenders</span><span class="sxs-lookup"><span data-stu-id="b6756-101">List acceptedSenders</span></span>

<span data-ttu-id="b6756-102">Obtiene una lista de usuarios o grupos que se encuentran en la lista de acceptedSenders de este grupo.</span><span class="sxs-lookup"><span data-stu-id="b6756-102">Get a list of users or groups that are in the acceptedSenders list for this group.</span></span>

<span data-ttu-id="b6756-p101">Los usuarios de la lista de remitentes aceptados pueden publicar conversaciones del grupo (identificado en la dirección URL de solicitud GET). Asegúrese de no especificar el mismo usuario o grupo en las listas de remitentes aceptados y de remitentes rechazados, de lo contrario se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="b6756-p101">Users in the accepted senders list can post to conversations of the group (identified in the GET request URL). Make sure you do not specify the same user or group in the accepted senders and rejected senders lists, otherwise you will get an error.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b6756-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b6756-105">Prerequisites</span></span>
<span data-ttu-id="b6756-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Group.Read.All* o *Group.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="b6756-106">One of the following **scopes** is required to execute this API: *Group.Read.All* or *Group.ReadWrite.All*</span></span>
## <a name="http-request"></a><span data-ttu-id="b6756-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6756-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/acceptedSenders
```
## <a name="optional-query-parameters"></a><span data-ttu-id="b6756-108">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b6756-108">Optional query parameters</span></span>
<span data-ttu-id="b6756-109">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6756-109">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b6756-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6756-110">Request headers</span></span>
| <span data-ttu-id="b6756-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6756-111">Header</span></span>       | <span data-ttu-id="b6756-112">Valor</span><span class="sxs-lookup"><span data-stu-id="b6756-112">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b6756-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="b6756-113">Authorization</span></span>  | <span data-ttu-id="b6756-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b6756-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b6756-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6756-116">Request body</span></span>
<span data-ttu-id="b6756-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b6756-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b6756-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6756-118">Response</span></span>

<span data-ttu-id="b6756-119">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6756-119">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b6756-120">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6756-120">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b6756-121">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6756-121">Request</span></span>
<span data-ttu-id="b6756-122">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6756-122">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_acceptedsenders"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/acceptedSenders
```
##### <a name="response"></a><span data-ttu-id="b6756-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6756-123">Response</span></span>
<span data-ttu-id="b6756-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6756-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List acceptedSenders",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->