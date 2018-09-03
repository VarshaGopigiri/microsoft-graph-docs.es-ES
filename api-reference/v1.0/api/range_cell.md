# <a name="range-cell"></a><span data-ttu-id="de42e-101">Range: Cell</span><span class="sxs-lookup"><span data-stu-id="de42e-101">Range: Cell</span></span>

<span data-ttu-id="de42e-p101">Obtiene el objeto de intervalo que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del intervalo principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo. La celda devuelta se ubica con respecto a la celda superior izquierda del intervalo.</span><span class="sxs-lookup"><span data-stu-id="de42e-p101">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid. The returned cell is located relative to the top left cell of the range.</span></span>
## <a name="permissions"></a><span data-ttu-id="de42e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="de42e-105">Permissions</span></span>
<span data-ttu-id="de42e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="de42e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="de42e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="de42e-108">Permission type</span></span>      | <span data-ttu-id="de42e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="de42e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="de42e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="de42e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="de42e-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="de42e-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="de42e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="de42e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="de42e-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de42e-113">Not supported.</span></span>    |
|<span data-ttu-id="de42e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="de42e-114">Application</span></span> | <span data-ttu-id="de42e-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="de42e-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="de42e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="de42e-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names/{name}/range/cell
GET /workbook/worksheets/{id|name}/range(address='<address>')/cell
GET /workbook/tables/{id|name}/columns/{id|name}/range/cell

```
## <a name="request-headers"></a><span data-ttu-id="de42e-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="de42e-117">Request headers</span></span>
| <span data-ttu-id="de42e-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="de42e-118">Name</span></span>       | <span data-ttu-id="de42e-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="de42e-119">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="de42e-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="de42e-120">Authorization</span></span>  | <span data-ttu-id="de42e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="de42e-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="de42e-123">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="de42e-123">Workbook-Session-Id</span></span>  | <span data-ttu-id="de42e-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="de42e-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="path-parameters"></a><span data-ttu-id="de42e-126">Parámetros de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="de42e-126">Path parameters</span></span>
<span data-ttu-id="de42e-127">En la ruta de acceso, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="de42e-127">In the path, provide the following parameters.</span></span>

| <span data-ttu-id="de42e-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="de42e-128">Parameter</span></span>    | <span data-ttu-id="de42e-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="de42e-129">Type</span></span>   |<span data-ttu-id="de42e-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="de42e-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="de42e-131">row</span><span class="sxs-lookup"><span data-stu-id="de42e-131">row</span></span>|<span data-ttu-id="de42e-132">Int32</span><span class="sxs-lookup"><span data-stu-id="de42e-132">Int32</span></span>|<span data-ttu-id="de42e-p105">Número de fila de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="de42e-p105">Row number of the cell to be retrieved. Zero-indexed.</span></span>|
|<span data-ttu-id="de42e-135">columna</span><span class="sxs-lookup"><span data-stu-id="de42e-135">column</span></span>|<span data-ttu-id="de42e-136">Int32</span><span class="sxs-lookup"><span data-stu-id="de42e-136">Int32</span></span>|<span data-ttu-id="de42e-p106">Número de columna de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="de42e-p106">Column number of the cell to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="de42e-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de42e-139">Response</span></span>

<span data-ttu-id="de42e-140">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="de42e-140">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="de42e-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="de42e-141">Example</span></span>
<span data-ttu-id="de42e-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="de42e-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="de42e-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="de42e-143">Request</span></span>
<span data-ttu-id="de42e-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="de42e-144">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "range_cell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names/{name}/range/cell(row=5,column=6)
```

##### <a name="response"></a><span data-ttu-id="de42e-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="de42e-145">Response</span></span>
<span data-ttu-id="de42e-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="de42e-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.workbookRange"
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