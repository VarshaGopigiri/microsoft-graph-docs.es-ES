# <a name="list-attachments"></a><span data-ttu-id="8ebde-101">Listar attachments</span><span class="sxs-lookup"><span data-stu-id="8ebde-101">List attachments</span></span>

<span data-ttu-id="8ebde-102">Recupera una lista de objetos [attachment](../resources/attachment.md) asociados a un evento.</span><span class="sxs-lookup"><span data-stu-id="8ebde-102">Retrieve a list of [attachment](../resources/attachment.md) objects attached to an event.</span></span>
## <a name="permissions"></a><span data-ttu-id="8ebde-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="8ebde-103">Permissions</span></span>
<span data-ttu-id="8ebde-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8ebde-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8ebde-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8ebde-106">Permission type</span></span>      | <span data-ttu-id="8ebde-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8ebde-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8ebde-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8ebde-108">Delegated (work or school account)</span></span> | <span data-ttu-id="8ebde-109">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="8ebde-109">Calendars.Read</span></span>    |
|<span data-ttu-id="8ebde-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8ebde-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8ebde-111">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="8ebde-111">Calendars.Read</span></span>    |
|<span data-ttu-id="8ebde-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8ebde-112">Application</span></span> | <span data-ttu-id="8ebde-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="8ebde-113">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="8ebde-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8ebde-114">HTTP request</span></span>
<span data-ttu-id="8ebde-115">Datos adjuntos de un [event](../resources/event.md) en el [calendar](../resources/calendar.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="8ebde-115">Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).</span></span>

<!--
Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).
-->

<!-- { "blockType": "ignored" } -->
```http
GET /me/events/{id}/attachments
GET /users/{id | userPrincipalName}/events/{id}/attachments

GET /me/calendar/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendar/events/{id}/attachments
```

<!--
GET /groups/{id}/events/{id}/attachments
GET /groups/{id}/calendar/events/{id}/attachments
-->

<span data-ttu-id="8ebde-116">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="8ebde-116">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments

GET /me/calendargroup/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments
```
<span data-ttu-id="8ebde-117">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="8ebde-117">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="8ebde-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="8ebde-118">Optional query parameters</span></span>
<span data-ttu-id="8ebde-119">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ebde-119">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="8ebde-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8ebde-120">Request headers</span></span>
| <span data-ttu-id="8ebde-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="8ebde-121">Name</span></span>       | <span data-ttu-id="8ebde-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ebde-122">Type</span></span> | <span data-ttu-id="8ebde-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ebde-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="8ebde-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="8ebde-124">Authorization</span></span>  | <span data-ttu-id="8ebde-125">cadena</span><span class="sxs-lookup"><span data-stu-id="8ebde-125">string</span></span>  | <span data-ttu-id="8ebde-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8ebde-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="8ebde-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8ebde-128">Request body</span></span>
<span data-ttu-id="8ebde-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="8ebde-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="8ebde-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ebde-130">Response</span></span>

<span data-ttu-id="8ebde-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ebde-131">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8ebde-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ebde-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8ebde-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ebde-133">Request</span></span>
<span data-ttu-id="8ebde-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8ebde-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="8ebde-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ebde-135">Response</span></span>
<span data-ttu-id="8ebde-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8ebde-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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