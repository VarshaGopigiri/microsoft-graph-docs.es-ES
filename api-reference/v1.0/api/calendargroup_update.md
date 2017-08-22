# <a name="update-calendargroup"></a><span data-ttu-id="b9887-101">Actualizar grupo de calendario</span><span class="sxs-lookup"><span data-stu-id="b9887-101">Update calendargroup</span></span>

<span data-ttu-id="b9887-102">Actualiza las propiedades del objeto calendargroup.</span><span class="sxs-lookup"><span data-stu-id="b9887-102">Update the properties of calendargroup object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b9887-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b9887-103">Prerequisites</span></span>
<span data-ttu-id="b9887-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: _Calendars.ReadWrite_</span><span class="sxs-lookup"><span data-stu-id="b9887-104">One of the following **scopes** is required to execute this API: _Calendars.ReadWrite_</span></span>
## <a name="http-request"></a><span data-ttu-id="b9887-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b9887-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="b9887-106">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="b9887-106">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>
```http
PATCH /me/calendarGroups/{id}
PATCH /users/{id | userPrincipalName}/calendarGroups/{id}
```
## <a name="request-headers"></a><span data-ttu-id="b9887-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b9887-107">Request headers</span></span>
| <span data-ttu-id="b9887-108">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9887-108">Header</span></span>       | <span data-ttu-id="b9887-109">Valor</span><span class="sxs-lookup"><span data-stu-id="b9887-109">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="b9887-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="b9887-110">Authorization</span></span>  | <span data-ttu-id="b9887-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9887-p101">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="b9887-113">Content-Type</span><span class="sxs-lookup"><span data-stu-id="b9887-113">Content-Type</span></span>  | <span data-ttu-id="b9887-p102">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9887-p102">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b9887-116">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b9887-116">Request body</span></span>
<span data-ttu-id="b9887-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="b9887-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="b9887-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9887-120">Property</span></span>     | <span data-ttu-id="b9887-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9887-121">Type</span></span>   |<span data-ttu-id="b9887-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9887-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b9887-123">name</span><span class="sxs-lookup"><span data-stu-id="b9887-123">name</span></span>|<span data-ttu-id="b9887-124">String</span><span class="sxs-lookup"><span data-stu-id="b9887-124">String</span></span>|<span data-ttu-id="b9887-125">Nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="b9887-125">The group name.</span></span>|

## <a name="response"></a><span data-ttu-id="b9887-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9887-126">Response</span></span>

<span data-ttu-id="b9887-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendarGroup](../resources/calendargroup.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b9887-127">If successful, this method returns a `200 OK` response code and updated [calendarGroup](../resources/calendargroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="b9887-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b9887-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b9887-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b9887-129">Request</span></span>
<span data-ttu-id="b9887-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b9887-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_calendargroup"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/calendarGroups/{id}
Content-type: application/json
Content-length: 30

{
  "name": "name-value"
}
```
##### <a name="response"></a><span data-ttu-id="b9887-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b9887-131">Response</span></span>
<span data-ttu-id="b9887-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b9887-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Update calendargroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
