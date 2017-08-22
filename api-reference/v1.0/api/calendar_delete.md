# <a name="delete-calendar"></a><span data-ttu-id="716c6-101">Eliminar calendario</span><span class="sxs-lookup"><span data-stu-id="716c6-101">Delete calendar</span></span>

<span data-ttu-id="716c6-102">Elimine un calendario que no sea el predeterminado.</span><span class="sxs-lookup"><span data-stu-id="716c6-102">Delete a calendar other than the default calendar.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="716c6-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="716c6-103">Prerequisites</span></span>
<span data-ttu-id="716c6-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="716c6-104">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="716c6-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="716c6-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="716c6-106">Un [calendar](../resources/calendar.md) de usuario que no sea el calendario predeterminado del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="716c6-106">A user's [calendar](../resources/calendar.md) other than the default calendar in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendars/{id}

DELETE /me/calendarGroup/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="716c6-107">Un [calendar](../resources/calendar.md) que no sea el calendario predeterminado de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="716c6-107">A [calendar](../resources/calendar.md) other than the default calendar, in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
DELETE /me/calendarGroups/{id}/calendars/{id}
DELETE /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="request-headers"></a><span data-ttu-id="716c6-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="716c6-108">Request headers</span></span>
| <span data-ttu-id="716c6-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="716c6-109">Name</span></span>           |  <span data-ttu-id="716c6-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="716c6-110">Type</span></span>    | <span data-ttu-id="716c6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="716c6-111">Description</span></span>|
|:---------------|:---------|:----------|
| <span data-ttu-id="716c6-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="716c6-112">Authorization</span></span>  |  <span data-ttu-id="716c6-113">string</span><span class="sxs-lookup"><span data-stu-id="716c6-113">string</span></span>  | <span data-ttu-id="716c6-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="716c6-p101">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="716c6-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="716c6-116">Request body</span></span>
<span data-ttu-id="716c6-117">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="716c6-117">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="716c6-118">Respuesta</span><span class="sxs-lookup"><span data-stu-id="716c6-118">Response</span></span>

<span data-ttu-id="716c6-p102">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="716c6-p102">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="716c6-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="716c6-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="716c6-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="716c6-122">Request</span></span>
<span data-ttu-id="716c6-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="716c6-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_calendar"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/calendar
```
##### <a name="response"></a><span data-ttu-id="716c6-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="716c6-124">Response</span></span>
<span data-ttu-id="716c6-125">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="716c6-125">Here is an example of the response.</span></span> 
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
  "description": "Delete calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
