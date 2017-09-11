# <a name="get-calendar"></a><span data-ttu-id="c442b-101">Get calendar</span><span class="sxs-lookup"><span data-stu-id="c442b-101">Get calendar</span></span>

<span data-ttu-id="c442b-102">Recupera las propiedades y relaciones del objeto calendar.</span><span class="sxs-lookup"><span data-stu-id="c442b-102">Retrieve the properties and relationships of calendar object.</span></span>
## <a name="permissions"></a><span data-ttu-id="c442b-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c442b-103">Permissions</span></span>
<span data-ttu-id="c442b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c442b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c442b-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c442b-106">Permission type</span></span>      | <span data-ttu-id="c442b-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c442b-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c442b-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c442b-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c442b-109">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="c442b-109">Calendars.Read</span></span>    |
|<span data-ttu-id="c442b-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c442b-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c442b-111">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="c442b-111">Calendars.Read</span></span>    |
|<span data-ttu-id="c442b-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c442b-112">Application</span></span> | <span data-ttu-id="c442b-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="c442b-113">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="c442b-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c442b-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="c442b-115">[calendar](../resources/calendar.md) predeterminado de un usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="c442b-115">A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
GET /me/calendar
GET /users/{id | userPrincipalName}/calendar
GET /groups/{id}/calendar
```
<span data-ttu-id="c442b-116">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="c442b-116">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendars/{id}
GET /users/{id | userPrincipalName}/calendars/{id}

GET /me/calendarGroup/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="c442b-117">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="c442b-117">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendarGroups/{id}/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="c442b-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c442b-118">Optional query parameters</span></span>
<span data-ttu-id="c442b-119">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c442b-119">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="c442b-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c442b-120">Request headers</span></span>
| <span data-ttu-id="c442b-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="c442b-121">Name</span></span>       | <span data-ttu-id="c442b-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="c442b-122">Type</span></span> | <span data-ttu-id="c442b-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="c442b-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c442b-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="c442b-124">Authorization</span></span>  | <span data-ttu-id="c442b-125">string</span><span class="sxs-lookup"><span data-stu-id="c442b-125">string</span></span>  | <span data-ttu-id="c442b-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c442b-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c442b-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c442b-128">Request body</span></span>
<span data-ttu-id="c442b-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c442b-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c442b-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c442b-130">Response</span></span>

<span data-ttu-id="c442b-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c442b-131">If successful, this method returns a `200 OK` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c442b-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c442b-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c442b-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c442b-133">Request</span></span>
<span data-ttu-id="c442b-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c442b-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendar"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendar
```
##### <a name="response"></a><span data-ttu-id="c442b-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c442b-135">Response</span></span>
<span data-ttu-id="c442b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c442b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
        "name":"Samantha Booth",
        "address":"samanthab@adatum.onmicrosoft.com"
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
