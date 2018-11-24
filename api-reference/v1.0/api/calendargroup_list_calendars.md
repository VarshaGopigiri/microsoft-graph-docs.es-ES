# <a name="list-calendars"></a><span data-ttu-id="c7e5f-101">List calendars</span><span class="sxs-lookup"><span data-stu-id="c7e5f-101">List calendars</span></span>

<span data-ttu-id="c7e5f-102">Recupera una lista de calendarios que pertenecen a un grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="c7e5f-102">Retrieve a list of calendars belonging to a calendar group.</span></span>

## <a name="permissions"></a><span data-ttu-id="c7e5f-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c7e5f-103">Permissions</span></span>

<span data-ttu-id="c7e5f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c7e5f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="c7e5f-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c7e5f-106">Permission type</span></span>                        | <span data-ttu-id="c7e5f-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c7e5f-107">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="c7e5f-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c7e5f-108">Delegated (work or school account)</span></span>     | <span data-ttu-id="c7e5f-109">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="c7e5f-109">Calendars.Read</span></span>                              |
| <span data-ttu-id="c7e5f-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7e5f-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c7e5f-111">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="c7e5f-111">Calendars.Read</span></span>                              |
| <span data-ttu-id="c7e5f-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c7e5f-112">Application</span></span>                            | <span data-ttu-id="c7e5f-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="c7e5f-113">Calendars.Read</span></span>                              |

## <a name="http-request"></a><span data-ttu-id="c7e5f-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7e5f-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

<span data-ttu-id="c7e5f-115">[calendarGroup](../resources/calendargroup.md) predeterminado de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c7e5f-115">A user's default [calendarGroup](../resources/calendargroup.md).</span></span>

```http
GET /me/calendarGroup/calendars
GET /users/{id | userPrincipalName}/calendarGroup/calendars
```

<span data-ttu-id="c7e5f-116">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c7e5f-116">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>

```http
GET /me/calendarGroups/{id}/calendars
GET /users/{id | userPrincipalName}/calendarGroups/{id}/calendars
```

## <a name="optional-query-parameters"></a><span data-ttu-id="c7e5f-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c7e5f-117">Optional query parameters</span></span>

<span data-ttu-id="c7e5f-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7e5f-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="c7e5f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7e5f-119">Request headers</span></span>

| <span data-ttu-id="c7e5f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="c7e5f-120">Name</span></span>          | <span data-ttu-id="c7e5f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7e5f-121">Type</span></span>   | <span data-ttu-id="c7e5f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7e5f-122">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="c7e5f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c7e5f-123">Authorization</span></span> | <span data-ttu-id="c7e5f-124">string</span><span class="sxs-lookup"><span data-stu-id="c7e5f-124">string</span></span> | <span data-ttu-id="c7e5f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c7e5f-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c7e5f-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7e5f-127">Request body</span></span>

<span data-ttu-id="c7e5f-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c7e5f-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c7e5f-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7e5f-129">Response</span></span>

<span data-ttu-id="c7e5f-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [Calendar](../resources/calendar.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7e5f-130">If successful, this method returns a `200 OK` response code and collection of [Calendar](../resources/calendar.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c7e5f-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7e5f-131">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c7e5f-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7e5f-132">Request</span></span>

<span data-ttu-id="c7e5f-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7e5f-133">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_calendars"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/calendarGroups/{id}/calendars
```

##### <a name="response"></a><span data-ttu-id="c7e5f-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7e5f-134">Response</span></span>

<span data-ttu-id="c7e5f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7e5f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendar",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 147

{
  "value": [
    {
      "name": "name-value",
      "color": {
      },
      "changeKey": "changeKey-value",
      "id": "id-value"
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
