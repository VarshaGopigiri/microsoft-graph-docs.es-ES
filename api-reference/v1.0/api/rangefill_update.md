# <a name="update-rangefill"></a><span data-ttu-id="dbcbf-101">Update rangefill</span><span class="sxs-lookup"><span data-stu-id="dbcbf-101">Update rangefill</span></span>

<span data-ttu-id="dbcbf-102">Actualizar las propiedades del objeto rangefill.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-102">Update the properties of rangefill object.</span></span>
## <a name="permissions"></a><span data-ttu-id="dbcbf-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="dbcbf-103">Permissions</span></span>
<span data-ttu-id="dbcbf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="dbcbf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="dbcbf-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dbcbf-106">Permission type</span></span>      | <span data-ttu-id="dbcbf-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dbcbf-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dbcbf-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dbcbf-108">Delegated (work or school account)</span></span> | <span data-ttu-id="dbcbf-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dbcbf-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="dbcbf-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dbcbf-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dbcbf-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-111">Not supported.</span></span>    |
|<span data-ttu-id="dbcbf-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dbcbf-112">Application</span></span> | <span data-ttu-id="dbcbf-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="dbcbf-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dbcbf-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format/fill
PATCH /workbook/worksheets/{id|name}/range(address='<address>')/format/fill
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/fill
```
## <a name="optional-request-headers"></a><span data-ttu-id="dbcbf-115">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="dbcbf-115">Optional request headers</span></span>
| <span data-ttu-id="dbcbf-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="dbcbf-116">Name</span></span>       | <span data-ttu-id="dbcbf-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbcbf-117">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="dbcbf-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="dbcbf-118">Authorization</span></span>  | <span data-ttu-id="dbcbf-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dbcbf-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dbcbf-121">Request body</span></span>
<span data-ttu-id="dbcbf-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="dbcbf-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dbcbf-125">Property</span></span>     | <span data-ttu-id="dbcbf-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="dbcbf-126">Type</span></span>   |<span data-ttu-id="dbcbf-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbcbf-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dbcbf-128">color</span><span class="sxs-lookup"><span data-stu-id="dbcbf-128">color</span></span>|<span data-ttu-id="dbcbf-129">string</span><span class="sxs-lookup"><span data-stu-id="dbcbf-129">string</span></span>|<span data-ttu-id="dbcbf-130">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="dbcbf-130">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange")</span></span>|

## <a name="response"></a><span data-ttu-id="dbcbf-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbcbf-131">Response</span></span>

<span data-ttu-id="dbcbf-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [RangeFill](../resources/rangefill.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-132">If successful, this method returns a `200 OK` response code and updated [RangeFill](../resources/rangefill.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="dbcbf-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dbcbf-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="dbcbf-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dbcbf-134">Request</span></span>
<span data-ttu-id="dbcbf-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_rangefill"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/format/fill
Content-type: application/json
Content-length: 28

{
  "color": "color-value"
}
```
##### <a name="response"></a><span data-ttu-id="dbcbf-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbcbf-136">Response</span></span>
<span data-ttu-id="dbcbf-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dbcbf-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.rangeFill"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 28

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update rangefill",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->