# <a name="event-accept"></a><span data-ttu-id="bc099-101">event: accept</span><span class="sxs-lookup"><span data-stu-id="bc099-101">event: accept</span></span>

<span data-ttu-id="bc099-102">Acepta el evento especificado.</span><span class="sxs-lookup"><span data-stu-id="bc099-102">Accept the specified event.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bc099-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bc099-103">Prerequisites</span></span>
<span data-ttu-id="bc099-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="bc099-104">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="bc099-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bc099-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/accept
POST /users/{id | userPrincipalName}/events/{id}/accept
POST /groups/{id}/events/{id}/accept

POST /me/calendar/events/{id}/accept
POST /users/{id | userPrincipalName}/calendar/events/{id}/accept
POST /groups/{id}/calendar/events/{id}/accept

POST /me/calendars/{id}/events/{id}/accept
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/accept

POST /me/calendargroup/calendars/{id}/events/{id}/accept
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/accept

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/accept
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/accept
```
## <a name="request-headers"></a><span data-ttu-id="bc099-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bc099-106">Request headers</span></span>
| <span data-ttu-id="bc099-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="bc099-107">Name</span></span>       | <span data-ttu-id="bc099-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc099-108">Type</span></span> | <span data-ttu-id="bc099-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc099-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="bc099-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="bc099-110">Authorization</span></span>  | <span data-ttu-id="bc099-111">string</span><span class="sxs-lookup"><span data-stu-id="bc099-111">string</span></span>  | <span data-ttu-id="bc099-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc099-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bc099-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="bc099-114">Content-Type</span></span> | <span data-ttu-id="bc099-115">string</span><span class="sxs-lookup"><span data-stu-id="bc099-115">string</span></span>  | <span data-ttu-id="bc099-p102">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bc099-p102">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="bc099-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bc099-118">Request body</span></span>
<span data-ttu-id="bc099-119">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="bc099-119">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="bc099-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bc099-120">Parameter</span></span>    | <span data-ttu-id="bc099-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="bc099-121">Type</span></span>   |<span data-ttu-id="bc099-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="bc099-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bc099-123">comment</span><span class="sxs-lookup"><span data-stu-id="bc099-123">comment</span></span>|<span data-ttu-id="bc099-124">String</span><span class="sxs-lookup"><span data-stu-id="bc099-124">String</span></span>|<span data-ttu-id="bc099-p103">Texto incluido en la respuesta. Opcional.</span><span class="sxs-lookup"><span data-stu-id="bc099-p103">Text included in the response. Optional.</span></span>|
|<span data-ttu-id="bc099-127">sendResponse</span><span class="sxs-lookup"><span data-stu-id="bc099-127">sendResponse</span></span>|<span data-ttu-id="bc099-128">Boolean</span><span class="sxs-lookup"><span data-stu-id="bc099-128">Boolean</span></span>|<span data-ttu-id="bc099-p104">`true` si se va a enviar una respuesta al organizador; de lo contrario, `false`. Opcional. El valor predeterminado es `true`.</span><span class="sxs-lookup"><span data-stu-id="bc099-p104">`true` if a response is to be sent to the organizer; otherwise, `false`. Optional. Default is `true`.</span></span>|

## <a name="response"></a><span data-ttu-id="bc099-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc099-132">Response</span></span>

<span data-ttu-id="bc099-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc099-p105">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bc099-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bc099-135">Example</span></span>
<span data-ttu-id="bc099-136">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bc099-136">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="bc099-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bc099-137">Request</span></span>
<span data-ttu-id="bc099-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bc099-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_accept"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/accept
Content-type: application/json
Content-length: 56

{
  "comment": "comment-value",
  "sendResponse": true
}
```

##### <a name="response"></a><span data-ttu-id="bc099-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bc099-139">Response</span></span>
<span data-ttu-id="bc099-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bc099-140">Here is an example of the response.</span></span>
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
  "description": "event: accept",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
