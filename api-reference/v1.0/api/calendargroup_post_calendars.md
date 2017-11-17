# <a name="create-calendar"></a><span data-ttu-id="543ee-101">Create Calendar</span><span class="sxs-lookup"><span data-stu-id="543ee-101">Create Calendar</span></span>

<span data-ttu-id="543ee-102">Use esta API para crear un calendario en un grupo de calendarios para un [usuario](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="543ee-102">Use this API to create a new Calendar in a calendar group.</span></span> 
## <a name="permissions"></a><span data-ttu-id="543ee-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="543ee-103">Permissions</span></span>
<span data-ttu-id="543ee-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="543ee-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="543ee-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="543ee-106">Permission type</span></span>      | <span data-ttu-id="543ee-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="543ee-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="543ee-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="543ee-108">Delegated (work or school account)</span></span> | <span data-ttu-id="543ee-109">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="543ee-109">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="543ee-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="543ee-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="543ee-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="543ee-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="543ee-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="543ee-112">Application</span></span> | <span data-ttu-id="543ee-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="543ee-113">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="543ee-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="543ee-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="543ee-115">[calendarGroup](../resources/calendargroup.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="543ee-115">A user's default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
POST /me/calendarGroup/calendars
POST /users/{id | userPrincipalName}/calendarGroup/calendars
```
<span data-ttu-id="543ee-116">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="543ee-116">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>
```http
POST /me/calendarGroups/{id}/calendars
POST /users/{id | userPrincipalName}/calendarGroups/{id}/calendars
```
## <a name="request-headers"></a><span data-ttu-id="543ee-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="543ee-117">Request headers</span></span>
| <span data-ttu-id="543ee-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="543ee-118">Header</span></span>       | <span data-ttu-id="543ee-119">Valor</span><span class="sxs-lookup"><span data-stu-id="543ee-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="543ee-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="543ee-120">Authorization</span></span>  | <span data-ttu-id="543ee-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="543ee-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="543ee-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="543ee-123">Content-Type</span></span>  | <span data-ttu-id="543ee-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="543ee-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="543ee-126">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="543ee-126">Request body</span></span>
<span data-ttu-id="543ee-127">En el cuerpo de la solicitud, especifique una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="543ee-127">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="543ee-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="543ee-128">Response</span></span>

<span data-ttu-id="543ee-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="543ee-129">If successful, this method returns `201 Created` response code and [calendar](../resources/calendar.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="543ee-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="543ee-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="543ee-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="543ee-131">Request</span></span>
<span data-ttu-id="543ee-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="543ee-132">Here is an example of the request.</span></span>
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
<span data-ttu-id="543ee-133">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendar](../resources/calendar.md).</span><span class="sxs-lookup"><span data-stu-id="543ee-133">In the request body, supply a JSON representation of [calendar](../resources/calendar.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="543ee-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="543ee-134">Response</span></span>
<span data-ttu-id="543ee-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="543ee-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
