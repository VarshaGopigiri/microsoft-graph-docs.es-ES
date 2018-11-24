# <a name="list-attachments"></a><span data-ttu-id="6f647-101">List attachments</span><span class="sxs-lookup"><span data-stu-id="6f647-101">List attachments</span></span>

<span data-ttu-id="6f647-102">Recupera una lista de objetos [attachment](../resources/attachment.md) asociados a un evento.</span><span class="sxs-lookup"><span data-stu-id="6f647-102">Retrieve a list of [attachment](../resources/attachment.md) objects attached to an event.</span></span>
## <a name="permissions"></a><span data-ttu-id="6f647-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6f647-103">Permissions</span></span>
<span data-ttu-id="6f647-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6f647-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6f647-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6f647-106">Permission type</span></span>      | <span data-ttu-id="6f647-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6f647-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6f647-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6f647-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6f647-109">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="6f647-109">Calendars.Read</span></span>    |
|<span data-ttu-id="6f647-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f647-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6f647-111">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="6f647-111">Calendars.Read</span></span>    |
|<span data-ttu-id="6f647-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6f647-112">Application</span></span> | <span data-ttu-id="6f647-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="6f647-113">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="6f647-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f647-114">HTTP request</span></span>
<span data-ttu-id="6f647-115">Los datos adjuntos para un [evento](../resources/event.md) en el usuario de forma predeterminada [calendario](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="6f647-115">Attachments for an [event](../resources/event.md) in the user's default [calendar](../resources/calendar.md).</span></span>

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

<span data-ttu-id="6f647-116">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="6f647-116">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments

GET /me/calendargroup/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments
```
<span data-ttu-id="6f647-117">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="6f647-117">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>

<!-- { "blockType": "ignored" } -->
```http
GET /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments
GET /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments
```
## <a name="optional-query-parameters"></a><span data-ttu-id="6f647-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6f647-118">Optional query parameters</span></span>
<span data-ttu-id="6f647-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f647-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="6f647-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f647-120">Request headers</span></span>
| <span data-ttu-id="6f647-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="6f647-121">Name</span></span>       | <span data-ttu-id="6f647-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f647-122">Type</span></span> | <span data-ttu-id="6f647-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f647-123">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6f647-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="6f647-124">Authorization</span></span>  | <span data-ttu-id="6f647-125">string</span><span class="sxs-lookup"><span data-stu-id="6f647-125">string</span></span>  | <span data-ttu-id="6f647-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6f647-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6f647-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f647-128">Request body</span></span>
<span data-ttu-id="6f647-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6f647-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6f647-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f647-130">Response</span></span>

<span data-ttu-id="6f647-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f647-131">If successful, this method returns a `200 OK` response code and collection of [Attachment](../resources/attachment.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6f647-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f647-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6f647-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f647-133">Request</span></span>
<span data-ttu-id="6f647-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f647-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_attachments"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/events/{id}/attachments
```
##### <a name="response"></a><span data-ttu-id="6f647-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f647-135">Response</span></span>
<span data-ttu-id="6f647-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f647-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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