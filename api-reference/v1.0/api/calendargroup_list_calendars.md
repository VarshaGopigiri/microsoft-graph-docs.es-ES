# <a name="list-calendars"></a><span data-ttu-id="3695a-101">List calendars</span><span class="sxs-lookup"><span data-stu-id="3695a-101">List calendars</span></span>

<span data-ttu-id="3695a-102">Recupera una lista de calendarios que pertenecen a un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="3695a-102">Retrieve a list of calendars belonging to a calendar group.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3695a-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3695a-103">Prerequisites</span></span>
<span data-ttu-id="3695a-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: _Calendars.Read_</span><span class="sxs-lookup"><span data-stu-id="3695a-104">One of the following **scopes** is required to execute this API: _Calendars.Read_</span></span>
## <a name="http-request"></a><span data-ttu-id="3695a-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3695a-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="3695a-106">[calendarGroup](../resources/calendargroup.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3695a-106">A user's default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendarGroup/calendars
GET /users/{id | userPrincipalName}/calendarGroup/calendars
```
<span data-ttu-id="3695a-107">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3695a-107">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>
```http
GET /me/calendarGroups/{id}/calendars
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars
```
## <a name="optional-query-parameters"></a><span data-ttu-id="3695a-108">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3695a-108">Optional query parameters</span></span>
<span data-ttu-id="3695a-109">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3695a-109">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3695a-110">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3695a-110">Request headers</span></span>
| <span data-ttu-id="3695a-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="3695a-111">Name</span></span>       | <span data-ttu-id="3695a-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="3695a-112">Type</span></span> | <span data-ttu-id="3695a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="3695a-113">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="3695a-114">Authorization</span><span class="sxs-lookup"><span data-stu-id="3695a-114">Authorization</span></span>  | <span data-ttu-id="3695a-115">string</span><span class="sxs-lookup"><span data-stu-id="3695a-115">string</span></span>  | <span data-ttu-id="3695a-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3695a-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="3695a-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3695a-118">Request body</span></span>
<span data-ttu-id="3695a-119">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3695a-119">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3695a-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3695a-120">Response</span></span>

<span data-ttu-id="3695a-121">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3695a-121">If successful, this method returns a `200 OK` response code and collection of [Calendar](../resources/calendar.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="3695a-122">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3695a-122">Example</span></span>
##### <a name="request"></a><span data-ttu-id="3695a-123">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3695a-123">Request</span></span>
<span data-ttu-id="3695a-124">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3695a-124">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendars"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarGroups/{id}/calendars
```
##### <a name="response"></a><span data-ttu-id="3695a-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3695a-125">Response</span></span>
<span data-ttu-id="3695a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3695a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 147

{
  "value": [
    {
      "name": "name-value",
      "color": {
      },
      "changeKey": "changeKey-value",
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List calendars",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
