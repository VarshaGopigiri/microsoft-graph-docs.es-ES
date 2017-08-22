# <a name="delete-event"></a><span data-ttu-id="86ef0-101">Delete event</span><span class="sxs-lookup"><span data-stu-id="86ef0-101">Delete event</span></span>

<span data-ttu-id="86ef0-102">Elimina el evento.</span><span class="sxs-lookup"><span data-stu-id="86ef0-102">Delete event.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="86ef0-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="86ef0-103">Prerequisites</span></span>
<span data-ttu-id="86ef0-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="86ef0-104">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span> 
## <a name="http-request"></a><span data-ttu-id="86ef0-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="86ef0-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/events/{id}
DELETE /users/{id | userPrincipalName}/events/{id}
DELETE /groups/{id}/events/{id}

DELETE /me/calendar/events/{id}
DELETE /users/{id | userPrincipalName}/calendar/events/{id}
DELETE /groups/{id}/calendar/events/{id}/

DELETE /me/calendars/{id}/events/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}/events/{id}

DELETE /me/calendargroup/calendars/{id}/events/{id}
DELETE /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}

DELETE /me/calendargroups/{id}/calendars/{id}/events/{id}
DELETE /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}
```
## <a name="request-headers"></a><span data-ttu-id="86ef0-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="86ef0-106">Request headers</span></span>
| <span data-ttu-id="86ef0-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="86ef0-107">Name</span></span>       | <span data-ttu-id="86ef0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="86ef0-108">Type</span></span> | <span data-ttu-id="86ef0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="86ef0-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="86ef0-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="86ef0-110">Authorization</span></span>  | <span data-ttu-id="86ef0-111">string</span><span class="sxs-lookup"><span data-stu-id="86ef0-111">string</span></span>  | <span data-ttu-id="86ef0-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="86ef0-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="86ef0-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="86ef0-114">Request body</span></span>
<span data-ttu-id="86ef0-115">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="86ef0-115">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="86ef0-116">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86ef0-116">Response</span></span>

<span data-ttu-id="86ef0-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86ef0-p102">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="86ef0-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86ef0-119">Example</span></span>
##### <a name="request"></a><span data-ttu-id="86ef0-120">Solicitud</span><span class="sxs-lookup"><span data-stu-id="86ef0-120">Request</span></span>
<span data-ttu-id="86ef0-121">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="86ef0-121">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_event"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/events/{id}
```
##### <a name="response"></a><span data-ttu-id="86ef0-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86ef0-122">Response</span></span>
<span data-ttu-id="86ef0-123">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86ef0-123">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete event",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
