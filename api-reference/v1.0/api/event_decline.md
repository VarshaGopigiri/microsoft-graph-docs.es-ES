# <a name="event-decline"></a><span data-ttu-id="c1e03-101">event: decline</span><span class="sxs-lookup"><span data-stu-id="c1e03-101">event: decline</span></span>

<span data-ttu-id="c1e03-102">Rechaza la invitación al evento especificado.</span><span class="sxs-lookup"><span data-stu-id="c1e03-102">Decline invitation to the specified event.</span></span>

## <a name="permissions"></a><span data-ttu-id="c1e03-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c1e03-103">Permissions</span></span>

<span data-ttu-id="c1e03-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c1e03-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c1e03-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c1e03-106">Permission type</span></span>      | <span data-ttu-id="c1e03-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c1e03-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c1e03-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c1e03-108">Delegated (work or school account)</span></span> | <span data-ttu-id="c1e03-109">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c1e03-109">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="c1e03-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c1e03-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c1e03-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c1e03-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="c1e03-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c1e03-112">Application</span></span> | <span data-ttu-id="c1e03-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c1e03-113">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="c1e03-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c1e03-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/events/{id}/decline
POST /users/{id | userPrincipalName}/events/{id}/decline
POST /groups/{id}/events/{id}/decline

POST /me/calendar/events/{id}/decline
POST /users/{id | userPrincipalName}/calendar/events/{id}/decline
POST /groups/{id}/calendar/events/{id}/decline

POST /me/calendars/{id}/events/{id}/decline
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/decline

POST /me/calendargroup/calendars/{id}/events/{id}/decline
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/decline

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/decline
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/decline
```

<br/>

## <a name="request-headers"></a><span data-ttu-id="c1e03-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c1e03-115">Request headers</span></span>

| <span data-ttu-id="c1e03-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="c1e03-116">Name</span></span>       | <span data-ttu-id="c1e03-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1e03-117">Type</span></span> | <span data-ttu-id="c1e03-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1e03-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c1e03-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="c1e03-119">Authorization</span></span>  | <span data-ttu-id="c1e03-120">string</span><span class="sxs-lookup"><span data-stu-id="c1e03-120">string</span></span>  | <span data-ttu-id="c1e03-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c1e03-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c1e03-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c1e03-123">Content-Type</span></span> | <span data-ttu-id="c1e03-124">string</span><span class="sxs-lookup"><span data-stu-id="c1e03-124">string</span></span>  | <span data-ttu-id="c1e03-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c1e03-p103">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c1e03-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c1e03-127">Request body</span></span>

<span data-ttu-id="c1e03-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c1e03-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c1e03-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c1e03-129">Parameter</span></span>    | <span data-ttu-id="c1e03-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1e03-130">Type</span></span>   |<span data-ttu-id="c1e03-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1e03-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c1e03-132">comment</span><span class="sxs-lookup"><span data-stu-id="c1e03-132">comment</span></span>|<span data-ttu-id="c1e03-133">String</span><span class="sxs-lookup"><span data-stu-id="c1e03-133">String</span></span>|<span data-ttu-id="c1e03-p104">Texto incluido en la respuesta. Opcional.</span><span class="sxs-lookup"><span data-stu-id="c1e03-p104">Text included in the response. Optional.</span></span>|
|<span data-ttu-id="c1e03-136">sendResponse</span><span class="sxs-lookup"><span data-stu-id="c1e03-136">sendResponse</span></span>|<span data-ttu-id="c1e03-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="c1e03-137">Boolean</span></span>|<span data-ttu-id="c1e03-p105">`true` si se va a enviar una respuesta al organizador; de lo contrario, `false`. Opcional. El valor predeterminado es `true`.</span><span class="sxs-lookup"><span data-stu-id="c1e03-p105">`true` if a response is to be sent to the organizer; otherwise, `false`. Optional. Default is `true`.</span></span>|

## <a name="response"></a><span data-ttu-id="c1e03-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1e03-141">Response</span></span>

<span data-ttu-id="c1e03-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `202, Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c1e03-p106">If successful, this method returns `202, Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c1e03-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c1e03-144">Example</span></span>

<span data-ttu-id="c1e03-145">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c1e03-145">Here is an example of how to call this API.</span></span>

### <a name="request"></a><span data-ttu-id="c1e03-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c1e03-146">Request</span></span>

<span data-ttu-id="c1e03-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c1e03-147">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "event_decline"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/decline
Content-type: application/json
Content-length: 56

{
  "comment": "comment-value",
  "sendResponse": true
}
```

<br/>

### <a name="response"></a><span data-ttu-id="c1e03-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c1e03-148">Response</span></span>

<span data-ttu-id="c1e03-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c1e03-149">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 200 OK
```

<br/>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event: decline",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
