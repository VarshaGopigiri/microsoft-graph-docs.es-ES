# <a name="update-calendar"></a><span data-ttu-id="1a4b6-101">Actualizar calendario</span><span class="sxs-lookup"><span data-stu-id="1a4b6-101">Update calendar</span></span>

<span data-ttu-id="1a4b6-102">Actualiza las propiedades del objeto de calendario.</span><span class="sxs-lookup"><span data-stu-id="1a4b6-102">Update the properties of calendar object.</span></span>
## <a name="permissions"></a><span data-ttu-id="1a4b6-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="1a4b6-103">Permissions</span></span>
<span data-ttu-id="1a4b6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1a4b6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1a4b6-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1a4b6-106">Permission type</span></span>      | <span data-ttu-id="1a4b6-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1a4b6-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="1a4b6-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1a4b6-108">Delegated (work or school account)</span></span> | <span data-ttu-id="1a4b6-109">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1a4b6-109">Calendars.ReadWrite</span></span>    | 
|<span data-ttu-id="1a4b6-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1a4b6-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1a4b6-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1a4b6-111">Calendars.ReadWrite</span></span>    | 
|<span data-ttu-id="1a4b6-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1a4b6-112">Application</span></span> | <span data-ttu-id="1a4b6-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1a4b6-113">Calendars.ReadWrite</span></span> | 

## <a name="http-request"></a><span data-ttu-id="1a4b6-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1a4b6-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="1a4b6-115">[calendar](../resources/calendar.md) predeterminado de un usuario o grupo.</span><span class="sxs-lookup"><span data-stu-id="1a4b6-115">A user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
PATCH /me/calendar
PATCH /users/{id | userPrincipalName}/calendar
PATCH /groups/{id}/calendar
```
<span data-ttu-id="1a4b6-116">[calendar](../resources/calendar.md) de un usuario del [calendarGroup](../resources/calendargroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1a4b6-116">A user's [calendar](../resources/calendar.md) in the default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
PATCH /me/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendars/{id}

PATCH /me/calendarGroup/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendarGroup/calendars/{id}
```
<span data-ttu-id="1a4b6-117">[calendar](../resources/calendar.md) de un usuario de un [calendarGroup](../resources/calendargroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="1a4b6-117">A user's [calendar](../resources/calendar.md) in a specific [calendarGroup](../resources/calendargroup.md).</span></span>
```http
PATCH /me/calendarGroups/{id}/calendars/{id}
PATCH /users/{id | userPrincipalName}/calendarGroups/{id}/calendars/{id}
```
## <a name="request-headers"></a><span data-ttu-id="1a4b6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1a4b6-118">Request headers</span></span>
| <span data-ttu-id="1a4b6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a4b6-119">Header</span></span>       | <span data-ttu-id="1a4b6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1a4b6-120">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="1a4b6-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="1a4b6-121">Authorization</span></span>  | <span data-ttu-id="1a4b6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a4b6-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="1a4b6-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="1a4b6-124">Content-Type</span></span>  | <span data-ttu-id="1a4b6-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1a4b6-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="1a4b6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1a4b6-127">Request body</span></span>
<span data-ttu-id="1a4b6-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="1a4b6-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="1a4b6-131">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1a4b6-131">Property</span></span>     | <span data-ttu-id="1a4b6-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="1a4b6-132">Type</span></span>   |<span data-ttu-id="1a4b6-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="1a4b6-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1a4b6-134">color</span><span class="sxs-lookup"><span data-stu-id="1a4b6-134">color</span></span>|<span data-ttu-id="1a4b6-135">String</span><span class="sxs-lookup"><span data-stu-id="1a4b6-135">String</span></span>|<span data-ttu-id="1a4b6-p105">Especifica el tema de color para distinguir el calendario de otros calendarios en una interfaz de usuario. Los valores de propiedad son: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1</span><span class="sxs-lookup"><span data-stu-id="1a4b6-p105">Specifies the color theme to distinguish the calendar from other calendars in a UI. The property values are: LightBlue=0, LightGreen=1, LightOrange=2, LightGray=3, LightYellow=4, LightTeal=5, LightPink=6, LightBrown=7, LightRed=8, MaxColor=9, Auto=-1</span></span>|
|<span data-ttu-id="1a4b6-138">name</span><span class="sxs-lookup"><span data-stu-id="1a4b6-138">name</span></span>|<span data-ttu-id="1a4b6-139">String</span><span class="sxs-lookup"><span data-stu-id="1a4b6-139">String</span></span>|<span data-ttu-id="1a4b6-140">El nombre del calendario.</span><span class="sxs-lookup"><span data-stu-id="1a4b6-140">The calendar name.</span></span>|

## <a name="response"></a><span data-ttu-id="1a4b6-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a4b6-141">Response</span></span>

<span data-ttu-id="1a4b6-142">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendar](../resources/calendar.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1a4b6-142">If successful, this method returns a `200 OK` response code and updated [calendar](../resources/calendar.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1a4b6-143">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1a4b6-143">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1a4b6-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1a4b6-144">Request</span></span>
<span data-ttu-id="1a4b6-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1a4b6-145">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="1a4b6-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1a4b6-146">Response</span></span>
<span data-ttu-id="1a4b6-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1a4b6-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
