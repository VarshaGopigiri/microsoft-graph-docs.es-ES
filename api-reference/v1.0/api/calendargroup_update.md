# <a name="update-calendargroup"></a><span data-ttu-id="13e1d-101">Actualizar grupo de calendario</span><span class="sxs-lookup"><span data-stu-id="13e1d-101">Update calendargroup</span></span>

<span data-ttu-id="13e1d-102">Actualiza las propiedades del objeto calendargroup.</span><span class="sxs-lookup"><span data-stu-id="13e1d-102">Update the properties of calendargroup object.</span></span>
## <a name="permissions"></a><span data-ttu-id="13e1d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="13e1d-103">Permissions</span></span>
<span data-ttu-id="13e1d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="13e1d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="13e1d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="13e1d-106">Permission type</span></span>      | <span data-ttu-id="13e1d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="13e1d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="13e1d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="13e1d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="13e1d-109">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="13e1d-109">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="13e1d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="13e1d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="13e1d-111">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="13e1d-111">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="13e1d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="13e1d-112">Application</span></span> | <span data-ttu-id="13e1d-113">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="13e1d-113">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="13e1d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="13e1d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="13e1d-115">Cualquier [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="13e1d-115">Any [calendarGroup](../resources/calendargroup.md) of a user.</span></span>
```http
PATCH /me/calendarGroups/{id}
PATCH /users/{id | userPrincipalName}/calendarGroups/{id}
```
## <a name="request-headers"></a><span data-ttu-id="13e1d-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="13e1d-116">Request headers</span></span>
| <span data-ttu-id="13e1d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="13e1d-117">Header</span></span>       | <span data-ttu-id="13e1d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="13e1d-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="13e1d-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="13e1d-119">Authorization</span></span>  | <span data-ttu-id="13e1d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="13e1d-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="13e1d-122">Content-Type</span><span class="sxs-lookup"><span data-stu-id="13e1d-122">Content-Type</span></span>  | <span data-ttu-id="13e1d-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="13e1d-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="13e1d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="13e1d-125">Request body</span></span>
<span data-ttu-id="13e1d-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="13e1d-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="13e1d-129">Propiedad</span><span class="sxs-lookup"><span data-stu-id="13e1d-129">Property</span></span>     | <span data-ttu-id="13e1d-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="13e1d-130">Type</span></span>   |<span data-ttu-id="13e1d-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="13e1d-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="13e1d-132">name</span><span class="sxs-lookup"><span data-stu-id="13e1d-132">name</span></span>|<span data-ttu-id="13e1d-133">String</span><span class="sxs-lookup"><span data-stu-id="13e1d-133">String</span></span>|<span data-ttu-id="13e1d-134">Nombre del grupo.</span><span class="sxs-lookup"><span data-stu-id="13e1d-134">The group name.</span></span>|

## <a name="response"></a><span data-ttu-id="13e1d-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13e1d-135">Response</span></span>

<span data-ttu-id="13e1d-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [calendarGroup](../resources/calendargroup.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="13e1d-136">If successful, this method returns a `200 OK` response code and updated [calendarGroup](../resources/calendargroup.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="13e1d-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="13e1d-137">Example</span></span>
##### <a name="request"></a><span data-ttu-id="13e1d-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="13e1d-138">Request</span></span>
<span data-ttu-id="13e1d-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="13e1d-139">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="13e1d-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="13e1d-140">Response</span></span>
<span data-ttu-id="13e1d-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="13e1d-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
