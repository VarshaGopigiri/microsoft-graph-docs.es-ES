# <a name="event-tentativelyaccept"></a><span data-ttu-id="c0b49-101">event: tentativelyAccept</span><span class="sxs-lookup"><span data-stu-id="c0b49-101">event: tentativelyAccept</span></span>

<span data-ttu-id="c0b49-102">Acepta provisionalmente el evento especificado.</span><span class="sxs-lookup"><span data-stu-id="c0b49-102">Tentatively accept the specified event.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c0b49-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c0b49-103">Prerequisites</span></span>
<span data-ttu-id="c0b49-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="c0b49-104">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="c0b49-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c0b49-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/tentativelyAccept
POST /users/{id | userPrincipalName}/events/{id}/tentativelyAccept
POST /groups/{id}/events/{id}/tentativelyAccept

POST /me/calendar/events/{id}/tentativelyAccept
POST /users/{id | userPrincipalName}/calendar/events/{id}/tentativelyAccept
POST /groups/{id}/calendar/events/{id}/tentativelyAccept

POST /me/calendars/{id}/events/{id}/tentativelyAccept
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/tentativelyAccept

POST /me/calendargroup/calendars/{id}/events/{id}/tentativelyAccept
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/tentativelyAccept

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/tentativelyAccept
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/tentativelyAccept
```
## <a name="request-headers"></a><span data-ttu-id="c0b49-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c0b49-106">Request headers</span></span>
| <span data-ttu-id="c0b49-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="c0b49-107">Name</span></span>       | <span data-ttu-id="c0b49-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0b49-108">Type</span></span> | <span data-ttu-id="c0b49-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0b49-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c0b49-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="c0b49-110">Authorization</span></span>  | <span data-ttu-id="c0b49-111">string</span><span class="sxs-lookup"><span data-stu-id="c0b49-111">string</span></span>  | <span data-ttu-id="c0b49-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0b49-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c0b49-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c0b49-114">Content-Type</span></span> | <span data-ttu-id="c0b49-115">string</span><span class="sxs-lookup"><span data-stu-id="c0b49-115">string</span></span>  | <span data-ttu-id="c0b49-p102">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c0b49-p102">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c0b49-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c0b49-118">Request body</span></span>
<span data-ttu-id="c0b49-119">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c0b49-119">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c0b49-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c0b49-120">Parameter</span></span>    | <span data-ttu-id="c0b49-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0b49-121">Type</span></span>   |<span data-ttu-id="c0b49-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0b49-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c0b49-123">comment</span><span class="sxs-lookup"><span data-stu-id="c0b49-123">comment</span></span>|<span data-ttu-id="c0b49-124">String</span><span class="sxs-lookup"><span data-stu-id="c0b49-124">String</span></span>|<span data-ttu-id="c0b49-p103">Texto incluido en la respuesta. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c0b49-p103">Text included in the response. Optional.</span></span>|
|<span data-ttu-id="c0b49-127">sendResponse</span><span class="sxs-lookup"><span data-stu-id="c0b49-127">sendResponse</span></span>|<span data-ttu-id="c0b49-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="c0b49-128">Boolean</span></span>|<span data-ttu-id="c0b49-p104">`true` si se va a enviar una respuesta al organizador; de lo contrario, `false`. Opcional. El valor predeterminado es `true`.</span><span class="sxs-lookup"><span data-stu-id="c0b49-p104">`true` if a response is to be sent to the organizer; otherwise, `false`. Optional. Default is `true`.</span></span>|

## <a name="response"></a><span data-ttu-id="c0b49-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0b49-132">Response</span></span>

<span data-ttu-id="c0b49-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0b49-p105">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c0b49-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c0b49-135">Example</span></span>
<span data-ttu-id="c0b49-136">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c0b49-136">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c0b49-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c0b49-137">Request</span></span>
<span data-ttu-id="c0b49-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c0b49-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_tentativelyaccept"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/tentativelyAccept
Content-type: application/json
Content-length: 56

{
  "comment": "comment-value",
  "sendResponse": true
}
```

##### <a name="response"></a><span data-ttu-id="c0b49-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0b49-139">Response</span></span>
##### <a name="response"></a><span data-ttu-id="c0b49-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c0b49-140">Response</span></span>
<span data-ttu-id="c0b49-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c0b49-141">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event: tentativelyAccept",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
