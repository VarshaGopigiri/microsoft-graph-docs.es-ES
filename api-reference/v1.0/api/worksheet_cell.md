# <a name="worksheet-cell"></a><span data-ttu-id="d9d3a-101">Worksheet: Cell</span><span class="sxs-lookup"><span data-stu-id="d9d3a-101">Worksheet: Cell</span></span>

<span data-ttu-id="d9d3a-p101">Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-p101">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid.</span></span>
## <a name="permissions"></a><span data-ttu-id="d9d3a-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="d9d3a-104">Permissions</span></span>
<span data-ttu-id="d9d3a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d9d3a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d9d3a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d9d3a-107">Permission type</span></span>      | <span data-ttu-id="d9d3a-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d9d3a-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d9d3a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d9d3a-109">Delegated (work or school account)</span></span> | <span data-ttu-id="d9d3a-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d9d3a-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="d9d3a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d9d3a-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d9d3a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-112">Not supported.</span></span>    |
|<span data-ttu-id="d9d3a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d9d3a-113">Application</span></span> | <span data-ttu-id="d9d3a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="d9d3a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d9d3a-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/cell(row=<row>,column=<column>)

```
## <a name="request-headers"></a><span data-ttu-id="d9d3a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d9d3a-116">Request headers</span></span>
| <span data-ttu-id="d9d3a-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="d9d3a-117">Name</span></span>       | <span data-ttu-id="d9d3a-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9d3a-118">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="d9d3a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="d9d3a-119">Authorization</span></span>  | <span data-ttu-id="d9d3a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="d9d3a-122">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="d9d3a-122">Workbook-Session-Id</span></span>  | <span data-ttu-id="d9d3a-p104">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-p104">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="parameters"></a><span data-ttu-id="d9d3a-125">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d9d3a-125">Parameters</span></span>
<span data-ttu-id="d9d3a-126">En la ruta de acceso de la solicitud, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="d9d3a-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="d9d3a-127">Parameter</span></span>    | <span data-ttu-id="d9d3a-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9d3a-128">Type</span></span>   |<span data-ttu-id="d9d3a-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9d3a-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d9d3a-130">row</span><span class="sxs-lookup"><span data-stu-id="d9d3a-130">row</span></span>|<span data-ttu-id="d9d3a-131">Int32</span><span class="sxs-lookup"><span data-stu-id="d9d3a-131">Int32</span></span>|<span data-ttu-id="d9d3a-p105">Número de fila de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-p105">Row number of the cell to be retrieved. Zero-indexed.</span></span>|
|<span data-ttu-id="d9d3a-134">column</span><span class="sxs-lookup"><span data-stu-id="d9d3a-134">column</span></span>|<span data-ttu-id="d9d3a-135">Int32</span><span class="sxs-lookup"><span data-stu-id="d9d3a-135">Int32</span></span>|<span data-ttu-id="d9d3a-p106">Número de columna de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-p106">Column number of the cell to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="d9d3a-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9d3a-138">Response</span></span>

<span data-ttu-id="d9d3a-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-139">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d9d3a-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d9d3a-140">Example</span></span>
<span data-ttu-id="d9d3a-141">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-141">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="d9d3a-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d9d3a-142">Request</span></span>
<span data-ttu-id="d9d3a-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-143">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "worksheet_cell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/cell(row=<row>,column=<column>)
```

##### <a name="response"></a><span data-ttu-id="d9d3a-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d9d3a-144">Response</span></span>
<span data-ttu-id="d9d3a-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d9d3a-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "cellCount": 1,
  "columnCount": 1,
  "columnIndex": 3,
  "valueTypes": "valueTypes-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Worksheet: Cell",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
