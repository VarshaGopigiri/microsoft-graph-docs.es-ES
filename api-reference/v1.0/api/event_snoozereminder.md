# <a name="event-snoozereminder"></a><span data-ttu-id="30e76-101">event: snoozeReminder</span><span class="sxs-lookup"><span data-stu-id="30e76-101">event: snoozeReminder</span></span>

<span data-ttu-id="30e76-102">Posponga un aviso para un [evento](../resources/event.md) en un [calendario](../resources/calendar.md) de usuario hasta una nueva hora.</span><span class="sxs-lookup"><span data-stu-id="30e76-102">Postpone a reminder for an [event](../resources/event.md) in a user [calendar](../resources/calendar.md) until a new time.</span></span>

## <a name="permissions"></a><span data-ttu-id="30e76-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="30e76-103">Permissions</span></span>
<span data-ttu-id="30e76-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="30e76-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="30e76-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="30e76-106">Permission type</span></span>      | <span data-ttu-id="30e76-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="30e76-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="30e76-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="30e76-108">Delegated (work or school account)</span></span> | <span data-ttu-id="30e76-109">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="30e76-109">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="30e76-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="30e76-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="30e76-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="30e76-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="30e76-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="30e76-112">Application</span></span> | <span data-ttu-id="30e76-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="30e76-113">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="30e76-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="30e76-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/events/{id}/snoozeReminder

POST /me/calendar/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendar/events/{id}/snoozeReminder

POST /me/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/snoozeReminder

POST /me/calendargroup/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/snoozeReminder

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/snoozeReminder
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/snoozeReminder
```
## <a name="request-headers"></a><span data-ttu-id="30e76-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="30e76-115">Request headers</span></span>
| <span data-ttu-id="30e76-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="30e76-116">Name</span></span>       | <span data-ttu-id="30e76-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="30e76-117">Type</span></span> | <span data-ttu-id="30e76-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="30e76-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="30e76-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="30e76-119">Authorization</span></span>  | <span data-ttu-id="30e76-120">cadena</span><span class="sxs-lookup"><span data-stu-id="30e76-120">string</span></span>  | <span data-ttu-id="30e76-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="30e76-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="30e76-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="30e76-123">Content-Type</span></span> | <span data-ttu-id="30e76-124">cadena</span><span class="sxs-lookup"><span data-stu-id="30e76-124">string</span></span>  | <span data-ttu-id="30e76-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="30e76-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="30e76-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="30e76-127">Request body</span></span>
<span data-ttu-id="30e76-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="30e76-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="30e76-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="30e76-129">Parameter</span></span>    | <span data-ttu-id="30e76-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="30e76-130">Type</span></span>   |<span data-ttu-id="30e76-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="30e76-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="30e76-132">newReminderTime</span><span class="sxs-lookup"><span data-stu-id="30e76-132">newReminderTime</span></span>|<span data-ttu-id="30e76-133">DateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="30e76-133">DateTimeTimeZone</span></span>|<span data-ttu-id="30e76-134">Nueva fecha y hora para desencadenar el aviso.</span><span class="sxs-lookup"><span data-stu-id="30e76-134">The new date and time to trigger the reminder.</span></span>|

## <a name="response"></a><span data-ttu-id="30e76-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30e76-135">Response</span></span>

<span data-ttu-id="30e76-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30e76-p104">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="30e76-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="30e76-138">Example</span></span>
<span data-ttu-id="30e76-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="30e76-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="30e76-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="30e76-140">Request</span></span>
<span data-ttu-id="30e76-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="30e76-141">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="30e76-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="30e76-142">Response</span></span>
<span data-ttu-id="30e76-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="30e76-143">Here is an example of the response.</span></span>
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
