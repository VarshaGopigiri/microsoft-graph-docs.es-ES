# <a name="range-column"></a><span data-ttu-id="b383f-101">Range: Column</span><span class="sxs-lookup"><span data-stu-id="b383f-101">Range: Column</span></span>

<span data-ttu-id="b383f-102">Obtiene una columna contenida en el intervalo.</span><span class="sxs-lookup"><span data-stu-id="b383f-102">Gets a column contained in the range.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b383f-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b383f-103">Prerequisites</span></span>
<span data-ttu-id="b383f-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="b383f-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="b383f-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b383f-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="b383f-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b383f-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/Column
GET /workbook/worksheets/{id|name}/range(<address>)/Column
GET /workbook/tables/{id|name}/columns/{id|name}/range/Column

```
## <a name="request-headers"></a><span data-ttu-id="b383f-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b383f-107">Request headers</span></span>
| <span data-ttu-id="b383f-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="b383f-108">Name</span></span>       | <span data-ttu-id="b383f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b383f-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="b383f-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="b383f-110">Authorization</span></span>  | <span data-ttu-id="b383f-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b383f-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="b383f-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b383f-113">Request body</span></span>
<span data-ttu-id="b383f-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="b383f-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="b383f-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="b383f-115">Parameter</span></span>    | <span data-ttu-id="b383f-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="b383f-116">Type</span></span>   |<span data-ttu-id="b383f-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="b383f-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b383f-118">column</span><span class="sxs-lookup"><span data-stu-id="b383f-118">column</span></span>|<span data-ttu-id="b383f-119">number</span><span class="sxs-lookup"><span data-stu-id="b383f-119">number</span></span>|<span data-ttu-id="b383f-p102">Número de columna del intervalo que se va a recuperar. Indizado con cero.</span><span class="sxs-lookup"><span data-stu-id="b383f-p102">Column number of the range to be retrieved. Zero-indexed.</span></span>|

## <a name="response"></a><span data-ttu-id="b383f-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b383f-122">Response</span></span>

<span data-ttu-id="b383f-123">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b383f-123">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b383f-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b383f-124">Example</span></span>
<span data-ttu-id="b383f-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="b383f-125">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="b383f-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b383f-126">Request</span></span>
<span data-ttu-id="b383f-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b383f-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_column"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/Column
Content-type: application/json
Content-length: 21

{
  "column": {
  }
}
```

##### <a name="response"></a><span data-ttu-id="b383f-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b383f-128">Response</span></span>
<span data-ttu-id="b383f-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b383f-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: Column",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->