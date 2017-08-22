# <a name="list-attachments"></a><span data-ttu-id="66d31-101">List attachments</span><span class="sxs-lookup"><span data-stu-id="66d31-101">List attachments</span></span>

<span data-ttu-id="66d31-102">Recupera una lista de objetos [attachment](../resources/attachment.md) asociados a un evento.</span><span class="sxs-lookup"><span data-stu-id="66d31-102">Retrieve a list of [attachment](../resources/attachment.md) objects attached to an event.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="66d31-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="66d31-103">Prerequisites</span></span>
<span data-ttu-id="66d31-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.Read*</span><span class="sxs-lookup"><span data-stu-id="66d31-104">One of the following **scopes** is required to execute this API: *Calendars.Read*</span></span> 
## <a name="http-request"></a><span data-ttu-id="66d31-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="66d31-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="66d31-106">Datos adjuntos de un [event](../resources/event.md) en el [calendar](../resources/calendar.md) predeterminado del usuario o del grupo.</span><span class="sxs-lookup"><span data-stu-id="66d31-106">Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
GET /me/events/{id}/attachments
GET /users/{id | userPrincipalName}/events/{id}/attachments
GET /groups/{id}/events/{id}/attachments

GET /me/calendar/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendar/events/{id}/attachments
GET /groups/{id}/calendar/events/{id}/attachments
```
<span data-ttu-id="66d31-107">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="66d31-107">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments

GET /me/calendargroup/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments
```
<span data-ttu-id="66d31-108">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="66d31-108">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
```http
GET /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="66d31-109">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="66d31-109">Optional query parameters</span></span>
<span data-ttu-id="66d31-110">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66d31-110">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="66d31-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="66d31-111">Request headers</span></span>
| <span data-ttu-id="66d31-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="66d31-112">Name</span></span>       | <span data-ttu-id="66d31-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="66d31-113">Type</span></span> | <span data-ttu-id="66d31-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="66d31-114">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="66d31-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="66d31-115">Authorization</span></span>  | <span data-ttu-id="66d31-116">string</span><span class="sxs-lookup"><span data-stu-id="66d31-116">string</span></span>  | <span data-ttu-id="66d31-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="66d31-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="66d31-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="66d31-119">Request body</span></span>
<span data-ttu-id="66d31-120">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="66d31-120">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="66d31-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66d31-121">Response</span></span>

<span data-ttu-id="66d31-122">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="66d31-122">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="66d31-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="66d31-123">Example</span></span>
##### <a name="request"></a><span data-ttu-id="66d31-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="66d31-124">Request</span></span>
<span data-ttu-id="66d31-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="66d31-125">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="66d31-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="66d31-126">Response</span></span>
<span data-ttu-id="66d31-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="66d31-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 215

{
  "value": [
    {
      "@odata.type": "#Microsoft.OutlookServices.FileAttachment",
      "contentType": "contentType-value",
      "contentLocation": "contentLocation-value",
      "contentBytes": "contentBytes-value",
      "contentId": "null",
      "lastModifiedDateTime": "datetime-value",
      "id": "id-value",
      "isInline": false,
      "isContactPhoto": false,
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