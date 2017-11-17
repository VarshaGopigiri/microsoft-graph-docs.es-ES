# <a name="event-dismissreminder"></a><span data-ttu-id="d31a4-101">event: dismissReminder</span><span class="sxs-lookup"><span data-stu-id="d31a4-101">event: dismissReminder</span></span>

<span data-ttu-id="d31a4-102">Descarta un recordatorio que se ha desencadenado.</span><span class="sxs-lookup"><span data-stu-id="d31a4-102">Dismiss a reminder that has been triggered.</span></span>

## <a name="permissions"></a><span data-ttu-id="d31a4-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d31a4-103">Permissions</span></span>
<span data-ttu-id="d31a4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d31a4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d31a4-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d31a4-106">Permission type</span></span>      | <span data-ttu-id="d31a4-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d31a4-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d31a4-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d31a4-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d31a4-109">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d31a4-109">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d31a4-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d31a4-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d31a4-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d31a4-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d31a4-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d31a4-112">Application</span></span> | <span data-ttu-id="d31a4-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d31a4-113">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d31a4-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d31a4-114">HTTP request</span></span>

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

<br/>

## <a name="request-headers"></a><span data-ttu-id="d31a4-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d31a4-115">Request headers</span></span>
| <span data-ttu-id="d31a4-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="d31a4-116">Name</span></span>       | <span data-ttu-id="d31a4-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="d31a4-117">Type</span></span> | <span data-ttu-id="d31a4-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d31a4-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="d31a4-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d31a4-119">Authorization</span></span>  | <span data-ttu-id="d31a4-120">string</span><span class="sxs-lookup"><span data-stu-id="d31a4-120">string</span></span>  | <span data-ttu-id="d31a4-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d31a4-p102">Bearer {token}. Required.</span></span> |

<br/>

## <a name="response"></a><span data-ttu-id="d31a4-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d31a4-123">Response</span></span>

<span data-ttu-id="d31a4-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d31a4-p103">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d31a4-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d31a4-126">Example</span></span>

<span data-ttu-id="d31a4-127">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d31a4-127">Here is an example of how to call this API.</span></span>

### <a name="request"></a><span data-ttu-id="d31a4-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d31a4-128">Request</span></span>
<span data-ttu-id="d31a4-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d31a4-129">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "event_dismissreminder"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/dismissReminder
```

<br/>

### <a name="response"></a><span data-ttu-id="d31a4-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d31a4-130">Response</span></span>
<span data-ttu-id="d31a4-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d31a4-131">Here is an example of the response.</span></span>

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
