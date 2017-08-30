# <a name="update-tablecolumn"></a><span data-ttu-id="2d045-101">Update tablecolumn</span><span class="sxs-lookup"><span data-stu-id="2d045-101">Update tablecolumn</span></span>

<span data-ttu-id="2d045-102">Actualizar las propiedades del objeto tablecolumn.</span><span class="sxs-lookup"><span data-stu-id="2d045-102">Update the properties of tablecolumn object.</span></span>
## <a name="permissions"></a><span data-ttu-id="2d045-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="2d045-103">Permissions</span></span>
<span data-ttu-id="2d045-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2d045-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2d045-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2d045-106">Permission type</span></span>      | <span data-ttu-id="2d045-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2d045-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2d045-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2d045-108">Delegated (work or school account)</span></span> | <span data-ttu-id="2d045-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2d045-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="2d045-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2d045-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2d045-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d045-111">Not supported.</span></span>    |
|<span data-ttu-id="2d045-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2d045-112">Application</span></span> | <span data-ttu-id="2d045-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d045-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="2d045-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2d045-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/tables/{id|name}/columns/{id|name}
PATCH /workbook/worksheets/{id|name}/tables/{id|name}/columns/{id|name}
```
## <a name="optional-request-headers"></a><span data-ttu-id="2d045-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="2d045-115">Optional request headers</span></span>
| <span data-ttu-id="2d045-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="2d045-116">Name</span></span>       | <span data-ttu-id="2d045-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d045-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="2d045-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="2d045-118">Authorization</span></span>  | <span data-ttu-id="2d045-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2d045-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2d045-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2d045-121">Request body</span></span>
<span data-ttu-id="2d045-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="2d045-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="2d045-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2d045-125">Property</span></span>     | <span data-ttu-id="2d045-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d045-126">Type</span></span>   |<span data-ttu-id="2d045-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d045-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2d045-128">values</span><span class="sxs-lookup"><span data-stu-id="2d045-128">values</span></span>|<span data-ttu-id="2d045-129">json</span><span class="sxs-lookup"><span data-stu-id="2d045-129">json</span></span>|<span data-ttu-id="2d045-p104">Representa los valores sin formato del rango especificado. Los datos devueltos pueden ser de tipo string, number o boolean. La celda que contenga un error devolverá la cadena de error.</span><span class="sxs-lookup"><span data-stu-id="2d045-p104">Represents the raw values of the specified range. The data returned could be of type string, number, or a boolean. Cell that contain an error will return the error string.</span></span>|

## <a name="response"></a><span data-ttu-id="2d045-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d045-133">Response</span></span>

<span data-ttu-id="2d045-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [TableColumn](../resources/tablecolumn.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d045-134">If successful, this method returns a `200 OK` response code and updated [TableColumn](../resources/tablecolumn.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="2d045-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d045-135">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2d045-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2d045-136">Request</span></span>
<span data-ttu-id="2d045-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2d045-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_tablecolumn"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/tables/{id|name}/columns/{id|name}
Content-type: application/json
Content-length: 81

{
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```
##### <a name="response"></a><span data-ttu-id="2d045-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d045-138">Response</span></span>
<span data-ttu-id="2d045-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2d045-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.tableColumn"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 81

{
  "id": 99,
  "name": "name-value",
  "index": 99,
  "values": "values-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update tablecolumn",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->