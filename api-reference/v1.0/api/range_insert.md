# <a name="range-insert"></a><span data-ttu-id="dbfa6-101">Range: insert</span><span class="sxs-lookup"><span data-stu-id="dbfa6-101">Range: insert</span></span>

<span data-ttu-id="dbfa6-p101">Inserta una celda o un rango de celdas en la hoja de cálculo en lugar de este rango y desplaza las demás celdas para crear espacio. Devuelve un objeto Range en el espacio que queda en blanco.</span><span class="sxs-lookup"><span data-stu-id="dbfa6-p101">Inserts a cell or a range of cells into the worksheet in place of this range, and shifts the other cells to make space. Returns a new Range object at the now blank space.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dbfa6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dbfa6-104">Prerequisites</span></span>
<span data-ttu-id="dbfa6-105">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="dbfa6-105">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="dbfa6-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="dbfa6-106">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="dbfa6-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dbfa6-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/insert
POST /workbook/worksheets/{id|name}/range(<address>)/insert
POST /workbook/tables/{id|name}/columns/{id|name}/range/insert

```
## <a name="request-headers"></a><span data-ttu-id="dbfa6-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dbfa6-108">Request headers</span></span>
| <span data-ttu-id="dbfa6-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="dbfa6-109">Name</span></span>       | <span data-ttu-id="dbfa6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbfa6-110">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="dbfa6-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="dbfa6-111">Authorization</span></span>  | <span data-ttu-id="dbfa6-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dbfa6-p102">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="dbfa6-114">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dbfa6-114">Request body</span></span>
<span data-ttu-id="dbfa6-115">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="dbfa6-115">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="dbfa6-116">Parámetro</span><span class="sxs-lookup"><span data-stu-id="dbfa6-116">Parameter</span></span>    | <span data-ttu-id="dbfa6-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="dbfa6-117">Type</span></span>   |<span data-ttu-id="dbfa6-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbfa6-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dbfa6-119">Shift</span><span class="sxs-lookup"><span data-stu-id="dbfa6-119">shift</span></span>|<span data-ttu-id="dbfa6-120">string</span><span class="sxs-lookup"><span data-stu-id="dbfa6-120">string</span></span>|<span data-ttu-id="dbfa6-p103">Especifica hacia dónde se desplazarán las celdas.  Valores posibles: `Down`, `Right`.</span><span class="sxs-lookup"><span data-stu-id="dbfa6-p103">Specifies which way to shift the cells.  Possible values are: `Down`, `Right`.</span></span>|

## <a name="response"></a><span data-ttu-id="dbfa6-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbfa6-123">Response</span></span>

<span data-ttu-id="dbfa6-124">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dbfa6-124">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dbfa6-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dbfa6-125">Example</span></span>
<span data-ttu-id="dbfa6-126">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="dbfa6-126">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="dbfa6-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dbfa6-127">Request</span></span>
<span data-ttu-id="dbfa6-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dbfa6-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_insert"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/insert
Content-type: application/json
Content-length: 28

{
  "shift": "shift-value"
}
```

##### <a name="response"></a><span data-ttu-id="dbfa6-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbfa6-129">Response</span></span>
<span data-ttu-id="dbfa6-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dbfa6-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: insert",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->