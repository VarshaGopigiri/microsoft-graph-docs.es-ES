# <a name="get-calendargroup"></a><span data-ttu-id="1ec2d-101">Get calendarGroup</span><span class="sxs-lookup"><span data-stu-id="1ec2d-101">Get calendarGroup</span></span>

<span data-ttu-id="1ec2d-102">Recupera las propiedades y relaciones de un objeto de grupo de calendarios.</span><span class="sxs-lookup"><span data-stu-id="1ec2d-102">Retrieve the properties and relationships of a calendar group object.</span></span>
## <a name="permissions"></a><span data-ttu-id="1ec2d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="1ec2d-103">Permissions</span></span>
<span data-ttu-id="1ec2d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1ec2d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1ec2d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1ec2d-106">Permission type</span></span>      | <span data-ttu-id="1ec2d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1ec2d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="1ec2d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1ec2d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="1ec2d-109">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="1ec2d-109">Calendars.Read</span></span>    |
|<span data-ttu-id="1ec2d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1ec2d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1ec2d-111">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="1ec2d-111">Calendars.Read</span></span>    |
|<span data-ttu-id="1ec2d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1ec2d-112">Application</span></span> | <span data-ttu-id="1ec2d-113">Calendars.Read</span><span class="sxs-lookup"><span data-stu-id="1ec2d-113">Calendars.Read</span></span> |

## <a name="http-request"></a><span data-ttu-id="1ec2d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1ec2d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="1ec2d-115">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="1ec2d-115">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>
```http
GET /me/calendarGroups/{id}
GET /users/{id | userPrincipalName}/calendarGroups/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1ec2d-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1ec2d-116">Optional query parameters</span></span>
<span data-ttu-id="1ec2d-117">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ec2d-117">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="1ec2d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1ec2d-118">Request headers</span></span>
| <span data-ttu-id="1ec2d-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="1ec2d-119">Name</span></span>       | <span data-ttu-id="1ec2d-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ec2d-120">Type</span></span> | <span data-ttu-id="1ec2d-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ec2d-121">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="1ec2d-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="1ec2d-122">Authorization</span></span>  | <span data-ttu-id="1ec2d-123">string</span><span class="sxs-lookup"><span data-stu-id="1ec2d-123">string</span></span>  | <span data-ttu-id="1ec2d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1ec2d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="1ec2d-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1ec2d-126">Request body</span></span>
<span data-ttu-id="1ec2d-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1ec2d-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1ec2d-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ec2d-128">Response</span></span>

<span data-ttu-id="1ec2d-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendarGroup](../resources/calendargroup.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1ec2d-129">If successful, this method returns a `200 OK` response code and [calendarGroup](../resources/calendargroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1ec2d-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1ec2d-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1ec2d-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1ec2d-131">Request</span></span>
<span data-ttu-id="1ec2d-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1ec2d-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_calendargroup"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
```
##### <a name="response"></a><span data-ttu-id="1ec2d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1ec2d-133">Response</span></span>
<span data-ttu-id="1ec2d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1ec2d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
