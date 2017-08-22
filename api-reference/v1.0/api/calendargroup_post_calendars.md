# <a name="create-calendar"></a><span data-ttu-id="5134b-101">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="5134b-101">Create Calendar</span></span>

<span data-ttu-id="5134b-102">Use esta API para crear un calendario en un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="5134b-102">Use this API to create a new Calendar in a calendar group.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5134b-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5134b-103">Prerequisites</span></span>
<span data-ttu-id="5134b-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: _Calendars.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="5134b-104">One of the following **scopes** is required to execute this API: _Calendars.ReadWrite_</span></span>
## <a name="http-request"></a><span data-ttu-id="5134b-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5134b-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="5134b-106">[calendarGroup](../resources/calendargroup.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="5134b-106">A user's default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
POST /me/calendarGroup/calendars
POST /users/{id | userPrincipalName}/calendarGroup/calendars
```
<span data-ttu-id="5134b-107">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="5134b-107">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>
```http
POST /me/calendarGroups/{id}/calendars
POST /users/{id | userPrincipalName}/calendarGroups/{id}/calendars
```
## <a name="request-headers"></a><span data-ttu-id="5134b-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5134b-108">Request headers</span></span>
| <span data-ttu-id="5134b-109">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5134b-109">Header</span></span>       | <span data-ttu-id="5134b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="5134b-110">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5134b-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="5134b-111">Authorization</span></span>  | <span data-ttu-id="5134b-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5134b-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="5134b-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="5134b-114">Content-Type</span></span>  | <span data-ttu-id="5134b-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5134b-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5134b-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5134b-117">Request body</span></span>
<span data-ttu-id="5134b-118">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [Calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="5134b-118">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="5134b-119">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5134b-119">Response</span></span>

<span data-ttu-id="5134b-120">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [Calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5134b-120">If successful, this method returns `201, Created` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5134b-121">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5134b-121">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5134b-122">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5134b-122">Request</span></span>
<span data-ttu-id="5134b-123">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5134b-123">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_calendar_from_calendargroup"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/calendarGroups/{id}/calendars
Content-type: application/json
Content-length: 78

{
  "name": "name-value",
  "color": {
  }
}
```
<span data-ttu-id="5134b-124">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="5134b-124">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="5134b-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5134b-125">Response</span></span>
<span data-ttu-id="5134b-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5134b-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 98

{
  "name": "name-value",
  "color": {
  },
  "changeKey": "changeKey-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
