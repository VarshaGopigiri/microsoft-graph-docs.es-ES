# <a name="get-calendargroup"></a><span data-ttu-id="a7c18-101">Get calendarGroup</span><span class="sxs-lookup"><span data-stu-id="a7c18-101">Get calendarGroup</span></span>

<span data-ttu-id="a7c18-102">Recupera las propiedades y relaciones de un objeto de grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="a7c18-102">Retrieve the properties and relationships of a calendar group object.</span></span>

## <a name="permissions"></a><span data-ttu-id="a7c18-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="a7c18-103">Permissions</span></span>

<span data-ttu-id="a7c18-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a7c18-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

| <span data-ttu-id="a7c18-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7c18-106">Permission type</span></span>                        | <span data-ttu-id="a7c18-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7c18-107">Permissions (from least to most privileged)</span></span> |
| :------------------------------------- | :------------------------------------------ |
| <span data-ttu-id="a7c18-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7c18-108">Delegated (work or school account)</span></span>     | <span data-ttu-id="a7c18-109">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a7c18-109">Calendars.Read</span></span>                              |
| <span data-ttu-id="a7c18-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7c18-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a7c18-111">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a7c18-111">Calendars.Read</span></span>                              |
| <span data-ttu-id="a7c18-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7c18-112">Application</span></span>                            | <span data-ttu-id="a7c18-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="a7c18-113">Calendars.Read</span></span>                              |

## <a name="http-request"></a><span data-ttu-id="a7c18-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7c18-114">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

<span data-ttu-id="a7c18-115">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="a7c18-115">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>

```http
GET /me/calendarGroups/{id}
GET /users/{id | userPrincipalName}/calendarGroups/{id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a7c18-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a7c18-116">Optional query parameters</span></span>

<span data-ttu-id="a7c18-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7c18-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a7c18-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7c18-118">Request headers</span></span>

| <span data-ttu-id="a7c18-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="a7c18-119">Name</span></span>          | <span data-ttu-id="a7c18-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7c18-120">Type</span></span>   | <span data-ttu-id="a7c18-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7c18-121">Description</span></span>               |
| :------------ | :----- | :------------------------ |
| <span data-ttu-id="a7c18-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="a7c18-122">Authorization</span></span> | <span data-ttu-id="a7c18-123">string</span><span class="sxs-lookup"><span data-stu-id="a7c18-123">string</span></span> | <span data-ttu-id="a7c18-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a7c18-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a7c18-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a7c18-126">Request body</span></span>

<span data-ttu-id="a7c18-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a7c18-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a7c18-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7c18-128">Response</span></span>

<span data-ttu-id="a7c18-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7c18-129">If successful, this method returns a `200 OK` response code and [calendarGroup](../resources/calendargroup.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a7c18-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7c18-130">Example</span></span>

##### <a name="request"></a><span data-ttu-id="a7c18-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7c18-131">Request</span></span>

<span data-ttu-id="a7c18-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7c18-132">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_calendargroup"
}-->

```http
GET https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
```

##### <a name="response"></a><span data-ttu-id="a7c18-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7c18-133">Response</span></span>

<span data-ttu-id="a7c18-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a7c18-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.calendarGroup"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 110

{
  "name": "name-value",
  "classId": "11b0131d-43c8-4bbb-b2c8-e80f9a50834a",
  "changeKey": "changeKey-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "Get calendarGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
