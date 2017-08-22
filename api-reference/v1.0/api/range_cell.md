# <a name="range-cell"></a><span data-ttu-id="876c9-101">Range: Cell</span><span class="sxs-lookup"><span data-stu-id="876c9-101">Range: Cell</span></span>

<span data-ttu-id="876c9-p101">Obtiene el objeto de intervalo que contiene la celda en función de los números de fila y columna. La celda puede estar fuera de los límites del intervalo principal, siempre y cuando permanezca dentro de la cuadrícula de la hoja de cálculo. La celda devuelta se ubica con respecto a la celda superior izquierda del intervalo.</span><span class="sxs-lookup"><span data-stu-id="876c9-p101">Gets the range object containing the single cell based on row and column numbers. The cell can be outside the bounds of its parent range, so long as it's stays within the worksheet grid. The returned cell is located relative to the top left cell of the range.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="876c9-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="876c9-105">Prerequisites</span></span>
<span data-ttu-id="876c9-106">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="876c9-106">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="876c9-107">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="876c9-107">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="876c9-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="876c9-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/Cell
GET /workbook/worksheets/{id|name}/range(<address>)/Cell
GET /workbook/tables/{id|name}/columns/{id|name}/range/Cell

```
## <a name="request-headers"></a><span data-ttu-id="876c9-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="876c9-109">Request headers</span></span>
| <span data-ttu-id="876c9-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="876c9-110">Name</span></span>       | <span data-ttu-id="876c9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="876c9-111">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="876c9-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="876c9-112">Authorization</span></span>  | <span data-ttu-id="876c9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="876c9-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="876c9-115">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="876c9-115">Request body</span></span>
<span data-ttu-id="876c9-116">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="876c9-116">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="876c9-117">Parámetro</span><span class="sxs-lookup"><span data-stu-id="876c9-117">Parameter</span></span>    | <span data-ttu-id="876c9-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="876c9-118">Type</span></span>   |<span data-ttu-id="876c9-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="876c9-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="876c9-120">row</span><span class="sxs-lookup"><span data-stu-id="876c9-120">row</span></span>|<span data-ttu-id="876c9-121">number</span><span class="sxs-lookup"><span data-stu-id="876c9-121">number</span></span>|<span data-ttu-id="876c9-p103">Número de fila de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="876c9-p103">Row number of the cell to be retrieved. Zero-indexed.</span></span>|
|<span data-ttu-id="876c9-124">column</span><span class="sxs-lookup"><span data-stu-id="876c9-124">column</span></span>|<span data-ttu-id="876c9-125">number</span><span class="sxs-lookup"><span data-stu-id="876c9-125">number</span></span>|<span data-ttu-id="876c9-p104">Número de columna de la celda que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="876c9-p104">Column number of the cell to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="876c9-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="876c9-128">Response</span></span>

<span data-ttu-id="876c9-129">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="876c9-129">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="876c9-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="876c9-130">Example</span></span>
<span data-ttu-id="876c9-131">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="876c9-131">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="876c9-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="876c9-132">Request</span></span>
<span data-ttu-id="876c9-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="876c9-133">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="876c9-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="876c9-134">Response</span></span>
<span data-ttu-id="876c9-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="876c9-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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