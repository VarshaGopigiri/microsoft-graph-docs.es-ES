# <a name="get-calendar"></a><span data-ttu-id="298d5-101">Obtener calendario</span><span class="sxs-lookup"><span data-stu-id="298d5-101">Get calendar</span></span>

<span data-ttu-id="298d5-102">Obtiene las propiedades y relaciones de un objeto de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="298d5-102">Get the properties and relationships of a [calendar](../resources/calendar.md) object.</span></span> <span data-ttu-id="298d5-103">El calendario puede ser de un [usuario](../resources/user.md) o el calendario predeterminado de un [grupo](../resources/group.md) de Office 365.</span><span class="sxs-lookup"><span data-stu-id="298d5-103">The calendar can be one for a [user](../resources/user.md), or the default calendar of an Office 365 [group](../resources/group.md).</span></span>

<span data-ttu-id="298d5-104">Hay dos escenarios donde una aplicación puede obtener el calendario de otro usuario:</span><span class="sxs-lookup"><span data-stu-id="298d5-104">There are two scenarios where an app can get another user's calendar:</span></span>

* <span data-ttu-id="298d5-105">Si la aplicación tiene permisos de aplicación, o bien,</span><span class="sxs-lookup"><span data-stu-id="298d5-105">If the app has application permissions, or,</span></span>
* <span data-ttu-id="298d5-106">Si la aplicación tiene la adecuada delega [los permisos](#permissions) de un usuario y otro usuario ha compartido un calendario con ese usuario o, se le concede acceso delegado a ese usuario.</span><span class="sxs-lookup"><span data-stu-id="298d5-106">If the app has the appropriate delegated [permissions](#permissions) from one user, and another user has shared a calendar with that user, or, has given delegated access to that user.</span></span> <span data-ttu-id="298d5-107">Consulte los [Detalles y un ejemplo](../../../concepts/outlook-get-shared-events-calendars.md).</span><span class="sxs-lookup"><span data-stu-id="298d5-107">See [details and an example](../../../concepts/outlook-get-shared-events-calendars.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="298d5-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="298d5-108">Permissions</span></span>
<span data-ttu-id="298d5-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="298d5-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="298d5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="298d5-111">Permission type</span></span>      | <span data-ttu-id="298d5-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="298d5-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="298d5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="298d5-113">Delegated (work or school account)</span></span> | <span data-ttu-id="298d5-114">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="298d5-114">Calendars.Read</span></span>    |
|<span data-ttu-id="298d5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="298d5-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="298d5-116">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="298d5-116">Calendars.Read</span></span>    |
|<span data-ttu-id="298d5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="298d5-117">Application</span></span> | <span data-ttu-id="298d5-118">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="298d5-118">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="298d5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="298d5-119">HTTP request</span></span>
<span data-ttu-id="298d5-120"><!-- { "blockType": "ignored" } -->Un usuario o del grupo predeterminado de [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="298d5-120"><!-- { "blockType": "ignored" } --> A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
GET /me/calendar
GET /users/{id | userPrincipalName}/calendar
GET /groups/{id}/calendar
```
<span data-ttu-id="298d5-121">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="298d5-121">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendars/{id}
GET /users/{id | userPrincipalName}/calendars/{id}

GET /me/calendarGroup/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="298d5-122">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="298d5-122">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendarGroups/{id}/calendars/{id}
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="298d5-123">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="298d5-123">Optional query parameters</span></span>
<span data-ttu-id="298d5-124">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="298d5-124">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="298d5-125">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="298d5-125">Request headers</span></span>
| <span data-ttu-id="298d5-126">Nombre</span><span class="sxs-lookup"><span data-stu-id="298d5-126">Name</span></span>       | <span data-ttu-id="298d5-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="298d5-127">Type</span></span> | <span data-ttu-id="298d5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="298d5-128">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="298d5-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="298d5-129">Authorization</span></span>  | <span data-ttu-id="298d5-130">string</span><span class="sxs-lookup"><span data-stu-id="298d5-130">string</span></span>  | <span data-ttu-id="298d5-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="298d5-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="298d5-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="298d5-133">Request body</span></span>
<span data-ttu-id="298d5-134">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="298d5-134">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="298d5-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="298d5-135">Response</span></span>

<span data-ttu-id="298d5-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="298d5-136">If successful, this method returns a `200 OK` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="298d5-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="298d5-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="298d5-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="298d5-138">Request</span></span>
<span data-ttu-id="298d5-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="298d5-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendar"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendar
```
##### <a name="response"></a><span data-ttu-id="298d5-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="298d5-140">Response</span></span>
<span data-ttu-id="298d5-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="298d5-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
