# <a name="update-rangefill"></a><span data-ttu-id="eeae9-101">Update rangefill</span><span class="sxs-lookup"><span data-stu-id="eeae9-101">Update rangefill</span></span>

<span data-ttu-id="eeae9-102">Actualiza las propiedades del objeto rangefill.</span><span class="sxs-lookup"><span data-stu-id="eeae9-102">Update the properties of rangefill object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="eeae9-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="eeae9-103">Prerequisites</span></span>
<span data-ttu-id="eeae9-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="eeae9-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="eeae9-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="eeae9-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="eeae9-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="eeae9-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /workbook/names(<name>)/range/format/fill
PATCH /workbook/worksheets/{id|name}/range(<address>)/format/fill
PATCH /workbook/tables/{id|name}/columns/{id|name}/range/format/fill
```
## <a name="optional-request-headers"></a><span data-ttu-id="eeae9-107">Encabezados de solicitud opcionales</span><span class="sxs-lookup"><span data-stu-id="eeae9-107">Optional request headers</span></span>
| <span data-ttu-id="eeae9-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="eeae9-108">Name</span></span>       | <span data-ttu-id="eeae9-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="eeae9-109">Description</span></span>|
|:-----------|:-----------|
| <span data-ttu-id="eeae9-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="eeae9-110">Authorization</span></span>  | <span data-ttu-id="eeae9-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="eeae9-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="eeae9-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="eeae9-113">Request body</span></span>
<span data-ttu-id="eeae9-p102">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="eeae9-p102">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="eeae9-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eeae9-117">Property</span></span>     | <span data-ttu-id="eeae9-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="eeae9-118">Type</span></span>   |<span data-ttu-id="eeae9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="eeae9-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="eeae9-120">color</span><span class="sxs-lookup"><span data-stu-id="eeae9-120">color</span></span>|<span data-ttu-id="eeae9-121">string</span><span class="sxs-lookup"><span data-stu-id="eeae9-121">string</span></span>|<span data-ttu-id="eeae9-122">Código de color HTML que representa el color de la línea de borde con el formato #RRGGBB (por ejemplo, "FFA500") o como un color HTML con nombre (por ejemplo, "naranja").</span><span class="sxs-lookup"><span data-stu-id="eeae9-122">HTML color code representing the color of the border line, of the form #RRGGBB (e.g. "FFA500") or as a named HTML color (e.g. "orange")</span></span>|

## <a name="response"></a><span data-ttu-id="eeae9-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eeae9-123">Response</span></span>

<span data-ttu-id="eeae9-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [RangeFill](../resources/rangefill.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="eeae9-124">If successful, this method returns a `200 OK` response code and updated [RangeFill](../resources/rangefill.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="eeae9-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="eeae9-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="eeae9-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="eeae9-126">Request</span></span>
<span data-ttu-id="eeae9-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="eeae9-127">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="eeae9-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="eeae9-128">Response</span></span>
<span data-ttu-id="eeae9-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="eeae9-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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