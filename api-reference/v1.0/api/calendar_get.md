# <a name="get-calendar"></a><span data-ttu-id="e0d97-101">Get calendar</span><span class="sxs-lookup"><span data-stu-id="e0d97-101">Get calendar</span></span>

<span data-ttu-id="e0d97-102">Recupera las propiedades y relaciones del objeto calendar.</span><span class="sxs-lookup"><span data-stu-id="e0d97-102">Retrieve the properties and relationships of calendar object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e0d97-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e0d97-103">Prerequisites</span></span>
<span data-ttu-id="e0d97-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.Read*</span><span class="sxs-lookup"><span data-stu-id="e0d97-104">One of the following **scopes** is required to execute this API: *Calendars.Read*</span></span>
## <a name="http-request"></a><span data-ttu-id="e0d97-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e0d97-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="e0d97-106">[calendar](../resources/calendar.md) predeterminado de un usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="e0d97-106">A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
GET /me/calendar
GET /users/{id | userPrincipalName}/calendar
GET /groups/{id}/calendar
```
<span data-ttu-id="e0d97-107">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e0d97-107">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendars/{id}
GET /users/{id | userPrincipalName}/calendars/{id}

GET /me/calendarGroup/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="e0d97-108">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="e0d97-108">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendarGroups/{id}/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="e0d97-109">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e0d97-109">Optional query parameters</span></span>
<span data-ttu-id="e0d97-110">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0d97-110">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e0d97-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e0d97-111">Request headers</span></span>
| <span data-ttu-id="e0d97-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="e0d97-112">Name</span></span>       | <span data-ttu-id="e0d97-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0d97-113">Type</span></span> | <span data-ttu-id="e0d97-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0d97-114">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e0d97-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="e0d97-115">Authorization</span></span>  | <span data-ttu-id="e0d97-116">string</span><span class="sxs-lookup"><span data-stu-id="e0d97-116">string</span></span>  | <span data-ttu-id="e0d97-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e0d97-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e0d97-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e0d97-119">Request body</span></span>
<span data-ttu-id="e0d97-120">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e0d97-120">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e0d97-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0d97-121">Response</span></span>

<span data-ttu-id="e0d97-122">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e0d97-122">If successful, this method returns a `200 OK` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e0d97-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0d97-123">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e0d97-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e0d97-124">Request</span></span>
<span data-ttu-id="e0d97-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e0d97-125">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendar"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendar
```
##### <a name="response"></a><span data-ttu-id="e0d97-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e0d97-126">Response</span></span>
<span data-ttu-id="e0d97-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e0d97-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#me/calendars/$entity",
    "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/calendars('AAMkAGI2TGuLAAA=')",
    "id": "AAMkAGI2TGuLAAA=",
    "name": "Calendar",
    "color": "auto",
    "changeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w==",
    "canShare":true,
    "canViewPrivateItems":true,
    "canEdit":true,
    "owner":{
        "name":"Fanny Downs",
        "address":"fannyd@adatum.onmicrosoft.com"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
