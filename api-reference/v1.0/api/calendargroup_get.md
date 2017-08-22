# <a name="get-calendargroup"></a><span data-ttu-id="62f39-101">Get calendarGroup</span><span class="sxs-lookup"><span data-stu-id="62f39-101">Get calendarGroup</span></span>

<span data-ttu-id="62f39-102">Recupera las propiedades y relaciones de un objeto de grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="62f39-102">Retrieve the properties and relationships of a calendar group object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="62f39-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="62f39-103">Prerequisites</span></span>
<span data-ttu-id="62f39-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.Read*</span><span class="sxs-lookup"><span data-stu-id="62f39-104">One of the following **scopes** is required to execute this API: *Calendars.Read*</span></span>
## <a name="http-request"></a><span data-ttu-id="62f39-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="62f39-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="62f39-106">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="62f39-106">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>
```http
GET /me/calendarGroups/{id}
GET /users/{id | userPrincipalName}/calendarGroups/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="62f39-107">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="62f39-107">Optional query parameters</span></span>
<span data-ttu-id="62f39-108">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62f39-108">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="62f39-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="62f39-109">Request headers</span></span>
| <span data-ttu-id="62f39-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="62f39-110">Name</span></span>       | <span data-ttu-id="62f39-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="62f39-111">Type</span></span> | <span data-ttu-id="62f39-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="62f39-112">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="62f39-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="62f39-113">Authorization</span></span>  | <span data-ttu-id="62f39-114">string</span><span class="sxs-lookup"><span data-stu-id="62f39-114">string</span></span>  | <span data-ttu-id="62f39-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="62f39-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="62f39-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="62f39-117">Request body</span></span>
<span data-ttu-id="62f39-118">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="62f39-118">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="62f39-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62f39-119">Response</span></span>

<span data-ttu-id="62f39-120">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62f39-120">If successful, this method returns a `200 OK` response code and [calendarGroup](../resources/calendargroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="62f39-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="62f39-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="62f39-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="62f39-122">Request</span></span>
<span data-ttu-id="62f39-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="62f39-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendargroup"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
```
##### <a name="response"></a><span data-ttu-id="62f39-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62f39-124">Response</span></span>
<span data-ttu-id="62f39-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="62f39-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarGroup"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 110

{
  "name": "name-value",
  "classId": "11b0131d-43c8-4bbb-b2c8-e80f9a50834a",
  "changeKey": "changeKey-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get calendarGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
