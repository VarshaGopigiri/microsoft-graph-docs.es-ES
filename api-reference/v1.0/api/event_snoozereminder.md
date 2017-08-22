# <a name="event-snoozereminder"></a><span data-ttu-id="eefad-101">event: snoozeReminder</span><span class="sxs-lookup"><span data-stu-id="eefad-101">event: snoozeReminder</span></span>

<span data-ttu-id="eefad-102">Pospone un aviso hasta una nueva hora.</span><span class="sxs-lookup"><span data-stu-id="eefad-102">Postpone a reminder until a new time.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="eefad-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eefad-103">Prerequisites</span></span>
<span data-ttu-id="eefad-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="eefad-104">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="eefad-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eefad-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/events/{id}/snoozeReminder
POST /groups/{id}/events/{id}/snoozeReminder

POST /me/calendar/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendar/events/{id}/snoozeReminder
POST /groups/{id}/calendar/events/{id}/snoozeReminder

POST /me/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/snoozeReminder

POST /me/calendargroup/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/snoozeReminder

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/snoozeReminder
```
## <a name="request-headers"></a><span data-ttu-id="eefad-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="eefad-106">Request headers</span></span>
| <span data-ttu-id="eefad-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="eefad-107">Name</span></span>       | <span data-ttu-id="eefad-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="eefad-108">Type</span></span> | <span data-ttu-id="eefad-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="eefad-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="eefad-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="eefad-110">Authorization</span></span>  | <span data-ttu-id="eefad-111">string</span><span class="sxs-lookup"><span data-stu-id="eefad-111">string</span></span>  | <span data-ttu-id="eefad-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eefad-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="eefad-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="eefad-114">Content-Type</span></span> | <span data-ttu-id="eefad-115">string</span><span class="sxs-lookup"><span data-stu-id="eefad-115">string</span></span>  | <span data-ttu-id="eefad-p102">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eefad-p102">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="eefad-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eefad-118">Request body</span></span>
<span data-ttu-id="eefad-119">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="eefad-119">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="eefad-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="eefad-120">Parameter</span></span>    | <span data-ttu-id="eefad-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="eefad-121">Type</span></span>   |<span data-ttu-id="eefad-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="eefad-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="eefad-123">newReminderTime</span><span class="sxs-lookup"><span data-stu-id="eefad-123">newReminderTime</span></span>|<span data-ttu-id="eefad-124">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="eefad-124">DateTimeTimeZone</span></span>|<span data-ttu-id="eefad-125">Nueva fecha y hora para desencadenar el aviso.</span><span class="sxs-lookup"><span data-stu-id="eefad-125">The new date and time to trigger the reminder.</span></span>|

## <a name="response"></a><span data-ttu-id="eefad-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eefad-126">Response</span></span>

<span data-ttu-id="eefad-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eefad-p103">If successful, this method returns `200, OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="eefad-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eefad-129">Example</span></span>
<span data-ttu-id="eefad-130">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="eefad-130">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="eefad-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eefad-131">Request</span></span>
<span data-ttu-id="eefad-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eefad-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "event_snoozereminder"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/snoozeReminder
Content-type: application/json
Content-length: 97

{
  "newReminderTime": {
    "dateTime": "dateTime-value",
    "timeZone": "timeZone-value"
  }
}
```

##### <a name="response"></a><span data-ttu-id="eefad-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eefad-133">Response</span></span>
<span data-ttu-id="eefad-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eefad-134">Here is an example of the response.</span></span>
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
  "description": "event: snoozeReminder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
