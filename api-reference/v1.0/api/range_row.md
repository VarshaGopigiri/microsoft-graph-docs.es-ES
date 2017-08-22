# <a name="range-row"></a><span data-ttu-id="c2cc0-101">Range: Row</span><span class="sxs-lookup"><span data-stu-id="c2cc0-101">Range: Row</span></span>

<span data-ttu-id="c2cc0-102">Obtiene una fila contenida en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="c2cc0-102">Gets a row contained in the range.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c2cc0-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c2cc0-103">Prerequisites</span></span>
<span data-ttu-id="c2cc0-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="c2cc0-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="c2cc0-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c2cc0-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="c2cc0-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2cc0-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /workbook/names(<name>)/range/Row
POST /workbook/worksheets/{id|name}/range(<address>)/Row
POST /workbook/tables/{id|name}/columns/{id|name}/range/Row

```
## <a name="request-headers"></a><span data-ttu-id="c2cc0-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c2cc0-107">Request headers</span></span>
| <span data-ttu-id="c2cc0-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="c2cc0-108">Name</span></span>       | <span data-ttu-id="c2cc0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2cc0-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="c2cc0-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="c2cc0-110">Authorization</span></span>  | <span data-ttu-id="c2cc0-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c2cc0-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="c2cc0-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2cc0-113">Request body</span></span>
<span data-ttu-id="c2cc0-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="c2cc0-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="c2cc0-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c2cc0-115">Parameter</span></span>    | <span data-ttu-id="c2cc0-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2cc0-116">Type</span></span>   |<span data-ttu-id="c2cc0-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2cc0-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c2cc0-118">row</span><span class="sxs-lookup"><span data-stu-id="c2cc0-118">row</span></span>|<span data-ttu-id="c2cc0-119">number</span><span class="sxs-lookup"><span data-stu-id="c2cc0-119">number</span></span>|<span data-ttu-id="c2cc0-p102">Número de fila del intervalo que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="c2cc0-p102">Row number of the range to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="c2cc0-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2cc0-122">Response</span></span>

<span data-ttu-id="c2cc0-123">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2cc0-123">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c2cc0-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2cc0-124">Example</span></span>
<span data-ttu-id="c2cc0-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c2cc0-125">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c2cc0-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2cc0-126">Request</span></span>
<span data-ttu-id="c2cc0-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c2cc0-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_row"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/Row
Content-type: application/json
Content-length: 18

{
  "row": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="c2cc0-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2cc0-128">Response</span></span>
<span data-ttu-id="c2cc0-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c2cc0-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: Row",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->