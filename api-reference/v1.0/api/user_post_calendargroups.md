# <a name="create-calendargroup"></a><span data-ttu-id="debcd-101">Create CalendarGroup</span><span class="sxs-lookup"><span data-stu-id="debcd-101">Create CalendarGroup</span></span>

<span data-ttu-id="debcd-102">Usa esta API para crear un objeto CalendarGroup.</span><span class="sxs-lookup"><span data-stu-id="debcd-102">Use this API to create a new CalendarGroup.</span></span>
## <a name="permissions"></a><span data-ttu-id="debcd-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="debcd-103">Permissions</span></span>
<span data-ttu-id="debcd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="debcd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="debcd-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="debcd-106">Permission type</span></span>      | <span data-ttu-id="debcd-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="debcd-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="debcd-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="debcd-108">Delegated (work or school account)</span></span> | <span data-ttu-id="debcd-109">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="debcd-109">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="debcd-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="debcd-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="debcd-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="debcd-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="debcd-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="debcd-112">Application</span></span> | <span data-ttu-id="debcd-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="debcd-113">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="debcd-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="debcd-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /users/{id | userPrincipalName}/calendarGroups
```
## <a name="request-headers"></a><span data-ttu-id="debcd-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="debcd-115">Request headers</span></span>
| <span data-ttu-id="debcd-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="debcd-116">Header</span></span>       | <span data-ttu-id="debcd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="debcd-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="debcd-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="debcd-118">Authorization</span></span>  | <span data-ttu-id="debcd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="debcd-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="debcd-121">Content-Type</span><span class="sxs-lookup"><span data-stu-id="debcd-121">Content-Type</span></span>  | <span data-ttu-id="debcd-122">application/json</span><span class="sxs-lookup"><span data-stu-id="debcd-122">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="debcd-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="debcd-123">Request body</span></span>
<span data-ttu-id="debcd-124">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [CalendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="debcd-124">In the request body, supply a JSON representation of [CalendarGroup](../resources/calendargroup.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="debcd-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="debcd-125">Response</span></span>

<span data-ttu-id="debcd-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el objeto [CalendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="debcd-126">If successful, this method returns `201 Created` response code and [CalendarGroup](../resources/calendargroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="debcd-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="debcd-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="debcd-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="debcd-128">Request</span></span>
<span data-ttu-id="debcd-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="debcd-129">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_calendargroup_from_user"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/calendarGroups
Content-type: application/json
Content-length: 90

{
  "name": "name-value",
  "classId": "classId-value",
  "changeKey": "changeKey-value"
}
```
<span data-ttu-id="debcd-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [calendarGroup](../resources/calendargroup.md).</span><span class="sxs-lookup"><span data-stu-id="debcd-130">In the request body, supply a JSON representation of [calendarGroup](../resources/calendargroup.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="debcd-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="debcd-131">Response</span></span>
<span data-ttu-id="debcd-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="debcd-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarGroup"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json
Content-length: 110

{
  "name": "name-value",
  "classId": "classId-value",
  "changeKey": "changeKey-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create CalendarGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
