# <a name="event-dismissreminder"></a><span data-ttu-id="d2049-101">event: dismissReminder</span><span class="sxs-lookup"><span data-stu-id="d2049-101">event: dismissReminder</span></span>

<span data-ttu-id="d2049-102">Descarta un aviso que desencadena un [evento](../resources/event.md) en un [calendario](../resources/calendar.md)de usuario.</span><span class="sxs-lookup"><span data-stu-id="d2049-102">Dismiss a reminder that has been triggered for an [event](../resources/event.md) in a user [calendar](../resources/calendar.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="d2049-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d2049-103">Permissions</span></span>
<span data-ttu-id="d2049-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d2049-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d2049-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d2049-106">Permission type</span></span>      | <span data-ttu-id="d2049-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d2049-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d2049-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d2049-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d2049-109">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2049-109">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d2049-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d2049-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d2049-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2049-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="d2049-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d2049-112">Application</span></span> | <span data-ttu-id="d2049-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d2049-113">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="d2049-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d2049-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/events/{id}/dismissReminder

POST /me/calendar/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendar/events/{id}/dismissReminder

POST /me/calendars/{id}/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/dismissReminder

POST /me/calendargroup/calendars/{id}/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/dismissReminder

POST /me/calendargroups/{id}/calendars/{id}/events/{id}/dismissReminder
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/dismissReminder
```

<br/>

## <a name="request-headers"></a><span data-ttu-id="d2049-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d2049-115">Request headers</span></span>
| <span data-ttu-id="d2049-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="d2049-116">Name</span></span>       | <span data-ttu-id="d2049-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2049-117">Type</span></span> | <span data-ttu-id="d2049-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2049-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="d2049-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d2049-119">Authorization</span></span>  | <span data-ttu-id="d2049-120">cadena</span><span class="sxs-lookup"><span data-stu-id="d2049-120">string</span></span>  | <span data-ttu-id="d2049-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d2049-p102">Bearer {token}. Required.</span></span> |

<br/>

## <a name="response"></a><span data-ttu-id="d2049-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2049-123">Response</span></span>

<span data-ttu-id="d2049-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2049-p103">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d2049-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d2049-126">Example</span></span>

<span data-ttu-id="d2049-127">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d2049-127">Here is an example of how to call this API.</span></span>

### <a name="request"></a><span data-ttu-id="d2049-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d2049-128">Request</span></span>
<span data-ttu-id="d2049-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d2049-129">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "event_dismissreminder"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/events/{id}/dismissReminder
```

<br/>

### <a name="response"></a><span data-ttu-id="d2049-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d2049-130">Response</span></span>
<span data-ttu-id="d2049-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d2049-131">Here is an example of the response.</span></span>

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
