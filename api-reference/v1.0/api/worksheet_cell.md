# <a name="worksheet-cell"></a><span data-ttu-id="0f848-101">Worksheet: Cell</span><span class="sxs-lookup"><span data-stu-id="0f848-101">Worksheet: Cell</span></span>

<span data-ttu-id="0f848-p101">Obtiene el objeto de rango que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del rango principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="0f848-p101">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid.</span></span>
## <a name="permissions"></a><span data-ttu-id="0f848-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="0f848-104">Permissions</span></span>
<span data-ttu-id="0f848-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0f848-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0f848-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0f848-107">Permission type</span></span>      | <span data-ttu-id="0f848-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0f848-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="0f848-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0f848-109">Delegated (work or school account)</span></span> | <span data-ttu-id="0f848-110">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0f848-110">Files.ReadWrite</span></span>    |
|<span data-ttu-id="0f848-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0f848-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="0f848-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0f848-112">Not supported.</span></span>    |
|<span data-ttu-id="0f848-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0f848-113">Application</span></span> | <span data-ttu-id="0f848-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0f848-114">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="0f848-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0f848-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/worksheets/{id|name}/cell(row={row},column={column})

```

## <a name="function-parameters"></a><span data-ttu-id="0f848-116">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="0f848-116">Function parameters</span></span>
<span data-ttu-id="0f848-117">En la ruta de acceso de la solicitud, proporcione los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="0f848-117">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="0f848-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="0f848-118">Parameter</span></span>    | <span data-ttu-id="0f848-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f848-119">Type</span></span>   |<span data-ttu-id="0f848-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f848-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0f848-121">row</span><span class="sxs-lookup"><span data-stu-id="0f848-121">row</span></span>|<span data-ttu-id="0f848-122">Int32</span><span class="sxs-lookup"><span data-stu-id="0f848-122">Int32</span></span>|<span data-ttu-id="0f848-p103">Número de fila de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="0f848-p103">Row number of the cell to be retrieved. Zero-indexed.</span></span>|
|<span data-ttu-id="0f848-125">column</span><span class="sxs-lookup"><span data-stu-id="0f848-125">column</span></span>|<span data-ttu-id="0f848-126">Int32</span><span class="sxs-lookup"><span data-stu-id="0f848-126">Int32</span></span>|<span data-ttu-id="0f848-p104">Número de columna de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="0f848-p104">Column number of the cell to be retrieved. Zero-indexed.</span></span>|

## <a name="request-headers"></a><span data-ttu-id="0f848-129">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0f848-129">Request headers</span></span>
| <span data-ttu-id="0f848-130">Nombre</span><span class="sxs-lookup"><span data-stu-id="0f848-130">Name</span></span>       | <span data-ttu-id="0f848-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f848-131">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="0f848-132">Autorización</span><span class="sxs-lookup"><span data-stu-id="0f848-132">Authorization</span></span>  | <span data-ttu-id="0f848-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="0f848-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="0f848-135">Workbook-Session-Id</span><span class="sxs-lookup"><span data-stu-id="0f848-135">Workbook-Session-Id</span></span>  | <span data-ttu-id="0f848-p106">Identificador de sesión de libro que determina si los cambios se conservan o no. Opcional.</span><span class="sxs-lookup"><span data-stu-id="0f848-p106">Workbook session Id that determines if changes are persisted or not. Optional.</span></span>|

## <a name="request-body"></a><span data-ttu-id="0f848-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0f848-138">Request body</span></span>
<span data-ttu-id="0f848-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0f848-139">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0f848-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f848-140">Response</span></span>

<span data-ttu-id="0f848-141">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0f848-141">If successful, this method returns `200 OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0f848-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f848-142">Example</span></span>
<span data-ttu-id="0f848-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="0f848-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="0f848-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0f848-144">Request</span></span>
<span data-ttu-id="0f848-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0f848-145">Here is an example of the request.</span></span>
<!--{
  "blockType": "request",
  "isComposable": true,
  "name": "worksheet_cell"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/worksheets/{id|name}/cell(row=<row>,column=<column>)
```

##### <a name="response"></a><span data-ttu-id="0f848-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f848-146">Response</span></span>
<span data-ttu-id="0f848-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0f848-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
