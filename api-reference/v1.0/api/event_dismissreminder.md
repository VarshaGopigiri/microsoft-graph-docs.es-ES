# <a name="event-dismissreminder"></a><span data-ttu-id="b969d-101">event: dismissReminder</span><span class="sxs-lookup"><span data-stu-id="b969d-101">event: dismissReminder</span></span>

<span data-ttu-id="b969d-102">Descarta un recordatorio que se ha desencadenado.</span><span class="sxs-lookup"><span data-stu-id="b969d-102">Dissmiss a reminder that has been triggered.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b969d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b969d-103">Prerequisites</span></span>
<span data-ttu-id="b969d-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="b969d-104">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="b969d-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b969d-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/events/{id}/dismissReminder
POST /groups/{id}/events/{id}/dismissReminder

POST /me/calendar/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendar/events/{id}/dismissReminder
POST /groups/{id}/calendar/events/{id}/dismissReminder

POST /me/calendars/{id}/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/dismissReminder

POST /me/calendargroup/calendars/{id}/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/dismissReminder

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/dismissReminder
```
## <a name="request-headers"></a><span data-ttu-id="b969d-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b969d-106">Request headers</span></span>
| <span data-ttu-id="b969d-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="b969d-107">Name</span></span>       | <span data-ttu-id="b969d-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b969d-108">Type</span></span> | <span data-ttu-id="b969d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b969d-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b969d-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="b969d-110">Authorization</span></span>  | <span data-ttu-id="b969d-111">string</span><span class="sxs-lookup"><span data-stu-id="b969d-111">string</span></span>  | <span data-ttu-id="b969d-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b969d-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b969d-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b969d-114">Request body</span></span>

## <a name="response"></a><span data-ttu-id="b969d-115">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b969d-115">Response</span></span>

<span data-ttu-id="b969d-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b969d-p102">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b969d-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b969d-118">Example</span></span>
<span data-ttu-id="b969d-119">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b969d-119">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b969d-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b969d-120">Request</span></span>
<span data-ttu-id="b969d-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b969d-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_dismissreminder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/dismissReminder
```

##### <a name="response"></a><span data-ttu-id="b969d-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b969d-122">Response</span></span>
##### <a name="response"></a><span data-ttu-id="b969d-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b969d-123">Response</span></span>
<span data-ttu-id="b969d-124">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b969d-124">Here is an example of the response.</span></span>
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
  "description": "event: dismissReminder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
