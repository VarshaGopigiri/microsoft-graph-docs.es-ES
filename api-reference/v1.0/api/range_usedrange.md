# <a name="range-usedrange"></a><span data-ttu-id="e3608-101">Range: UsedRange</span><span class="sxs-lookup"><span data-stu-id="e3608-101">Range: UsedRange</span></span>

<span data-ttu-id="e3608-102">Devuelve el rango usado del objeto de rango especificado.</span><span class="sxs-lookup"><span data-stu-id="e3608-102">Returns the used range of the given range object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e3608-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e3608-103">Prerequisites</span></span>
<span data-ttu-id="e3608-104">Se requieren los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="e3608-104">The following **scopes** are required to execute this API:</span></span> 

    * <span data-ttu-id="e3608-105">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e3608-105">Files.ReadWrite</span></span>

## <a name="http-request"></a><span data-ttu-id="e3608-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3608-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /workbook/names(<name>)/range/UsedRange
GET /workbook/worksheets/{id|name}/range(<address>)/UsedRange
GET /workbook/tables/{id|name}/columns/{id|name}/range/UsedRange

```
## <a name="request-headers"></a><span data-ttu-id="e3608-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3608-107">Request headers</span></span>
| <span data-ttu-id="e3608-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="e3608-108">Name</span></span>       | <span data-ttu-id="e3608-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3608-109">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="e3608-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="e3608-110">Authorization</span></span>  | <span data-ttu-id="e3608-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e3608-p101">Bearer {token}. Required.</span></span> |


## <a name="request-body"></a><span data-ttu-id="e3608-113">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e3608-113">Request body</span></span>
<span data-ttu-id="e3608-114">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="e3608-114">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="e3608-115">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e3608-115">Parameter</span></span>    | <span data-ttu-id="e3608-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3608-116">Type</span></span>   |<span data-ttu-id="e3608-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3608-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e3608-118">valuesOnly</span><span class="sxs-lookup"><span data-stu-id="e3608-118">valuesOnly</span></span>|<span data-ttu-id="e3608-119">boolean</span><span class="sxs-lookup"><span data-stu-id="e3608-119">boolean</span></span>|<span data-ttu-id="e3608-p102">Opcional. Solo tiene en cuenta las celdas con valores como celdas usadas.</span><span class="sxs-lookup"><span data-stu-id="e3608-p102">Optional. Considers only cells with values as used cells.</span></span>|

## <a name="response"></a><span data-ttu-id="e3608-122">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3608-122">Response</span></span>

<span data-ttu-id="e3608-123">Si se ejecuta correctamente, este método devuelve el código de respuesta `200, OK` y el objeto [Range](../resources/range.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3608-123">If successful, this method returns `200, OK` response code and [Range](../resources/range.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e3608-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3608-124">Example</span></span>
<span data-ttu-id="e3608-125">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="e3608-125">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="e3608-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e3608-126">Request</span></span>
<span data-ttu-id="e3608-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3608-127">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "range_usedrange"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/items/{id}/workbook/names(<name>)/range/UsedRange
Content-type: application/json
Content-length: 24

{
  "valuesOnly": true
}
```

##### <a name="response"></a><span data-ttu-id="e3608-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3608-128">Response</span></span>
<span data-ttu-id="e3608-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e3608-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Range: UsedRange",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->