# <a name="update-calendar"></a><span data-ttu-id="2a102-101">Actualizar calendario</span><span class="sxs-lookup"><span data-stu-id="2a102-101">Update calendar</span></span>

<span data-ttu-id="2a102-102">Actualice las propiedades del objeto de calendario.</span><span class="sxs-lookup"><span data-stu-id="2a102-102">Update the properties of calendar object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2a102-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2a102-103">Prerequisites</span></span>
<span data-ttu-id="2a102-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Calendars.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="2a102-104">One of the following **scopes** is required to execute this API: *Calendars.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="2a102-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2a102-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="2a102-106">[calendar](../resources/calendar.md) predeterminado de un usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="2a102-106">A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
PATCH /me/calendar
PATCH /users/{id | userPrincipalName}/calendar
PATCH /groups/{id}/calendar
```
<span data-ttu-id="2a102-107">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2a102-107">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
PATCH /me/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendars/{id}

PATCH /me/calendarGroup/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="2a102-108">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="2a102-108">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
PATCH /me/calendarGroups/{id}/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="request-headers"></a><span data-ttu-id="2a102-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2a102-109">Request headers</span></span>
| <span data-ttu-id="2a102-110">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a102-110">Header</span></span>       | <span data-ttu-id="2a102-111">Valor</span><span class="sxs-lookup"><span data-stu-id="2a102-111">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="2a102-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="2a102-112">Authorization</span></span>  | <span data-ttu-id="2a102-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a102-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="2a102-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2a102-115">Content-Type</span></span>  | <span data-ttu-id="2a102-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a102-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="2a102-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2a102-118">Request body</span></span>
<span data-ttu-id="2a102-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="2a102-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="2a102-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2a102-122">Property</span></span>     | <span data-ttu-id="2a102-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a102-123">Type</span></span>   |<span data-ttu-id="2a102-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a102-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2a102-125">color</span><span class="sxs-lookup"><span data-stu-id="2a102-125">color</span></span>|<span data-ttu-id="2a102-126">String</span><span class="sxs-lookup"><span data-stu-id="2a102-126">String</span></span>|<span data-ttu-id="2a102-p104">Especifica el tema de color para distinguir el calendario de otros calendarios en una interfaz de usuario. Los valores de propiedad son: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1</span><span class="sxs-lookup"><span data-stu-id="2a102-p104">Specifies the color theme to distinguish the calendar from other calendars in a UI. The property values are: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1</span></span>|
|<span data-ttu-id="2a102-129">name</span><span class="sxs-lookup"><span data-stu-id="2a102-129">name</span></span>|<span data-ttu-id="2a102-130">String</span><span class="sxs-lookup"><span data-stu-id="2a102-130">String</span></span>|<span data-ttu-id="2a102-131">El nombre del calendario.</span><span class="sxs-lookup"><span data-stu-id="2a102-131">The calendar name.</span></span>|

## <a name="response"></a><span data-ttu-id="2a102-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a102-132">Response</span></span>

<span data-ttu-id="2a102-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendar](../resources/calendar.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2a102-133">If successful, this method returns a `200 OK` response code and updated [calendar](../resources/calendar.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2a102-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2a102-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2a102-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2a102-135">Request</span></span>
<span data-ttu-id="2a102-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2a102-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_calendar"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/calendar
Content-type: application/json

{
  "name": "Social events"
}
```
##### <a name="response"></a><span data-ttu-id="2a102-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2a102-137">Response</span></span>
<span data-ttu-id="2a102-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2a102-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#me/calendars/$entity",
    "@odata.id":"https://graph.microsoft.com/v1.0/users('266efe5a-0fd7-4edd-877b-b2d1e561f193@ae01a323-3934-4475-a32d-af1274312bb0')/calendars('AAMkADJmMVAAA=')",
    "id":"AAMkADJmMVAAA=",
    "name":"Social events",
    "color":"auto",
    "changeKey":"DxYSthXJXEWwAQSYQnXvIgAAIxGttg==",
    "canShare":true,
    "canViewPrivateItems":true,
    "canEdit":true,
    "owner":{
        "name":"Fanny Downs",
        "address":"fannyd@adatum.onmicrosoft.com"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update calendar",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
