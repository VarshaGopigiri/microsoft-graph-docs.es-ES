# <a name="range-cell"></a><span data-ttu-id="0016f-101">Range: Cell</span><span class="sxs-lookup"><span data-stu-id="0016f-101">Range: Cell</span></span>

<span data-ttu-id="0016f-p101">Obtiene el objeto de intervalo que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del intervalo principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo. La celda devuelta se ubica con respecto a la celda superior izquierda del intervalo.</span><span class="sxs-lookup"><span data-stu-id="0016f-p101">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid. The returned cell is located relative to the top left cell of the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="0016f-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="0016f-105">Permissions</span></span>
<span data-ttu-id="0016f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0016f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0016f-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0016f-108">Permission type</span></span>      | <span data-ttu-id="0016f-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0016f-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0016f-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0016f-110">Delegated (work or school account)</span></span> | <span data-ttu-id="0016f-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0016f-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0016f-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0016f-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0016f-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0016f-113">Not supported.</span></span>    |
|<span data-ttu-id="0016f-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0016f-114">Application</span></span> | <span data-ttu-id="0016f-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0016f-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0016f-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0016f-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/Cell
GET /workbook/worksheets/{id|name}/range(<address>)/Cell
GET /workbook/tables/{id|name}/columns/{id|name}/range/Cell

```
## <a name="request-headers"></a><span data-ttu-id="0016f-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0016f-117">Request headers</span></span>
| <span data-ttu-id="0016f-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="0016f-118">Name</span></span>       | <span data-ttu-id="0016f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0016f-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0016f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="0016f-120">Authorization</span></span>  | <span data-ttu-id="0016f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0016f-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="0016f-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0016f-123">Request body</span></span>
<span data-ttu-id="0016f-124">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="0016f-124">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="0016f-125">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0016f-125">Parameter</span></span>    | <span data-ttu-id="0016f-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="0016f-126">Type</span></span>   |<span data-ttu-id="0016f-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="0016f-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0016f-128">row</span><span class="sxs-lookup"><span data-stu-id="0016f-128">row</span></span>|<span data-ttu-id="0016f-129">number</span><span class="sxs-lookup"><span data-stu-id="0016f-129">number</span></span>|<span data-ttu-id="0016f-p104">Número de fila de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="0016f-p104">Row number of the cell to be retrieved. Zero-indexed.</span></span>|
|<span data-ttu-id="0016f-132">column</span><span class="sxs-lookup"><span data-stu-id="0016f-132">column</span></span>|<span data-ttu-id="0016f-133">number</span><span class="sxs-lookup"><span data-stu-id="0016f-133">number</span></span>|<span data-ttu-id="0016f-p105">Número de columna de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="0016f-p105">Column number of the cell to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="0016f-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0016f-136">Response</span></span>

<span data-ttu-id="0016f-137">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0016f-137">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0016f-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0016f-138">Example</span></span>
<span data-ttu-id="0016f-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0016f-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0016f-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0016f-140">Request</span></span>
<span data-ttu-id="0016f-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0016f-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_cell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/Cell
Content-type: application/json
Content-length: 37

{
  "row": {
  },
  "column": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="0016f-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0016f-142">Response</span></span>
<span data-ttu-id="0016f-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0016f-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.range"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 169

{
  "address": "address-value",
  "addressLocal": "addressLocal-value",
  "cellCount": 99,
  "columnCount": 99,
  "columnIndex": 99,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Range: Cell",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->