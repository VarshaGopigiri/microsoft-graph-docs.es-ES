# <a name="list-calendars"></a><span data-ttu-id="6043e-101">List calendars</span><span class="sxs-lookup"><span data-stu-id="6043e-101">List calendars</span></span>

<span data-ttu-id="6043e-102">Obtiene todos los calendarios del usuario (propiedad de navegación `/calendars`), los calendarios del grupo de calendarios predeterminado o de un grupo de calendarios específico.</span><span class="sxs-lookup"><span data-stu-id="6043e-102">Get all the user's calendars (`/calendars` navigation property), get the calendars from the default calendar group or from a specific calendar group.</span></span> 
## <a name="permissions"></a><span data-ttu-id="6043e-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6043e-103">Permissions</span></span>
<span data-ttu-id="6043e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6043e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6043e-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6043e-106">Permission type</span></span>      | <span data-ttu-id="6043e-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6043e-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6043e-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6043e-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6043e-109">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6043e-109">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="6043e-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6043e-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6043e-111">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6043e-111">Calendars.Read, Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="6043e-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6043e-112">Application</span></span> | <span data-ttu-id="6043e-113">Calendars.Read, Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6043e-113">Calendars.Read, Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="6043e-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6043e-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

<span data-ttu-id="6043e-115">Todos los calendarios del usuario.</span><span class="sxs-lookup"><span data-stu-id="6043e-115">All the user's calendars.</span></span>
```http
GET /me/calendars
GET /users/{id | userPrincipalName}/calendars
```

<span data-ttu-id="6043e-116">Calendarios del usuario en el [calendarGroup](../resources/calendarGroup.md) predeterminado.</span><span class="sxs-lookup"><span data-stu-id="6043e-116">The user's calendars in the default [calendarGroup](../resources/calendarGroup.md).</span></span>
```http
GET /me/calendargroups/{calendar_group_id}/calendars
GET /users/{id | userPrincipalName}/calendarGroup/calendars
```

<span data-ttu-id="6043e-117">Calendarios del usuario en un [calendarGroup](../resources/calendarGroup.md) específico.</span><span class="sxs-lookup"><span data-stu-id="6043e-117">The user's calendars in a specific [calendarGroup](../resources/calendarGroup.md).</span></span>
```http
GET /me/calendarGroups/{calendar_group_id}/calendars
GET /users/{id | userPrincipalName}/calendarGroups/{calendar_group_id}/calendars
```

## <a name="optional-query-parameters"></a><span data-ttu-id="6043e-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="6043e-118">Optional query parameters</span></span>
<span data-ttu-id="6043e-119">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6043e-119">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="6043e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6043e-120">Request headers</span></span>
| <span data-ttu-id="6043e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6043e-121">Header</span></span>       | <span data-ttu-id="6043e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6043e-122">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="6043e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6043e-123">Authorization</span></span>  | <span data-ttu-id="6043e-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6043e-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="6043e-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6043e-126">Content-Type</span></span>   | <span data-ttu-id="6043e-127">application/json</span><span class="sxs-lookup"><span data-stu-id="6043e-127">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="6043e-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6043e-128">Request body</span></span>
<span data-ttu-id="6043e-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6043e-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6043e-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6043e-130">Response</span></span>

<span data-ttu-id="6043e-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6043e-131">If successful, this method returns a `200 OK` response code and collection of [Calendar](../resources/calendar.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6043e-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6043e-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6043e-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6043e-133">Request</span></span>
<span data-ttu-id="6043e-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6043e-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendars"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendars
```
##### <a name="response"></a><span data-ttu-id="6043e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6043e-135">Response</span></span>
<span data-ttu-id="6043e-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6043e-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "@odata.context": "https://graph.microsoft.com/v1.0/$metadata#me/calendars",
    "value": [
        {
            "@odata.id": "https://graph.microsoft.com/v1.0/users('ddfcd489-628b-40d7-b48b-57002df800e5@1717622f-1d94-4d0c-9d74-709fad664b77')/calendars('AAMkAGI2TGuLAAA=')",
            "id": "AAMkAGI2TGuLAAA=",
            "name": "Calendar",
            "color": "auto",
            "changeKey": "nfZyf7VcrEKLNoU37KWlkQAAA0x0+w==",
            "canShare":true,
            "canViewPrivateItems":true,
            "canEdit":true,
            "owner":{
                "name":"Fanny Downs",
                "address":"fannyd@adatum.onmicrosoft.com"
            }
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List calendars",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->